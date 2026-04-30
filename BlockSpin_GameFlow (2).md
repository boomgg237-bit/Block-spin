# BlockSpin - วิเคราะห์ระบบเกมทั้งหมด

## สถาปัตยกรรมเครือข่าย

ทุก client-server communication ผ่าน **Net module** (`ReplicatedStorage.Modules.Core.Net`)

### Remote ทั้งหมด
| Remote | ชนิด | Path |
|--------|------|------|
| Send | RemoteEvent | `ReplicatedStorage.Remotes.Send` |
| Get | RemoteFunction | `ReplicatedStorage.Remotes.Get` |
| ClientLog | RemoteEvent | `ReplicatedStorage.ClientLog` |
| LogRequest | RemoteEvent | `ReplicatedStorage.LogRequest` |

### รูปแบบการส่ง
```
Send:FireServer(counter, eventName, ...args)
Get:InvokeServer(counter, eventName, ...args)
```
- `counter` = เลขเพิ่มขึ้นเรื่อยๆ จัดการภายใน Net module
- มี Anti-exec check (`u19`): ใช้ `getfenv(3)` ตรวจจับ executor

### กฎสำคัญ: ชนิดของ Arguments
- args ส่วนใหญ่เป็น **Instance reference จาก workspace** ไม่ใช่ string
- ต้องหา Instance จริงจาก workspace ก่อนส่ง

---

## FireServer Events ทั้งหมด (Net.send)

### ระบบงาน (Jobs)

| Event | Args | ชนิด Args | ที่มา |
|-------|------|-----------|-------|
| `apply_for_job` | `beaconInstance` | Instance (workspace beacon) | JobApplicationBeacon |
| `leave_job` | *(ไม่มี)* | - | JobApplicationBeacon |
| `player_moved_from_puddle` | `puddleInstance` | Instance (workspace puddle) | Janitor |

### ระบบ ATM Hacker

| Event | Args | ชนิด Args | ที่มา |
|-------|------|-----------|-------|
| `request_begin_hacking_3` | `jobValue`, `itemName` | state value, string | ATM |
| `atm_win_3` | `atmInstance` | Instance | ATM |
| `atm_fail_early` | `atmInstance` | Instance | ATM |

### ระบบประตู

| Event | Args | ชนิด Args | ที่มา |
|-------|------|-----------|-------|
| `request_door_ownership` | `doorInstance` | Instance (DoorSystem) | DoorClient |

### ระบบวิ่ง

| Event | Args | ชนิด Args | ที่มา |
|-------|------|-----------|-------|
| `set_sprinting_1` | `boolean` | true/false | Sprint |
| `replicate_stamina_bar_1` | `value` | number | Sprint |

### ระบบรถ

| Event | Args | ชนิด Args | ที่มา |
|-------|------|-----------|-------|
| `horn_vehicle` | `vehicleInstance` | Instance | VehicleGui |
| `lock_vehicle` | `vehicleInstance`, `lockState` | Instance, boolean | VehicleGui |
| `lockpick_success` | `vehicleInstance` | Instance | VehicleSeat |
| `lockpick_fail` | `vehicleInstance` | Instance | VehicleSeat |
| `crashed_car` | `carInstance`, `speed` | Instance, number | car |
| `run_over` | `carInstance`, `player`, `velocity` | Instance, Player, Vector3 | car |

### ระบบต่อสู้

| Event | Args | ชนิด Args | ที่มา |
|-------|------|-----------|-------|
| `shoot_gun` | `gunInstance`, `cframe`, `target` | Instance, CFrame, target | Gun |
| `melee_attack` | `meleeInstance`, `u68`, `cframe`, `damageValue` | Instance, unknown, CFrame, number | Melee |
| `throw_item` | `itemInstance`, `direction`, `power` | Instance, Vector3, number | Throwable |
| `throw_hit` | `itemInstance`, `target`, `cframe` | Instance, target, CFrame | Throwable |
| `begin_pour` | `itemInstance` | Instance | Throwable |

### ระบบตกปลา

| Event | Args | ชนิด Args | ที่มา |
|-------|------|-----------|-------|
| `cancel_throw` | `rodInstance` | Instance | FishingRod |
| `reel_ended` | `fishingInstance`, `result` | Instance, value | FishingRod |

### ระบบปลูกผัก

| Event | Args | ชนิด Args | ที่มา |
|-------|------|-----------|-------|
| `add_to_pot` | `farmItemType`, `potInstance`, `itemInstance` | string, Instance, Instance | Farming |
| `harvest` | `potInstance` | Instance | Farming |

### ระบบร้านค้า

| Event | Args | ชนิด Args | ที่มา |
|-------|------|-----------|-------|
| `set_purchase_location` | `locationString` | string ("Store", "JobBoard") | StoreUI |
| `client_reward_sequence_finished` | *(ไม่มี)* | - | StoreUI |
| `drop_item` | `itemGuid` | string (GUID) | ItemsUI |

### ระบบบ้าน

| Event | Args | ชนิด Args | ที่มา |
|-------|------|-----------|-------|
| `set_shutters` | `homeInstance`, `boolean` | Instance, boolean | Home |
| `set_mass_lock` | `boolean` | boolean | Home |
| `set_lock_door` | `doorInstance`, `boolean` | Instance, boolean | Home |
| `set_lock_garage` | `garageInstance`, `boolean` | Instance, boolean | Home |

### ระบบ Character Creator

| Event | Args | ชนิด Args | ที่มา |
|-------|------|-----------|-------|
| `change_height` | `heightValue`, `widthMultiplier?` | number, number? | Heights |
| `change_face` | `itemName` | string | Faces |
| `change_skin_color` | `skinColor` | Color3 | SkinColors |
| `replicate_cc_cframe` | `cframe` | CFrame | CharacterCreator |

### อื่นๆ

| Event | Args | ชนิด Args | ที่มา |
|-------|------|-----------|-------|
| `cd` | `clickTarget` | Instance | ObjectClick |
| `interact_server_switch_van` | *(ไม่มี)* | - | ServerSwitchVan |
| `end_ragdoll_early` | *(ไม่มี)* | - | Ragdoll |
| `death_screen_request_respawn` | *(ไม่มี)* | - | DeathScreen |

---

## InvokeServer Events ทั้งหมด (Net.get)

| Event | Args | Return | ที่มา |
|-------|------|--------|-------|
| `transfer_funds` | `from`, `to`, `amount` | result | ATMUI |
| `can_purchase_products` | *(ไม่มี)* | boolean | StoreUI |
| `set_gifting_products` | `nil` | boolean | StoreUI |
| `get_max_inventory_space` | *(ไม่มี)* | table | ItemCustomizationUI |
| `toggle_equip_upgrade` | `guid`, `upgradeName` | result, error? | ItemCustomizationUI |
| `toggle_equip_cosmetic` | `guid`, `cosmeticId` | result, error?, extra? | ItemCustomizationUI |
| `toggle_equip_item` | `guid` | result | ItemsUI |
| `equip_ammo_on_item` | `itemGuid`, `ammoGuid` | result, error? | ItemsUI |
| `repair_item` | `itemGuid` | result | ItemsUI |
| `sell_item` | `itemGuid`, `value` | boolean | ItemsUI / SellFishBeacon |
| `sell_all_fish` | *(ไม่มี)* | result | SellFishBeacon |
| `request_change_item_location` | `itemGuid`, `location` | boolean | ItemsUI |
| `throw_dice` | *(ไม่มี)* | boolean | Dice |
| `purchase_item` | `itemName` | boolean | CharacterCreator |
| `change_hair` | `itemName` | result | Hairs |
| `change_accessory` | `scriptName`, `itemName`, `equip` | result | Accessories |
| `player_started_stocking_shelf` | `shelfInstance` | boolean | ShelfStocking |
| `player_stocked_shelf` | `shelfInstance` | boolean | ShelfStocking |
| `stock_reset_item_name` | `stockKey` | result | ShelfStocking |
| `force_update` | *(ไม่มี)* | result, error? | Data |
| `pickup_dropped_item` | `droppedItemInstance` | result, error? | DroppedItem |
| `claim_quest` | `questId` | boolean | QuestsUI |
| `fix_desync_hip_height` | *(ไม่มี)* | result | AutomaticScalingEnabled |

---

## ตัวอย่างจริงจาก Remote Spy

```lua
-- request_door_ownership — ส่ง DoorSystem Instance
Send:FireServer(120, "request_door_ownership",
    workspace.Map.Tiles.GasStationTile.Quick11.Interior.DoorSystem)

-- set_sprinting_1 — boolean เท่านั้น
Send:FireServer(124, "set_sprinting_1", true)
Send:FireServer(125, "set_sprinting_1", false)

-- leave_job — ไม่มี args
Send:FireServer(123, "leave_job")

-- transfer_funds — ถอน/ฝากเงิน
Get:InvokeServer(9, "transfer_funds", "bank", "hand", 93)
Get:InvokeServer(10, "transfer_funds", "hand", "bank", 93)

-- player_started_stocking_shelf — ส่ง Shelf Instance
Get:InvokeServer(13, "player_started_stocking_shelf",
    workspace.Map.Tiles.GasStationTile.Quick11.Interior
    .ShelfStockingJob.Shelves.Shelf)
```

---

## ข้อมูลงาน (JobData)

| Key | ชื่อ | ค่าจ้าง |
|-----|------|---------|
| `janitor` | Janitor | $9–$18 |
| `shelf_stocker` | Shelf Stocker | $15–$30 |
| `steakhouse_cook` | Steakhouse Cook | $15–$30 |
| `atm_hacker` | Swiper | $30–$60 |

### Janitor — ชนิด Puddle
| ชนิด | ตัวคูณ | เวลาถู | Respawn | ต้อง Skill |
|------|--------|--------|---------|-----------|
| SmallPuddle | 1x | 5 วิ | 30 วิ | ไม่ |
| LargePuddle | 2x | 10 วิ | 45 วิ | JanitorUnlockLarge |
| NastyPuddle | 3x | 15 วิ | 60 วิ | JanitorUnlockNasty |
| OilPuddle | 4x | 20 วิ | 90 วิ | JanitorUnlockOil |
| ToxicPuddle | 8x | 30 วิ | 120 วิ | JanitorUnlockToxic |

### Shelf Stocker — ชนิด Box
| ชนิด | ตัวคูณ | สต็อก | Refresh |
|------|--------|-------|---------|
| NormalBox | 1x | ไม่จำกัด | - |
| SunflowerSeedsBox | 3x | 100 | 1 ชม. |
| ElectronicsBox | 5x | 50 | 1 ชม. |
| GoldenBox | 25x | 5 | 6 ชม. |

### Steakhouse Cook
- เวลาทำสเต็ก: 10–15 วินาที
- Perfect zone: 60%–70% ของเวลา
- ค่าจ้างขั้นต่ำต้องทำอย่างน้อย 8 วินาที

---

## ClientLog
```
ClientLog:FireServer(logLevel, timestamp, message)
```
- logLevel: 2 = warn, 3 = error
- ใช้สำหรับส่ง error/warning กลับ server

---

## ทุกโมดูลในเกม — รายละเอียดครบ

### Core Modules (Modules.Core.*)

| โมดูล | หน้าที่ | รายละเอียด |
|--------|---------|-----------|
| **Net** | ระบบ Remote | ห่อ FireServer/InvokeServer ทุกตัว, มี anti-exec check `u19`, counter อัตโนมัติ, hook system สำหรับรับ event จาก server |
| **State** | Reactive State | `.new(value)` สร้าง state, `.get()` อ่าน, `.set(v)` เขียน, `.hook(fn)` ฟัง — ใช้ทั่วทั้งเกม |
| **StatefulObject** | Class System | `.new_class(createStates, name)` สร้าง class, `.hook(fn)` ผูก behavior กับ instance, `.objects` เก็บ instances ทั้งหมด — ใช้กับ game objects ที่ stream เข้า/ออก |
| **UI** | UI Manager | `.get(name)` หา UI element, `.on_click(name, fn)` ผูก click, จัดการ ScreenGui ทั้งหมด |
| **UIFX** | UI Effects | `scale_open/close()` animation เปิด/ปิด UI |
| **UIFX.Scaler** | Scale Animation | จัดการ UIScale animation |
| **UIFX.Scrolling** | Scroll Effects | Smooth scrolling สำหรับ ScrollingFrame |
| **UIFX.RotationEffects** | หมุน UI | Rotation animation effects |
| **UIFX.Buttons** | Button Effects | Hover/press effects สำหรับปุ่ม |
| **UIFX.TextBoxEffects** | TextBox Effects | Effects สำหรับ TextBox |
| **UIFX.MoveEffects** | Move Animation | Position animation effects |
| **UIFX.StrokeEffects** | Stroke Effects | UIStroke animation |
| **UIFX.FrameEffects** | Frame Effects | Frame animation effects |
| **Data** | Player Data Sync | ดึง/sync ข้อมูลผู้เล่นจาก server, `.hook(key, fn)` ฟังการเปลี่ยนแปลง, ใช้ `Net.get("force_update")` |
| **Char** | Character Utils | `get_hrp()` = HumanoidRootPart, `get_hum()` = Humanoid, `current_char/hum/hrp` = reactive states, `enable/disable_controls()` |
| **Cam** | Camera Control | จัดการ Camera, FOV spring, lock/unlock camera, cutscene camera |
| **Util** | General Utils | `watch_attribute()` ฟัง attribute เปลี่ยน, `db(fn)` = debounce, `formatted_time()`, `wait_for_descendant_which_is_a()` |
| **Input** | Input Handler | จัดการ keyboard/mouse/touch input |
| **Tween** | Tween Wrapper | ห่อ TweenService ให้ใช้ง่าย |
| **Timer** | Timer | `.new(interval, fn, immediate)` สร้าง timer วนซ้ำ, `.start()/.stop()` |
| **Signal** | Custom Events | ระบบ event/signal แบบ custom, `.new()`, `:Fire()`, `:Connect()` |
| **Zone** | Zone Detection | ตรวจจับเข้า/ออกโซน, `on_enter/on_exit` |
| **Spring** | Physics Spring | Spring animation สำหรับ number values |
| **ColorSpring** | Color Spring | Spring animation สำหรับ Color3 |
| **CFrameSpring** | CFrame Spring | Spring animation สำหรับ CFrame |
| **CFrameSpring.Quaternion** | Quaternion | Quaternion math สำหรับ CFrame spring |
| **CFrameSpringTest** | Test | Test สำหรับ CFrame spring |
| **Tbl** | Table Utils | Table manipulation helpers |
| **List** | Ordered List | `.new()` สร้าง ordered list, add/remove/iterate |
| **Octree** | Spatial Index | Octree สำหรับ spatial queries (หาของใกล้ๆ) |
| **Octree.OctreeNode** | Octree Node | Node ของ Octree |
| **Octree.OctreeRegionUtils** | Region Utils | Math utils สำหรับ Octree regions |
| **ObjectClick** | Click System | Raycast ตรวจจับการคลิก object, ส่ง `Net.send("cd", target)` เมื่อคลิก, เช็คระยะ < 50 studs |
| **RateLimiter** | Rate Limit | จำกัดความถี่การเรียกฟังก์ชัน |
| **Music** | Music Player | เล่นเพลง background |
| **Audio** | Sound System | `.play(soundId, volume)` เล่นเสียง |
| **Blur** | Blur Effect | เปิด/ปิด blur effect |
| **Ease** | Easing Functions | Math easing functions |
| **Cutscene** | Cutscene | ระบบ cutscene/cinematic |
| **Snippets** | Code Snippets | Helper snippets ที่ใช้ซ้ำ |
| **Attrib** | Attribute Helper | จัดการ Instance attributes |
| **V3** | Vector3 Utils | Vector3 math helpers |
| **CatmullRomSpline** | Spline | Catmull-Rom spline interpolation สำหรับ smooth paths |
| **DeveloperTools** | Dev Tools | เครื่องมือ debug สำหรับ developer |
| **FPSTracker** | FPS Monitor | ติดตาม FPS, ใช้ปรับ quality |
| **TextCompression** | Text Compress | บีบอัดข้อความ |
| **PropertyEncoding** | Prop Encode | Encode/decode property values |
| **LazyLoading** | Lazy Load | โหลดของเมื่อจำเป็น |
| **StringManipulation** | String Utils | String manipulation helpers |
| **Friend** | Friend System | ระบบเพื่อน |

---

### Game Modules — ระบบงาน (Modules.Game.Jobs.*)

| โมดูล | หน้าที่ | Net Events | รายละเอียด |
|--------|---------|-----------|-----------|
| **JobApplicationBeacon** | สมัคร/ลาออก | `send: apply_for_job, leave_job` | เมื่อเข้าโซน beacon → แสดง UI สมัคร/ลาออก, ส่ง beacon Instance ไปกับ event |
| **ShelfStocking** | งานเติมของ | `get: player_started_stocking_shelf, player_stocked_shelf, stock_reset_item_name` | หยิบกล่อง (ProximityPrompt) → ถือ BoxTool → เดินไปชั้น (Shelf.Touched) → รอ timer → Net.get("player_stocked_shelf"), มี stock system ที่หมดแล้ว restock ได้ |
| **Janitor** | งานถูพื้น | `send: player_moved_from_puddle` | เข้าโซน puddle → แสดง progress bar → ถ้าออกก่อนเสร็จส่ง event, puddle มี 5 ระดับ ต้อง unlock skill |
| **SteakhouseCook** | งานทำสเต็ก | *(ผ่าน hook system)* | Timing minigame — ต้องกดตอน 60-70% ของเวลา |
| **JobData** | ข้อมูลงาน | *(ไม่มี)* | เก็บค่าจ้าง, ข้อมูล puddle types, box types, steakhouse config |
| **JobUtil** | Job Helpers | *(ไม่มี)* | `create_arrow()` สร้างลูกศรนำทาง, `place_beacon()` วาง beacon marker |

---

### Game Modules — ระบบต่อสู้/อาวุธ (Modules.Game.ItemTypes.*)

| โมดูล | หน้าที่ | Net Events | รายละเอียด |
|--------|---------|-----------|-----------|
| **Gun** | ระบบปืน | `send: shoot_gun` | Raycast ยิง, ส่ง gunInstance + Camera CFrame (offset Z-2) + target, มี crosshair, recoil, ammo system |
| **Melee** | ระบบมีด | `send: melee_attack` | ส่ง meleeInstance + hit data + CFrame + damage, มี animation, walk speed reduction ตอนโจมตี |
| **Throwable** | ขว้างของ | `send: throw_item, throw_hit, begin_pour` | ระบบฟิสิกส์ขว้าง, trajectory calculation, แต่ละชนิดมี behavior ต่างกัน |
| **Throwable.ThrowableTypes** | ข้อมูลขว้าง | *(ไม่มี)* | เก็บ config ของแต่ละชนิด |
| — Brick | อิฐ | | damage ปกติ |
| — Bottle | ขวด | | แตกเมื่อกระทบ |
| — Cinder Block | บล็อกปูน | | heavy damage |
| — Molotov | ระเบิดเพลิง | | สร้างไฟ |
| — Rock | หิน | | damage ปกติ |
| — Glass | แก้ว | | แตกเป็นชิ้น |
| — Grenade | ระเบิด | | explosion effect |
| — Fire Cracker | ประทัด | | FirecrackerExplosion effect |
| — Dumbbell Plate | แผ่นดัมเบล | | heavy |
| — Jerry Can | ถังน้ำมัน | | pour + fire |
| — Bowling Pin | พินโบว์ลิ่ง | | bounce |
| — Spray Can | กระป๋องสเปรย์ | | spray effect |
| — Soda Can | กระป๋องน้ำอัดลม | | light |
| — Jar | ขวดโหล | | แตก |
| — Mug | แก้วกาแฟ | | แตก |
| — Milkshake | มิลค์เชค | | pour |
| — Snowball | ก้อนหิมะ | | แตก |
| **WeaponTypes** | ข้อมูลอาวุธ | *(ไม่มี)* | เก็บ config อาวุธทั้งหมด |
| **PowerUp** | Power-up | *(ไม่มี)* | ระบบ power-up items |
| **Dice** | ลูกเต๋า | `get: throw_dice` | ทอยลูกเต๋า, animation + result จาก server |
| **Lockpick** | ล็อคพิค | *(ผ่าน VehicleSeat)* | เครื่องมืองัดรถ |
| **Utility** | Utility Items | *(ไม่มี)* | ไอเท็มอื่นๆ ที่ไม่ใช่อาวุธ |
| **FishingRod** | เบ็ดตกปลา | `send: cancel_throw, reel_ended` | ระบบตกปลา — cast, รอปลากิน, reel in, ส่ง result ไป server |

---

### Game Modules — ระบบรถ (Modules.Game.VehicleSystem.*)

| โมดูล | หน้าที่ | Net Events | รายละเอียด |
|--------|---------|-----------|-----------|
| **VehicleGui** | UI รถ | `send: horn_vehicle, lock_vehicle` | ปุ่มบีบแตร + ล็อค/ปลดล็อครถ, แสดง/ซ่อนตาม current_driving state |
| **Vehicle** | ระบบรถหลัก | *(ไม่มี)* | จัดการ vehicle physics, input, streaming |
| **Vehicle.VehicleTypes.car** | รถยนต์ | `send: crashed_car, run_over` | ตรวจจับ crash (speed > 15), run over ผู้เล่น (ระยะ < 1/3 ของ raycast) |
| **Vehicle.VehicleTypes.bike** | จักรยาน | *(ไม่มี)* | Physics สำหรับ bike (BMX, EScooter) |
| **VehicleSeat** | ที่นั่งรถ | `send: lockpick_success, lockpick_fail` | ระบบ lockpick minigame — สำเร็จ/ล้มเหลว |

---

### Game Modules — ระบบบ้าน (Modules.Game.Home.*)

| โมดูล | หน้าที่ | Net Events | รายละเอียด |
|--------|---------|-----------|-----------|
| **Home** | ระบบบ้าน | `send: set_shutters, set_mass_lock, set_lock_door, set_lock_garage` | จัดการประตู/โรงรถ/หน้าต่าง, ล็อค/ปลดล็อค, มี ProximityPrompt สำหรับแต่ละอัน |
| **SecurityCamera** | กล้องวงจรปิด | *(ไม่มี)* | ระบบดูกล้อง CCTV ในบ้าน |

---

### Game Modules — ระบบปลูกผัก (Modules.Game.Farming.*)

| โมดูล | หน้าที่ | Net Events | รายละเอียด |
|--------|---------|-----------|-----------|
| **Farming** | ระบบปลูก | `send: add_to_pot, harvest` | Flow: ใส่กระถาง → ใส่ดิน → ปลูกเมล็ด → รดน้ำ → รอโต → เก็บเกี่ยว, เช็ค FarmItem attribute ของ item |
| **FarmingOptionsUI** | UI ปลูก | *(ไม่มี)* | UI แสดง options สำหรับ farming |
| **PotClient** | กระถาง | *(ไม่มี)* | จัดการ pot instance, states (current_pot, current_soil, current_plant, planted_stamp, growth_multiplier, watered_stamp) |
| **FarmingInfo** | ข้อมูลพืช | *(ไม่มี)* | เก็บ config พืช: time_to_grow, payout |

---

### Game Modules — ระบบร้านค้า (Modules.Game.Store.*)

| โมดูล | หน้าที่ | Net Events | รายละเอียด |
|--------|---------|-----------|-----------|
| **StoreUI** | ร้านค้าหลัก | `send: set_purchase_location, client_reward_sequence_finished` / `get: can_purchase_products, set_gifting_products` | จัดการ product purchase ผ่าน Roblox PromptProductPurchase, gift mode, reward sequence animation |
| **StoreData** | ข้อมูลร้าน | *(ไม่มี)* | เก็บ product data, SKUs, ราคา |
| **CycleItems** | Cycle Items | *(ไม่มี)* | ระบบหมุนเวียนสินค้า |
| **RewardsToString** | แปลง Reward | *(ไม่มี)* | แปลง reward data เป็น string แสดงผล |
| **BlockSpinSubscriptionClient** | Subscription | *(ไม่มี)* | ระบบ subscription/VIP pass |
| **BlockSpinSubscriptionData** | Sub Data | *(ไม่มี)* | เก็บข้อมูล subscription tiers |

---

### Game Modules — ระบบ Inventory (Modules.Game.Inventory.*)

| โมดูล | หน้าที่ | Net Events | รายละเอียด |
|--------|---------|-----------|-----------|
| **ItemsUI** | UI ไอเท็ม | `send: drop_item` / `get: request_change_item_location, sell_item, toggle_equip_item, equip_ammo_on_item, repair_item` | จัดการ inventory — equip/unequip, drop, sell, repair, เปลี่ยนตำแหน่ง (hand/safe) |
| **ItemUtils** | Item Helpers | *(ไม่มี)* | `get_item_icon()`, `get_item_type()` etc. |
| **Hotbar** | Hotbar | *(ไม่มี)* | แสดง equipped items, durability bar, hotbar slots |
| **SafeBeacon** | ตู้เซฟ | *(ไม่มี)* | Beacon zone เปิด/ปิดตู้เซฟ, มี sound |
| **PawnShop** | ร้านรับจำนำ | *(ไม่มี)* | ระบบขายของให้ pawn shop |
| **PawnShopBeacon** | Beacon จำนำ | *(ไม่มี)* | Zone beacon สำหรับ pawn shop |
| **SellFishBeacon** | ขายปลา | `get: sell_item, sell_all_fish` | ขายปลาทีละตัวหรือขายทั้งหมด, แสดงราคาก่อนขาย |
| **RepairBenchBeacon** | ซ่อมของ | *(ไม่มี)* | Zone beacon สำหรับ repair bench |
| **RarityIndicator** | แสดง Rarity | *(ไม่มี)* | สี/effect ตาม rarity ของ item |
| **Recovery** | กู้คืนของ | *(ไม่มี)* | ระบบกู้คืน item ที่หาย |
| **TestBuyPrompt** | Test Buy | *(ไม่มี)* | Test purchase prompt |
| **BeaconUtil** | Beacon Helper | *(ไม่มี)* | `init_beacon()` สร้าง beacon zone detection, `on_enter/on_exit` events |

---

### Game Modules — ระบบ Character Creator (Modules.Game.CharacterCreator.*)

| โมดูล | หน้าที่ | Net Events | รายละเอียด |
|--------|---------|-----------|-----------|
| **CharacterCreator** | สร้างตัวละคร | `send: replicate_cc_cframe` / `get: purchase_item` | ระบบสร้าง/แต่งตัวละคร, ซื้อ items, เปลี่ยนหน้า/ผม/สี |
| **CharacterCreatorTypes** | ชนิดข้อมูล | *(ไม่มี)* | Type definitions สำหรับ CC items |
| **CharacterCreatorSlot** | Slot System | *(ไม่มี)* | จัดการ slot ของ character |
| **Animations** | CC Animation | *(ไม่มี)* | Animation สำหรับหน้า character creator |
| **FillPages** | เติมหน้า | *(ไม่มี)* | สร้าง UI pages จาก item data |
| **Items.SkinColors** | สีผิว | `send: change_skin_color` | เปลี่ยนสีผิว — ส่ง Color3 |
| **Items.Hairs** | ทรงผม | `get: change_hair` | เปลี่ยนทรงผม — ส่ง itemName |
| **Items.Heights** | ความสูง | `send: change_height` | เปลี่ยนความสูง + ความกว้าง |
| **Items.Faces** | หน้า | `send: change_face` | เปลี่ยนหน้า — ส่ง itemName |
| **Items.Gender** | เพศ | *(ไม่มี)* | เปลี่ยนเพศตัวละคร |
| **Items.TemplatePage** | Template | *(ไม่มี)* | Template page สำหรับ items |
| **Items.HatAccessories** | หมวก | *(ผ่าน change_accessory)* | เปลี่ยนหมวก |
| **Items.ShoeAccessories** | รองเท้า | `get: change_accessory` | เปลี่ยนรองเท้า — ส่ง scriptName + itemName + equip |
| **Items.TopAccessories** | เสื้อ | `get: change_accessory` | เปลี่ยนเสื้อ — ส่ง scriptName + itemName + equip |
| **Items.BottomAccessories** | กางเกง | *(ผ่าน change_accessory)* | เปลี่ยนกางเกง |
| **BarberSeat** | เก้าอี้ตัดผม | *(ไม่มี)* | ที่นั่งร้านตัดผม — เปิด CC เมื่อนั่ง |
| **ClothingStore** | ร้านเสื้อผ้า | *(ไม่มี)* | Zone beacon เปิด character creator |

---

### Game Modules — ระบบ Customization (Modules.Game.ItemCustomization.*)

| โมดูล | หน้าที่ | Net Events | รายละเอียด |
|--------|---------|-----------|-----------|
| **ItemCustomizationUI** | UI แต่งไอเท็ม | `get: get_max_inventory_space, toggle_equip_upgrade, toggle_equip_cosmetic` | แต่ง cosmetics/upgrades บนไอเท็ม |
| **CustomizationCategories** | หมวดหมู่ | *(ไม่มี)* | เก็บ categories ของ customization |
| **UpdateCosmetics** | อัพเดท Cosmetic | *(ไม่มี)* | อัพเดท visual ของ cosmetic บน item |
| **UpdateUpgrades** | อัพเดท Upgrade | *(ไม่มี)* | อัพเดท upgrade effects |
| **ValidCosmeticTypes** | Valid Types | *(ไม่มี)* | เช็คว่า cosmetic ใส่กับ item ได้ไหม |

---

### Game Modules — ระบบ ATM (Modules.Game.ATM.*)

| โมดูล | หน้าที่ | Net Events | รายละเอียด |
|--------|---------|-----------|-----------|
| **ATM** | ระบบ ATM | `send: request_begin_hacking_3, atm_win_3, atm_fail_early` | ATM hacking minigame — เลือก tool → hack → สำเร็จ/ล้มเหลว |
| **ATMUI** | UI ATM | `get: transfer_funds` | โอนเงิน bank↔hand, ถอน/ฝาก, แสดงยอดเงิน |

---

### Game Modules — ระบบ Crate/ลัง (Modules.Game.CrateSystem.*)

| โมดูล | หน้าที่ | Net Events | รายละเอียด |
|--------|---------|-----------|-----------|
| **Crate** | ระบบลัง | *(ผ่าน hooks)* | เปิดลัง, animation unboxing, แสดง reward, rare item effects |
| **CrateUI** | UI ลัง | *(ไม่มี)* | แสดง options ลัง, tokens, ราคา, ปุ่มซื้อ |
| **CrateSettings.Weapons** | ลังอาวุธ | *(ไม่มี)* | Config ของที่อยู่ในลังอาวุธ |
| **CrateSettings.Cars** | ลังรถ | *(ไม่มี)* | Config ของที่อยู่ในลังรถ |
| **CrateSettings.Bike** | ลังจักรยาน | *(ไม่มี)* | Config ของที่อยู่ในลังจักรยาน |
| **CrateSettings.Garage** | ลัง Garage | *(ไม่มี)* | Config ของที่อยู่ในลัง garage |
| **CrateSettings.CrateSettingsTypes** | Types | *(ไม่มี)* | Type definitions |

---

### Game Modules — ระบบ Skills (Modules.Game.Skills.*)

| โมดูล | หน้าที่ | รายละเอียด |
|--------|---------|-----------|
| **SkillsUI** | UI Skills | แสดงรายการ skill ทั้งหมด, level, progress |
| **SkillsProgressUI** | Progress Bar | แสดง XP bar, level up animation, shockwave effect |
| **XPFormula** | สูตร XP | คำนวณ XP ที่ต้องการต่อ level |
| **SkillsList** | รายการ Skill | เก็บ skill ทั้งหมด + rewards |
| **SkillsList.cook** | Skill ทำอาหาร | Skill tree สำหรับ steakhouse cook |
| **SkillsList.shelf_stocker** | Skill เติมของ | Skill tree — speed increase, extra box |
| **SkillsList.stamina** | Skill สแตมินา | Skill tree สำหรับ sprint stamina |
| **SkillsList.total_level** | Total Level | รวม level ทั้งหมด |
| **SkillsList.janitor** | Skill ภารโรง | Skill tree — unlock puddle types |
| **SkillsList.atm_hacker** | Skill แฮก | Skill tree สำหรับ ATM hacking |
| **SkillsList.farmer** | Skill เกษตร | Skill tree สำหรับ farming |
| **SkillsList.fishing** | Skill ตกปลา | Skill tree สำหรับ fishing |

---

### Game Modules — ระบบ Quest (Modules.Game.Quests.*)

| โมดูล | หน้าที่ | Net Events | รายละเอียด |
|--------|---------|-----------|-----------|
| **QuestsUI** | UI เควส | `get: claim_quest` | แสดงรายการเควส, progress, ปุ่ม claim reward |
| **QuestsData** | ข้อมูลเควส | *(ไม่มี)* | เก็บ quest definitions |
| **QuestInfoRewardsUI** | UI Rewards | *(ไม่มี)* | แสดง reward ของเควส |
| **Milestones.mopping** | เควสถูพื้น | | ถูพื้น X ครั้ง |
| **Milestones.work_num_jobs** | เควสทำงาน | | ทำงาน X ครั้ง |
| **Milestones.BadSignal** | Bad Signal | | เควส bad signal |
| **Milestones.pro_skimmer** | Pro Skimmer | | เควส skimmer |
| **Milestones.play_for_length** | เล่นนาน | | เล่นเกม X นาที |
| **Milestones.death_by_distance** | ตายไกล | | ตายจากระยะไกล |
| **Milestones.glass_cracking** | ทุบกระจก | | ทุบกระจก X ครั้ง |
| **Milestones.join_for_num_days** | เข้าเกม | | เข้าเกม X วัน |
| **Milestones.DrivingVehicleQuests** | ขับรถ | | ขับรถ X studs |
| **Milestones.PawnItems** | ขายของ | | ขายของที่ pawn shop |

---

### Game Modules — ระบบ Emotes/Animation (Modules.Game.Emotes.*)

| โมดูล | หน้าที่ | รายละเอียด |
|--------|---------|-----------|
| **EmotesUI** | UI Emotes | Radial menu เลือก emote |
| **EmotesList** | รายการ Emote | เก็บ emote ทั้งหมด + animation IDs |
| **AssassinationsList** | รายการ Assassination | เก็บ assassination/finisher animations |

### Multi-Player Animations (Modules.Game.MultiAnimations.*)

| โมดูล | หน้าที่ | รายละเอียด |
|--------|---------|-----------|
| **FinisherAnimationsUI** | UI Finisher | เลือก finisher animation |
| **MultiPlayerAnimation** | ระบบ Multi Anim | จัดการ animation ที่ต้อง sync 2 คน |
| **Types** | Type Defs | ชนิดข้อมูล multi animation |
| **Sequences.execution_1** | Execution 1 | Finisher sequence แบบ 1 |
| **Sequences.execution_2** | Execution 2 | Finisher sequence แบบ 2 |
| **Sequences.execution_3** | Execution 3 | Finisher sequence แบบ 3 |
| **Sequences.stomp_execution** | Stomp | เหยียบ finisher |
| **Sequences.headbutt** | Headbutt | โขก finisher |
| **Sequences.baseball_bat** | Baseball Bat | ตีด้วยไม้เบสบอล |
| **Sequences.mj** | MJ | MJ finisher |
| **Sequences.slap** | Slap | ตบ finisher |
| **Sequences.shoe_kiss** | Shoe Kiss | จูบรองเท้า finisher |
| **FinisherOverlays.LiveStreamUI** | Live Stream UI | Overlay แบบ live stream เมื่อทำ finisher |
| **FinisherOverlays.LiveStreamUI.Messages** | Messages | ข้อความ chat ใน live stream overlay |

---

### Game Modules — ระบบ Character (Modules.Game.Character.*)

| โมดูล | หน้าที่ | รายละเอียด |
|--------|---------|-----------|
| **Jumping** | กระโดด | จัดการ jump power, double jump |
| **AutomaticScalingEnabled** | Auto Scale | `get: fix_desync_hip_height` — แก้ hip height desync |
| **TestAntiTeleport** | Anti-TP | ตรวจจับ teleport cheat |
| **TemporarySeatWeldFix** | Seat Fix | แก้บัค seat weld |
| **OldTemporarySeatWeldFix** | Old Seat Fix | version เก่าของ seat fix |
| **WalkingSounds** | เสียงเดิน | เล่นเสียงเท้าตาม material |
| **CameraModifications** | Camera Mods | ปรับกล้องเพิ่มเติม |

---

### Game Modules — ระบบ Gangs (Modules.Game.Gangs.*)

| โมดูล | หน้าที่ | รายละเอียด |
|--------|---------|-----------|
| **GangUI** | UI แก๊ง | จัดการ gang — สร้าง/เข้าร่วม/ออก |
| **GangDataTypes** | Types | ชนิดข้อมูล gang |
| **GangUtils** | Utils | Helper functions สำหรับ gang |

---

### Game Modules — ระบบ Effects (Modules.Game.Effects.*)

| โมดูล | หน้าที่ | รายละเอียด |
|--------|---------|-----------|
| **Blood** | เลือด | Particle effect เลือดเมื่อโดนโจมตี |
| **Sparks** | ประกายไฟ | Spark particles |
| **Breakable** | ของแตก | `send: Net event` — แตกวัตถุ (กระจก etc.), particle + sound |
| **Explosion** | ระเบิด | Explosion effect + damage area |
| **FirecrackerExplosion** | ประทัดระเบิด | Firecracker specific explosion |
| **StaticShock** | ไฟฟ้าช็อต | Static shock visual effect |
| **Fire** | ไฟ | Fire particle effect (molotov, jerry can) |

---

### Game Modules — ระบบ World (Modules.Game.World.*)

| โมดูล | หน้าที่ | Net Events | รายละเอียด |
|--------|---------|-----------|-----------|
| **AnimatedRig** | NPC Animation | *(ไม่มี)* | เล่น animation บน NPC/rig ที่ไม่ใช่ player |
| **Dumpster** | ถังขยะ | *(ไม่มี)* | Interact กับถังขยะ |
| **SewerEntrance** | ทางเข้าท่อ | *(ไม่มี)* | ประตูเข้าท่อระบายน้ำ (VentDoor) |
| **SewersAmbience** | เสียงท่อ | *(ไม่มี)* | Ambient sound ในท่อระบายน้ำ |
| **Highlight** | Highlight | *(ไม่มี)* | Highlight effect บน objects |
| **ServerSwitchVan** | รถเปลี่ยน Server | `send: interact_server_switch_van` | เข้าไปในรถ → ย้าย server |
| **BasementDoor** | ประตูห้องใต้ดิน | *(ไม่มี)* | ประตูเข้า basement |
| **DirectTo** | นำทาง | *(ไม่มี)* | ระบบนำทางไปจุดต่างๆ |

---

### Game Modules — ระบบ UI (Modules.Game.UI.*)

| โมดูล | หน้าที่ | รายละเอียด |
|--------|---------|-----------|
| **Crosshair** | เป้าเล็ง | แสดง crosshair + bullet count, recoil animation |
| **RadialModule** | Radial Menu | เมนูวงกลม (emotes, options) |
| **SettingsUI** | ตั้งค่า | หน้าตั้งค่าเกม |
| **ProgressBar** | แถบ Progress | แถบ progress สำหรับงาน/กิจกรรม, มี bar types ต่างๆ |
| **HealthBar** | แถบเลือด | แสดง HP + ตัวเลข HP |
| **DamageIndicator** | ทิศโจมตี | แสดงทิศทางที่โดนโจมตี + damage overlay |
| **UISlider** | Slider | UI slider (ใช้ใน ATM, settings) |
| **InfoPromptUI** | Prompt ข้อมูล | แสดง popup ข้อมูล + ปุ่มปิด |
| **ConsumableBuyUI** | ซื้อ Consumable | UI ซื้อ consumable items |
| **SelectOptionUI** | เลือก Option | UI เลือกจากหลาย options |
| **TransitionUI** | Transition | หน้าจอ transition/loading, logo, session locked |
| **XPUI** | แสดง XP | แสดง XP ที่ได้รับ |
| **InterfaceVisibilityHandler** | ซ่อน UI | จัดการซ่อน/แสดง UI elements |
| **LevelUI** | Level Up | แสดง level up animation, XP text effect, shockwave |
| **NotificationsUI** | แจ้งเตือน | `hook: ฟัง event จาก server` — แสดง notification toast + image |
| **SidebarMenu** | เมนูด้านข้าง | Sidebar slide menu |
| **SubMenuBackground** | พื้นหลัง Sub | พื้นหลังสำหรับ sub-menus |
| **DisplayNotification** | Display Notif | แจ้งเตือนแบบ display |
| **PowerUpEffect** | Effect PowerUp | Visual effect เมื่อได้ power-up |
| **BuyPromptUI** | Prompt ซื้อ | Prompt ยืนยันการซื้อ |
| **Viewport** | Viewport | 3D viewport สำหรับแสดง model |
| **CombatLoggingUI** | Combat Log | แจ้งเตือน combat logging (ออกเกมตอนสู้) |
| **AwardUI** | Award | แสดง award/achievement animation |
| **CinematicUI** | Cinematic | แถบ cinematic (upper/lower bars) |
| **PassivesUI** | Passives | แสดง passive buffs/boosters ที่ active |
| **DisableKeybinds** | ปิด Keybinds | ปิดการใช้งาน keybinds ชั่วคราว |
| **Slideshow** | Slideshow | แสดง slideshow (tutorial, info) |
| **SelectPlayerUI** | เลือก Player | UI เลือกผู้เล่น (gift, trade) |
| **PingWarnerUI** | เตือน Ping | แจ้งเตือนเมื่อ ping สูง |
| **Spinner** | Spinner | Loading spinner animation |
| **ExtendDeviceUI** | Extend Device | UI สำหรับ mobile device |
| **WarningUI** | เตือน | แสดงข้อความเตือน |
| **CursorModeHint** | Cursor Hint | แสดง hint cursor mode |
| **TeleportingUI** | Teleporting | แสดง UI ระหว่าง teleport ไป server อื่น |
| **ProductsOfferFrame** | Offer | แสดง product offers |

---

### Game Modules — ระบบอื่นๆ

| โมดูล | หน้าที่ | Net Events | รายละเอียด |
|--------|---------|-----------|-----------|
| **Sprint** | วิ่ง/สแตมินา | `send: set_sprinting_1, replicate_stamina_bar_1` | ระบบวิ่ง, stamina bar, walk speed management, มี skill tree |
| **ShoulderCamera** | กล้องไหล่ | *(ไม่มี)* | Third-person shoulder camera, ซ้าย/ขวา, FOV adjust |
| **CrouchSystem** | ย่อตัว | *(ไม่มี)* | ระบบ crouch/ย่อตัว |
| **ToolUtil** | Tool Helpers | *(ไม่มี)* | Helper สำหรับจัดการ tools ที่ equip |
| **TouchButton** | ปุ่ม Touch | *(ไม่มี)* | ปุ่มสำหรับ mobile/touch |
| **Trajectory** | คำนวณวิถี | *(ไม่มี)* | คำนวณวิถีกระสุน/ของที่ขว้าง |
| **CashEffect** | Effect เงิน | *(ไม่มี)* | Animation เมื่อได้เงิน |
| **MoneyUI** | UI เงิน | *(ไม่มี)* | แสดงจำนวนเงิน |
| **InteriorSoundZone** | เสียงภายใน | *(ไม่มี)* | เปลี่ยนเสียง ambient เมื่อเข้าอาคาร |
| **ResetCallback** | Reset | *(ไม่มี)* | จัดการ character reset |
| **SplashScreen** | จอเริ่ม | *(ไม่มี)* | หน้าจอ loading/splash |
| **CharacterBillboardGui** | ป้ายหัว | *(ไม่มี)* | Billboard GUI เหนือหัวตัวละคร (ชื่อ, level) |
| **SafeZone** | โซนปลอดภัย | *(ไม่มี)* | ตรวจจับเข้า/ออก safe zone — ห้ามต่อสู้ |
| **NPC** | NPC | *(ไม่มี)* | จัดการ NPC, dialog, interaction |
| **DamageClient** | ระบบ Damage | *(ไม่มี)* | คำนวณ/แสดง damage |
| **AlternateInputHandler** | Input อื่น | *(ไม่มี)* | จัดการ input ทางเลือก (controller) |
| **HitDetection** | ตรวจจับโดน | *(ไม่มี)* | Raycast/hitbox detection |
| **DownedClient** | ล้ม/หมดสติ | *(ไม่มี)* | ระบบ downed state (ก่อนตาย) |
| **Job** | Job Manager | *(ไม่มี)* | จัดการ job state กลาง |
| **Admin** | Admin | *(ไม่มี)* | ระบบ admin — spectate, controls |
| **AirDrop** | AirDrop | `hook: airdrop_spawn` | รับ notification เมื่อ airdrop ลง, แสดง notification + sound, มี states: point, landing_stamp, drop_type, destroy_stamp, opened |
| **DeathScreen** | จอตาย | `send: death_screen_request_respawn` | แสดง death screen, ปุ่ม respawn, revenge pack |
| **DayNightCycle** | กลางวัน/คืน | *(ไม่มี)* | ระบบวันเวลาในเกม |
| **AmbientNoise** | เสียงรอบข้าง | *(ไม่มี)* | เสียง ambient ตาม location (indoors/outdoors) |
| **SafeLog** | Safe Log | *(ไม่มี)* | ปุ่ม safe log (ออกเกมปลอดภัย) |
| **Keybinds** | ปุ่มกด | *(ไม่มี)* | จัดการ keybinds ทั้งหมด, touch buttons, hint UI |
| **Keybinds.KeybindUIHints** | Hint ปุ่ม | *(ไม่มี)* | แสดง keybind hints บนหน้าจอ |
| **DoorClient** | ประตู | `send: request_door_ownership` | เมื่อ touch DoorBase → ส่ง request, debounce 0.3s |
| **PolicyInfo** | Policy | *(ไม่มี)* | จัดการ policy info (China etc.) |
| **ChatMessages** | Chat | *(ไม่มี)* | ระบบ chat messages |
| **Ragdoll** | Ragdoll | `send: end_ragdoll_early` | ระบบล้ม ragdoll, สามารถยกเลิกก่อนเวลา |
| **Ragdoll.RagdollTypes** | Types | *(ไม่มี)* | ชนิด ragdoll (death, hit, explosion) |
| **StockTimes** | Stock Times | *(ไม่มี)* | จัดการ stock restock timing |
| **StockTimesUtil** | Stock Utils | *(ไม่มี)* | `get_product_for_length()` หา product สำหรับ restock |
| **SellingPointBeacon** | จุดขาย | *(ไม่มี)* | Beacon zone สำหรับจุดขายของ |
| **DroppedItem** | ของตกพื้น | `get: pickup_dropped_item` | หยิบของที่ตกพื้น — ส่ง Instance |
| **ConsumableShop** | ร้าน Consumable | *(ไม่มี)* | ร้านขาย consumable — เข้าโซน → เปิด ConsumableBuyUI, มี unlock_level check |
| **SatelliteDish** | จานดาวเทียม | *(ไม่มี)* | interact กับจานดาวเทียม |
| **CarDealershipRotation** | หมุนรถ | *(ไม่มี)* | รถหมุนใน car dealership |
| **Fishing.FishingPlot** | แปลงตกปลา | *(ไม่มี)* | จุดตกปลาใน workspace |
| **Fishing.FishingUtils** | Utils ตกปลา | *(ไม่มี)* | Helper สำหรับ fishing |

---

### Game Modules — ระบบ Ads/Analytics

| โมดูล | หน้าที่ | รายละเอียด |
|--------|---------|-----------|
| **Ads.TVVideoAdsClient** | โฆษณา TV | แสดง video ads บน TV ในเกม |
| **Ads.AdClient** | Ad Client | จัดการ ad system |
| **Analytics.Funnel** | Funnel | ติดตาม funnel analytics |
| **Analytics.UpvoteBoard** | Upvote | กระดาน upvote |

---

### Game Modules — ระบบ Referral/Booster

| โมดูล | หน้าที่ | รายละเอียด |
|--------|---------|-----------|
| **Referral.ReferralUI** | UI Referral | ระบบเชิญเพื่อน |
| **Referral.ReferralDataTypes** | Types | ชนิดข้อมูล referral |
| **Booster.Boosters** | Boosters | `hook: boosters` — แสดง/อัพเดท active boosters |
| **Booster.BoostersInfo** | Info | เก็บข้อมูล booster types |

---

### Game Modules — ระบบ Gunsmith/Garage

| โมดูล | หน้าที่ | รายละเอียด |
|--------|---------|-----------|
| **GunsmithSystem.GunsmithBeaconClient** | Gunsmith | Beacon zone สำหรับ gunsmith — customize อาวุธ |
| **GarageSystem.GarageClient** | Garage | ระบบ garage — เก็บ/เอารถออก |

---

### Game Modules — ระบบ Visuals/GameInfo

| โมดูล | หน้าที่ | รายละเอียด |
|--------|---------|-----------|
| **Visuals.CastVisuals** | Cast Visuals | Visual effects สำหรับ cast (ตกปลา etc.) |
| **GameInfo.Updates** | Updates | แสดง update notes |
| **GameInfo.FlagManager** | Feature Flags | จัดการ feature flags (FLAG_*) |
| **GameInfo.PlaceInfo** | Place Info | ข้อมูล place/server |
| **GameInfo.GlobalNotification** | Global Notif | รับ global notification จาก server |
| **GameInfo.RepairExtras** | Repair Info | คำนวณค่าซ่อม — durability ลดลงทุกครั้งที่ซ่อม, ราคาเพิ่มขึ้น, พังถ้าซ่อมเยอะ |
| **DataTypes.ItemDataTypes** | Item Types | ชนิดข้อมูล items ทั้งหมด |
| **Tools.BoxTool** | Box Tool | Tool สำหรับถือกล่อง (shelf stocking job) |

---

## Workspace — สถานที่สำคัญ

### ร้านค้า
Steak House, Jack's Hardware Store, Gun Store, Bike Shop, Pawn Shop, Urban Store, Barber Shop, BoxClub Store, Quick11

### Shop Zones (มี ProximityPrompt)
ShopZone_Illegal, ShopZone_BasketballCourtDealer, ShopZone_IllegalNightclub, ShopZone_Quick11, ShopZone_Burger, ShopZone_Hardware, ShopZone_Hospital

### Beacons
- `Beacon` — สมัครงาน (มี TouchPart + JobIndex attribute)
- `SellingPointBeacon` — จุดขายของ
- `SellFishBeacon` — ขายปลา
- `BurgePlaceBeacon` — ร้านเบอร์เกอร์

### Interactive Objects
- `PickUpPrompt` (ProximityPrompt) — หยิบของ/กล่อง
- `FinishPrompt` (ProximityPrompt) — ส่งงาน
