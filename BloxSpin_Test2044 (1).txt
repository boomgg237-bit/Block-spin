getgenv().SkipBypassCheck2044 = true
type RequestOptions__DARKLUA_TYPE_a = {
    Url:string,
    Method:'GET' | 'HEAD' | 'POST' | 'PUT' | 'DELETE' | 'OPTIONS' | 'PATCH'?,
    Body:string?,
    Headers:{
        [string]:string
    }?,
    Cookies:{
        [string]:string
    }?,
    Timeout:number?
}
type Response__DARKLUA_TYPE_b = {
    Success:boolean,
    Body:string,
    StatusCode:number,
    StatusMessage:string,
    Headers:{
        [string]:string
    }
}
type QuadDrawing__DARKLUA_TYPE_c = {
    Visible:boolean,
    Color:Color3,
    Transparency:number,
    PointA:Vector2,
    PointB:Vector2,
    PointC:Vector2,
    PointD:Vector2,
    Remove:(QuadDrawing__DARKLUA_TYPE_c)->()
}
type LineDrawing__DARKLUA_TYPE_d = {
    Visible:boolean,
    Color:Color3,
    Transparency:number,
    Thickness:number,
    From:Vector2,
    To:Vector2,
    Remove:(LineDrawing__DARKLUA_TYPE_d)->()
}
type TextDrawing__DARKLUA_TYPE_e = {
    Visible:boolean,
    Color:Color3,
    Transparency:number,
    Text:string,
    Position:Vector2,
    Size:number,
    Center:boolean,
    Outline:boolean,
    Font:number,
    Remove:(TextDrawing__DARKLUA_TYPE_e)->()
}
type HighlightInstance__DARKLUA_TYPE_f = Highlight type DrawingRecord__DARKLUA_TYPE_g = {
    key:string,
    kind:string,
    object:QuadDrawing__DARKLUA_TYPE_c | LineDrawing__DARKLUA_TYPE_d | TextDrawing__DARKLUA_TYPE_e,
    player:Player?,
    character:Model?,
    root:BasePart?,
    metadata:any
}
type PlayerKeySet__DARKLUA_TYPE_h = {
    [string]:true
}
type HighlightRecord__DARKLUA_TYPE_i = {
    player:Player,
    character:Model,
    highlight:HighlightInstance__DARKLUA_TYPE_f
}
type BoxFacade__DARKLUA_TYPE_j = {
    Keys:{
        string
    },
    Destroy:(BoxFacade__DARKLUA_TYPE_j)->(),
    Destroyed:boolean
}
type HighlightFacade__DARKLUA_TYPE_k = {
    Instance:HighlightInstance__DARKLUA_TYPE_f?,
    Destroy:(HighlightFacade__DARKLUA_TYPE_k)->(),
    Destroyed:boolean
}
type TracerFacade__DARKLUA_TYPE_l = {
    Key:string?,
    Destroy:(TracerFacade__DARKLUA_TYPE_l)->(),
    Destroyed:boolean
}
type PlayerVisualEntry__DARKLUA_TYPE_m = {
    Character:Model,
    Root:BasePart,
    Box:BoxFacade__DARKLUA_TYPE_j?,
    HighlightObject:HighlightFacade__DARKLUA_TYPE_k?,
    TracerObject:TracerFacade__DARKLUA_TYPE_l?
}
type CustomHandle__DARKLUA_TYPE_n = {
    Id:number,
    Destroy:(CustomHandle__DARKLUA_TYPE_n)->(),
    Destroyed:boolean
}
type CustomEntry__DARKLUA_TYPE_o = {
    Id:number,
    Update:(number)->(),
    Validate:((number)->boolean)?,
    Cleanup:((CustomHandle__DARKLUA_TYPE_n?)->())?,
    Handle:CustomHandle__DARKLUA_TYPE_n?
}
type BoxUpdateParams__DARKLUA_TYPE_p = {
    Pivot:CFrame,
    Size:Vector3,
    Distance:number?,
    Color:Color3?,
    Enabled:boolean?,
    Transparency:number?,
    StaticSize:Vector2?,
    Channel:string?,
    ZIndex:number?,
    ZIndexOffset:number?
}
type BoxLineUpdateParams__DARKLUA_TYPE_q = {
    Pivot:CFrame,
    Size:Vector3,
    Distance:number?,
    Color:Color3?,
    Enabled:boolean?,
    Transparency:number?,
    Index:number,
    Channel:string?,
    ZIndex:number?,
    ZIndexOffset:number?,
    Thickness:number?
}
type TextUpdateParams__DARKLUA_TYPE_r = {
    Text:string?,
    Color:Color3?,
    Position:Vector3?,
    ScreenPosition:Vector2?,
    Distance:number?,
    Enabled:boolean?,
    Font:number?,
    Size:number?,
    VerticalOffsetMultiplier:number?,
    Channel:string?,
    ZIndex:number?,
    ZIndexOffset:number?,
    Transparency:number?
}
type TracerUpdateParams__DARKLUA_TYPE_s = {
    FromWorld:Vector3?,
    ToWorld:Vector3,
    Thickness:number?,
    Color:Color3?,
    Enabled:boolean?,
    Distance:number?,
    Channel:string?,
    ZIndex:number?,
    ZIndexOffset:number?,
    Transparency:number?
}
type BoxCornerUpdateParams__DARKLUA_TYPE_t = BoxUpdateParams__DARKLUA_TYPE_p & {
    CornerSize:number?,
    Thickness:number?
}
type MarkerObject__DARKLUA_TYPE_u = {
    Object:Part,
    Destroy:(self:MarkerObject__DARKLUA_TYPE_u)->(),
    SetColor:(self:MarkerObject__DARKLUA_TYPE_u,
    Color:Color3)->(),
    SetPosition:(self:MarkerObject__DARKLUA_TYPE_u,
    Position:Vector3)->()
}
type IRay__DARKLUA_TYPE_v = {
    Draw:(self:IRay__DARKLUA_TYPE_v,
    Origin:Vector3,
    End:Vector3)->(),
    Create:(self:IRay__DARKLUA_TYPE_v,
    Origin:Vector3,
    End:Vector3)->{
        Origin:Vector3,
        End:Vector3,
        Color3:Color3,
        AlwaysOnTop:boolean,
        Transparency:number
    }
}
type IBox__DARKLUA_TYPE_w = {
    Draw:(self:IBox__DARKLUA_TYPE_w,
    Transform:CFrame,
    Size:Vector3,
    DrawTriangles:boolean)->(),
    Create:(self:IBox__DARKLUA_TYPE_w,
    Transform:CFrame,
    Size:Vector3,
    DrawTriangles:boolean)->{
        Transform:CFrame,
        Size:Vector3,
        DrawTriangles:boolean,
        Color3:Color3,
        AlwaysOnTop:boolean,
        Transparency:number,
        Enabled:boolean,
        Destroy:boolean
    }
}
type IPlane__DARKLUA_TYPE_x = {
    Draw:(self:IPlane__DARKLUA_TYPE_x,
    Position:Vector3,
    Normal:Vector3,
    Size:Vector3)->(),
    Create:(self:IPlane__DARKLUA_TYPE_x,
    Position:Vector3,
    Normal:Vector3,
    Size:Vector3)->{
        Position:Vector3,
        Normal:Vector3,
        Size:Vector3,
        DrawTriangles:boolean,
        Color3:Color3,
        AlwaysOnTop:boolean,
        Transparency:number,
        Enabled:boolean,
        Destroy:boolean
    }
}
type IWedge__DARKLUA_TYPE_y = {
    Draw:(self:IWedge__DARKLUA_TYPE_y,
    Transform:CFrame,
    Size:Vector3,
    DrawTriangles:boolean)->(),
    Create:(self:IWedge__DARKLUA_TYPE_y,
    Transform:CFrame,
    Size:Vector3,
    DrawTriangles:boolean)->{
        Transform:CFrame,
        Size:Vector3,
        DrawTriangles:boolean,
        Color3:Color3,
        AlwaysOnTop:boolean,
        Transparency:number,
        Enabled:boolean,
        Destroy:boolean
    }
}
type ICircle__DARKLUA_TYPE_z = {
    Draw:(self:ICircle__DARKLUA_TYPE_z,
    Transform:CFrame,
    Radius:number,
    Subdivisions:number,
    Angle:number,
    ConnectToStart:boolean?)->(),
    Create:(self:ICircle__DARKLUA_TYPE_z,
    Transform:CFrame,
    Radius:number,
    Subdivisions:number,
    Angle:number,
    ConnectToStart:boolean?)->{
        Transform:CFrame,
        Radius:number,
        Subdivisions:number,
        ConnectToStart:boolean?,
        Color3:Color3,
        AlwaysOnTop:boolean,
        Transparency:number,
        Enabled:boolean,
        Destroy:boolean
    }
}
type ISphere__DARKLUA_TYPE_A = {
    Draw:(self:ISphere__DARKLUA_TYPE_A,
    Transform:CFrame,
    Radius:number,
    Subdivisions:number,
    Angle:number)->(),
    Create:(self:ISphere__DARKLUA_TYPE_A,
    Transform:CFrame,
    Radius:number,
    Subdivisions:number,
    Angle:number)->{
        Transform:CFrame,
        Radius:number,
        Subdivisions:number,
        Angle:number,
        Color3:Color3,
        AlwaysOnTop:boolean,
        Transparency:number,
        Enabled:boolean,
        Destroy:boolean
    }
}
type ICylinder__DARKLUA_TYPE_B = {
    Draw:(self:ICylinder__DARKLUA_TYPE_B,
    Transform:CFrame,
    Radius:number,
    Length:number,
    Subdivisions:number)->(),
    Create:(self:ICylinder__DARKLUA_TYPE_B,
    Transform:CFrame,
    Radius:number,
    Length:number,
    Subdivisions:number)->{
        Transform:CFrame,
        Radius:number,
        Length:number,
        Subdivisions:number,
        Color3:Color3,
        AlwaysOnTop:boolean,
        Transparency:number,
        Enabled:boolean,
        Destroy:boolean
    }
}
type ICapsule__DARKLUA_TYPE_C = {
    Draw:(self:ICapsule__DARKLUA_TYPE_C,
    Transform:CFrame,
    Radius:number,
    Length:number,
    Subdivisions:number)->(),
    Create:(self:ICapsule__DARKLUA_TYPE_C,
    Transform:CFrame,
    Radius:number,
    Length:number,
    Subdivisions:number)->{
        Transform:CFrame,
        Radius:number,
        Length:number,
        Subdivisions:number,
        Color3:Color3,
        AlwaysOnTop:boolean,
        Transparency:number,
        Enabled:boolean,
        Destroy:boolean
    }
}
type ICone__DARKLUA_TYPE_D = {
    Draw:(self:ICone__DARKLUA_TYPE_D,
    Transform:CFrame,
    Radius:number,
    Length:number,
    Subdivisions:number)->(),
    Create:(self:ICone__DARKLUA_TYPE_D,
    Transform:CFrame,
    Radius:number,
    Length:number,
    Subdivisions:number)->{
        Transform:CFrame,
        Radius:number,
        Length:number,
        Subdivisions:number,
        Color3:Color3,
        AlwaysOnTop:boolean,
        Transparency:number,
        Enabled:boolean,
        Destroy:boolean
    }
}
type IArrow__DARKLUA_TYPE_E = {
    Draw:(self:IArrow__DARKLUA_TYPE_E,
    Origin:Vector3,
    End:Vector3,
    Radius:number,
    Length:number,
    Subdivisions:number)->(),
    Create:(self:IArrow__DARKLUA_TYPE_E,
    Origin:Vector3,
    End:Vector3,
    Radius:number,
    Length:number,
    Subdivisions:number)->{
        Origin:Vector3,
        End:Vector3,
        Radius:number,
        Length:number,
        Subdivisions:number,
        Color3:Color3,
        AlwaysOnTop:boolean,
        Transparency:number,
        Enabled:boolean,
        Destroy:boolean
    }
}
type IMesh__DARKLUA_TYPE_F = {
    Draw:(self:IMesh__DARKLUA_TYPE_F,
    Transform:CFrame,
    Size:Vector3,
    Vertices:{
    },
    Faces:{
    })->(),
    Create:(self:IMesh__DARKLUA_TYPE_F,
    Transform:CFrame,
    Size:Vector3,
    Vertices:{
    },
    Faces:{
    })->{
        Transform:CFrame,
        Size:Vector3,
        Vertices:{
        },
        Faces:{
        },
        Color3:Color3,
        AlwaysOnTop:boolean,
        Transparency:number,
        Enabled:boolean,
        Destroy:boolean
    }
}
type ILine__DARKLUA_TYPE_G = {
    Draw:(self:ILine__DARKLUA_TYPE_G,
    Transform:CFrame,
    Length:number)->(),
    Create:(self:ILine__DARKLUA_TYPE_G,
    Transform:CFrame,
    Length:number)->{
        Transform:CFrame,
        Length:number,
        Color3:Color3,
        AlwaysOnTop:boolean,
        Transparency:number,
        Enabled:boolean,
        Destroy:boolean
    }
}
type IVolumeCone__DARKLUA_TYPE_H = {
    Draw:(self:IVolumeCone__DARKLUA_TYPE_H,
    Transform:CFrame,
    Radius:number,
    Length:number)->(),
    Create:(self:IVolumeCone__DARKLUA_TYPE_H,
    Transform:CFrame,
    Radius:number,
    Length:number)->{
        Transform:CFrame,
        Radius:number,
        Length:number,
        Color3:Color3,
        AlwaysOnTop:boolean,
        Transparency:number,
        Enabled:boolean,
        Destroy:boolean
    }
}
type IVolumeBox__DARKLUA_TYPE_I = {
    Draw:(self:IVolumeBox__DARKLUA_TYPE_I,
    Transform:CFrame,
    Size:Vector3)->(),
    Create:(self:IVolumeBox__DARKLUA_TYPE_I,
    Transform:CFrame,
    Size:Vector3)->{
        Transform:CFrame,
        Size:Vector3,
        Color3:Color3,
        AlwaysOnTop:boolean,
        Transparency:number,
        Enabled:boolean,
        Destroy:boolean
    }
}
type IVolumeSphere__DARKLUA_TYPE_J = {
    Draw:(self:IVolumeSphere__DARKLUA_TYPE_J,
    Transform:CFrame,
    Radius:number)->(),
    Create:(self:IVolumeSphere__DARKLUA_TYPE_J,
    Transform:CFrame,
    Radius:number)->{
        Transform:CFrame,
        Radius:number,
        Color3:Color3,
        AlwaysOnTop:boolean,
        Transparency:number,
        Enabled:boolean,
        Destroy:boolean
    }
}
type IVolumeCylinder__DARKLUA_TYPE_K = {
    Draw:(self:IVolumeCylinder__DARKLUA_TYPE_K,
    Transform:CFrame,
    Radius:number,
    Length:number,
    InnerRadius:number?,
    Angle:number?)->(),
    Create:(self:IVolumeCylinder__DARKLUA_TYPE_K,
    Transform:CFrame,
    Radius:number,
    Length:number,
    InnerRadius:number?,
    Angle:number?)->{
        Transform:CFrame,
        Radius:number,
        Length:number,
        InnerRadius:number?,
        Angle:number?,
        Color3:Color3,
        AlwaysOnTop:boolean,
        Transparency:number,
        Enabled:boolean,
        Destroy:boolean
    }
}
type IVolumeArrow__DARKLUA_TYPE_L = {
    Draw:(self:IVolumeArrow__DARKLUA_TYPE_L,
    Origin:Vector3,
    End:Vector3,
    CylinderRadius:number,
    ConeRadius:number,
    Length:number,
    UseCylinder:boolean?)->(),
    Create:(self:IVolumeArrow__DARKLUA_TYPE_L,
    Origin:Vector3,
    End:Vector3,
    CylinderRadius:number,
    ConeRadius:number,
    Length:number,
    UseCylinder:boolean?)->{
        Origin:Vector3,
        End:Vector3,
        CylinderRadius:number,
        ConeRadius:number,
        Length:number,
        UseCylinder:boolean?,
        Color3:Color3,
        AlwaysOnTop:boolean,
        Transparency:number,
        Enabled:boolean,
        Destroy:boolean
    }
}
type IText__DARKLUA_TYPE_M = {
    Draw:(self:IText__DARKLUA_TYPE_M,
    Origin:Vector3,
    Text:string,
    Size:number?)->(),
    Create:(self:IText__DARKLUA_TYPE_M,
    Origin:Vector3,
    Text:string,
    Size:number?)->{
        Origin:Vector3,
        Text:string,
        Size:number?,
        Color3:Color3,
        AlwaysOnTop:boolean,
        Transparency:number,
        Enabled:boolean,
        Destroy:boolean
    }
}
type ICFrame__DARKLUA_TYPE_N = {
    Draw:(self:ICFrame__DARKLUA_TYPE_N,
    Transform:CFrame,
    Scale:number)->(),
    Create:(self:ICFrame__DARKLUA_TYPE_N,
    Transform:CFrame,
    Scale:number)->{
        Transform:CFrame,
        Scale:number,
        AlwaysOnTop:boolean,
        Transparency:number,
        Enabled:boolean,
        Destroy:boolean
    }
}
type IRoundedFrustum__DARKLUA_TYPE_O = {
    Draw:(self:IRoundedFrustum__DARKLUA_TYPE_O,
    Transform:CFrame,
    Radius0:number,
    Radius1:number,
    Length:number,
    Subdivisions:number)->(),
    Create:(self:IRoundedFrustum__DARKLUA_TYPE_O,
    Transform:CFrame,
    Radius0:number,
    Radius1:number,
    Length:number,
    Subdivisions:number)->{
        Transform:CFrame,
        Radius0:number,
        Radius1:number,
        Length:number,
        Subdivisions:number,
        Color3:Color3,
        AlwaysOnTop:boolean,
        Transparency:number,
        Enabled:boolean,
        Destroy:boolean
    }
}
type IStyles__DARKLUA_TYPE_P = {
    Color:string,
    Transparency:number,
    AlwaysOnTop:boolean
}
type IStyle__DARKLUA_TYPE_Q = 'Color3' | 'Transparency' | 'AlwaysOnTop' type ICeive__DARKLUA_TYPE_R = {
    ActiveRays:number,
    ActiveInstances:number,
    PushProperty:(Property:IStyle__DARKLUA_TYPE_Q,
    Value:any?)->(),
    PopProperty:(Property:IStyle__DARKLUA_TYPE_Q)->any?,
    SetStyle:(Color:Color3?,
    Transparency:number?,
    AlwaysOnTop:boolean?)->(),
    AddDebrisInSeconds:(Seconds:number,
    Callback:()->())->(),
    AddDebrisInFrames:(Frames:number,
    Callback:()->())->(),
    SetEnabled:(Value:boolean)->(),
    RemoveAdornments:()->(),
    DoCleaning:()->(),
    ScheduleCleaning:()->(),
    TweenProperies:(Properties:{
    },
    Goal:{
    },
    TweenInfo:TweenInfo)->()->(),
    Init:()->(),
    Styles:IStyles__DARKLUA_TYPE_P,
    Ray:IRay__DARKLUA_TYPE_v,
    Line:ILine__DARKLUA_TYPE_G,
    Box:IBox__DARKLUA_TYPE_w,
    Plane:IPlane__DARKLUA_TYPE_x,
    Wedge:IWedge__DARKLUA_TYPE_y,
    Circle:ICircle__DARKLUA_TYPE_z,
    Sphere:ISphere__DARKLUA_TYPE_A,
    Cylinder:ICylinder__DARKLUA_TYPE_B,
    Capsule:ICapsule__DARKLUA_TYPE_C,
    Cone:ICone__DARKLUA_TYPE_D,
    Arrow:IArrow__DARKLUA_TYPE_E,
    Mesh:IMesh__DARKLUA_TYPE_F,
    Text:IText__DARKLUA_TYPE_M,
    CFrame:ICFrame__DARKLUA_TYPE_N,
    RoundedFrustum:IRoundedFrustum__DARKLUA_TYPE_O,
    VolumeCone:IVolumeCone__DARKLUA_TYPE_H,
    VolumeBox:IVolumeBox__DARKLUA_TYPE_I,
    VolumeSphere:IVolumeSphere__DARKLUA_TYPE_J,
    VolumeCylinder:IVolumeCylinder__DARKLUA_TYPE_K,
    VolumeArrow:IVolumeArrow__DARKLUA_TYPE_L
}
local __DARKLUA_BUNDLE_MODULES
__DARKLUA_BUNDLE_MODULES = {
    cache = {
    },
    load = function(m)
        if not __DARKLUA_BUNDLE_MODULES.cache[m]then
             __DARKLUA_BUNDLE_MODULES.cache[m] = {
                c = __DARKLUA_BUNDLE_MODULES[m]()
            }
        end
        return __DARKLUA_BUNDLE_MODULES.cache[m].c
     end
}do
     function __DARKLUA_BUNDLE_MODULES.a()
        local HttpService = game:GetService('HttpService')
        local env = getfenv()
        local http_request = rawget(env, 'http_request')
        local plainRequest = rawget(env, 'request')
        local syn = rawget(env, 'syn')
        local httpLib = rawget(env, 'http')
        local fluxus = rawget(env, 'fluxus')
        local krnl = rawget(env, 'krnl')
        local sharedTable = rawget(env, 'shared')
        local rconsoleprintFn = rawget(env, 'rconsoleprint')
        local warnFn = (type(env.warn) == 'function' and env.warn) or print
        local taskLib = rawget(env, 'task')
        local waitFn = (type(env.wait) == 'function' and env.wait) or function(seconds)
            if seconds then
                 local target = os.clock() + seconds
                repeat
                 until os.clock() >= target
             end
         end
        local taskWait = taskLib and taskLib.wait or waitFn
        local taskSpawn = taskLib and taskLib.spawn or function(callback, ...)
            local thread = coroutine.create(callback)
            local ok, err = coroutine.resume(thread, ...)
            if not ok then
                 warnFn(err)
            end
         end
        local SecureRequest = {
        }
        local function resolveRequestImpl()
            local impl = nil
            if type(http_request) == 'function' then
                 impl = http_request
             elseif  type(request) == 'function' then
                 impl = request
             elseif  type(plainRequest) == 'function' then
                 impl = plainRequest
             elseif  syn and type(syn.request) == 'function' then
                 impl = syn.request
             elseif  type(httpLib) == 'table' and type(httpLib.request) == 'function' then
                 impl = httpLib.request
             elseif  fluxus and type(fluxus.request) == 'function' then
                 impl = fluxus.request
             elseif  krnl and type(krnl.request) == 'function' then
                 impl = krnl.request
             end
            return impl
         end
        local BaseRequest = resolveRequestImpl()
        assert(type(BaseRequest) == 'function', [[[secure_request] No HTTP request implementation is available]])
        local RETRYABLE_STATUS = {
            [408] = true,
            [425] = true,
            [429] = true,
            [500] = true,
            [502] = true,
            [503] = true,
            [504] = true,
            [522] = true,
            [524] = true
        }
        local INITIAL_DELAY = 0.5
        local MAX_DELAY = 10
        local function shallowCopy(dict:{
                [string]:any
            })
            local copy = {
            }
            for key, value in pairs(dict)do
                 copy[key] = value
             end
            return copy
         end
        local function sanitizeUrl(url:string)
            :string
            if#url <= 120 then
                 return url
             end
            return url:sub(1, 117) .. '...'
         end
        local function consoleMessage(text:string)
            if type(rconsoleprintFn) == 'function' then
                 rconsoleprintFn(text .. '\n')
            else
                 warnFn(text)
            end
         end
        local function startNotifier(method:string, url:string)
            :()->()
            local overlay = sharedTable and sharedTable.StatusText or nil
            local previousText = overlay and overlay.Text or nil
            local message = ("[HTTP]Waiting for %s %s"):format(method, sanitizeUrl(url))
            local active = true taskSpawn(function()
                taskWait(1)if not active then
                     return
                 end
                if overlay then
                     overlay.Text = message
                 else
                     consoleMessage(message)
                end
             end)
            return function()
                active = false
                if overlay and previousText and overlay.Text == message then
                     overlay.Text = previousText
                 end
             end
         end
        local function isRetryable(response:Response__DARKLUA_TYPE_b?, err:string?)
            :boolean
            if err then
                 return true
             end
            if not response then
                 return true
             end
            local statusCode = response.StatusCode
            if response.Success and statusCode and statusCode >= 200 and statusCode < 400 then
                 return false
             end
            if statusCode == nil then
                 return not response.Success
             end
            if RETRYABLE_STATUS[statusCode]then
                 return true
             end
            if statusCode >= 500 then
                 return true
             end
            return false
         end function SecureRequest.request(options:RequestOptions__DARKLUA_TYPE_a)
            :Response__DARKLUA_TYPE_b
            assert(type(options) == 'table', 'secure_request.request expects an options table')
            assert(type(options.Url) == 'string', 'secure_request.request requires options.Url')
            local normalized = shallowCopy(options)
            local timeout = normalized.Timeout
            normalized.Timeout = nil normalized.Method = string.upper(normalized.Method or 'GET')
            local startTime = os.clock()
            local attempt = 0
            local notifierDone = startNotifier(normalized.Method, normalized.Url)
            local lastError:string? = nil
            while true do
                 attempt+=1
                local success, responseOrError = pcall(BaseRequest, normalized)
                if success then
                     local response = responseOrError :: Response__DARKLUA_TYPE_b
                    if response and not isRetryable(response)then
                         notifierDone()
                        return response
                     end lastError = response and ("HTTP %s %s"):format(response.StatusCode or '?', response.StatusMessage or '')
                else
                     lastError = tostring(responseOrError)
                end
                if timeout and (os.clock() - startTime) >= timeout then
                     notifierDone()
                    error(("[secure_request]Request timed out after %d attempts: %s"):format(attempt, lastError or 'Unknown error'))
                end taskWait(math.min(INITIAL_DELAY * 2 ^ math.min(attempt, 5), MAX_DELAY) + math.random() * 0.25)
            end
         end function SecureRequest:HttpGet(url:string, nocache:boolean?, timeoutSeconds:number?)
            :string
            assert(type(url) == 'string', 'secure_request:HttpGet expects a URL string')
            local targetUrl = url
            if nocache then
                 local sep = url:find('?', 1, true) and '&' or '?'
                targetUrl = ("%s%scachebuster=%s"):format(url, sep, HttpService:GenerateGUID(false))
            end
            local response = SecureRequest.request({
                Url = targetUrl,
                Method = 'GET',
                Timeout = timeoutSeconds
            })
            if response.Success then
                 return response.Body
             end error((`[secure_request]HttpGet failed(HTTP %s %s)`):format(response.StatusCode or '?', response.StatusMessage or ''))
        end
        return table.freeze(SecureRequest)
    end function __DARKLUA_BUNDLE_MODULES.b()
        local Webhooks = {
        }
        local Default = {
            username = 'Sasware Webhook',
            avatar_url = 'https://i.ibb.co/Xf3j8wTD/Sasware-Logo-1.png'
        }
        local HttpService = game:GetService('HttpService')
        function Webhooks._ConstructEmbed(Data)
            local Embed = {
                title = Data.title or 'No Title',
                description = Data.description or 'No Description',
                color = Data.color or 0xffffff,
                timestamp = os.date('!%Y-%m-%dT%H:%M:%SZ')
            }
            if Data.footer then
                 Embed.footer = {
                    text = Data.footer.text or 'No Footer',
                    icon_url = Data.footer.icon_url
                }
            end
            if Data.fields then
                 Embed.fields = {
                }
                for _, field in ipairs(Data.fields)do
                     table.insert(Embed.fields, {
                        name = field.name or 'No Name',
                        value = field.value or 'No Value',
                        inline = field.inline or false
                    })
                end
             end
            return Embed
         end function Webhooks._Construct(Data)
            local Payload = {
                username = Data.username or Default.username,
                avatar_url = Data.avatar_url or Default.avatar_url,
                content = Data.content or '',
                embeds = {
                }
            }
            if Data.embeds then
                 for _, embedData in ipairs(Data.embeds)do
                     table.insert(Payload.embeds, Webhooks._ConstructEmbed(embedData))
                end
             end
            return HttpService:JSONEncode(Payload)
        end function Webhooks.Color3ToDecimal(Color)
            if not Color or not Color.R or not Color.G or not Color.B then
                 error('Invalid Color3 value provided.')
            end
            return (Color.R * 255) * 65536 + (Color.G * 255) * 256 + (Color.B * 255)
        end function Webhooks.SendWebhook(Data)
            local Url = Data.url
            if not Url or type(Url) ~= 'string' then
                 error('Invalid webhook URL provided.')
            end
            local Payload = Webhooks._Construct(Data)
            local Success, Response = pcall(function()
                return request({
                    Url = Url,
                    Method = 'POST',
                    Headers = {
                        ['Content-Type'] = 'application/json'
                    },
                    Body = Payload
                })
            end)
            if not Success then
                 warn('Failed to send webhook:', Response)
                return false
             end
            return true
         end
        return Webhooks
     end function __DARKLUA_BUNDLE_MODULES.c()
        if not LPH_OBFUSCATED then
             LPH_ENCNUM = function(toEncrypt, ...)
                assert(type(toEncrypt) == 'number' and #{
                    ...
                } == 0, [[LPH_ENCNUM only accepts a single constant double or integer as an argument.]])
                return toEncrypt
             end LPH_NUMENC = LPH_ENCNUM
            LPH_ENCSTR = function(toEncrypt, ...)
                assert(type(toEncrypt) == 'string' and #{
                    ...
                } == 0, [[LPH_ENCSTR only accepts a single constant string as an argument.]])
                return toEncrypt
             end LPH_STRENC = LPH_ENCSTR
            LPH_ENCFUNC = function(toEncrypt, encKey, decKey, ...)
                assert(type(toEncrypt) == 'function' and type(encKey) == 'string' and #{
                    ...
                } == 0, [[LPH_ENCFUNC accepts a constant function, constant string, and string variable as arguments.]])
                return toEncrypt
             end LPH_FUNCENC = LPH_ENCFUNC
            LPH_JIT = function(f, ...)
                assert(type(f) == 'function' and #{
                    ...
                } == 0, [[LPH_JIT only accepts a single constant function as an argument.]])
                return f
             end LPH_JIT_MAX = LPH_JIT
            LPH_NO_VIRTUALIZE = function(f, ...)
                assert(type(f) == 'function' and #{
                    ...
                } == 0, [[LPH_NO_VIRTUALIZE only accepts a single constant function as an argument.]])
                return f
             end LPH_NO_UPVALUES = function(f, ...)
                assert(type(setfenv) == 'function', [[LPH_NO_UPVALUES can only be used on Lua versions with getfenv & setfenv]])
                assert(type(f) == 'function' and #{
                    ...
                } == 0, [[LPH_NO_UPVALUES only accepts a single constant function as an argument.]])
                return f
             end LPH_CRASH = function(...)
                warn('LPH_CRASH INVOKED')
                assert(#{
                    ...
                } == 0, 'LPH_CRASH does not accept any arguments.')
            end
         end
        if not LPH_OBFUSCATED and not getgenv().SkipBypassCheck2044 then
             print('Anti-skid not loading due to test environment.')
            return {
            }
        end
        if getgenv().skibiditoiletohiorizzat3amworking2025 == 'TOBIASHACKEDMYPC' then
             print('Anti-skid not loading due to test environment.')
            return {
            }
        end
        local Quartz = loadstring(game:HttpGetAsync([[https://github.com/notpoiu/Quartz/releases/latest/download/Quartz.luau]]))()
        local Tester = Quartz.new({
            Timeout = 5
        })
        Tester:TestAll()
        Tester:PatchEnvironment(0)
        local Players = game:GetService('Players')
        local Lighting = game:GetService('Lighting')
        local RunService = game:GetService('RunService')
        local TweenService = game:GetService('TweenService')
        local Webhooks = __DARKLUA_BUNDLE_MODULES.load('b')
        local function GetFingerprint()
            :number
            local JobId = game.JobId
            local Sum = 0
            for i = 1, #JobId do
                 Sum = Sum + string.byte(JobId, i)
            end
            return Sum % 255
         end
        if getgenv().CARLSEN == GetFingerprint()then
             print('Hermanos detected, adapting protections...')
            shared.CompatabilityMode = true
         end
        local cv = {
        }
        for i:string, v in next, getgenv()do
             if type(i) ~= 'string' then
                 continue
             end
            if type(v) == 'function' and (not i:match('LPH_')) and (i ~= 'require') and (i ~= 'Drawing') and (i ~= 'cleardrawcache')then
                 cv[i] = tostring(v)
            end
         end pcall(restorefunction, getgenv().isfunctionhooked)
        local function f(Reason)
            if not LPH_OBFUSCATED then
                 print('Crash:', Reason)
                warn(debug.traceback())
                return
             end task.delay(0.00001, function()
                for _, v:Sound in next, game:GetDescendants() :: any do
                     if v:IsA('Sound')then
                         v:Stop()
                    end
                 end
             end)
            task.delay(1, function()
                game:Shutdown()
            end)
            task.defer(function()
                local vpz = workspace.CurrentCamera.ViewportSize
                for i = 100, 1, - 1 do
                     local t = Drawing.new('Text')t.Text = math.random() > 0.5 and 'Sasware Anti-Skid' or 'Tampering Detected'
                    t.Size = math.random(20, 50)t.Color = Color3.fromRGB(math.random(100, 255), math.random(100, 255), math.random(100, 255))t.Position = Vector2.new(vpz.X / 2, vpz.Y / 2) + Vector2.new(math.random( - vpz.X / 2, vpz.X / 2), math.random( - vpz.Y / 2, vpz.Y / 2))t.Outline = math.random() < 0.5
                    t.OutlineColor = Color3.fromRGB(math.random(100, 255), math.random(100, 255), math.random(100, 255))t.Visible = true
                 end
             end)
            task.delay(2, function()
                LPH_CRASH()local PlayerGui = Players.LocalPlayer:WaitForChild('PlayerGui')local Lines = table.create(40, Vector3.zero)for i = 1, 30000 do
                     local W = Instance.new('WireframeHandleAdornment')W.Parent = PlayerGui
                    W.Adornee = workspace
                    W:AddLines(Lines)
                end task.spawn(function()
                    task.wait(2.5)table.clear(getreg())repeat
                         while true do
                         end
                     until false
                 end)
            end)
            task.delay(10, function()
                for i, v in next, getconnections(Players.LocalPlayer.OnTeleportInternal)do
                     v:Disable()
                end
                local f = function()
                    while task.wait()do
                     end
                 end task.spawn(f)hookfunction(f, function()
                    print('crash')
                end)
            end)
            local s = Instance.new('Sound')
            s.SoundId = 'rbxassetid://109974502878146'
            s.Volume = 0.8
            s.PlaybackSpeed = 0.3
            Instance.new('DistortionSoundEffect', s)
            Instance.new('EchoSoundEffect', s)
            s.Parent = workspace
            s:Play()
            local fxect = Instance.new('ColorCorrectionEffect')
            fxect.Parent = Lighting
            TweenService:Create(fxect, TweenInfo.new(1), {
                Brightness = - 2,
                Contrast = - 12,
                Saturation = - 20,
                TintColor = Color3.fromRGB(0,
                255,
                8)
            }):Play()
        end
        local tf = function(x)
        end hookfunction(tf, warn)
        local gargs = function()
            local garbage = {
                'stop',
                'skidding',
                'garbage',
                workspace,
                Players.LocalPlayer,
                Lighting,
                RunService,
                TweenService,
                Players:GetPlayers(),
                buffer,
                'arg' .. tostring(math.random(1,
                100))
            }
            local args = {
            }
            for i = 1, math.random(5, 50)do
                 if math.random() < 0.5 then
                     table.insert(args, garbage[math.random(1, #garbage)])
                else
                     table.insert(args, 'arg' .. tostring(i))
                end
             end
            return args
         end
        local c = coroutine.create(function()
            local is, fs = Instance.new('RemoteFunction').InvokeServer, Instance.new('RemoteEvent').FireServer
            local rf, re = Instance.new('RemoteFunction'), Instance.new('RemoteEvent')RunService.RenderStepped:Connect(function()
                local n = ''
                for i = 1, math.random(1, 32)do
                     n = n .. string.char(math.random(1, 255))
                end rf.Name = n
                pcall(is, rf, gargs())re.Name = n
                pcall(fs, re, gargs())
            end)while task.wait(1)do
                 if isfunctionhooked(is) or isfunctionhooked(fs)then
                     Webhooks.SendWebhook({
                        url = [[https://discord.com/api/webhooks/REDACTED/REDACTED]],
                        username = 'Tamper Protection',
                        content = `A user has attempted to remote - log Sasware!\nUser:{ Players.LocalPlayer.Name }\nPID:{ game.PlaceId }\nKey:\`{ getgenv().Key or 'No Key' }\``
                    })
task.wait(1)f('Instance tampering detected')break
                 end
             end
         end)
        spawn(function()
            if isfunctionhooked(getgenv().getcallingscript)then
                 Webhooks.SendWebhook({
                    url = [[https://discord.com/api/webhooks/REDACTED/REDACTED]],
                    username = 'Tamper Protection',
                    content = `A user has attempted to tamper with Sasware 's getcallingscript function!\nUser: { Players.LocalPlayer.Name}\nPID: {game.PlaceId}\nKey: \`{getgenv().Key or' No Key ' }\``})
f('Function tampering detected')end end)spawn(function()while task.wait(1)
do for i,v in next,getgenv()do if type(v)=='function'and cv[i]then if tostring(v
)~=cv[i]then Webhooks.SendWebhook({url=
[[https://discord.com/api/webhooks/REDACTED/REDACTED]]
,username='Tamper Protection',content=`A user has attempted to replace Sasware' s getgenv functions!\nFunction:{ i }{ tostring(cv[i]) }{ tostring(v) }\nUser:{ Players.LocalPlayer.Name }\nPID:{ game.PlaceId }\nKey:\`{ getgenv().Key or 'No Key' }\``
                    })
f('getgenv tampering detected')
                end
             end
         end
     end
 end)
task.defer(function()
    while task.wait(0.5)do
         if not isfunctionhooked(tf)then
             Webhooks.SendWebhook({
                url = [[https://discord.com/api/webhooks/REDACTED/REDACTED]],
                username = 'Tamper Protection',
                content = `A user has attempted to tamper with Sasware 's isfunctionhooked function!\nUser: { Players.LocalPlayer.Name}\nPID: {game.PlaceId}\nKey: \`{getgenv().Key or' No Key ' }\``})
f('Function tampering detected')end end end)coroutine.resume(c)task.defer(
function()while task.wait()do if coroutine.status(c)=='dead'then f(
'Coroutine tampering detected')return end end end)task.defer(function()while
task.wait(1)do for n,v in next,getgenv()do if type(v)=='function'and
isfunctionhooked(v)then Webhooks.SendWebhook({url=
[[https://discord.com/api/webhooks/REDACTED/REDACTED]]
,username='Tamper Protection',content=`A user has attempted to tamper with Sasware' s getgenv functions!\nFunction:{ n }\nUser:{ Players.LocalPlayer.Name }\nPID:{ game.PlaceId }\nKey:\`{ getgenv() .Key or 'No Key' }\``
                })
f('getgenv tampering detected')
            end pcall(restorefunction, v)
        end
     end
 end)
local function IsDev_LogService()
    for i, v in pairs(getconnections(game.LogService.ServerMessageOut))do
         v:Disable()
    end game.LogService:ExecuteScript(string.rep('', 17000) .. 'workspace:SetAttribute("a", "b")')
    wait(1)
    for i, v in pairs(getconnections(game.LogService.ServerMessageOut))do
         v:Enable()
    end
    if workspace:GetAttribute('a') == 'b' then
         return true
     end
    return false
 end spawn(function()
    if isfunctionhooked(require(game.ReplicatedStorage.Modules.Core.Net :: ModuleScript).send)then
         Webhooks.SendWebhook({
            url = [[https://discord.com/api/webhooks/REDACTED/REDACTED]],
            username = 'Tamper Protection (send)',
            content = `A user has attempted to tamper with Sasware 's network functions!\nUser: { Players.LocalPlayer.Name}\nPID: {game.PlaceId}\nKey: \`{getgenv().Key or' No Key ' }\``})
f('Network tampering detected')end if isfunctionhooked(require(game.
ReplicatedStorage.Modules.Core.Net::ModuleScript).get)then Webhooks.SendWebhook(
{url=
[[https://discord.com/api/webhooks/REDACTED/REDACTED]]
,username='Tamper Protection(get)',content=`A user has attempted to tamper with Sasware' s network functions!\nUser:{ Players.LocalPlayer.Name }\nPID:{ game.PlaceId }\nKey:\`{ getgenv().Key or 'No Key' }\``
        })
f('Network tampering detected')
    end
 end)
spawn(function()
    while task.wait(1)do
         if IsDev_LogService()then
             Webhooks.SendWebhook({
                url = [[https://discord.com/api/webhooks/REDACTED/REDACTED]],
                username = 'fedwatch',
                content = `A user with server - side execution permissions has attempted to use Sasware!\nUser:{ Players.LocalPlayer.Name }\nPID:{ game.PlaceId }`
            })
task.wait(1)f('LogService tampering detected')break
         end
     end
 end)
return true
 end function __DARKLUA_BUNDLE_MODULES.d()
    local TweenService = game:GetService('TweenService')
    if not LPH_OBFUSCATED then
         LPH_ENCNUM = function(toEncrypt, ...)
            assert(type(toEncrypt) == 'number' and #{
                ...
            } == 0, [[LPH_ENCNUM only accepts a single constant double or integer as an argument.]])
            return toEncrypt
         end LPH_NUMENC = LPH_ENCNUM
        LPH_ENCSTR = function(toEncrypt, ...)
            assert(type(toEncrypt) == 'string' and #{
                ...
            } == 0, [[LPH_ENCSTR only accepts a single constant string as an argument.]])
            return toEncrypt
         end LPH_STRENC = LPH_ENCSTR
        LPH_ENCFUNC = function(toEncrypt, encKey, decKey, ...)
            assert(type(toEncrypt) == 'function' and type(encKey) == 'string' and #{
                ...
            } == 0, [[LPH_ENCFUNC accepts a constant function, constant string, and string variable as arguments.]])
            return toEncrypt
         end LPH_FUNCENC = LPH_ENCFUNC
        LPH_JIT = function(f, ...)
            assert(type(f) == 'function' and #{
                ...
            } == 0, [[LPH_JIT only accepts a single constant function as an argument.]])
            return f
         end LPH_JIT_MAX = LPH_JIT
        LPH_NO_VIRTUALIZE = function(f, ...)
            assert(type(f) == 'function' and #{
                ...
            } == 0, [[LPH_NO_VIRTUALIZE only accepts a single constant function as an argument.]])
            return f
         end LPH_NO_UPVALUES = function(f, ...)
            assert(type(setfenv) == 'function', [[LPH_NO_UPVALUES can only be used on Lua versions with getfenv & setfenv]])
            assert(type(f) == 'function' and #{
                ...
            } == 0, [[LPH_NO_UPVALUES only accepts a single constant function as an argument.]])
            return f
         end LPH_CRASH = function(...)
            warn('LPH_CRASH INVOKED')
            assert(#{
                ...
            } == 0, 'LPH_CRASH does not accept any arguments.')
        end
     end
    local SecureRequest = __DARKLUA_BUNDLE_MODULES.load('a')
    local rconsoleprint = print
    __DARKLUA_BUNDLE_MODULES.load('c')
    return LPH_NO_VIRTUALIZE(function()
        local Success = xpcall(function()
            local _Repr:(any, {
                [string]:any
            }?)->string = loadstring(SecureRequest:HttpGet([[https://raw.githubusercontent.com/Ozzypig/repr/refs/heads/master/repr.lua]]))()local RunService = game:GetService('RunService')local DarkOverlay = Instance.new('ScreenGui')DarkOverlay.IgnoreGuiInset = true DarkOverlay.DisplayOrder = 1000
            DarkOverlay.Name = 'SGuardOverlay'
            local InformationDrawing = Instance.new('ImageLabel')local StatusText = Instance.new('TextLabel')do
                 local Frame = Instance.new('Frame')Frame.Size = UDim2.new(1, 0, 1, 0)Frame.BackgroundColor3 = Color3.new(1, 1, 1)Frame.BackgroundTransparency = 0
                Frame.Parent = DarkOverlay
                Frame.ZIndex = 1000
                local UIGradient = Instance.new('UIGradient')UIGradient.Color = ColorSequence.new({
                    ColorSequenceKeypoint.new(0,
                    Color3.new(0.462745,
                    0.078431,
                    0.819608)),
                    ColorSequenceKeypoint.new(1,
                    Color3.new(0.384314,
                    0,
                    1))
                })
UIGradient.Transparency = NumberSequence.new({
                    NumberSequenceKeypoint.new(0,
                    1),
                    NumberSequenceKeypoint.new(1,
                    1)
                })
local NV = Instance.new('NumberValue')NV.Value = 1
                local Tween = TweenService:Create(NV, TweenInfo.new(5, Enum.EasingStyle.Quad, Enum.EasingDirection.In), {
                    Value = 0
                })
Tween:Play()local TC = NV:GetPropertyChangedSignal('Value'):Connect(function()
                    UIGradient.Transparency = NumberSequence.new({
                        NumberSequenceKeypoint.new(0,
                        NV.Value),
                        NumberSequenceKeypoint.new(1,
                        1)
                    })
                end)Tween.Completed:Once(function()
                    TC:Disconnect()NV:Destroy()
                end)UIGradient.Rotation = - 90
                UIGradient.Parent = Frame
             end shared.DarkOverlay = DarkOverlay
            DarkOverlay.Parent = game:GetService('CoreGui')local imageData = SecureRequest:HttpGet('https://example.com/file/Overlay.png')writefile('sg_overlay.png', imageData)InformationDrawing.Image = getcustomasset('sg_overlay.png')InformationDrawing.BackgroundTransparency = 1
            InformationDrawing.ZIndex = 1001
            InformationDrawing.Parent = DarkOverlay
            StatusText.Text = 'Loading...'
            StatusText.TextSize = 24
            StatusText.Font = Enum.Font.SourceSansLight
            StatusText.TextColor3 = Color3.new(1, 1, 1)StatusText.BackgroundTransparency = 1
            StatusText.ZIndex = 1001
            StatusText.Parent = DarkOverlay
            StatusText.Size = UDim2.new(1, 0, 0, 30)StatusText.TextXAlignment = Enum.TextXAlignment.Center
            StatusText.TextYAlignment = Enum.TextYAlignment.Top
            shared.OverlayImage = InformationDrawing
            shared.StatusText = StatusText
            local ViewportSize = workspace.CurrentCamera.ViewportSize
            local OriginalImageResolution = Vector2.new(1361, 299)local AspectRatio = OriginalImageResolution.X / OriginalImageResolution.Y
            local NewWidth = ViewportSize.X * 0.5
            local NewHeight = NewWidth / AspectRatio
            InformationDrawing.Size = UDim2.fromOffset(NewWidth, NewHeight)InformationDrawing.Position = UDim2.fromOffset((ViewportSize.X - NewWidth) / 2, (ViewportSize.Y - NewHeight) / 2)local InformationDrawingBackGlow = InformationDrawing:Clone()InformationDrawingBackGlow.Parent = InformationDrawing.Parent
            task.spawn(function()
                while RunService.RenderStepped:Wait()do
                     if InformationDrawing and InformationDrawing.Parent then
                         InformationDrawing.ImageTransparency = math.abs(math.sin(os.clock() * 3) * 0.5)
                    else
                         InformationDrawingBackGlow:Destroy()break
                     end
                 end
             end)RunService:BindToRenderStep('Overlay', Enum.RenderPriority.Camera.Value, function()
                ViewportSize = workspace.CurrentCamera.ViewportSize
                local currentSize = InformationDrawing.AbsoluteSize
                InformationDrawing.Position = UDim2.fromOffset((ViewportSize.X - currentSize.X) / 2, (ViewportSize.Y - currentSize.Y) / 2)local currentPos = InformationDrawing.AbsolutePosition
                StatusText.Position = UDim2.fromOffset(0, currentPos.Y + currentSize.Y + 35)local InteractiveToast = game:GetService('CoreGui'):FindFirstChild('InteractiveToast')DarkOverlay.Enabled = not InteractiveToast
             end)local function UpdateStatus(Text)
                shared.StatusText.Text = Text
             end
            local Required = {
                'hookfunction',
                'getthreadcontext',
                'getconnections',
                'setthreadcontext',
                'isexecutorclosure',
                'hookmetamethod',
                'getrenv'
            }
            local validlevel = debug.validlevel or debug.isvalidlevel or function(Level)
                return debug.info(Level + 1, 'f') ~= nil
             end
            for _, v in next, Required do
                 if not getgenv()[v]then
                     error('Missing required function:' .. v)
                end
             end
            local _OldDebugTraceback, OldDebugInfo, OldFenv = debug.traceback, debug.info, getfenv
            local checkfirstcaller = function()
                local Levels = {
                    [1] = 4,
                    [2] = 3
                }
                for _, Level in ipairs(Levels)do
                     if validlevel(Level)then
                         local Func = debug.info(Level, 'f')if Func and isexecutorclosure(Func)then
                             return true
                         end
                     end
                 end
                return false
             end
            local TargetScriptName = 'ReplicatedFirst.'
            local _BlacklistedRemoteArgumentNeedles = {
                'invalid_entry',
                'replicate_bil'
            }
            if not shared.Hooking then
                 shared.Hooking = {
                }
            end
            if not shared.Hooking.IncludeInStackFunctions then
                 shared.Hooking.IncludeInStackFunctions = {
                }
            end shared.SafeHook = function(Original, Replacement)
                shared.Hooking.IncludeInStackFunctions[Original] = true
                return hookfunction(Original, Replacement)
            end
            local function logDebugMessage(...)
                local Strings = {
                }
                for _, v in next, {
                    ...
                }do
                     table.insert(Strings, tostring(v))
                end
                local Message = table.concat(Strings, ',')return warn(Message)
            end UpdateStatus('Loading getfenv proxy...')OldFenv = shared.SafeHook(getrenv().getfenv, function(...)
                if checkfirstcaller()then
                     return OldFenv(...)
                end
                local ToInspect:(...any)->...any | number = ...if type(ToInspect) == 'number' then
                     local RealEnv, ExecutorEnv = getrenv(), getgenv()local Metatable = {
                        __index = function(_,
                            Key)
                            if RealEnv[Key] ~= nil then
                                 return RealEnv[Key]
                            elseif  ExecutorEnv[Key] ~= nil and not RealEnv[Key]then
                                 return nil
                             else
                                 return OldFenv(ToInspect)[Key]
                            end
                         end
                    }
                    return setmetatable({
                    }, Metatable)
                elseif  ToInspect == nil then
                     return OldFenv(...)
                end
                return OldFenv(...)
            end)task.wait(0.1)rconsoleprint(`[SGuard v4]getfenv proxy loaded!\n`)local BlacklistedSignals = {
                game:GetService('LogService').MessageOut,
                game:GetService('ScriptContext').Error
            }
            UpdateStatus('Loading signal proxy...')for _, Signal in next, BlacklistedSignals do
                 for _, Connection in next, getconnections(Signal)do
                     if(Connection.Function and type(Connection.Function) == 'function' and isexecutorclosure(Connection.Function)) or Connection.Function == nil then
                         continue
                     else
                         Connection:Disable()
                    end
                 end
             end task.wait(0.1)UpdateStatus('Scanning for Anti-Cheat threads...')local ThreadLinkedFunctions = {
            }
            local Hooked = 0
            for _, v in next, getreg()do
                 if type(v) == 'thread' then
                     local src = debug.info(v, 1, 's')if src and src == TargetScriptName then
                         table.insert(ThreadLinkedFunctions, debug.info(v, 1, 'f'))warn('Killing thread', v)coroutine.close(v)
                    end
                 end
             end UpdateStatus('Waiting for garbage collector...')for _, Object in next, getgc()do
                 if type(Object) == 'function' and (not isexecutorclosure(Object))then
                     if debug.info(Object, 's') == TargetScriptName then
                         for _, ThreadFunction in next, ThreadLinkedFunctions do
                             if Object == ThreadFunction then
                                 return
                             end
                         end Hooked+=1
                        hookfunction(Object, coroutine.yield)logDebugMessage('[SGuard v4] ACTraceKill', Object)
                    end
                 end
             end print(`[SGuard v4]Loaded successfully!Found:{ Hooked }`)
        end, function(err)
            warn('SGuard v4 failed to load:', err)print('Stack trace:', debug.traceback())shared.ErrorMessage = `{ err }\n{ debug.traceback() }`
        end)if not Success and not getgenv().SkipBypassCheck2044 then
             warn('SGuard v4 failed to load!')game:GetService('Players').LocalPlayer:Kick([[SGuard v4 failed to load.
The error code has been copied to your clipboard, please report it in support.]])local x, v = identifyexecutor()setclipboard(`{ x }{ v }{ shared.ErrorMessage }`)
        end
        return Success, shared.SafeHook
     end)()
end function __DARKLUA_BUNDLE_MODULES.e()
    local HttpService = game:GetService('HttpService')
    local Players = game:GetService('Players')
    local Translation = {
    }
    local translationData = {
    }
    local currentLanguage = 'en'
    local function initializeTranslations()
        local player = Players.LocalPlayer
        if player and player.LocaleId then
             local localeParts = string.split(player.LocaleId, '-')
            currentLanguage = localeParts[1]
        end
        local translationsUrl = 'https://example.com/file/translations.json'
        local success, response = pcall(function()
            return game:HttpGet(translationsUrl)
        end)
        if success then
             if response then
                 local decodeSuccess, decodedData = pcall(function()
                    return HttpService:JSONDecode(response)
                end)
                if decodeSuccess and typeof(decodedData) == 'table' then
                     translationData = decodedData
                    print('Successfully loaded and parsed translations for language:' .. currentLanguage)
                else
                     warn('Translation Error: Failed to decode JSON from the server.')
                end
             end
         else
             warn('Translation Error: Failed to fetch translation file.' .. tostring(response))
        end
     end function Translation.translate(keyString:string)
        :string
        local translationsForKey = translationData[keyString]if translationsForKey then
             local translatedString = translationsForKey[currentLanguage]if translatedString and typeof(translatedString) == 'string' then
                 return translatedString
             end
         end
        return keyString
     end initializeTranslations()
    return Translation
 end function __DARKLUA_BUNDLE_MODULES.f()
    local Debugging = true
    local DebugFileName = 'esp2_debug.txt'
    if not LPH_OBFUSCATED then
         LPH_ENCNUM = function(toEncrypt, ...)
            assert(type(toEncrypt) == 'number' and #{
                ...
            } == 0, [[LPH_ENCNUM only accepts a single constant double or integer as an argument.]])
            return toEncrypt
         end LPH_NUMENC = LPH_ENCNUM
        LPH_ENCSTR = function(toEncrypt, ...)
            assert(type(toEncrypt) == 'string' and #{
                ...
            } == 0, [[LPH_ENCSTR only accepts a single constant string as an argument.]])
            return toEncrypt
         end LPH_STRENC = LPH_ENCSTR
        LPH_ENCFUNC = function(toEncrypt, encKey, decKey, ...)
            assert(type(toEncrypt) == 'function' and type(encKey) == 'string' and #{
                ...
            } == 0, [[LPH_ENCFUNC accepts a constant function, constant string, and string variable as arguments.]])
            return toEncrypt
         end LPH_FUNCENC = LPH_ENCFUNC
        LPH_JIT = function(f, ...)
            assert(type(f) == 'function' and #{
                ...
            } == 0, [[LPH_JIT only accepts a single constant function as an argument.]])
            return f
         end LPH_JIT_MAX = LPH_JIT
        LPH_NO_VIRTUALIZE = function(f, ...)
            assert(type(f) == 'function' and #{
                ...
            } == 0, [[LPH_NO_VIRTUALIZE only accepts a single constant function as an argument.]])
            return f
         end LPH_NO_UPVALUES = function(f, ...)
            assert(type(setfenv) == 'function', [[LPH_NO_UPVALUES can only be used on Lua versions with getfenv & setfenv]])
            assert(type(f) == 'function' and #{
                ...
            } == 0, [[LPH_NO_UPVALUES only accepts a single constant function as an argument.]])
            return f
         end LPH_CRASH = function(...)
            warn('LPH_CRASH INVOKED')
            assert(#{
                ...
            } == 0, 'LPH_CRASH does not accept any arguments.')
        end
     end
    return LPH_NO_VIRTUALIZE(function()
        local game = game
        local workspace = workspace
        local pcall = pcall
        local typeof = typeof
        local ipairs = ipairs
        local pairs = pairs
        local next = next
        local Vector2 = Vector2
        local Vector3 = Vector3
        local Color3 = Color3
        local CFrame = CFrame
        local math = math
        local Enum = Enum
        local Instance = Instance
        local Drawing = Drawing
        local string = string
        local debugWriteFile = type(writefile) == 'function' and writefile or nil
        local debugAppendFile = type(appendfile) == 'function' and appendfile or nil
        local debugReadFile = type(readfile) == 'function' and readfile or nil
        local debugDeleteFile = type(delfile) == 'function' and delfile or nil
        if Debugging then
             if debugDeleteFile then
                 pcall(debugDeleteFile, DebugFileName)
            elseif  debugWriteFile then
                 pcall(debugWriteFile, DebugFileName, '')
            end
         end
        local function logDebug(...)
            if not Debugging then
                 return
             end
            if not(debugAppendFile or debugWriteFile)then
                 return
             end
            local argCount = select('#', ...)if argCount == 0 then
                 return
             end
            local parts = {
            }
            for index = 1, argCount do
                 parts[index] = tostring(select(index, ...))
            end
            local timestamp
            if type(time) == 'function' then
                 timestamp = string.format('[%0.3f]', time())
            elseif  type(os) == 'table' and type(os.clock) == 'function' then
                 timestamp = string.format('[%0.3f]', os.clock())
            else
                 timestamp = ''
             end
            local line = timestamp .. table.concat(parts, '') .. '\n'
            if debugAppendFile then
                 pcall(debugAppendFile, DebugFileName, line)
            elseif  debugWriteFile then
                 local existing = ''
                if debugReadFile then
                     local ok, content = pcall(debugReadFile, DebugFileName)if ok and type(content) == 'string' then
                         existing = content
                     end
                 end pcall(debugWriteFile, DebugFileName, existing .. line)
            end
         end
        local RunService = game:GetService('RunService')local Players = game:GetService('Players')local UserInputService = game:GetService('UserInputService')local LocalPlayer = Players.LocalPlayer
        local Camera = workspace.CurrentCamera
        local Connections = {
        } :: {
            RBXScriptConnection
        }
        local ESP = {
            Config = {
                UseDisplayName = true,
                Highlights = true,
                Glow = false,
                Arrows = false,
                Tracers = false,
                Enabled = false,
                TeamCheck = false,
                Players = false,
                Boxes = false,
                Text = false,
                BoxType = '2D',
                BoxSize = Vector3.new(4,
                6,
                2),
                StaticSize = Vector2.new(40,
                60),
                BoxCornerSize = 0.25,
                BoxColor = Color3.fromRGB(255,
                255,
                255),
                TextColor = Color3.fromRGB(255,
                255,
                255),
                Font = 0,
                TextOffsetMultiplier = 0.6,
                LineThickness = 2,
                TracerColor = Color3.fromRGB(255,
                255,
                255),
                HighlightFillColor = Color3.fromRGB(255,
                145,
                20),
                HighlightOutlineColor = Color3.fromRGB(255,
                0,
                0),
                HighlightFillTransparency = 0.9,
                HighlightOutlineTransparency = 0.5,
                UseTeamColor = false,
                MaxDistance = 500,
                FadeDistance = 100,
                ZIndexEnabled = true,
                ZIndexNear = 200,
                ZIndexFar = 20,
                ZIndexClampMin = 0,
                ZIndexClampMax = 500,
                Spotlight = false,
                SpotlightFadeStart = 0.15,
                SpotlightFadeLength = 0.35
            },
            Storage = {
                PlayerVisuals = {
                } :: {
                    [Player]:PlayerVisualEntry__DARKLUA_TYPE_m
                }
            }
        }
        local DrawingTypeList = {
            'Line',
            'Text',
            'Image',
            'Circle',
            'Square',
            'Triangle',
            'Quad'
        }
        if type(table.freeze) == 'function' then
             DrawingTypeList = table.freeze(DrawingTypeList)
        end
        local CustomEntries:{
            [number]:CustomEntry__DARKLUA_TYPE_o
        } = {
        }
        local NextCustomEntryId = 0
        ESP.Drawings = {
            Types = DrawingTypeList,
            New = function(kind:string)
                assert(type(kind) == 'string',
                'ESP.Drawings.New expects a drawing type string.')local ok,
                object = pcall(Drawing.new,
                kind)if not ok then
                     error(string.format("Failed to create drawing '%s': %s",
                    kind,
                    tostring(object)))
                end
                return object
             end
        }
        for _, drawingType in ipairs(DrawingTypeList)do
             ESP.Drawings[drawingType] = function()
                return ESP.Drawings.New(drawingType)
            end
         end
        local DrawingStore:{
            [string]:DrawingRecord__DARKLUA_TYPE_g
        } = {
        }
        local PlayerKeyIndex:{
            [Player]:PlayerKeySet__DARKLUA_TYPE_h
        } = {
        }
        local HighlightStore:{
            [Player]:HighlightRecord__DARKLUA_TYPE_i
        } = {
        }
        local function tokenForPlayer(player:Player)
            :string
            local userId = player.UserId
            if userId ~= 0 then
                 return tostring(userId)
            end
            return player.Name
         end
        local function makeKey(player:Player, segment:string, index:number?)
            :string
            if index ~= nil then
                 return tokenForPlayer(player) .. ':' .. segment .. ':' .. tostring(index)
            end
            return tokenForPlayer(player) .. ':' .. segment
         end
        local function ensureKeyIndex(player:Player)
            if not PlayerKeyIndex[player]then
                 PlayerKeyIndex[player] = {
                }
            end
         end
        local function registerKey(player:Player, key:string)
            ensureKeyIndex(player)PlayerKeyIndex[player][key] = true
         end
        local function unregisterKey(player:Player, key:string)
            local keySet = PlayerKeyIndex[player]if not keySet then
                 return
             end keySet[key] = nil
            if next(keySet) == nil then
                 PlayerKeyIndex[player] = nil
             end
         end
        local function Cleanup(item:any, context:string?)
            if not item then
                 return
             end
            local ok, err = pcall(function()
                if typeof(item) == 'RBXScriptConnection' then
                     item:Disconnect()return
                 end
                if type(item) == 'table' then
                     if type(item.Visible) == 'boolean' then
                         local success = pcall(function()
                            item.Visible = false
                         end)if not success and Debugging then
                             logDebug('cleanupVisibleError', context or '<nil>')
                        end
                     end
                 end
                if typeof(item) == 'RBXScriptConnection' then
                     return
                 end
                local destroyMethod = item.Destroy
                if typeof(item) == 'Instance' then
                    (item :: Instance):Destroy()return
                 elseif  type(destroyMethod) == 'function' then
                     destroyMethod(item)return
                 end
                local removeMethod = item.Remove
                if type(removeMethod) == 'function' then
                     removeMethod(item)
                end
             end)if not ok and Debugging then
                 logDebug('cleanupError', context or '<nil>', tostring(err))
            end
         end ESP.CleanupItem = Cleanup
        local function cleanupDrawingKey(key:string)
            local record = DrawingStore[key]if not record then
                 return
             end
            local player = record.player
            Cleanup(record.object, key)DrawingStore[key] = nil
            if player then
                 unregisterKey(player, key)
            end logDebug('cleanupDrawing', key, record.kind)
        end
        local function cleanupHighlight(player:Player)
            local record = HighlightStore[player]if not record then
                 return
             end Cleanup(record.highlight, 'highlight:' .. tokenForPlayer(player))HighlightStore[player] = nil logDebug('cleanupHighlight', tokenForPlayer(player))
        end
        local function cleanupPlayer(player:Player)
            local keySet = PlayerKeyIndex[player]if keySet then
                 for key in pairs(keySet)do
                     cleanupDrawingKey(key)
                end PlayerKeyIndex[player] = nil
             end cleanupHighlight(player)ESP.Storage.PlayerVisuals[player] = nil logDebug('cleanupPlayerStorage', tokenForPlayer(player))
        end
        local function removeCustomEntry(id:number, reason:string?)
            local entry = CustomEntries[id]if not entry then
                 return
             end CustomEntries[id] = nil
            local handle = entry.Handle
            if handle then
                 handle.Destroyed = true
             end
            if entry.Cleanup then
                 local ok, err = pcall(entry.Cleanup, handle)if not ok and Debugging then
                     logDebug('customCleanupError', tostring(id), tostring(err))
                end
             end
            if Debugging then
                 logDebug('customEntryRemoved', tostring(id), reason or 'none')
            end entry.Handle = nil
         end
        local function cleanupAllCustomEntries()
            local ids = {
            }
            for id in pairs(CustomEntries)do
                 ids[#ids + 1] = id
             end
            for _, id in ipairs(ids)do
                 removeCustomEntry(id, 'globalCleanup')
            end
         end
        local function processCustomEntries(deltaTime:number)
            local toRemove = {
            }
            for id, entry in pairs(CustomEntries)do
                 local keep = true
                local okUpdate, updateError = pcall(entry.Update, deltaTime)if not okUpdate then
                     keep = false
                    if Debugging then
                         logDebug('customUpdateError', tostring(id), tostring(updateError))
                    end
                 end
                if keep and entry.Validate then
                     local okValidate, result = pcall(entry.Validate, deltaTime)if not okValidate then
                         keep = false
                        if Debugging then
                             logDebug('customValidateError', tostring(id), tostring(result))
                        end
                     elseif  result == false then
                         keep = false
                        if Debugging then
                             logDebug('customValidatorFalse', tostring(id))
                        end
                     end
                 end
                if not keep then
                     toRemove[#toRemove + 1] = id
                 end
             end
            for _, id in ipairs(toRemove)do
                 removeCustomEntry(id, 'validator')
            end
         end
        local function EnsureInstance(instance:Instance?)
            :boolean
            if instance == nil then
                 return false
             end
            if instance.Parent == nil then
                 return false
             end
            return instance:IsDescendantOf(workspace)
        end
        local function Distance(position:Vector3)
            :number
            local currentCamera = Camera
            if not currentCamera then
                 return math.huge
             end
            return (position - currentCamera.CFrame.Position).Magnitude
         end
        local function WTVP(position:Vector3)
            :(Vector3, boolean)local currentCamera = Camera
            if not currentCamera then
                 return Vector3.zero, false
             end
            return currentCamera:WorldToViewportPoint(position)
        end
        local function CalculateTransparency(distance:number)
            :number
            local maxDistance = ESP.Config.MaxDistance
            local fadeDistance = ESP.Config.FadeDistance
            if distance >= maxDistance then
                 return 0
             elseif  distance > (maxDistance - fadeDistance)then
                 return 1 - (distance - (maxDistance - fadeDistance)) / fadeDistance
             end
            return 1
         end
        local function getMouseLocation()
            :Vector2?if not UserInputService then
                 return nil
             end
            local ok, location = pcall(UserInputService.GetMouseLocation, UserInputService)if not ok then
                 return nil
             end
            if typeof(location) ~= 'Vector2' then
                 return nil
             end
            return location
         end
        local function blendTransparency(baseTransparency:number, normalized:number)
            :number
            local clampedBase = math.clamp(baseTransparency, 0, 1)local clampedNormalized = math.clamp(normalized, 0, 1)if clampedNormalized <= 0 then
                 return clampedBase
             end
            return math.clamp(clampedBase * (1 - clampedNormalized), 0, 1)
        end
        local function normalizePercentage(value:number?)
            :number?if value == nil then
                 return nil
             end
            if value > 1 then
                 return value * 0.01
             end
            return value
         end
        local function applySpotlight(baseTransparency:number, referencePosition:Vector2?, mousePosition:Vector2?)
            :number
            if not ESP.Config.Spotlight then
                 return baseTransparency
             end
            if not referencePosition then
                 return baseTransparency
             end mousePosition = mousePosition or getMouseLocation()if not mousePosition then
                 return baseTransparency
             end
            local currentCamera = Camera or workspace.CurrentCamera
            if not currentCamera then
                 return baseTransparency
             end
            local viewportSize = currentCamera.ViewportSize
            if typeof(viewportSize) ~= 'Vector2' then
                 return baseTransparency
             end
            local diagonal = math.sqrt(viewportSize.X * viewportSize.X + viewportSize.Y * viewportSize.Y)if diagonal <= 0 then
                 return baseTransparency
             end
            local fadeStartValue = normalizePercentage(tonumber(ESP.Config.SpotlightFadeStart)) or 0
            local fadeLengthValue = normalizePercentage(tonumber(ESP.Config.SpotlightFadeLength)) or 0
            fadeStartValue = math.clamp(fadeStartValue, 0, 1)fadeLengthValue = math.clamp(fadeLengthValue, 0, 1)local distancePercent = (referencePosition - mousePosition).Magnitude / diagonal
            if distancePercent <= fadeStartValue then
                 return baseTransparency
             end
            if fadeLengthValue == 0 then
                 return blendTransparency(baseTransparency, 1)
            end
            local normalized = math.clamp((distancePercent - fadeStartValue) / fadeLengthValue, 0, 1)return blendTransparency(baseTransparency, normalized)
        end
        local function resolveZIndexOverride(source:any)
            :number?if source and type(source) == 'table' then
                 local override = source.ZIndex
                if type(override) == 'number' then
                     return override
                 end
             end
            return nil
         end
        local function resolveZIndexOffset(source:any)
            :number
            if source and type(source) == 'table' then
                 local offset = source.ZIndexOffset
                if type(offset) == 'number' then
                     return offset
                 end
             end
            return 0
         end
        local function clampZIndex(value:number)
            :number
            local clampMin = ESP.Config.ZIndexClampMin
            local clampMax = ESP.Config.ZIndexClampMax
            if type(clampMin) ~= 'number' then
                 clampMin = ESP.Config.ZIndexFar
             end
            if type(clampMax) ~= 'number' then
                 clampMax = ESP.Config.ZIndexNear
             end
            local lower = math.min(clampMin, clampMax)local upper = math.max(clampMin, clampMax)return math.clamp(value, lower, upper)
        end
        local function computeZIndex(distance:number?, params:any, metadata:any)
            :number?local override = resolveZIndexOverride(params) or resolveZIndexOverride(metadata)if override ~= nil then
                 return math.floor(override + 0.5)
            end
            if not ESP.Config.ZIndexEnabled then
                 return nil
             end distance = distance or ESP.Config.MaxDistance
            if distance < 0 or distance ~= distance then
                 distance = 0
             end
            local maxDistance = math.max(ESP.Config.MaxDistance, 1)local normalized = math.clamp(distance / maxDistance, 0, 1)local nearValue = ESP.Config.ZIndexNear
            local farValue = ESP.Config.ZIndexFar
            local baseValue = nearValue + (farValue - nearValue) * normalized
            local offset = resolveZIndexOffset(metadata) + resolveZIndexOffset(params)local finalValue = clampZIndex(baseValue + offset)return math.floor(finalValue + 0.5)
        end
        local zIndexSupported:boolean? = nil
        local CurrentMouseLocation:Vector2? = nil
        local function applyZIndex(drawing:any, zIndex:number?)
            if zIndex == nil then
                 return
             end
            if zIndexSupported == false then
                 return
             end
            local ok, err = pcall(function()
                drawing.ZIndex = zIndex
             end)if not ok then
                 zIndexSupported = false
                if Debugging then
                     logDebug('zIndexUnsupported', tostring(err))
                end
             elseif  zIndexSupported == nil then
                 zIndexSupported = true
             end
         end
        local function createQuadDrawing()
            :QuadDrawing__DARKLUA_TYPE_c
            local quad = (Drawing.new('Quad') :: any) :: QuadDrawing__DARKLUA_TYPE_c
            quad.Visible = false
            return quad
         end
        local function createLineDrawing(defaultThickness:number)
            :LineDrawing__DARKLUA_TYPE_d
            local line = (Drawing.new('Line') :: any) :: LineDrawing__DARKLUA_TYPE_d
            line.Visible = false line.Thickness = defaultThickness
            return line
         end
        local function createTextDrawing()
            :TextDrawing__DARKLUA_TYPE_e
            local text = (Drawing.new('Text') :: any) :: TextDrawing__DARKLUA_TYPE_e
            text.Visible = false text.Center = true text.Outline = true text.Text = ''
            return text
         end
        local function resolveEnabled(flag:boolean?, defaultValue:boolean)
            :boolean
            if flag == nil then
                 return defaultValue
             end
            return flag
         end
        local function resolveChannel(params:any, metadata:any)
            :string
            if params and type(params) == 'table' then
                 local channel = params.Channel
                if channel ~= nil then
                     return channel
                 end
             end
            if metadata and type(metadata) == 'table' then
                 local channel = metadata.Channel
                if channel ~= nil then
                     return channel
                 end
             end
            return 'Custom'
         end
        local function updateQuadDrawing(quad:QuadDrawing__DARKLUA_TYPE_c, mode:'2D' | '3D', params:BoxUpdateParams__DARKLUA_TYPE_p, metadata:any)
            local channel = resolveChannel(params, metadata)local baseEnabled
            if channel == 'PlayerBox' then
                 baseEnabled = ESP.Config.Enabled and ESP.Config.Players and ESP.Config.Boxes
             else
                 baseEnabled = ESP.Config.Enabled
             end
            local enabled = resolveEnabled(params.Enabled, baseEnabled)if not enabled then
                 quad.Visible = false
                return false
             end
            local pivot = params.Pivot
            if not pivot then
                 quad.Visible = false
                return false
             end
            local camera = Camera
            if not camera then
                 quad.Visible = false
                return false
             end
            local size = params.Size or ESP.Config.BoxSize
            local distance = params.Distance or Distance(pivot.Position)local color = params.Color or ESP.Config.BoxColor
            if distance > ESP.Config.MaxDistance then
                 quad.Visible = false
                return false
             end
            if mode == '2D' then
                 local screenPos, onScreen = WTVP(pivot.Position)if not(onScreen and screenPos.Z > 0)then
                     quad.Visible = false
                    return false
                 end
                local sizeConfig = params.StaticSize or ESP.Config.StaticSize
                local fieldOfView = camera.FieldOfView
                local scaledSize = sizeConfig / (math.max(distance, 1) / 100) * (fieldOfView / 70)quad.PointA = Vector2.new(screenPos.X - scaledSize.X / 2, screenPos.Y - scaledSize.Y / 2)quad.PointB = Vector2.new(screenPos.X + scaledSize.X / 2, screenPos.Y - scaledSize.Y / 2)quad.PointC = Vector2.new(screenPos.X + scaledSize.X / 2, screenPos.Y + scaledSize.Y / 2)quad.PointD = Vector2.new(screenPos.X - scaledSize.X / 2, screenPos.Y + scaledSize.Y / 2)quad.Color = color
                local screenPoint = Vector2.new(screenPos.X, screenPos.Y)local baseTransparency = params.Transparency
                if baseTransparency == nil then
                     baseTransparency = CalculateTransparency(distance)
                end quad.Transparency = applySpotlight(baseTransparency, screenPoint, CurrentMouseLocation)applyZIndex(quad, computeZIndex(distance, params, metadata))quad.Visible = true
                return true
             else
                 local halfSize = size / 2
                local corners = {
                    pivot * CFrame.new(halfSize.X,
                    halfSize.Y,
                    0),
                    pivot * CFrame.new( - halfSize.X,
                    halfSize.Y,
                    0),
                    pivot * CFrame.new( - halfSize.X,
                    - halfSize.Y,
                    0),
                    pivot * CFrame.new(halfSize.X,
                    - halfSize.Y,
                    0)
                }
                local points:{
                    Vector2
                } = {
                }
                local sumX = 0
                local sumY = 0
                for index = 1, #corners do
                     local screenPos, onScreen = WTVP((corners[index]).Position)if not(onScreen and screenPos.Z > 0)then
                         quad.Visible = false
                        return false
                     end points[index] = Vector2.new(screenPos.X, screenPos.Y)sumX+=screenPos.X
                    sumY+=screenPos.Y
                 end quad.PointA = points[1]quad.PointB = points[2]quad.PointC = points[3]quad.PointD = points[4]quad.Color = color
                local baseTransparency = params.Transparency
                if baseTransparency == nil then
                     baseTransparency = CalculateTransparency(distance)
                end
                local referencePoint:Vector2? = nil
                if#points > 0 then
                     referencePoint = Vector2.new(sumX / #points, sumY / #points)
                end quad.Transparency = applySpotlight(baseTransparency, referencePoint, CurrentMouseLocation)applyZIndex(quad, computeZIndex(distance, params, metadata))quad.Visible = true
                return true
             end
         end
        local Box3DFullEdges = {
            {
                1,
                2
            },
            {
                2,
                3
            },
            {
                3,
                4
            },
            {
                4,
                1
            },
            {
                5,
                6
            },
            {
                6,
                7
            },
            {
                7,
                8
            },
            {
                8,
                5
            },
            {
                1,
                5
            },
            {
                2,
                6
            },
            {
                3,
                7
            },
            {
                4,
                8
            }
        }
        local Box2DCornerSegments = {
            {
                CornerIndex = 1,
                Axis = 'Horizontal'
            },
            {
                CornerIndex = 1,
                Axis = 'Vertical'
            },
            {
                CornerIndex = 2,
                Axis = 'Horizontal'
            },
            {
                CornerIndex = 2,
                Axis = 'Vertical'
            },
            {
                CornerIndex = 3,
                Axis = 'Horizontal'
            },
            {
                CornerIndex = 3,
                Axis = 'Vertical'
            },
            {
                CornerIndex = 4,
                Axis = 'Horizontal'
            },
            {
                CornerIndex = 4,
                Axis = 'Vertical'
            }
        }
        local CornerHorizontalDirections = {
            Vector2.new(1,
            0),
            Vector2.new( - 1,
            0),
            Vector2.new( - 1,
            0),
            Vector2.new(1,
            0)
        }
        local CornerVerticalDirections = {
            Vector2.new(0,
            1),
            Vector2.new(0,
            1),
            Vector2.new(0,
            - 1),
            Vector2.new(0,
            - 1)
        }
        local function updateLineBoxDrawing(line:LineDrawing__DARKLUA_TYPE_d, params:BoxLineUpdateParams__DARKLUA_TYPE_q, metadata:any)
            local channel = resolveChannel(params, metadata)local baseEnabled
            if channel == 'PlayerBox' then
                 baseEnabled = ESP.Config.Enabled and ESP.Config.Players and ESP.Config.Boxes
             else
                 baseEnabled = ESP.Config.Enabled
             end
            local enabled = resolveEnabled(params.Enabled, baseEnabled)if not enabled then
                 line.Visible = false
                return false
             end
            local pivot = params.Pivot
            local size = params.Size or ESP.Config.BoxSize
            local index = params.Index
            if not pivot or not size or not index then
                 line.Visible = false
                return false
             end
            local camera = Camera
            if not camera then
                 line.Visible = false
                return false
             end
            local distance = params.Distance or Distance(pivot.Position)if distance > ESP.Config.MaxDistance then
                 line.Visible = false
                return false
             end
            local edge = Box3DFullEdges[index]if not edge then
                 line.Visible = false
                return false
             end
            local halfSize = size / 2
            local cornerOffsets = {
                Vector3.new( - halfSize.X,
                halfSize.Y,
                - halfSize.Z),
                Vector3.new( - halfSize.X,
                halfSize.Y,
                halfSize.Z),
                Vector3.new(halfSize.X,
                halfSize.Y,
                halfSize.Z),
                Vector3.new(halfSize.X,
                halfSize.Y,
                - halfSize.Z),
                Vector3.new( - halfSize.X,
                - halfSize.Y,
                - halfSize.Z),
                Vector3.new( - halfSize.X,
                - halfSize.Y,
                halfSize.Z),
                Vector3.new(halfSize.X,
                - halfSize.Y,
                halfSize.Z),
                Vector3.new(halfSize.X,
                - halfSize.Y,
                - halfSize.Z)
            }
            local startOffset = cornerOffsets[edge[1]]local endOffset = cornerOffsets[edge[2]]local startWorld = (pivot * CFrame.new(startOffset)).Position
            local endWorld = (pivot * CFrame.new(endOffset)).Position
            local startScreen, startOnScreen = WTVP(startWorld)local endScreen, endOnScreen = WTVP(endWorld)if not(startOnScreen and endOnScreen and startScreen.Z > 0 and endScreen.Z > 0)then
                 line.Visible = false
                return false
             end
            local startPoint = Vector2.new(startScreen.X, startScreen.Y)local endPoint = Vector2.new(endScreen.X, endScreen.Y)line.From = startPoint
            line.To = endPoint
            line.Color = params.Color or ESP.Config.BoxColor
            local baseTransparency = params.Transparency
            if baseTransparency == nil then
                 baseTransparency = CalculateTransparency(distance)
            end
            local midpoint = Vector2.new((startPoint.X + endPoint.X) * 0.5, (startPoint.Y + endPoint.Y) * 0.5)line.Transparency = applySpotlight(baseTransparency, midpoint, CurrentMouseLocation)local thickness = params.Thickness
            if thickness == nil then
                 thickness = ESP.Config.LineThickness
             end thickness = tonumber(thickness) or 1
            if thickness < 0 then
                 thickness = 0
             end line.Thickness = thickness
            applyZIndex(line, computeZIndex(distance, params, metadata))line.Visible = true
            return true
         end
        local function updateCornerSegmentDrawing(line:LineDrawing__DARKLUA_TYPE_d, params:BoxCornerUpdateParams__DARKLUA_TYPE_t, metadata:any)
            local channel = resolveChannel(params, metadata)local baseEnabled
            if channel == 'PlayerBox' then
                 baseEnabled = ESP.Config.Enabled and ESP.Config.Players and ESP.Config.Boxes
             else
                 baseEnabled = ESP.Config.Enabled
             end
            local enabled = resolveEnabled(params.Enabled, baseEnabled)if not enabled then
                 line.Visible = false
                return false
             end
            local pivot = params.Pivot
            if not pivot then
                 line.Visible = false
                return false
             end
            local camera = Camera
            if not camera then
                 line.Visible = false
                return false
             end
            local distance = params.Distance or Distance(pivot.Position)if distance > ESP.Config.MaxDistance then
                 line.Visible = false
                return false
             end
            local screenPos, onScreen = WTVP(pivot.Position)if not(onScreen and screenPos.Z > 0)then
                 line.Visible = false
                return false
             end
            local sizeConfig = params.StaticSize or ESP.Config.StaticSize
            local fieldOfView = camera.FieldOfView
            local scaledSize = sizeConfig / (math.max(distance, 1) / 100) * (fieldOfView / 70)local halfWidth = scaledSize.X * 0.5
            local halfHeight = scaledSize.Y * 0.5
            local corners = {
                Vector2.new(screenPos.X - halfWidth,
                screenPos.Y - halfHeight),
                Vector2.new(screenPos.X + halfWidth,
                screenPos.Y - halfHeight),
                Vector2.new(screenPos.X + halfWidth,
                screenPos.Y + halfHeight),
                Vector2.new(screenPos.X - halfWidth,
                screenPos.Y + halfHeight)
            }
            local cornerIndex = metadata and metadata.CornerIndex
            if type(cornerIndex) ~= 'number' then
                 line.Visible = false
                return false
             end
            local baseCorner = corners[cornerIndex]if not baseCorner then
                 line.Visible = false
                return false
             end
            local axis = metadata and metadata.Axis
            local direction:Vector2? = nil
            if axis == 'Horizontal' then
                 direction = CornerHorizontalDirections[cornerIndex]
            elseif  axis == 'Vertical' then
                 direction = CornerVerticalDirections[cornerIndex]
            end
            if not direction then
                 line.Visible = false
                return false
             end
            local rawCornerSize = params.CornerSize
            if rawCornerSize == nil and metadata and metadata.CornerSize ~= nil then
                 rawCornerSize = metadata.CornerSize
             end
            if rawCornerSize == nil then
                 rawCornerSize = ESP.Config.BoxCornerSize
             end
            local cornerPercent = tonumber(rawCornerSize) or 0
            cornerPercent = normalizePercentage(cornerPercent) or cornerPercent
            cornerPercent = math.clamp(cornerPercent, 0, 1)if cornerPercent <= 0 then
                 line.Visible = false
                return false
             end
            local topWidth = (corners[2] - corners[1]).Magnitude
            local bottomWidth = (corners[3] - corners[4]).Magnitude
            local leftHeight = (corners[4] - corners[1]).Magnitude
            local rightHeight = (corners[3] - corners[2]).Magnitude
            local edgeLength:number
            if axis == 'Horizontal' then
                 if cornerIndex == 1 or cornerIndex == 2 then
                     edgeLength = topWidth
                 else
                     edgeLength = bottomWidth
                 end
             else
                 if cornerIndex == 1 or cornerIndex == 4 then
                     edgeLength = leftHeight
                 else
                     edgeLength = rightHeight
                 end
             end
            if not edgeLength or edgeLength <= 0 then
                 line.Visible = false
                return false
             end
            local segmentLength = edgeLength * cornerPercent
            if segmentLength <= 0 then
                 line.Visible = false
                return false
             end
            local endPoint = baseCorner + direction * segmentLength
            line.From = baseCorner
            line.To = endPoint
            line.Color = params.Color or ESP.Config.BoxColor
            local baseTransparency = params.Transparency
            if baseTransparency == nil then
                 baseTransparency = CalculateTransparency(distance)
            end
            local midpoint = Vector2.new((baseCorner.X + endPoint.X) * 0.5, (baseCorner.Y + endPoint.Y) * 0.5)line.Transparency = applySpotlight(baseTransparency, midpoint, CurrentMouseLocation)local thickness = params.Thickness
            if thickness == nil then
                 thickness = ESP.Config.LineThickness
             end thickness = tonumber(thickness) or 1
            if thickness < 0 then
                 thickness = 0
             end line.Thickness = thickness
            applyZIndex(line, computeZIndex(distance, params, metadata))line.Visible = true
            return true
         end
        local function updateTextDrawing(text:TextDrawing__DARKLUA_TYPE_e, params:TextUpdateParams__DARKLUA_TYPE_r, metadata:any)
            local channel = resolveChannel(params, metadata)local baseEnabled
            if channel == 'PlayerText' then
                 baseEnabled = ESP.Config.Enabled and ESP.Config.Players and ESP.Config.Text
             else
                 baseEnabled = ESP.Config.Enabled
             end
            local enabled = resolveEnabled(params.Enabled, baseEnabled)if not enabled then
                 text.Visible = false
                return false
             end
            local position3D = params.Position
            local screenPos = params.ScreenPosition
            local distance = params.Distance
            if not screenPos then
                 if not position3D then
                     text.Visible = false
                    return false
                 end
                local rawScreen, onScreen = WTVP(position3D)if not(onScreen and rawScreen.Z > 0)then
                     text.Visible = false
                    return false
                 end screenPos = Vector2.new(rawScreen.X, rawScreen.Y)distance = distance or Distance(position3D)
            else
                 distance = distance or 0
             end text.Text = params.Text or text.Text
            text.Color = params.Color or ESP.Config.TextColor
            text.Font = params.Font or ESP.Config.Font
            local computedSize = params.Size or math.max(16 / math.max(distance, 1) * 100, 13)text.Size = computedSize
            local offsetMultiplier = params.VerticalOffsetMultiplier
            if offsetMultiplier == nil and type(metadata) == 'table' then
                 offsetMultiplier = metadata.VerticalOffsetMultiplier
             end
            if offsetMultiplier == nil then
                 offsetMultiplier = ESP.Config.TextOffsetMultiplier
             end offsetMultiplier = tonumber(offsetMultiplier) or 0
            local normalizedOffset = normalizePercentage(offsetMultiplier)if normalizedOffset ~= nil then
                 offsetMultiplier = normalizedOffset
             end offsetMultiplier = math.max(offsetMultiplier, 0)if offsetMultiplier > 0 then
                 local offsetPixels = computedSize * offsetMultiplier
                screenPos = Vector2.new(screenPos.X, screenPos.Y - offsetPixels)
            end text.Position = screenPos
            local baseTransparency = params.Transparency
            if baseTransparency == nil then
                 baseTransparency = CalculateTransparency(distance)
            end text.Transparency = applySpotlight(baseTransparency, screenPos, CurrentMouseLocation)applyZIndex(text, computeZIndex(distance, params, metadata))text.Visible = true
            return true
         end
        local function updateTracerDrawing(line:LineDrawing__DARKLUA_TYPE_d, params:TracerUpdateParams__DARKLUA_TYPE_s, metadata:any)
            local channel = resolveChannel(params, metadata)local baseEnabled
            if channel == 'PlayerTracer' then
                 baseEnabled = ESP.Config.Enabled and ESP.Config.Tracers
             else
                 baseEnabled = ESP.Config.Enabled
             end
            local enabled = resolveEnabled(params.Enabled, baseEnabled)if not enabled then
                 line.Visible = false
                return false
             end
            local fromWorld = params.FromWorld
            if not fromWorld then
                 local localCharacter = LocalPlayer and LocalPlayer.Character or nil
                local localRoot = localCharacter and localCharacter:FindFirstChild('HumanoidRootPart')if not(localRoot and localRoot:IsA('BasePart') and EnsureInstance(localRoot))then
                     line.Visible = false
                    return false
                 end fromWorld = (localRoot :: BasePart).Position
             end
            local targetWorld = params.ToWorld
            local distance = params.Distance or Distance(targetWorld)local startScreen, onScreenStart = WTVP(fromWorld)local endScreen, onScreenEnd = WTVP(targetWorld)if not(onScreenEnd and endScreen.Z > 0 and onScreenStart and startScreen.Z > 0)then
                 line.Visible = false
                return false
             end line.From = Vector2.new(startScreen.X, startScreen.Y)line.To = Vector2.new(endScreen.X, endScreen.Y)local baseTransparency = params.Transparency
            if baseTransparency == nil then
                 baseTransparency = CalculateTransparency(distance * 0.5)
            end
            local referencePoint = Vector2.new(endScreen.X, endScreen.Y)line.Transparency = applySpotlight(baseTransparency, referencePoint, CurrentMouseLocation)line.Thickness = params.Thickness or math.clamp(5 - distance / 100, 1, 5)line.Color = params.Color or ESP.Config.TracerColor
            applyZIndex(line, computeZIndex(distance, params, metadata))line.Visible = true
            return true
         end
        local DrawingFactory = {
            Box2D = {
                Create = function(_:any)
                    return createQuadDrawing()
                end,
                Update = function(object:QuadDrawing__DARKLUA_TYPE_c,
                    params:BoxUpdateParams__DARKLUA_TYPE_p,
                    metadata:any)
                    return updateQuadDrawing(object,
                    '2D',
                    params,
                    metadata)
                end
            },
            Box2DCorners = {
                Create = function(_:any)
                    return createLineDrawing(1)
                end,
                Update = function(object:LineDrawing__DARKLUA_TYPE_d,
                    params:BoxCornerUpdateParams__DARKLUA_TYPE_t,
                    metadata:any)
                    return updateCornerSegmentDrawing(object,
                    params,
                    metadata)
                end
            },
            Box3D = {
                Create = function(_:any)
                    return createQuadDrawing()
                end,
                Update = function(object:QuadDrawing__DARKLUA_TYPE_c,
                    params:BoxUpdateParams__DARKLUA_TYPE_p,
                    metadata:any)
                    return updateQuadDrawing(object,
                    '3D',
                    params,
                    metadata)
                end
            },
            Box3DFull = {
                Create = function(_:any)
                    return createLineDrawing(1)
                end,
                Update = function(object:LineDrawing__DARKLUA_TYPE_d,
                    params:BoxLineUpdateParams__DARKLUA_TYPE_q,
                    metadata:any)
                    return updateLineBoxDrawing(object,
                    params,
                    metadata)
                end
            },
            Text = {
                Create = function(_:any)
                    return createTextDrawing()
                end,
                Update = function(object:TextDrawing__DARKLUA_TYPE_e,
                    params:TextUpdateParams__DARKLUA_TYPE_r,
                    metadata:any)
                    return updateTextDrawing(object,
                    params,
                    metadata)
                end
            },
            Tracer = {
                Create = function(_:any)
                    return createLineDrawing(2)
                end,
                Update = function(object:LineDrawing__DARKLUA_TYPE_d,
                    params:TracerUpdateParams__DARKLUA_TYPE_s,
                    metadata:any)
                    return updateTracerDrawing(object,
                    params,
                    metadata)
                end
            }
        }
        ESP.Drawings.Factory = DrawingFactory
        local function registerUseShortcut(kind:string)
            local functionName = 'Use' .. kind
            ESP.Drawings[functionName] = function(metadata:any?)
                return ESP.Drawings.Acquire(kind, metadata)
            end
         end
        local function refreshDrawingKinds()
            local kinds = {
            }
            for kind in pairs(DrawingFactory)do
                 kinds[#kinds + 1] = kind
             end table.sort(kinds)if type(table.freeze) == 'function' then
                 kinds = table.freeze(kinds)
            end ESP.Drawings.Kinds = kinds
            for _, kind in ipairs(kinds)do
                 registerUseShortcut(kind)
            end
         end refreshDrawingKinds()function ESP.Drawings.RegisterType(name:string, definition:{
                Create:(any)->any,
                Update:(any,
                any,
                any?)->boolean
            })
            assert(type(name) == 'string' and name ~= '', 'ESP.Drawings.RegisterType requires a name')assert(type(definition) == 'table', 'Definition must be a table')assert(type(definition.Create) == 'function', 'Definition.Create must be a function')assert(type(definition.Update) == 'function', 'Definition.Update must be a function')DrawingFactory[name] = definition
            refreshDrawingKinds()if Debugging then
                 logDebug('drawingTypeRegistered', name)
            end
         end function ESP.Drawings.Acquire(kind:string, metadata:any?)
            local definition = DrawingFactory[kind]assert(definition, string.format("Unknown drawing kind '%s'", tostring(kind)))local object = definition.Create(metadata)local destroyed = false
            return {
                Kind = kind,
                Object = object,
                Destroyed = false,
                Update = function(self,
                    params:any)
                    if destroyed then
                         return false
                     end
                    return definition.Update(object,
                    params,
                    metadata)
                end,
                Destroy = function(self)
                    if destroyed then
                         return
                     end destroyed = true self.Destroyed = true Cleanup(object)
                end
            }
        end function ESP.Drawings.Create3DBox()
            local segmentHandles = {
            }
            for index = 1, #Box3DFullEdges do
                 segmentHandles[index] = ESP.Drawings.Acquire('Box3DFull', {
                    Index = index,
                    Channel = 'Custom'
                })
            end
            local destroyed = false
            return {
                Handles = segmentHandles,
                Destroyed = false,
                Update = function(self,
                    params:BoxLineUpdateParams__DARKLUA_TYPE_q)
                    if destroyed then
                         return false
                     end
                    local enabled = params.Enabled
                    local updated = false
                    if enabled == false then
                         for _,
                        handle in ipairs(segmentHandles)do
                             if not handle.Destroyed then
                                 handle:Update({
                                    Enabled = false,
                                    Channel = params.Channel,
                                    ZIndex = params.ZIndex
                                })
updated = true
                             end
                         end
                        return updated
                     end
                    local channel = params.Channel
                    for index,
                    handle in ipairs(segmentHandles)do
                         if not handle.Destroyed then
                             handle:Update({
                                Pivot = params.Pivot,
                                Size = params.Size,
                                Distance = params.Distance,
                                Color = params.Color,
                                Enabled = params.Enabled,
                                Transparency = params.Transparency,
                                Index = index,
                                Channel = channel,
                                ZIndex = params.ZIndex,
                                ZIndexOffset = params.ZIndexOffset,
                                Thickness = params.Thickness
                            })
updated = true
                         end
                     end
                    return updated
                 end,
                Destroy = function(self)
                    if destroyed then
                         return
                     end destroyed = true self.Destroyed = true
                    for _,
                    handle in ipairs(segmentHandles)do
                         handle:Destroy()
                    end
                 end
            }
        end
        local function getBoxColor(model:Model, player:Player)
            :Color3
            if ESP.Config.UseTeamColor and player.TeamColor then
                 return player.TeamColor.Color
             end
            local humanoid = model:FindFirstChildOfClass('Humanoid')if humanoid then
                 if model:FindFirstChild('ForceField')then
                     return Color3.fromRGB(15, 207, 255)
                end
                local maxHealth = humanoid.MaxHealth
                if maxHealth > 0 then
                     return Color3.fromHSV(0.333 * (humanoid.Health / maxHealth), 1, 1)
                end
             end
            return ESP.Config.BoxColor
         end
        local function ensureHighlightRecord(player:Player, character:Model)
            :HighlightRecord__DARKLUA_TYPE_i
            local existing = HighlightStore[player]if existing then
                 existing.character = character
                return existing
             end
            local highlight = character:FindFirstChildWhichIsA('Highlight') :: HighlightInstance__DARKLUA_TYPE_f?if not highlight then
                 highlight = (Instance.new('Highlight') :: any) :: HighlightInstance__DARKLUA_TYPE_f
                highlight.Adornee = character
                highlight.Parent = character
             end
            local record:HighlightRecord__DARKLUA_TYPE_i = {
                player = player,
                character = character,
                highlight = highlight
            }
            HighlightStore[player] = record
            logDebug('createHighlight', tokenForPlayer(player))return record
         end
        local function ensureDrawingRecord(player:Player?, key:string, kind:string, character:Model?, root:BasePart?, metadata:any)
            :DrawingRecord__DARKLUA_TYPE_g
            local existing = DrawingStore[key]if existing then
                 existing.player = player
                existing.character = character
                existing.root = root
                if metadata ~= nil then
                     existing.metadata = metadata
                 end
                return existing
             end
            local definition = DrawingFactory[kind]assert(definition, string.format("Unknown drawing kind '%s'", tostring(kind)))local object = definition.Create(metadata)local record:DrawingRecord__DARKLUA_TYPE_g = {
                key = key,
                kind = kind,
                object = object,
                player = player,
                character = character,
                root = root,
                metadata = metadata
            }
            DrawingStore[key] = record
            if player then
                 registerKey(player, key)
            end
            if Debugging then
                 logDebug('createDrawing', key, kind)
            end
            return record
         end
        local function buildBoxFacade(player:Player, boxType:string, baseKey:string)
            :BoxFacade__DARKLUA_TYPE_j
            local keys:{
                string
            } = {
            }
            if boxType == '3DFull' then
                 for index = 1, #Box3DFullEdges do
                     keys[index] = makeKey(player, baseKey, index)
                end
             elseif  boxType == '2DCorners' then
                 for index = 1, #Box2DCornerSegments do
                     keys[index] = makeKey(player, baseKey, index)
                end
             else
                 keys[1] = makeKey(player, baseKey)
            end
            local destroyed = false
            return {
                Keys = keys,
                Destroyed = false,
                Destroy = function(self:BoxFacade__DARKLUA_TYPE_j)
                    if destroyed then
                         return
                     end destroyed = true self.Destroyed = true
                    for _,
                    key in ipairs(keys)do
                         cleanupDrawingKey(key)
                    end
                 end
            }
        end
        local function buildHighlightFacade(player:Player)
            :HighlightFacade__DARKLUA_TYPE_k
            local destroyed = false
            return {
                Instance = HighlightStore[player] and HighlightStore[player].highlight or nil,
                Destroyed = false,
                Destroy = function(self:HighlightFacade__DARKLUA_TYPE_k)
                    if destroyed then
                         return
                     end destroyed = true self.Destroyed = true cleanupHighlight(player)self.Instance = nil
                 end
            }
        end
        local function buildTracerFacade(player:Player, key:string)
            :TracerFacade__DARKLUA_TYPE_l
            local destroyed = false
            return {
                Key = key,
                Destroyed = false,
                Destroy = function(self:TracerFacade__DARKLUA_TYPE_l)
                    if destroyed then
                         return
                     end destroyed = true self.Destroyed = true
                    if self.Key then
                         cleanupDrawingKey(self.Key)self.Key = nil
                     end
                 end
            }
        end
        local function updateHighlight(record:HighlightRecord__DARKLUA_TYPE_i, character:Model, player:Player, distance:number)
            local highlight = record.highlight
            local enabled = ESP.Config.Enabled and ESP.Config.Highlights
            if ESP.Config.TeamCheck then
                 local localPlayer = LocalPlayer
                if localPlayer then
                     local localTeam = localPlayer.Team
                    local playerTeam = player.Team
                    if localTeam ~= nil and playerTeam ~= nil and playerTeam == localTeam then
                         enabled = false
                     end
                 end
             end highlight.Enabled = enabled
            if not enabled then
                 return
             end highlight.Adornee = character
            highlight.DepthMode = Enum.HighlightDepthMode.AlwaysOnTop
            highlight.FillColor = ESP.Config.HighlightFillColor
            highlight.OutlineColor = ESP.Config.HighlightOutlineColor
            local multiplier = CalculateTransparency(distance)highlight.FillTransparency = math.clamp(ESP.Config.HighlightFillTransparency + (1 - multiplier), 0, 1)highlight.OutlineTransparency = math.clamp(ESP.Config.HighlightOutlineTransparency + (1 - multiplier), 0, 1)
        end
        local function processPlayer(player:Player, desiredKeys:{
                [string]:true
            }, desiredHighlightPlayers:{
                [Player]:true
            }, desiredPlayerSet:{
                [Player]:true
            })
            local character = player.Character
            if not character then
                 return
             end
            local rootInstance = character:FindFirstChild('HumanoidRootPart')if not(rootInstance and rootInstance:IsA('BasePart') and EnsureInstance(rootInstance))then
                 return
             end
            local root = rootInstance :: BasePart
            local pivotCFrame:CFrame
            local success, result = pcall(function()
                :CFrame
                return character:GetPivot()
            end)if success then
                 pivotCFrame = result
             else
                 pivotCFrame = root.CFrame
             end
            local distance = Distance(pivotCFrame.Position)local color = getBoxColor(character, player)local baseKey = 'Box'
            local keepVisual = false
            local boxFacade:BoxFacade__DARKLUA_TYPE_j? = nil
            local highlightFacade:HighlightFacade__DARKLUA_TYPE_k? = nil
            local tracerFacade:TracerFacade__DARKLUA_TYPE_l? = nil
            local boxType = ESP.Config.BoxType
            if ESP.Config.Enabled and ESP.Config.Players and ESP.Config.Boxes then
                 keepVisual = true
                if boxType == '3DFull' then
                     for index = 1, #Box3DFullEdges do
                         local key = makeKey(player, baseKey, index)desiredKeys[key] = true
                        local metadata = {
                            Index = index,
                            Channel = 'PlayerBox',
                            ZIndexOffset = 0
                        }
                        local record = ensureDrawingRecord(player, key, 'Box3DFull', character, root, metadata)DrawingFactory.Box3DFull.Update((record.object :: any) :: LineDrawing__DARKLUA_TYPE_d, {
                            Pivot = pivotCFrame,
                            Size = ESP.Config.BoxSize,
                            Distance = distance,
                            Color = color,
                            Index = index,
                            ZIndexOffset = 0,
                            Thickness = ESP.Config.LineThickness
                        }, record.metadata)
                    end
                 elseif  boxType == '2DCorners' then
                     for index, segment in ipairs(Box2DCornerSegments)do
                         local key = makeKey(player, baseKey, index)desiredKeys[key] = true
                        local metadata = {
                            CornerIndex = segment.CornerIndex,
                            Axis = segment.Axis,
                            Channel = 'PlayerBox',
                            ZIndexOffset = 0
                        }
                        local record = ensureDrawingRecord(player, key, 'Box2DCorners', character, root, metadata)DrawingFactory.Box2DCorners.Update((record.object :: any) :: LineDrawing__DARKLUA_TYPE_d, {
                            Pivot = pivotCFrame,
                            Size = ESP.Config.BoxSize,
                            Distance = distance,
                            Color = color,
                            CornerSize = ESP.Config.BoxCornerSize,
                            ZIndexOffset = 0,
                            Thickness = ESP.Config.LineThickness
                        }, record.metadata)
                    end
                 else
                     local kind = boxType == '2D' and 'Box2D' or 'Box3D'
                    local key = makeKey(player, baseKey)desiredKeys[key] = true
                    local record = ensureDrawingRecord(player, key, kind, character, root, {
                        Channel = 'PlayerBox',
                        ZIndexOffset = 0
                    })
local definition = DrawingFactory[kind]if definition then
                         definition.Update((record.object :: any) :: QuadDrawing__DARKLUA_TYPE_c, {
                            Pivot = pivotCFrame,
                            Size = ESP.Config.BoxSize,
                            Distance = distance,
                            Color = color,
                            ZIndexOffset = 0
                        }, record.metadata)
                    end
                 end boxFacade = buildBoxFacade(player, boxType, baseKey)
            end
            if ESP.Config.Enabled and ESP.Config.Players and ESP.Config.Text then
                 keepVisual = true
                local key = makeKey(player, 'Text')desiredKeys[key] = true
                local textRecord = ensureDrawingRecord(player, key, 'Text', character, root, {
                    Channel = 'PlayerText',
                    ZIndexOffset = 5
                })
DrawingFactory.Text.Update((textRecord.object :: any) :: TextDrawing__DARKLUA_TYPE_e, {
                    Text = (ESP.Config.UseDisplayName and player.DisplayName) or player.Name or 'Unknown',
                    Position = root.Position + Vector3.new(0,
                    5,
                    0),
                    Distance = distance,
                    ZIndexOffset = 5
                }, textRecord.metadata)
            end
            if ESP.Config.Enabled and ESP.Config.Tracers then
                 keepVisual = true
                local tracerKey = makeKey(player, 'Tracer')desiredKeys[tracerKey] = true
                local tracerRecord = ensureDrawingRecord(player, tracerKey, 'Tracer', character, root, {
                    Channel = 'PlayerTracer',
                    ZIndexOffset = - 5
                })
DrawingFactory.Tracer.Update((tracerRecord.object :: any) :: LineDrawing__DARKLUA_TYPE_d, {
                    ToWorld = root.Position,
                    Distance = distance,
                    ZIndexOffset = - 5
                }, tracerRecord.metadata)tracerFacade = buildTracerFacade(player, tracerKey)
            end
            if ESP.Config.Enabled and ESP.Config.Highlights then
                 keepVisual = true desiredHighlightPlayers[player] = true
                local highlightRecord = ensureHighlightRecord(player, character)updateHighlight(highlightRecord, character, player, distance)highlightFacade = buildHighlightFacade(player)
            end
            if keepVisual then
                 desiredPlayerSet[player] = true
                local existing = ESP.Storage.PlayerVisuals[player]if existing and existing.Character == character then
                     existing.Root = root
                    existing.Box = boxFacade
                    existing.HighlightObject = highlightFacade
                    existing.TracerObject = tracerFacade
                 else
                     ESP.Storage.PlayerVisuals[player] = {
                        Character = character,
                        Root = root,
                        Box = boxFacade,
                        HighlightObject = highlightFacade,
                        TracerObject = tracerFacade
                    }
                end
             end
         end
        local function update(deltaTime:number)
            LocalPlayer = Players.LocalPlayer or LocalPlayer
            local desiredKeys:{
                [string]:true
            } = {
            }
            local desiredHighlightPlayers:{
                [Player]:true
            } = {
            }
            local desiredPlayerSet:{
                [Player]:true
            } = {
            }
            if ESP.Config.Spotlight then
                 CurrentMouseLocation = getMouseLocation()
            else
                 CurrentMouseLocation = nil
             end
            if not ESP.Config.Enabled then
                 for key in pairs(DrawingStore)do
                     cleanupDrawingKey(key)
                end
                for player in pairs(HighlightStore)do
                     cleanupHighlight(player)
                end
                local playersToCleanup = {
                } :: {
                    Player
                }
                for player in pairs(ESP.Storage.PlayerVisuals)do
                     playersToCleanup[#playersToCleanup + 1] = player
                 end
                for _, player in ipairs(playersToCleanup)do
                     cleanupPlayer(player)
                end cleanupAllCustomEntries()return
             end
            for _, player in ipairs(Players:GetPlayers())do
                 if player ~= LocalPlayer then
                     processPlayer(player, desiredKeys, desiredHighlightPlayers, desiredPlayerSet)
                end
             end
            for key in pairs(DrawingStore)do
                 if not desiredKeys[key]then
                     cleanupDrawingKey(key)
                end
             end
            for player, record in pairs(HighlightStore)do
                 if not desiredHighlightPlayers[player] or not EnsureInstance(record.character)then
                     cleanupHighlight(player)
                end
             end
            local playersToRemove = {
            } :: {
                Player
            }
            for player in pairs(ESP.Storage.PlayerVisuals)do
                 if not desiredPlayerSet[player]then
                     playersToRemove[#playersToRemove + 1] = player
                 end
             end
            for _, player in ipairs(playersToRemove)do
                 cleanupPlayer(player)
            end processCustomEntries(deltaTime or 0)
        end Connections[#Connections + 1] = workspace:GetPropertyChangedSignal('CurrentCamera'):Connect(function()
            Camera = workspace.CurrentCamera
         end)Connections[#Connections + 1] = Players.PlayerRemoving:Connect(function(player:Player)
            cleanupPlayer(player)
        end)Connections[#Connections + 1] = RunService.RenderStepped:Connect(update)function ESP.Unload()
            for _, connection in ipairs(Connections)do
                 Cleanup(connection)
            end Connections = {
            } :: {
                RBXScriptConnection
            }
            for key in pairs(DrawingStore)do
                 cleanupDrawingKey(key)
            end
            for player in pairs(HighlightStore)do
                 cleanupHighlight(player)
            end
            local playersToCleanup = {
            } :: {
                Player
            }
            for player in pairs(ESP.Storage.PlayerVisuals)do
                 playersToCleanup[#playersToCleanup + 1] = player
             end
            for _, player in ipairs(playersToCleanup)do
                 cleanupPlayer(player)
            end cleanupAllCustomEntries()
        end function ESP.Register(updateFn:(number)->(), validatorFn:((number)->boolean)?, cleanupFn:((CustomHandle__DARKLUA_TYPE_n?)->())?)
            assert(type(updateFn) == 'function', 'ESP.Register requires an update function.')if validatorFn ~= nil then
                 assert(type(validatorFn) == 'function', 'ESP.Register validator must be a function or nil.')
            end
            if cleanupFn ~= nil then
                 assert(type(cleanupFn) == 'function', 'ESP.Register cleanup must be a function or nil.')
            end NextCustomEntryId+=1
            local id = NextCustomEntryId
            local entry:CustomEntry__DARKLUA_TYPE_o = {
                Id = id,
                Update = updateFn,
                Validate = validatorFn,
                Cleanup = cleanupFn,
                Handle = nil
            }
            local handle:CustomHandle__DARKLUA_TYPE_n = {
                Id = id,
                Destroyed = false,
                Destroy = function(self:CustomHandle__DARKLUA_TYPE_n)
                    if self.Destroyed then
                         return
                     end removeCustomEntry(id,
                    'manual')
                end
            }
            entry.Handle = handle
            CustomEntries[id] = entry
            if Debugging then
                 logDebug('customEntryRegistered', tostring(id))
            end
            return handle
         end ESP.Config.Enabled = false ESP.Config.Players = false ESP.Config.Boxes = false
        return ESP
     end)()
end function __DARKLUA_BUNDLE_MODULES.g()
    if not LPH_OBFUSCATED then
         LPH_ENCNUM = function(toEncrypt, ...)
            assert(type(toEncrypt) == 'number' and #{
                ...
            } == 0, [[LPH_ENCNUM only accepts a single constant double or integer as an argument.]])
            return toEncrypt
         end LPH_NUMENC = LPH_ENCNUM
        LPH_ENCSTR = function(toEncrypt, ...)
            assert(type(toEncrypt) == 'string' and #{
                ...
            } == 0, [[LPH_ENCSTR only accepts a single constant string as an argument.]])
            return toEncrypt
         end LPH_STRENC = LPH_ENCSTR
        LPH_ENCFUNC = function(toEncrypt, encKey, decKey, ...)
            assert(type(toEncrypt) == 'function' and type(encKey) == 'string' and #{
                ...
            } == 0, [[LPH_ENCFUNC accepts a constant function, constant string, and string variable as arguments.]])
            return toEncrypt
         end LPH_FUNCENC = LPH_ENCFUNC
        LPH_JIT = function(f, ...)
            assert(type(f) == 'function' and #{
                ...
            } == 0, [[LPH_JIT only accepts a single constant function as an argument.]])
            return f
         end LPH_JIT_MAX = LPH_JIT
        LPH_NO_VIRTUALIZE = function(f, ...)
            assert(type(f) == 'function' and #{
                ...
            } == 0, [[LPH_NO_VIRTUALIZE only accepts a single constant function as an argument.]])
            return f
         end LPH_NO_UPVALUES = function(f, ...)
            assert(type(setfenv) == 'function', [[LPH_NO_UPVALUES can only be used on Lua versions with getfenv & setfenv]])
            assert(type(f) == 'function' and #{
                ...
            } == 0, [[LPH_NO_UPVALUES only accepts a single constant function as an argument.]])
            return f
         end LPH_CRASH = function(...)
            warn('LPH_CRASH INVOKED')
            assert(#{
                ...
            } == 0, 'LPH_CRASH does not accept any arguments.')
        end
     end
    return LPH_NO_VIRTUALIZE(function()
        local Players = game:GetService('Players')local RunService = game:GetService('RunService')local UserInputService = game:GetService('UserInputService')local Camera = workspace.CurrentCamera
        workspace:GetPropertyChangedSignal('CurrentCamera'):Connect(function()
            Camera = workspace.CurrentCamera
         end)local Aiming = {
            HitChance = 100,
            FOV = 60,
            NPCs = false,
            Players = true,
            Enabled = false,
            ShowFOV = true,
            AimTracer = true,
            DynamicFOV = true,
            FOVColor = Color3.fromRGB(255,
            255,
            255),
            AimTracerColor = Color3.fromRGB(255,
            0,
            0),
            CurrentTarget = nil,
            FilterFriends = false,
            CenterLockFOV = false,
            ClosestToCamera = false
        }
        local InternalFOV = Aiming.FOV
        local FOVCircle = Drawing.new('Circle')FOVCircle.NumSides = 20
        FOVCircle.Transparency = 1
        FOVCircle.Thickness = 2
        FOVCircle.Color = Aiming.FOVColor
        FOVCircle.Filled = false
        local FOVTracer = Drawing.new('Line')FOVTracer.Thickness = 2
        local function UpdateFOV()
            if Aiming.ShowFOV then
                 if Aiming.DynamicFOV then
                     InternalFOV = Aiming.FOV * (70 / Camera.FieldOfView)
                else
                     InternalFOV = Aiming.FOV
                 end FOVCircle.Visible = true FOVCircle.Radius = InternalFOV
                FOVCircle.Color = Aiming.FOVColor
                if Aiming.CenterLockFOV then
                     FOVCircle.Position = Camera.ViewportSize / 2
                 else
                     FOVCircle.Position = UserInputService:GetMouseLocation()
                end
             else
                 FOVCircle.Visible = false
             end
         end
        local function GetCharactersInViewport()
            :{
                {
                    Character:Model,
                    Position:Vector2
                }
            }
            local ToProcess = {
            }
            local CharactersOnScreen = {
            }
            if Aiming.Players then
                 for _, Player in ipairs(Players:GetPlayers())do
                     if Player == Players.LocalPlayer then
                         continue
                     end
                    if Aiming.FilterFriends then
                         if Player:GetAttribute('IsFriend') ~= nil then
                             local LastUpdate = Player:GetAttribute('LastUpdate')if LastUpdate and os.clock() - LastUpdate > 5 then
                                 Player:SetAttribute('IsFriend', Player:IsFriendsWith(Players.LocalPlayer.UserId))Player:SetAttribute('LastUpdate', os.clock())
                            end
                            if Player:GetAttribute('IsFriend') == true then
                                 continue
                             end
                         else
                             Player:SetAttribute('IsFriend', Player:IsFriendsWith(Players.LocalPlayer.UserId))Player:SetAttribute('LastUpdate', os.clock())if Player:GetAttribute('IsFriend') == true then
                                 continue
                             end
                         end
                     end
                    if Player.Character and Player.Character:FindFirstChild('HumanoidRootPart')then
                         local Humanoid = Player.Character:FindFirstChild('Humanoid')if Humanoid and Humanoid.Health > 0 then
                             table.insert(ToProcess, Player.Character)
                        end
                     end
                 end
             end
            if Aiming.NPCs then
                 for _, NPC in next, game:GetService('CollectionService'):GetTagged('NPC')do
                     if NPC:IsDescendantOf(workspace) and NPC:IsA('Model') and NPC:FindFirstChild('HumanoidRootPart') and game:GetService('CollectionService'):HasTag(NPC, 'ActiveCharacter')then
                         table.insert(ToProcess, NPC)
                    end
                 end
             end
            for _, Character in ipairs(ToProcess)do
                 local Position, OnScreen = Camera:WorldToViewportPoint(Character.HumanoidRootPart.Position)if OnScreen then
                     table.insert(CharactersOnScreen, {
                        Character = Character,
                        Position = Vector2.new(Position.X,
                        Position.Y)
                    })
                end
             end
            return CharactersOnScreen
         end
        local function DistanceFromMouse(Position:Vector2)
            :number
            if Aiming.CenterLockFOV then
                 return ((Camera.ViewportSize / 2) - Position).Magnitude
             else
                 return (UserInputService:GetMouseLocation() - Position).Magnitude
             end
         end
        local function GetPlayersInFOV()
            :{
                {
                    Character:Model,
                    Distance:number,
                    Position:Vector2,
                    DistanceFromCamera:number
                }
            }
            local Characters = GetCharactersInViewport()local PlayersInFOV = {
            }
            for _, Character in ipairs(Characters)do
                 local Distance = DistanceFromMouse(Character.Position)if Distance <= InternalFOV then
                     table.insert(PlayersInFOV, {
                        Character = Character.Character,
                        Distance = Distance,
                        Position = Character.Position,
                        DistanceFromCamera = (Camera.CFrame.Position - Character.Character:GetPivot().Position).Magnitude
                    })
                end
             end
            return PlayersInFOV
         end
        local function GetClosestPlayer()
            :(Model, number, Vector2)local PlayersInFOV = GetPlayersInFOV()local ClosestPlayer = nil
            local ClosestDistance = math.huge
            local ClosestPosition = nil
            if Aiming.ClosestToCamera then
                 table.sort(PlayersInFOV, function(a, b)
                    return a.DistanceFromCamera < b.DistanceFromCamera
                 end)
            else
                 table.sort(PlayersInFOV, function(a, b)
                    return a.Distance < b.Distance
                 end)
            end
            if#PlayersInFOV > 0 then
                 local Closest = PlayersInFOV[1]ClosestPlayer = Closest.Character
                ClosestPosition = Closest.Position
                ClosestDistance = Closest.Distance
             end
            return ClosestPlayer, ClosestDistance, ClosestPosition
         end
        local Connection = RunService.RenderStepped:Connect(function()
            if Aiming.Enabled then
                 UpdateFOV()local ClosestPlayer, Distance, Position = GetClosestPlayer()Aiming.CurrentTarget = ClosestPlayer
                if ClosestPlayer then
                     FOVTracer.Visible = Aiming.AimTracer
                    FOVTracer.From = Aiming.CenterLockFOV and (Camera.ViewportSize / 2) or UserInputService:GetMouseLocation()FOVTracer.To = Position
                    FOVTracer.Color = Aiming.AimTracerColor
                 else
                     FOVTracer.Visible = false
                 end
             else
                 FOVCircle.Visible = false FOVTracer.Visible = false Aiming.CurrentTarget = nil
             end
         end)function Aiming.ShouldMiss()
            local HitChance = Aiming.HitChance / 100
            local RandomValue = math.random(0, 100) / 100
            return RandomValue > HitChance
         end
        local function Unload()
            Connection:Disconnect()FOVCircle:Remove()FOVTracer:Remove()
        end Aiming.Unload = Unload
        return Aiming
     end)()
end function __DARKLUA_BUNDLE_MODULES.h()
    if not LPH_OBFUSCATED then
         LPH_ENCNUM = function(toEncrypt, ...)
            assert(type(toEncrypt) == 'number' and #{
                ...
            } == 0, [[LPH_ENCNUM only accepts a single constant double or integer as an argument.]])
            return toEncrypt
         end LPH_NUMENC = LPH_ENCNUM
        LPH_ENCSTR = function(toEncrypt, ...)
            assert(type(toEncrypt) == 'string' and #{
                ...
            } == 0, [[LPH_ENCSTR only accepts a single constant string as an argument.]])
            return toEncrypt
         end LPH_STRENC = LPH_ENCSTR
        LPH_ENCFUNC = function(toEncrypt, encKey, decKey, ...)
            assert(type(toEncrypt) == 'function' and type(encKey) == 'string' and #{
                ...
            } == 0, [[LPH_ENCFUNC accepts a constant function, constant string, and string variable as arguments.]])
            return toEncrypt
         end LPH_FUNCENC = LPH_ENCFUNC
        LPH_JIT = function(f, ...)
            assert(type(f) == 'function' and #{
                ...
            } == 0, [[LPH_JIT only accepts a single constant function as an argument.]])
            return f
         end LPH_JIT_MAX = LPH_JIT
        LPH_NO_VIRTUALIZE = function(f, ...)
            assert(type(f) == 'function' and #{
                ...
            } == 0, [[LPH_NO_VIRTUALIZE only accepts a single constant function as an argument.]])
            return f
         end LPH_NO_UPVALUES = function(f, ...)
            assert(type(setfenv) == 'function', [[LPH_NO_UPVALUES can only be used on Lua versions with getfenv & setfenv]])
            assert(type(f) == 'function' and #{
                ...
            } == 0, [[LPH_NO_UPVALUES only accepts a single constant function as an argument.]])
            return f
         end LPH_CRASH = function(...)
            warn('LPH_CRASH INVOKED')
            assert(#{
                ...
            } == 0, 'LPH_CRASH does not accept any arguments.')
        end
     end
    return LPH_NO_VIRTUALIZE(function()
        local ReplicatedStorage = game:GetService('ReplicatedStorage')local Modules = ReplicatedStorage:WaitForChild('Modules')local Core = Modules:WaitForChild('Core')local Data = require(Core:WaitForChild('Data') :: ModuleScript)local ToolHashes = {
        }
        local InventoryLib = {
        }
        function InventoryLib.ListInventory()
            local InventoryItems = {
            }
            for ItemType, ItemsByType in pairs(Data.items or {
            })
do
                 for ItemName, Items in pairs(ItemsByType)do
                     for _, ItemData in ipairs(Items)do
                         table.insert(InventoryItems, {
                            Type = ItemType,
                            Name = ItemData.name,
                            Guid = ItemData.guid,
                            Location = ItemData.location or 'hand',
                            Amount = ItemData.amount or 1,
                            Durability = ItemData.durability,
                            Health = ItemData.health,
                            Class = ItemData.class and ItemData.class.name or nil,
                            Destroyed = ItemData.destroyed
                        })
                    end
                 end
             end
            return InventoryItems
         end function InventoryLib.GetItemsByType(ItemType)
            local ItemsByType = {
            }
            for Type, Items in pairs(Data.items or {
            })
do
                 if Type == ItemType then
                     for ItemName, ItemData in pairs(Items)do
                         ItemsByType[ItemName] = ItemData
                     end
                 end
             end
            return ItemsByType
         end function InventoryLib.GetItemsByName(ItemName)
            local ItemsByName = {
            }
            local InventoryItems = InventoryLib.ListInventory()for _, Item in ipairs(InventoryItems)do
                 if Item.Name == ItemName then
                     table.insert(ItemsByName, Item)
                end
             end
            return ItemsByName
         end function InventoryLib.FilterByLocation(InventoryItems, Location)
            local FilteredItems = {
            }
            for _, Item in ipairs(InventoryItems)do
                 if Item.Location == Location then
                     table.insert(FilteredItems, Item)
                end
             end
            return FilteredItems
         end function InventoryLib.GetInventoryStats()
            local Data = require(Core.Data :: ModuleScript)local Net = require(Core.Net :: ModuleScript)local function GetItems()
                local counts = {
                    hand = 0,
                    safe = 0
                }
                if Data.items then
                     for _, itemsByType in Data.items do
                         for _, itemsByName in itemsByType do
                             for _, itemData in itemsByName do
                                 if itemData and not itemData.destroyed then
                                     local rawLocation = itemData.location
                                    if typeof(rawLocation) ~= 'string' or rawLocation == '' then
                                         continue
                                     end
                                    local location = string.lower(rawLocation)if location == 'safe' then
                                         counts.safe+=1
                                     elseif  location == 'hand' then
                                         counts.hand+=1
                                     end
                                 end
                             end
                         end
                     end
                 end counts.hand = math.max(counts.hand, 0)counts.safe = math.max(counts.safe, 0)return counts
             end
            local Item_Limits = Net.get('get_max_inventory_space') or {
            }
            local Current_Items = GetItems()local handMax = tonumber(Item_Limits.hand) or 0
            local safeMax = tonumber(Item_Limits.safe) or 0
            local handCurrent = math.max(0, math.floor(Current_Items.hand))local safeCurrent = math.max(0, math.floor(Current_Items.safe))return {
                hand = {
                    current = handCurrent,
                    max = handMax
                },
                safe = {
                    current = safeCurrent,
                    max = safeMax
                }
            }
        end function InventoryLib.GetMoney()
            :(number, number)local MoneyData = Data.money
            return MoneyData.hand or 0, MoneyData.bank or 0
         end function InventoryLib.GetMoneyT()
            :{
                Cash:number,
                Bank:number
            }
            local MoneyData = Data.money
            return {
                Cash = MoneyData.hand or 0,
                Bank = MoneyData.bank or 0
            }
        end
        local function GenerateToolHash(Tool:Tool)
            local AssetIds = {
            }
            for _, Descendant in next, Tool:GetDescendants()do
                 if Descendant:IsA('MeshPart')then
                     local MeshId = Descendant.MeshId
                    if MeshId and MeshId ~= '' then
                         table.insert(AssetIds, MeshId)
                    end
                    if Descendant.TextureID and Descendant.TextureID ~= '' then
                         table.insert(AssetIds, Descendant.TextureID)
                    end table.insert(AssetIds, Descendant.Material.Name)
                elseif  Descendant:IsA('SpecialMesh')then
                     local MeshId = Descendant.MeshId
                    if MeshId and MeshId ~= '' then
                         table.insert(AssetIds, MeshId)
                    end
                    if Descendant.TextureId and Descendant.TextureId ~= '' then
                         table.insert(AssetIds, Descendant.TextureId)
                    end
                    if Descendant.Parent and Descendant.Parent:IsA('BasePart')then
                         table.insert(AssetIds, Descendant.Parent.Material.Name)
                    end
                 end
             end table.sort(AssetIds, function(a, b)
                if tonumber(a:match('%d+')) and tonumber(b:match('%d+'))then
                     return tonumber(a:match('%d+')) < tonumber(b:match('%d+'))
                end
                return a < b
             end)local ConcatenatedIDs = table.concat(AssetIds, ',')local Hash = 0
            for i = 1, #ConcatenatedIDs do
                 Hash = (Hash * 31 + ConcatenatedIDs:byte(i)) % 2 ^ 32
             end
            return Hash
         end function InventoryLib.ResolveDataFromHashedTool(Tool:Tool)
            local Hash = GenerateToolHash(Tool)local ToolReference = ToolHashes[Hash]local ValidCategories = {
                gun = true,
                melee = true,
                accessory = true,
                consumable = true,
                throwable = true
            }
            if not ToolReference then
                 for _, ItemCategory in next, ReplicatedStorage.Items:GetChildren()do
                     if not ValidCategories[ItemCategory.Name]then
                         continue
                     end
                    for _, Item in next, ItemCategory:GetChildren()do
                         local ToolHash = GenerateToolHash(Item)ToolHashes[ToolHash] = Item
                        if ToolHash == Hash then
                             ToolReference = Item break
                         end
                     end
                 end
             end
            if ToolReference then
                 return {
                    Name = ToolReference.Name,
                    Description = ToolReference:GetAttribute('Description'),
                    Rarity = ToolReference:GetAttribute('RarityName'),
                    ImageId = ToolReference:GetAttribute('ImageId'),
                    Price = ToolReference:GetAttribute('RarityPrice')
                }
            end
            return nil
         end function InventoryLib.GetItemsFromCategory(Category:string)
            local Items = {
            }
            local CategoryFolder = ReplicatedStorage.Items:FindFirstChild(Category)if CategoryFolder then
                 for _, Item in next, CategoryFolder:GetChildren()do
                     table.insert(Items, {
                        Name = Item.Name,
                        Description = Item:GetAttribute('Description'),
                        Rarity = Item:GetAttribute('RarityName'),
                        ImageId = Item:GetAttribute('ImageId'),
                        Price = Item:GetAttribute('RarityPrice')
                    })
                end
             end
            return Items
         end function InventoryLib.GetAllItems()
            local Items = {
            }
            local NonItemCategories = {
                'bike',
                'car',
                'cosmetic',
                'money'
            }
            for _, Category in next, ReplicatedStorage.Items:GetChildren()do
                 if table.find(NonItemCategories, Category.Name)then
                     continue
                 end
                for _, Item in next, Category:GetChildren()do
                     table.insert(Items, {
                        Name = Item.Name,
                        Description = Item:GetAttribute('Description'),
                        Rarity = Item:GetAttribute('RarityName'),
                        ImageId = Item:GetAttribute('ImageId'),
                        Price = Item:GetAttribute('RarityPrice')
                    })
                end
             end
            return Items
         end
        local VehicleCategories = {
            'bike',
            'car'
        }
        InventoryLib.VehicleReferences = {
        }
        for _, CategoryName in next, VehicleCategories do
             local Category = ReplicatedStorage:FindFirstChild('Items'):FindFirstChild(CategoryName)if Category then
                 for _, Vehicle in next, Category:GetChildren()do
                     if Vehicle:IsA('Model')then
                         InventoryLib.VehicleReferences[Vehicle.Name] = Vehicle
                     end
                 end
             end
         end
        return InventoryLib
     end)()
end function __DARKLUA_BUNDLE_MODULES.i()
    if not LPH_OBFUSCATED then
         LPH_ENCNUM = function(toEncrypt, ...)
            assert(type(toEncrypt) == 'number' and #{
                ...
            } == 0, [[LPH_ENCNUM only accepts a single constant double or integer as an argument.]])
            return toEncrypt
         end LPH_NUMENC = LPH_ENCNUM
        LPH_ENCSTR = function(toEncrypt, ...)
            assert(type(toEncrypt) == 'string' and #{
                ...
            } == 0, [[LPH_ENCSTR only accepts a single constant string as an argument.]])
            return toEncrypt
         end LPH_STRENC = LPH_ENCSTR
        LPH_ENCFUNC = function(toEncrypt, encKey, decKey, ...)
            assert(type(toEncrypt) == 'function' and type(encKey) == 'string' and #{
                ...
            } == 0, [[LPH_ENCFUNC accepts a constant function, constant string, and string variable as arguments.]])
            return toEncrypt
         end LPH_FUNCENC = LPH_ENCFUNC
        LPH_JIT = function(f, ...)
            assert(type(f) == 'function' and #{
                ...
            } == 0, [[LPH_JIT only accepts a single constant function as an argument.]])
            return f
         end LPH_JIT_MAX = LPH_JIT
        LPH_NO_VIRTUALIZE = function(f, ...)
            assert(type(f) == 'function' and #{
                ...
            } == 0, [[LPH_NO_VIRTUALIZE only accepts a single constant function as an argument.]])
            return f
         end LPH_NO_UPVALUES = function(f, ...)
            assert(type(setfenv) == 'function', [[LPH_NO_UPVALUES can only be used on Lua versions with getfenv & setfenv]])
            assert(type(f) == 'function' and #{
                ...
            } == 0, [[LPH_NO_UPVALUES only accepts a single constant function as an argument.]])
            return f
         end LPH_CRASH = function(...)
            warn('LPH_CRASH INVOKED')
            assert(#{
                ...
            } == 0, 'LPH_CRASH does not accept any arguments.')
        end
     end
    return LPH_NO_VIRTUALIZE(function()
        local RarityColors = {
            ['Common'] = Color3.fromRGB(255,
            255,
            255),
            ['Uncommon'] = Color3.fromRGB(99,
            255,
            52),
            ['Rare'] = Color3.fromRGB(51,
            170,
            255),
            ['Epic'] = Color3.fromRGB(237,
            44,
            255),
            ['Legendary'] = Color3.fromRGB(255,
            150,
            0),
            ['Omega'] = Color3.fromRGB(255,
            20,
            51)
        }
        local InventoryLib = __DARKLUA_BUNDLE_MODULES.load('h')local Collection = {
        }
        local function Collect(Item:RBXScriptConnection | thread)
            table.insert(Collection, Item)return Item
         end
        local function Cleanup(Item:any)
            if typeof(Item) == 'Instance' then
                 Item:Destroy()return
             end
            if typeof(Item) == 'RBXScriptConnection' then
                 Item:Disconnect()return
             end
            if type(Item) == 'thread' then
                 coroutine.close(Item)return
             end
            if type(Item) == 'table' then
                 for Index, Value in pairs(Item)do
                     Cleanup(Value)
                end table.clear(Item)return
             end pcall(function()
                Item:Remove()return
             end)
        end
        local function Unload()
            for _, Item in next, Collection do
                 Cleanup(Item)
            end
         end
        local Players = game:GetService('Players')local CollectionService = game:GetService('CollectionService')local CoreGui = game:GetService('CoreGui')local AssetService = game:GetService('AssetService')local RunService = game:GetService('RunService')for _, Item in next, CoreGui:GetChildren()do
             if Item:IsA('Folder') and Item.Name == 'ItemViewLib' then
                 Item:Destroy()
            end
         end
        local Storage = Instance.new('Folder', CoreGui)Storage.Name = 'ItemViewLib'
        local ItemViewLib = {
            ItemTags = {
                'Gun',
                'Melee',
                'PowerUp',
                'Throwable'
            },
            Views = {
            },
            Cache = {
            },
            Scale = 50,
            MaxDistance = 500,
            Enabled = false,
            Color = Color3.fromRGB(255,
            255,
            255)
        }
        local function NewContainer()
            :BillboardGui
            local Container = Instance.new('BillboardGui')Container.Size = UDim2.new(0, ItemViewLib.Scale * 3, 0, ItemViewLib.Scale * 2)Container.AlwaysOnTop = true Container.StudsOffsetWorldSpace = Vector3.new(0, - 6, 0)Container.ResetOnSpawn = false Container.MaxDistance = ItemViewLib.MaxDistance
            Container.Enabled = ItemViewLib.Enabled
            local Grid = Instance.new('UIGridLayout')Grid.CellSize = UDim2.new(0, ItemViewLib.Scale, 0, ItemViewLib.Scale)Grid.CellPadding = UDim2.new(0, 0, 0, 0)Grid.FillDirection = Enum.FillDirection.Horizontal
            Grid.HorizontalAlignment = Enum.HorizontalAlignment.Center
            Grid.VerticalAlignment = Enum.VerticalAlignment.Center
            Grid.SortOrder = Enum.SortOrder.LayoutOrder
            Grid.Parent = Container
            local Connection = nil Connection = Collect(RunService.RenderStepped:Connect(function()
                if not Container.Parent then
                     Connection:Disconnect()return
                 end
                if not Container.Adornee then
                     Connection:Disconnect()return
                 end Container.MaxDistance = ItemViewLib.MaxDistance
                Container.Enabled = ItemViewLib.Enabled
                if not Container.Adornee then
                     return
                 end
                local Camera = workspace.CurrentCamera
                local CurrentDistance = (Container.Adornee.Position - Camera.CFrame.Position).Magnitude
                local Scale = math.clamp(1 - CurrentDistance / Container.MaxDistance, 0.2, 1) * (70 / Camera.FieldOfView)Grid.CellSize = UDim2.new(0, ItemViewLib.Scale * Scale, 0, ItemViewLib.Scale * Scale)Container.Size = UDim2.new(0, ItemViewLib.Scale * Scale * 3, 0, ItemViewLib.Scale * Scale * 2)for _, Item in next, Container:GetChildren()do
                     if Item:IsA('ImageLabel')then
                         Item.ImageTransparency = 1 - Scale
                        Item.ImageColor3 = ItemViewLib.Color
                     end
                 end
             end))return Container
         end
        local function NewItem(Item:Tool)
            :ImageLabel
            local Type = nil
            local Priority = 0
            for i, Tag in next, ItemViewLib.ItemTags do
                 if CollectionService:HasTag(Item, Tag)then
                     Type = Tag
                    Priority = i break
                 end
             end assert(Type, `Item{ Item } does not have a valid tag`)local ItemData = InventoryLib.ResolveDataFromHashedTool(Item)if not ItemData then
                 error(`Failed to resolve data for item{ Item }`)
            end
            if not ItemViewLib.Cache[ItemData.ImageId]then
                 local EImage = nil
                local MaxRetries = 3
                local RetryCount = 0
                while RetryCount < MaxRetries do
                     local Success, Result = pcall(function()
                        return AssetService:CreateEditableImageAsync(ItemData.ImageId)
                    end)if Success then
                         EImage = Result break
                     else
                         RetryCount+=1
                        warn(`Failed to load texture for{ ItemData.ImageId }, attempt{ RetryCount } / { MaxRetries }:{ Result }`)if RetryCount < MaxRetries then
                             task.wait(0.5)
                        end
                     end
                 end
                if not EImage then
                     warn(`All retries failed for{ ItemData.ImageId }, using fallback red square`)EImage = AssetService:CreateEditableImage({
                        Size = Vector2.new(255,
                        255)
                    })
local FallbackData = buffer.create(255 * 255 * 4)for i = 0, 255 * 255 - 1 do
                         buffer.writeu8(FallbackData, i * 4, 255)buffer.writeu8(FallbackData, i * 4 + 1, 0)buffer.writeu8(FallbackData, i * 4 + 2, 0)buffer.writeu8(FallbackData, i * 4 + 3, 255)
                    end(EImage :: EditableImage):WritePixelsBuffer(Vector2.zero, EImage.Size, FallbackData)
                else
                     local RarityColor = RarityColors[ItemData.Rarity] or Color3.fromRGB(255, 255, 255)local ImageData = EImage:ReadPixelsBuffer(Vector2.zero, EImage.Size)local ProcessedImageData = buffer.create(EImage.Size.X * EImage.Size.Y * 4)local Y = 0
                    for i = 0, EImage.Size.X * EImage.Size.Y - 1 do
                         Y = math.floor(i / EImage.Size.X)local offset = i * 4
                        local A = buffer.readu8(ImageData, offset + 3)if A > 250 then
                             local R = buffer.readu8(ImageData, offset + 0)local G = buffer.readu8(ImageData, offset + 1)local B = buffer.readu8(ImageData, offset + 2)buffer.writeu8(ProcessedImageData, offset + 0, R)buffer.writeu8(ProcessedImageData, offset + 1, G)buffer.writeu8(ProcessedImageData, offset + 2, B)buffer.writeu8(ProcessedImageData, offset + 3, A)
                        elseif  A ~= 0 then
                             local Gradient = math.max(Y / EImage.Size.Y, 0.7)local TintedR = 255 * RarityColor.R * Gradient
                            local TintedG = 255 * RarityColor.G * Gradient
                            local TintedB = 255 * RarityColor.B * Gradient
                            buffer.writeu8(ProcessedImageData, offset + 0, TintedR)buffer.writeu8(ProcessedImageData, offset + 1, TintedG)buffer.writeu8(ProcessedImageData, offset + 2, TintedB)buffer.writeu8(ProcessedImageData, offset + 3, math.min(A * 5, 255))
                        end
                     end EImage:WritePixelsBuffer(Vector2.zero, EImage.Size, ProcessedImageData)
                end ItemViewLib.Cache[ItemData.ImageId] = EImage
             end
            local EImage = ItemViewLib.Cache[ItemData.ImageId]local ItemImage = Instance.new('ImageLabel')ItemImage.Size = UDim2.new(0, 255, 0, 255)ItemImage.BackgroundTransparency = 1
            ItemImage.LayoutOrder = Priority
            ItemImage.ImageContent = Content.fromObject(EImage)return ItemImage
         end
        local function ValidateTool(Item:Tool)
            :boolean
            if(not Item) or (not Item.IsA)then
                 return false
             end
            if not Item:IsA('Tool')then
                 return false
             end
            if not Item:GetAttribute('ImageId')then
                 return false
             end
            if not Item:FindFirstChildOfClass('MeshPart')then
                 return false
             end
            local Valid = false
            for _, Tag in next, ItemViewLib.ItemTags do
                 if CollectionService:HasTag(Item, Tag)then
                     Valid = true break
                 end
             end
            if not Valid then
                 return false
             end
            return true
         end
        local function NewItemView(Player:Player)
            :BillboardGui
            local Character = Player.Character or Player.CharacterAdded:Wait()local Container = NewContainer()local Backpack = Player:WaitForChild('Backpack')Container.Parent = Storage
            Container.Adornee = Character:WaitForChild('HumanoidRootPart')Container.Enabled = true Container.Name = Player.Name
            local function Populate()
                Backpack = Player:WaitForChild('Backpack')Character = Player.Character
                if not(Character and Backpack)then
                     warn('Populate for cycle', Player, 'skipped due to Character or Backpack being nil.')return
                 end
                local HumanoidRootPart = Character:WaitForChild('HumanoidRootPart', 3)if not HumanoidRootPart then
                     return
                 end Container.Adornee = HumanoidRootPart
                for Item, ItemImage in pairs(ItemViewLib.Views)do
                     if ItemImage.Parent == Container then
                         ItemImage:Destroy()ItemViewLib.Views[Item] = nil
                     end
                 end
                for _, Tool in ipairs(Backpack:GetChildren())do
                     if ValidateTool(Tool) and not ItemViewLib.Views[Tool]then
                         local ItemImage = NewItem(Tool)ItemImage.Parent = Container
                        ItemViewLib.Views[Tool] = ItemImage
                     end
                 end
                for _, Tool in ipairs(Character:GetChildren())do
                     if ValidateTool(Tool) and not ItemViewLib.Views[Tool]then
                         local ItemImage = NewItem(Tool)ItemImage.Parent = Container
                        ItemViewLib.Views[Tool] = ItemImage
                     end
                 end
             end Populate()local RefreshLoop = Collect(coroutine.create(function()
                while true do
                     if not Container.Parent then
                         print('Container for', Player, 'cancelled due to NoParent')break
                     end
                    if not Player:IsDescendantOf(Players)then
                         print('Container for', Player, 'cancelled due to NotInPlayers')break
                     end Populate()task.wait(1.5)
                end
             end))coroutine.resume(RefreshLoop)return Container
         end function ItemViewLib:CreateItemView(Player:Player)
            :BillboardGui
            return NewItemView(Player)
        end function ItemViewLib:DestroyItemView(Player:Player)
            :nil
            local Container = Storage:FindFirstChild(Player.Name)if Container then
                 Container:Destroy()
            end
            return nil
         end function ItemViewLib:DestroyAllItemViews()
            :nil
            for _, View in next, Storage:GetChildren()do
                 if View:IsA('BillboardGui')then
                     View:Destroy()
                end
             end
            return nil
         end function ItemViewLib:Init()
            :nil Collect(Players.PlayerAdded:Connect(function(Player)
                Player.CharacterAdded:Wait()self:CreateItemView(Player)
            end))for _, Player in next, Players:GetPlayers()do
                 if Player == Players.LocalPlayer then
                     continue
                 end
                if Player.Character then
                     task.spawn(function()
                        self:CreateItemView(Player)
                    end)
                end
             end
            return nil
         end function ItemViewLib:Unload()
            :nil Storage:Destroy()Unload()return nil
         end ItemViewLib.RarityColors = RarityColors
        return ItemViewLib
     end)()
end function __DARKLUA_BUNDLE_MODULES.j()
    if not LPH_OBFUSCATED then
         LPH_ENCNUM = function(toEncrypt, ...)
            assert(type(toEncrypt) == 'number' and #{
                ...
            } == 0, [[LPH_ENCNUM only accepts a single constant double or integer as an argument.]])
            return toEncrypt
         end LPH_NUMENC = LPH_ENCNUM
        LPH_ENCSTR = function(toEncrypt, ...)
            assert(type(toEncrypt) == 'string' and #{
                ...
            } == 0, [[LPH_ENCSTR only accepts a single constant string as an argument.]])
            return toEncrypt
         end LPH_STRENC = LPH_ENCSTR
        LPH_ENCFUNC = function(toEncrypt, encKey, decKey, ...)
            assert(type(toEncrypt) == 'function' and type(encKey) == 'string' and #{
                ...
            } == 0, [[LPH_ENCFUNC accepts a constant function, constant string, and string variable as arguments.]])
            return toEncrypt
         end LPH_FUNCENC = LPH_ENCFUNC
        LPH_JIT = function(f, ...)
            assert(type(f) == 'function' and #{
                ...
            } == 0, [[LPH_JIT only accepts a single constant function as an argument.]])
            return f
         end LPH_JIT_MAX = LPH_JIT
        LPH_NO_VIRTUALIZE = function(f, ...)
            assert(type(f) == 'function' and #{
                ...
            } == 0, [[LPH_NO_VIRTUALIZE only accepts a single constant function as an argument.]])
            return f
         end LPH_NO_UPVALUES = function(f, ...)
            assert(type(setfenv) == 'function', [[LPH_NO_UPVALUES can only be used on Lua versions with getfenv & setfenv]])
            assert(type(f) == 'function' and #{
                ...
            } == 0, [[LPH_NO_UPVALUES only accepts a single constant function as an argument.]])
            return f
         end LPH_CRASH = function(...)
            warn('LPH_CRASH INVOKED')
            assert(#{
                ...
            } == 0, 'LPH_CRASH does not accept any arguments.')
        end
     end
    return LPH_NO_VIRTUALIZE(function()
        local PathfindingService = game:GetService('PathfindingService')local Players = game:GetService('Players')local LocalPlayer = Players.LocalPlayer
        local TweenService = game:GetService('TweenService')local Debris = game:GetService('Debris')local Camera = workspace.CurrentCamera
        local PathModule = {
            Visualization = true,
            RefreshRate = 1 / 30,
            CurrentTarget = nil,
            Storage = {
                Temporary = {
                }
            }
        }
        local function Marker(Position:Vector3, Index:number?)
            :MarkerObject__DARKLUA_TYPE_u
            local Marker = Instance.new('Part')Marker.Size = Vector3.new(0.5, 0.5, 0.5)Marker.Material = Enum.Material.Neon
            Marker.Color = Color3.fromRGB(255, 0, 0)Marker.Anchored = true Marker.CanCollide = false Marker.CanQuery = false Marker.CFrame = CFrame.new(Position)Marker.Parent = Camera
            Marker.Shape = Enum.PartType.Ball
            Marker.Name = `PathModuleMarker{ Index or 'nan' }`return {
                Object = Marker,
                Destroy = function(self)
                    if self.Object then
                         TweenService:Create(self.Object,
                        TweenInfo.new(1),
                        {
                            Transparency = 1,
                            Size = Vector3.zero
                        }):Play()Debris:AddItem(self.Object,
                        1)
                    end
                 end,
                SetColor = function(self,
                    Color:Color3)
                    self.Object.Color = Color
                 end,
                SetPosition = function(self,
                    Position:Vector3)
                    self.Object.CFrame = CFrame.new(Position)
                end
            }
        end
        local function PV2V3(PV:PVInstance | Vector3)
            :Vector3
            if typeof(PV) == 'Vector3' then
                 return PV
             elseif  typeof(PV) == 'Instance' and PV:IsA('PVInstance')then
                 return PV:GetPivot().Position
             else
                 error(`Invalid type "{typeof(PV)}" for PV2V3`)
            end
         end
        local function PV2CF(PV:PVInstance | Vector3)
            :CFrame
            if typeof(PV) == 'Vector3' then
                 return CFrame.new(PV)
            elseif  typeof(PV) == 'Instance' and PV:IsA('PVInstance')then
                 return PV:GetPivot()
            else
                 error(`Invalid type "{typeof(PV)}" for PV2CF`)
            end
         end
        local function FixDoors()
            for _, Descendant in workspace:GetDescendants()do
                 if(string.find(string.lower(Descendant.Name), 'door'))then
                     local modifier = Instance.new('PathfindingModifier', Descendant)do
                         modifier.Label = 'Door'
                        modifier.PassThrough = true
                     end
                 end
             end
         end
        local function GetHumanoid()
            :Humanoid
            local Character = LocalPlayer.Character
            if not Character then
                 repeat
                     task.wait()
                until LocalPlayer.Character
                Character = LocalPlayer.Character
             end
            local Humanoid = Character:FindFirstChildOfClass('Humanoid')if not Humanoid then
                 repeat
                     task.wait()
                until Character:FindFirstChildOfClass('Humanoid')Humanoid = Character:FindFirstChildOfClass('Humanoid')
            end
            return Humanoid
         end
        local function CreatePathWrapper(path:Path)
            local wrapper = {
            }
            setmetatable(wrapper, {
                __index = path
            })
function wrapper:GetWaypoints()
                local originalWaypoints = path:GetWaypoints()local modifiedWaypoints = {
                }
                for i, waypoint in ipairs(originalWaypoints)do
                     local pos = waypoint.Position
                    if pos.Y < 251 then
                         pos = Vector3.new(pos.X, 251, pos.Z)
                    end modifiedWaypoints[i] = {
                        Position = pos,
                        Action = waypoint.Action,
                        Label = waypoint.Label
                    }
                end
                return modifiedWaypoints
             end
            return wrapper
         end
        local function GetPath(Origin:Vector3 | PVInstance, Target:Vector3 | PVInstance)
            :Path?Origin = PV2V3(Origin)Target = PV2V3(Target)assert(typeof(Origin) == 'Vector3', 'Origin must be a Vector3')assert(typeof(Target) == 'Vector3', 'Target must be a Vector3')local Path = PathfindingService:CreatePath({
                AgentRadius = math.ceil(2 * (GetHumanoid():FindFirstChild('BodyWidthScale') :: NumberValue).Value),
                AgentHeight = math.ceil(5 * (GetHumanoid():FindFirstChild('BodyHeightScale') :: NumberValue).Value),
                AgentCanJump = true,
                AgentJumpHeight = 10,
                AgentMaxSlope = 70,
                Costs = {
                    Water = 20,
                    Door = 1
                }
            })
Path:ComputeAsync(Origin, Target :: Vector3)if Path.Status == Enum.PathStatus.Success then
                 return CreatePathWrapper(Path)
            elseif  Path.Status == Enum.PathStatus.NoPath then
                 warn('PathfindingService: No path found')return
             else
                 warn('Undefined pathfinding status:', Path.Status)return
             end
         end
        local function GetPathH(Origin:Vector3 | PVInstance, Target:Vector3 | PVInstance)
            :Path?Origin = PV2V3(Origin)Target = PV2V3(Target)assert(typeof(Origin) == 'Vector3', 'Origin must be a Vector3')assert(typeof(Target) == 'Vector3', 'Target must be a Vector3')local Path = PathfindingService:CreatePath({
                AgentRadius = 2,
                AgentHeight = 5,
                AgentCanJump = false,
                AgentJumpHeight = 10,
                AgentMaxSlope = 70
            })
Path:ComputeAsync(Origin, Target :: Vector3)if Path.Status == Enum.PathStatus.Success then
                 return CreatePathWrapper(Path)
            elseif  Path.Status == Enum.PathStatus.NoPath then
                 warn('PathfindingService: No path found')return
             else
                 warn('Undefined pathfinding status:', Path.Status)return
             end
         end
        local function VisualizePath(Path:Path)
            :({
                [PathWaypoint]:MarkerObject__DARKLUA_TYPE_u
            })?local PointMarkers = {
            }
            if PathModule.Visualization then
                 local Points = Path:GetWaypoints()for i, Point in next, Points do
                     local Marker = Marker(Point.Position, i)PointMarkers[Point] = Marker
                 end
                return PointMarkers
             else
                 warn('PathModule.Visualization is disabled')return nil
             end
         end
        local function MarkerFromWaypoint(PathMarkers:{
                [PathWaypoint]:MarkerObject__DARKLUA_TYPE_u
            }, Waypoint:PathWaypoint)
            :MarkerObject__DARKLUA_TYPE_u?for _, Marker in next, PathMarkers do
                 if Marker.Object.Position == Waypoint.Position then
                     return Marker
                 end
             end
            return nil
         end
        local function TweenColor(Object:BasePart, Color:Color3, Duration:number)
            local Tween = TweenService:Create(Object, TweenInfo.new(Duration), {
                Color = Color
            })
Tween:Play()return Tween
         end
        local function GetPathLength(Path:Path)
            :number
            local Length = 0
            local Points = Path:GetWaypoints()for i = 1, #Points - 1 do
                 Length+=(Points[i].Position - Points[i + 1].Position).Magnitude
             end
            return Length
         end
        local function GetTravelTime(Distance:number, Speed:number)
            :number
            return Distance / Speed
         end
        return {
            Marker = Marker,
            PV2V3 = PV2V3,
            PV2CF = PV2CF,
            GetPath = GetPath,
            VisualizePath = VisualizePath,
            TweenColor = TweenColor,
            PathModule = PathModule,
            GetPathLength = GetPathLength,
            GetTravelTime = GetTravelTime,
            MarkerFromWaypoint = MarkerFromWaypoint,
            GetPathH = GetPathH
        }
    end)()
end function __DARKLUA_BUNDLE_MODULES.k()
    if not LPH_OBFUSCATED then
         LPH_ENCNUM = function(toEncrypt, ...)
            assert(type(toEncrypt) == 'number' and #{
                ...
            } == 0, [[LPH_ENCNUM only accepts a single constant double or integer as an argument.]])
            return toEncrypt
         end LPH_NUMENC = LPH_ENCNUM
        LPH_ENCSTR = function(toEncrypt, ...)
            assert(type(toEncrypt) == 'string' and #{
                ...
            } == 0, [[LPH_ENCSTR only accepts a single constant string as an argument.]])
            return toEncrypt
         end LPH_STRENC = LPH_ENCSTR
        LPH_ENCFUNC = function(toEncrypt, encKey, decKey, ...)
            assert(type(toEncrypt) == 'function' and type(encKey) == 'string' and #{
                ...
            } == 0, [[LPH_ENCFUNC accepts a constant function, constant string, and string variable as arguments.]])
            return toEncrypt
         end LPH_FUNCENC = LPH_ENCFUNC
        LPH_JIT = function(f, ...)
            assert(type(f) == 'function' and #{
                ...
            } == 0, [[LPH_JIT only accepts a single constant function as an argument.]])
            return f
         end LPH_JIT_MAX = LPH_JIT
        LPH_NO_VIRTUALIZE = function(f, ...)
            assert(type(f) == 'function' and #{
                ...
            } == 0, [[LPH_NO_VIRTUALIZE only accepts a single constant function as an argument.]])
            return f
         end LPH_NO_UPVALUES = function(f, ...)
            assert(type(setfenv) == 'function', [[LPH_NO_UPVALUES can only be used on Lua versions with getfenv & setfenv]])
            assert(type(f) == 'function' and #{
                ...
            } == 0, [[LPH_NO_UPVALUES only accepts a single constant function as an argument.]])
            return f
         end LPH_CRASH = function(...)
            warn('LPH_CRASH INVOKED')
            assert(#{
                ...
            } == 0, 'LPH_CRASH does not accept any arguments.')
        end
     end
    return LPH_NO_VIRTUALIZE(function()
        local ReplicatedStorage = game:GetService('ReplicatedStorage')local StatefulObject = require(ReplicatedStorage:WaitForChild('Modules'):WaitForChild('Core'):WaitForChild('StatefulObject') :: ModuleScript)local Classes = debug.getupvalue(StatefulObject.new_class, 3)assert(Classes and type(Classes) == 'table', 'Classes table not found in StatefulObject module.')local ClassInterface = {
        }
        local function GetInstanceFromPath(path:string)
            local instance = game
            for part in path:gmatch('[^%.]+')do
                 instance = instance:FindFirstChild(part)if not instance then
                     return nil
                 end
             end
            return instance
         end function ClassInterface.GetClasses()
            Classes = debug.getupvalue(StatefulObject.new_class, 3)return Classes
         end function ClassInterface._GetClassInfo(Class:{
                new:(self:any,
                ...any)->any,
                objects:{
                    [any]:any
                }
            })
            if not Class or type(Class) ~= 'table' then
                 warn('Invalid class provided.')return nil
             end
            if not Class.new or type(Class.new) ~= 'function' then
                 warn("Class does not have a valid 'new' method.")return nil
             end
            local Info = {
                Name = '???',
                Module = nil,
                ModulePath = '???',
                Objects = {
                }
            }
            local ClassInitiator = debug.getupvalue(Class.new, 3)if not(ClassInitiator and type(ClassInitiator) == 'function')then
                 warn('ClassInitiator not found for class:', Class)return
             end
            local Module = getfenv(ClassInitiator).script or GetInstanceFromPath(debug.info(ClassInitiator, 's'))local ClassName = Module and Module.Name or '???'
            Info.Name = ClassName
            Info.Module = Module
            Info.ModulePath = Module and Module:GetFullName() or '???'
            Info.Objects = Class.objects
            return Info
         end function ClassInterface.GetClass(TargetClassName:string)
            for i, Class in next, Classes do
                 local ClassInfo = ClassInterface._GetClassInfo(Class)if ClassInfo and (ClassInfo.Name == TargetClassName or tostring(i) == TargetClassName)then
                     return Class
                 end
             end warn('Class not found:', TargetClassName)return nil
         end function ClassInterface.GetClassFromModule(TargetModule:ModuleScript)
            if not TargetModule or not TargetModule:IsA('ModuleScript')then
                 warn('Invalid module script provided.')return nil
             end
            for _, Class in next, Classes do
                 local ClassInfo = ClassInterface._GetClassInfo(Class)if ClassInfo and ClassInfo.Module == TargetModule then
                     return Class
                 end
             end warn('Class not found for module:', TargetModule:GetFullName())return nil
         end
        return ClassInterface
     end)()
end function __DARKLUA_BUNDLE_MODULES.l()
    local TeleportData = {
    }
    local HttpService = game:GetService('HttpService')
    if not isfolder('TeleportData')then
         makefolder('TeleportData')
    end function TeleportData:WriteData(Name:string, Data:{
            any
        })
        writefile(`TeleportData / { Name }.json`, HttpService:JSONEncode(Data))
    end function TeleportData:ReadData(Name:string)
        :{
            any
        }?if not isfile(`TeleportData / { Name }.json`)then
             return nil
         end
        return HttpService:JSONDecode(readfile(`TeleportData / { Name }.json`))
    end function TeleportData:ReadWipe(Name:string)
        :{
            any
        }?if not isfile(`TeleportData / { Name }.json`)then
             return nil
         end
        local Data = HttpService:JSONDecode(readfile(`TeleportData / { Name }.json`))
        delfile(`TeleportData / { Name }.json`)
        return Data
     end function TeleportData:WipeFile(Name:string)
        if isfile(`TeleportData / { Name }.json`)then
             delfile(`TeleportData / { Name }.json`)
        end
     end function TeleportData:WipeAll()
        if isfolder('TeleportData')then
             for _, file in next, listfiles('TeleportData')do
                 delfile(file)
            end
         end
     end
    return TeleportData
 end function __DARKLUA_BUNDLE_MODULES.m()
    if not LPH_OBFUSCATED then
         LPH_ENCNUM = function(toEncrypt, ...)
            assert(type(toEncrypt) == 'number' and #{
                ...
            } == 0, [[LPH_ENCNUM only accepts a single constant double or integer as an argument.]])
            return toEncrypt
         end LPH_NUMENC = LPH_ENCNUM
        LPH_ENCSTR = function(toEncrypt, ...)
            assert(type(toEncrypt) == 'string' and #{
                ...
            } == 0, [[LPH_ENCSTR only accepts a single constant string as an argument.]])
            return toEncrypt
         end LPH_STRENC = LPH_ENCSTR
        LPH_ENCFUNC = function(toEncrypt, encKey, decKey, ...)
            assert(type(toEncrypt) == 'function' and type(encKey) == 'string' and #{
                ...
            } == 0, [[LPH_ENCFUNC accepts a constant function, constant string, and string variable as arguments.]])
            return toEncrypt
         end LPH_FUNCENC = LPH_ENCFUNC
        LPH_JIT = function(f, ...)
            assert(type(f) == 'function' and #{
                ...
            } == 0, [[LPH_JIT only accepts a single constant function as an argument.]])
            return f
         end LPH_JIT_MAX = LPH_JIT
        LPH_NO_VIRTUALIZE = function(f, ...)
            assert(type(f) == 'function' and #{
                ...
            } == 0, [[LPH_NO_VIRTUALIZE only accepts a single constant function as an argument.]])
            return f
         end LPH_NO_UPVALUES = function(f, ...)
            assert(type(setfenv) == 'function', [[LPH_NO_UPVALUES can only be used on Lua versions with getfenv & setfenv]])
            assert(type(f) == 'function' and #{
                ...
            } == 0, [[LPH_NO_UPVALUES only accepts a single constant function as an argument.]])
            return f
         end LPH_CRASH = function(...)
            warn('LPH_CRASH INVOKED')
            assert(#{
                ...
            } == 0, 'LPH_CRASH does not accept any arguments.')
        end
     end
    return LPH_NO_VIRTUALIZE(function()
        local Identifier = {
            Registry = {
            },
            Visuals = {
            },
            AnimationId = 'http://www.roblox.com/asset/?id=507770818',
            OwnerAnimationId = 'rbxassetid://139658061151500',
            Initialized = false,
            Identify = false,
            AnimationTrack = nil,
            Visualize = true
        }
        local Players = game:GetService('Players')local CoreGui = game:GetService('CoreGui')local LocalPlayer = Players.LocalPlayer
        local GuiFolder = CoreGui:FindFirstChild('IdentifierGuis')if not GuiFolder then
             GuiFolder = Instance.new('Folder')GuiFolder.Name = 'IdentifierGuis'
            GuiFolder.Parent = CoreGui
         end
        local function CreateVisual(Player:Player, UserType:string)
            if Identifier.Visuals[Player]then
                 return
             end
            local Character = Player.Character
            local Head = Character and Character:FindFirstChild('Head')if not Head then
                 return
             end
            local BillboardGui = Instance.new('BillboardGui')BillboardGui.Name = Player.Name
            BillboardGui.Adornee = Head
            BillboardGui.AlwaysOnTop = true BillboardGui.LightInfluence = 0
            BillboardGui.Size = UDim2.new(4, 0, 4, 0)BillboardGui.StudsOffset = Vector3.new(0, 5, 0)BillboardGui.ClipsDescendants = false
            local Image = Instance.new('ImageLabel')Image.Image = 'rbxassetid://113209211300754'
            Image.BackgroundTransparency = 1
            Image.Size = UDim2.new(1, 0, 1, 0)Image.Parent = BillboardGui
            if UserType == 'Owner' then
                 local Text = Instance.new('TextLabel')Text.Text = 'Sasware Owner'
                Text.BackgroundTransparency = 1
                Text.Size = UDim2.new(2, 0, 0.5, 0)Text.Position = UDim2.new( - 0.5, 0, 0.8, 0)Text.Font = Enum.Font.SourceSansBold
                Text.TextColor3 = Color3.new(1, 1, 1)Text.TextScaled = true Text.Parent = Image
             end BillboardGui.Parent = GuiFolder
            Identifier.Visuals[Player] = BillboardGui
         end
        local function Scan(Player:Player)
            :string?if Player == LocalPlayer then
                 local userType = Identifier.Identify and (not LPH_OBFUSCATED and 'Owner' or 'User') or nil
                if userType then
                     print(`[Identifier]Local player registered as{ userType }`)
                end
                return userType
             end
            local Character = Player.Character
            if not Character then
                 return nil
             end
            local Humanoid = Character:FindFirstChild('Humanoid')if Humanoid then
                 if Humanoid:FindFirstChild('Animator')then
                     local Animator = Humanoid.Animator
                    for _, Animation in next, Animator:GetPlayingAnimationTracks()do
                         if Animation.Animation.AnimationId == Identifier.OwnerAnimationId then
                             print(`[Identifier]{ Player.Name } is playing the Owner animation.Registered as Owner.`)return 'Owner'
                         elseif  Animation.Animation.AnimationId == Identifier.AnimationId then
                             print(`[Identifier]{ Player.Name } is playing the User animation.Registered as User.`)return 'User'
                         end
                     end
                 end
             end
            return nil
         end function Identifier:Scan(Player:Player)
            :string?if not self.Registry[Player]then
                 self.Registry[Player] = Scan(Player)
            end
            return self.Registry[Player]
        end
        local function UpdateVisuals()
            for Player, Gui in pairs(Identifier.Visuals)do
                 local Character = Player.Character
                local Head = Character and Character:FindFirstChild('Head')local userType = Identifier:Scan(Player)local isOwner = userType == 'Owner'
                local hasOwnerText = Gui:FindFirstChild('ImageLabel') and Gui.ImageLabel:FindFirstChild('TextLabel')if not Head or not userType or not Identifier.Visualize or Player == LocalPlayer or (isOwner and not hasOwnerText) or (not isOwner and hasOwnerText)then
                     Gui:Destroy()Identifier.Visuals[Player] = nil
                 else
                     if Gui.Adornee ~= Head then
                         Gui.Adornee = Head
                     end
                 end
             end
            if Identifier.Visualize then
                 for _, Player in ipairs(Players:GetPlayers())do
                     if Player ~= LocalPlayer then
                         local userType = Identifier:Scan(Player)if userType and not Identifier.Visuals[Player]then
                             CreateVisual(Player, userType)
                        end
                     end
                 end
             end
         end function Identifier:Initialize()
            if self.Initialized then
                 return
             end self.Initialized = true task.spawn(function()
                while self.Initialized do
                     self.Registry = {
                    }
                    for _, Player in next, Players:GetPlayers()do
                         if Player ~= LocalPlayer then
                             self.Registry[Player] = Scan(Player)
                        end
                     end
                    if self.Visualize then
                         UpdateVisuals()
                    end
                    if self.Identify then
                         local Character = LocalPlayer.Character
                        local Humanoid = Character and Character:FindFirstChildOfClass('Humanoid')local Animator = Humanoid and Humanoid:FindFirstChildOfClass('Animator')if Animator then
                             if self.AnimationTrack then
                                 self.AnimationTrack:Stop()self.AnimationTrack:Destroy()
                            end
                            local Animation = Instance.new('Animation')Animation.AnimationId = not LPH_OBFUSCATED and self.OwnerAnimationId or self.AnimationId
                            self.AnimationTrack = Animator:LoadAnimation(Animation)self.AnimationTrack:Play(0, 0.001, 1)self.AnimationTrack.Looped = true self.AnimationTrack:AdjustSpeed(0)Animation:Destroy()
                        end
                     else
                         if self.AnimationTrack then
                             self.AnimationTrack:Stop()self.AnimationTrack:Destroy()self.AnimationTrack = nil
                         end
                     end task.wait(1)
                end
             end)
        end function Identifier:ToggleIdentify(Value:boolean)
            self.Identify = Value
            if Value then
                 self:Initialize()
            else
                 if self.AnimationTrack then
                     self.AnimationTrack:Stop()self.AnimationTrack:Destroy()self.AnimationTrack = nil
                 end
             end
         end function Identifier:Reset()
            self.Registry = {
            }
            self.AnimationTrack = nil self.Identify = false self.Initialized = false
            for _, visual in pairs(self.Visuals)do
                 visual:Destroy()
            end self.Visuals = {
            }
        end function Identifier:Destroy()
            if self.AnimationTrack then
                 self.AnimationTrack:Stop()self.AnimationTrack:Destroy()self.AnimationTrack = nil
             end
            for _, visual in pairs(self.Visuals)do
                 visual:Destroy()
            end self.Visuals = {
            }
            self.Registry = {
            }
            self.Initialized = false self.Identify = false
         end
        return Identifier
     end)()
end function __DARKLUA_BUNDLE_MODULES.n()
    if not LPH_OBFUSCATED then
         LPH_ENCNUM = function(toEncrypt, ...)
            assert(type(toEncrypt) == 'number' and #{
                ...
            } == 0, [[LPH_ENCNUM only accepts a single constant double or integer as an argument.]])
            return toEncrypt
         end LPH_NUMENC = LPH_ENCNUM
        LPH_ENCSTR = function(toEncrypt, ...)
            assert(type(toEncrypt) == 'string' and #{
                ...
            } == 0, [[LPH_ENCSTR only accepts a single constant string as an argument.]])
            return toEncrypt
         end LPH_STRENC = LPH_ENCSTR
        LPH_ENCFUNC = function(toEncrypt, encKey, decKey, ...)
            assert(type(toEncrypt) == 'function' and type(encKey) == 'string' and #{
                ...
            } == 0, [[LPH_ENCFUNC accepts a constant function, constant string, and string variable as arguments.]])
            return toEncrypt
         end LPH_FUNCENC = LPH_ENCFUNC
        LPH_JIT = function(f, ...)
            assert(type(f) == 'function' and #{
                ...
            } == 0, [[LPH_JIT only accepts a single constant function as an argument.]])
            return f
         end LPH_JIT_MAX = LPH_JIT
        LPH_NO_VIRTUALIZE = function(f, ...)
            assert(type(f) == 'function' and #{
                ...
            } == 0, [[LPH_NO_VIRTUALIZE only accepts a single constant function as an argument.]])
            return f
         end LPH_NO_UPVALUES = function(f, ...)
            assert(type(setfenv) == 'function', [[LPH_NO_UPVALUES can only be used on Lua versions with getfenv & setfenv]])
            assert(type(f) == 'function' and #{
                ...
            } == 0, [[LPH_NO_UPVALUES only accepts a single constant function as an argument.]])
            return f
         end LPH_CRASH = function(...)
            warn('LPH_CRASH INVOKED')
            assert(#{
                ...
            } == 0, 'LPH_CRASH does not accept any arguments.')
        end
     end
    return LPH_NO_VIRTUALIZE(function()
        local pi = math.pi
        local abs = math.abs
        local clamp = math.clamp
        local exp = math.exp
        local rad = math.rad
        local sign = math.sign
        local sqrt = math.sqrt
        local tan = math.tan
        local script = Instance.new('LocalScript')local ContextActionService = game:GetService('ContextActionService')local Players = game:GetService('Players')local RunService = game:GetService('RunService')local StarterGui = game:GetService('StarterGui')local UserInputService = game:GetService('UserInputService')local Workspace = game:GetService('Workspace')local Settings = UserSettings()local GameSettings = Settings.GameSettings
        local Lighting = game:GetService('Lighting')local LocalPlayer = Players.LocalPlayer
        if not LocalPlayer then
             Players:GetPropertyChangedSignal('LocalPlayer'):Wait()LocalPlayer = Players.LocalPlayer
         end
        local playerGui = nil
        local freecamGui = nil
        local Camera = Workspace.CurrentCamera
        Workspace:GetPropertyChangedSignal('CurrentCamera'):Connect(function()
            local newCamera = Workspace.CurrentCamera
            if newCamera then
                 Camera = newCamera
             end
         end)local FreecamDepthOfField = nil
        local customGui = nil
        local PlayerState = nil
        local FFlagUserExitFreecamBreaksWithShiftlock do
             local success, result = pcall(function()
                return UserSettings():IsUserFeatureEnabled('UserExitFreecamBreaksWithShiftlock')
            end)FFlagUserExitFreecamBreaksWithShiftlock = success and result
         end
        local FFlagUserShowGuiHideToggles do
             local success, result = pcall(function()
                return UserSettings():IsUserFeatureEnabled('UserShowGuiHideToggles')
            end)FFlagUserShowGuiHideToggles = success and result
         end
        local FFlagUserFixFreecamDeltaTimeCalculation do
             local success, result = pcall(function()
                return UserSettings():IsUserFeatureEnabled('UserFixFreecamDeltaTimeCalculation')
            end)FFlagUserFixFreecamDeltaTimeCalculation = success and result
         end
        local FFlagUserFixFreecamGuiChangeVisibility do
             local success, result = pcall(function()
                return UserSettings():IsUserFeatureEnabled('UserFixFreecamGuiChangeVisibility2')
            end)FFlagUserFixFreecamGuiChangeVisibility = success and result
         end
        local FFlagUserFreecamControlSpeed do
             local success, result = pcall(function()
                return UserSettings():IsUserFeatureEnabled('UserFreecamControlSpeed')
            end)FFlagUserFreecamControlSpeed = success and result
         end
        local FFlagUserFreecamTiltControl do
             local success, result = pcall(function()
                return UserSettings():IsUserFeatureEnabled('UserFreecamTiltControl')
            end)FFlagUserFreecamTiltControl = success and result
         end
        local FFlagUserFreecamSmoothnessControl do
             local success, result = pcall(function()
                return UserSettings():IsUserFeatureEnabled('UserFreecamSmoothnessControl')
            end)FFlagUserFreecamSmoothnessControl = success and result
         end
        local FFlagUserFreecamGuiDestabilization do
             local success, result = pcall(function()
                return UserSettings():IsUserFeatureEnabled('UserFreecamGuiDestabilization')
            end)FFlagUserFreecamGuiDestabilization = success and result
         end
        local FFlagUserFreecamDepthOfFieldEffect do
             local success, result = pcall(function()
                return UserSettings():IsUserFeatureEnabled('UserFreecamDepthOfFieldEffect3')
            end)FFlagUserFreecamDepthOfFieldEffect = success and result
         end
        local FFlagUserFreecamPlayerLock do
             local success, result = pcall(function()
                return UserSettings():IsUserFeatureEnabled('UserFreecamPlayerLock')
            end)FFlagUserFreecamPlayerLock = success and result
         end
        local FFlagUserFreecamCustomGui do
             local success, result = pcall(function()
                return UserSettings():IsUserFeatureEnabled('UserFreecamCustomGui')
            end)FFlagUserFreecamCustomGui = success and result
         end
        local FREECAM_ENABLED_ATTRIBUTE_NAME = 'FreecamEnabled'
        local TOGGLE_INPUT_PRIORITY = Enum.ContextActionPriority.Low.Value
        local INPUT_PRIORITY = Enum.ContextActionPriority.High.Value
        local FREECAM_MACRO_KB = {
            Enum.KeyCode.LeftShift,
            Enum.KeyCode.P
        }
        local FREECAM_TILT_RESET_KB = {
            [Enum.KeyCode.Z] = true,
            [Enum.KeyCode.C] = true
        }
        local FREECAM_TILT_RESET_GP = {
            [Enum.KeyCode.ButtonL1] = true,
            [Enum.KeyCode.ButtonR1] = true
        }
        local FREECAM_DOF_TOGGLE = {
            [Enum.KeyCode.BackSlash] = true
        }
        local FREECAM_PLAYER_LOCK_TOGGLE = {
            [Enum.KeyCode.Slash] = true
        }
        local FREECAM_PLAYER_LOCK_SWITCH = {
            [Enum.KeyCode.R] = true,
            [Enum.KeyCode.T] = true
        }
        local FREECAM_CUSTOM_GUI_TOGGLE = {
            [Enum.KeyCode.G] = true
        }
        local FREECAM_PLAYER_GUI_TOGGLE = {
            [Enum.KeyCode.X] = true
        }
        local FREECAM_LEADERBOARD_TOGGLE = {
            [Enum.KeyCode.L] = true
        }
        local NAV_GAIN = Vector3.new(1, 1, 1) * 64
        local PAN_GAIN = Vector2.new(0.75, 1) * 8
        local FOV_GAIN = 300
        local ROLL_GAIN = - pi / 2
        local PITCH_LIMIT = rad(90)local VEL_STIFFNESS = 1.5
        local PAN_STIFFNESS = 1
        local FOV_STIFFNESS = 4
        local ROLL_STIFFNESS = 1
        local VEL_ADJ_STIFFNESS = 0.75
        local PAN_ADJ_STIFFNESS = 0.75
        local FOV_ADJ_STIFFNESS = 0.75
        local ROLL_ADJ_STIFFNESS = 0.75
        local VEL_MIN_STIFFNESS = 0.01
        local PAN_MIN_STIFFNESS = 0.01
        local FOV_MIN_STIFFNESS = 0.01
        local ROLL_MIN_STIFFNESS = 0.01
        local VEL_MAX_STIFFNESS = 10
        local PAN_MAX_STIFFNESS = 10
        local FOV_MAX_STIFFNESS = 10
        local ROLL_MAX_STIFFNESS = 10
        local lastPressTime = {
        }
        local lastResetTime = 0
        local DOUBLE_TAP_TIME_THRESHOLD = 0.25
        local DOUBLE_TAP_DEBOUNCE_TIME = 0.1
        local postEffects = {
        }
        local playerGuiConnection = nil
        local cameraConnection = nil
        local lightingConnection = nil
        local playerAddedConnection = nil
        local playerRemovingConnection = nil
        local PLAYER_LOCK_DEFAULT_ZOOM = 20
        local PLAYER_LOCK_MIN_ZOOM = 5
        local PLAYER_LOCK_MAX_ZOOM = 50
        local playerLockEnabled = false
        local playerLockZoom = 20
        local playerList = {
        }
        local currentTargetIndex = 1
        local rootPart = nil
        local screenGuisEnabled = false
        local leaderboardEnabled = false
        local Spring = {
        }do
             Spring.__index = Spring function Spring.new(freq, pos)
                local self = setmetatable({
                }, Spring)self.f = freq
                self.p = pos
                self.v = pos * 0
                return self
             end function Spring:Update(dt, goal)
                local f = self.f * 2 * pi
                local p0 = self.p
                local v0 = self.v
                local offset = goal - p0
                local decay = exp( - f * dt)local p1 = goal + (v0 * dt - offset * (f * dt + 1)) * decay
                local v1 = (f * dt * (offset * f - v0) + v0) * decay
                self.p = p1
                self.v = v1
                return p1
             end function Spring:SetFreq(freq)
                self.f = freq
             end function Spring:Reset(pos)
                self.p = pos
                self.v = pos * 0
             end
         end
        local cameraPos = Vector3.new()local cameraRot
        if FFlagUserFreecamTiltControl then
             cameraRot = Vector3.new()
        else
             cameraRot = Vector2.new()
        end
        local cameraFov = 0
        local velSpring = Spring.new(VEL_STIFFNESS, Vector3.new())local panSpring = Spring.new(PAN_STIFFNESS, Vector2.new())local fovSpring = Spring.new(FOV_STIFFNESS, 0)local rollSpring = Spring.new(ROLL_STIFFNESS, 0)local Input = {
        }do
             local thumbstickCurve do
                 local K_CURVATURE = 2
                local K_DEADZONE = 0.15
                local function fCurve(x)
                    return (exp(K_CURVATURE * x) - 1) / (exp(K_CURVATURE) - 1)
                end
                local function fDeadzone(x)
                    return fCurve((x - K_DEADZONE) / (1 - K_DEADZONE))
                end function thumbstickCurve(x)
                    return sign(x) * clamp(fDeadzone(abs(x)), 0, 1)
                end
             end
            local gamepad = {
                ButtonX = 0,
                ButtonY = 0,
                DPadDown = 0,
                DPadUp = 0,
                DPadLeft = 0,
                DPadRight = 0,
                ButtonL2 = 0,
                ButtonR2 = 0,
                ButtonL1 = 0,
                ButtonR1 = 0,
                Thumbstick1 = Vector2.new(),
                Thumbstick2 = Vector2.new()
            }
            local keyboard = {
                W = 0,
                A = 0,
                S = 0,
                D = 0,
                E = 0,
                Q = 0,
                U = 0,
                H = 0,
                J = 0,
                K = 0,
                I = 0,
                Y = 0,
                Up = 0,
                Down = 0,
                Left = 0,
                Right = 0,
                LeftShift = 0,
                RightShift = 0,
                Z = 0,
                C = 0,
                Comma = 0,
                Period = 0,
                LeftBracket = 0,
                RightBracket = 0,
                Semicolon = 0,
                Quote = 0,
                V = 0,
                B = 0,
                N = 0,
                M = 0,
                BackSlash = 0,
                Minus = 0,
                Equals = 0,
                Slash = 0,
                R = 0,
                T = 0,
                G = 0,
                X = 0,
                L = 0
            }
            local mouse = {
                Delta = Vector2.new(),
                MouseWheel = 0
            }
            local DEFAULT_FPS = 60
            local NAV_GAMEPAD_SPEED = Vector3.new(1, 1, 1)local NAV_KEYBOARD_SPEED = Vector3.new(1, 1, 1)local PAN_MOUSE_SPEED = Vector2.new(1, 1) * (pi / 64)local PAN_MOUSE_SPEED_DT = PAN_MOUSE_SPEED / DEFAULT_FPS
            local PAN_GAMEPAD_SPEED = Vector2.new(1, 1) * (pi / 8)local FOV_WHEEL_SPEED = 1
            local FOV_WHEEL_SPEED_DT = FOV_WHEEL_SPEED / DEFAULT_FPS
            local FOV_GAMEPAD_SPEED = 0.25
            local ROLL_GAMEPAD_SPEED = 1
            local ROLL_KEYBOARD_SPEED = 1
            local NAV_ADJ_SPEED = 0.75
            local NAV_MIN_SPEED = 0.01
            local NAV_MAX_SPEED = 4
            local NAV_SHIFT_MUL = 0.25
            local FOV_ADJ_SPEED = 0.75
            local FOV_MIN_SPEED = 0.01
            local FOV_MAX_SPEED = 4
            local ROLL_ADJ_SPEED = 0.75
            local ROLL_MIN_SPEED = 0.01
            local ROLL_MAX_SPEED = 4
            local DoFConstants = {
                FarIntensity = {
                    ADJ = 0.1,
                    MIN = 0,
                    MAX = 1
                },
                NearIntensity = {
                    ADJ = 0.1,
                    MIN = 0,
                    MAX = 1
                },
                FocusDistance = {
                    ADJ = 20,
                    MIN = 0,
                    MAX = 200
                },
                FocusRadius = {
                    ADJ = 5,
                    MIN = 0,
                    MAX = 50
                }
            }
            local navSpeed = 1
            local rollSpeed = 1
            local fovSpeed = 1 function Input.Vel(dt)
                if FFlagUserFreecamControlSpeed then
                     navSpeed = clamp(navSpeed + dt * (keyboard.Up - keyboard.Down + gamepad.DPadUp - gamepad.DPadDown) * NAV_ADJ_SPEED, NAV_MIN_SPEED, NAV_MAX_SPEED)
                else
                     navSpeed = clamp(navSpeed + dt * (keyboard.Up - keyboard.Down) * NAV_ADJ_SPEED, 0.01, 4)
                end
                local kGamepad = Vector3.new(thumbstickCurve(gamepad.Thumbstick1.X), thumbstickCurve(gamepad.ButtonR2) - thumbstickCurve(gamepad.ButtonL2), thumbstickCurve( - gamepad.Thumbstick1.Y)) * NAV_GAMEPAD_SPEED
                local kKeyboard = Vector3.new(keyboard.D - keyboard.A + keyboard.K - keyboard.H, keyboard.E - keyboard.Q + keyboard.I - keyboard.Y, keyboard.S - keyboard.W + keyboard.J - keyboard.U) * NAV_KEYBOARD_SPEED
                local shift = UserInputService:IsKeyDown(Enum.KeyCode.LeftShift) or UserInputService:IsKeyDown(Enum.KeyCode.RightShift)return (kGamepad + kKeyboard) * (navSpeed * (shift and NAV_SHIFT_MUL or 1))
            end function Input.Pan(dt)
                local kGamepad = Vector2.new(thumbstickCurve(gamepad.Thumbstick2.Y), thumbstickCurve( - gamepad.Thumbstick2.X)) * PAN_GAMEPAD_SPEED
                local kMouse = mouse.Delta * PAN_MOUSE_SPEED
                if FFlagUserFixFreecamDeltaTimeCalculation then
                     if dt > 0 then
                         kMouse = (mouse.Delta / dt) * PAN_MOUSE_SPEED_DT
                     end
                 end mouse.Delta = Vector2.new()return kGamepad + kMouse
             end function Input.Fov(dt)
                if FFlagUserFreecamControlSpeed then
                     fovSpeed = clamp(fovSpeed + dt * (keyboard.Right - keyboard.Left + gamepad.DPadRight - gamepad.DPadLeft) * FOV_ADJ_SPEED, FOV_MIN_SPEED, FOV_MAX_SPEED)
                end
                local kGamepad = (gamepad.ButtonX - gamepad.ButtonY) * FOV_GAMEPAD_SPEED
                local kMouse = mouse.MouseWheel * FOV_WHEEL_SPEED
                if FFlagUserFixFreecamDeltaTimeCalculation then
                     if dt > 0 then
                         kMouse = (mouse.MouseWheel / dt) * FOV_WHEEL_SPEED_DT
                     end
                 end mouse.MouseWheel = 0
                if FFlagUserFreecamControlSpeed then
                     return (kGamepad + kMouse) * fovSpeed
                 else
                     return kGamepad + kMouse
                 end
             end function Input.Roll(dt)
                rollSpeed = clamp(rollSpeed + dt * (keyboard.Period - keyboard.Comma) * ROLL_ADJ_SPEED, ROLL_MIN_SPEED, ROLL_MAX_SPEED)local kGamepad = (gamepad.ButtonR1 - gamepad.ButtonL1) * ROLL_GAMEPAD_SPEED
                local kKeyboard = (keyboard.C - keyboard.Z) * ROLL_KEYBOARD_SPEED
                return (kGamepad + kKeyboard) * rollSpeed
             end function Input.SpringControl(dt)
                if FFlagUserFreecamDepthOfFieldEffect then
                     local shiftIsDown = UserInputService:IsKeyDown(Enum.KeyCode.LeftShift) or UserInputService:IsKeyDown(Enum.KeyCode.RightShift)local ctrlIsDown = UserInputService:IsKeyDown(Enum.KeyCode.LeftControl) or UserInputService:IsKeyDown(Enum.KeyCode.RightControl)if shiftIsDown or ctrlIsDown then
                         return
                     end
                 end VEL_STIFFNESS = clamp(VEL_STIFFNESS + dt * (keyboard.RightBracket - keyboard.LeftBracket) * VEL_ADJ_STIFFNESS, VEL_MIN_STIFFNESS, VEL_MAX_STIFFNESS)velSpring:SetFreq(VEL_STIFFNESS)PAN_STIFFNESS = clamp(PAN_STIFFNESS + dt * (keyboard.Quote - keyboard.Semicolon) * PAN_ADJ_STIFFNESS, PAN_MIN_STIFFNESS, PAN_MAX_STIFFNESS)panSpring:SetFreq(PAN_STIFFNESS)FOV_STIFFNESS = clamp(FOV_STIFFNESS + dt * (keyboard.B - keyboard.V) * FOV_ADJ_STIFFNESS, FOV_MIN_STIFFNESS, FOV_MAX_STIFFNESS)fovSpring:SetFreq(FOV_STIFFNESS)ROLL_STIFFNESS = clamp(ROLL_STIFFNESS + dt * (keyboard.M - keyboard.N) * ROLL_ADJ_STIFFNESS, ROLL_MIN_STIFFNESS, ROLL_MAX_STIFFNESS)rollSpring:SetFreq(ROLL_STIFFNESS)
            end function Input.DoF(dt)
                local shiftIsDown = UserInputService:IsKeyDown(Enum.KeyCode.LeftShift) or UserInputService:IsKeyDown(Enum.KeyCode.RightShift)local ctrlIsDown = UserInputService:IsKeyDown(Enum.KeyCode.LeftControl) or UserInputService:IsKeyDown(Enum.KeyCode.RightControl)if shiftIsDown then
                     FreecamDepthOfField.FarIntensity = clamp(FreecamDepthOfField.FarIntensity + dt * (keyboard.RightBracket - keyboard.LeftBracket) * DoFConstants.FarIntensity.ADJ, DoFConstants.FarIntensity.MIN, DoFConstants.FarIntensity.MAX)FreecamDepthOfField.InFocusRadius = clamp(FreecamDepthOfField.InFocusRadius + dt * (keyboard.Equals - keyboard.Minus) * DoFConstants.FocusRadius.ADJ, DoFConstants.FocusRadius.MIN, DoFConstants.FocusRadius.MAX)
                elseif  ctrlIsDown then
                     FreecamDepthOfField.NearIntensity = clamp(FreecamDepthOfField.NearIntensity + dt * (keyboard.RightBracket - keyboard.LeftBracket) * DoFConstants.NearIntensity.ADJ, DoFConstants.NearIntensity.MIN, DoFConstants.NearIntensity.MAX)
                else
                     FreecamDepthOfField.FocusDistance = clamp(FreecamDepthOfField.FocusDistance + dt * (keyboard.Equals - keyboard.Minus) * DoFConstants.FocusDistance.ADJ, DoFConstants.FocusDistance.MIN, DoFConstants.FocusDistance.MAX)
                end
             end do
                 local function resetKeys(keys, table)
                    for keyEnum, _ in pairs(keys)do
                         if table[keyEnum.Name]then
                             table[keyEnum.Name] = 0
                         end
                     end
                 end
                local function handleDoubleTapReset(keyCode)
                    local currentTime = os.clock()local previousPressTime = lastPressTime[keyCode]local timeSinceLastPress = previousPressTime and (currentTime - previousPressTime) or - 1
                    if previousPressTime and (timeSinceLastPress <= DOUBLE_TAP_TIME_THRESHOLD)then
                         if(currentTime - lastResetTime) >= DOUBLE_TAP_DEBOUNCE_TIME then
                             cameraRot = Vector3.new(cameraRot.x, cameraRot.y, 0)rollSpring:Reset(0)if FFlagUserFreecamDepthOfFieldEffect then
                                 resetKeys(FREECAM_TILT_RESET_GP, gamepad)resetKeys(FREECAM_TILT_RESET_KB, keyboard)
                            else
                                 gamepad.ButtonL1 = 0
                                gamepad.ButtonR1 = 0
                                keyboard.C = 0
                                keyboard.Z = 0
                             end lastResetTime = currentTime
                         end
                     end lastPressTime[keyCode] = currentTime
                 end
                local function findPlayerLockRootPart()
                    if not playerList or #playerList < 1 then
                         return nil
                     end
                    local targetPlayer = playerList[currentTargetIndex]local targetCharacter = targetPlayer and targetPlayer.Character
                    return targetCharacter and (targetCharacter:FindFirstChild('HumanoidRootPart') or targetCharacter:FindFirstChild('Torso') or targetCharacter:FindFirstChild('UpperTorso') or targetCharacter:FindFirstChild('Head'))
                end
                local function Keypress(action, state, input)
                    keyboard[input.KeyCode.Name] = state == Enum.UserInputState.Begin and 1 or 0
                    if FFlagUserFreecamTiltControl then
                         if FREECAM_TILT_RESET_KB[input.KeyCode] and input.UserInputState == Enum.UserInputState.Begin then
                             handleDoubleTapReset(input.KeyCode)
                        end
                     end
                    if FFlagUserFreecamDepthOfFieldEffect then
                         if FREECAM_DOF_TOGGLE[input.KeyCode] and input.UserInputState == Enum.UserInputState.Begin then
                             if not FreecamDepthOfField.Enabled then
                                 postEffects = {
                                }
                                for _, effect in ipairs(Camera:GetChildren())do
                                     if effect:IsA('DepthOfFieldEffect') and effect.Enabled then
                                         postEffects[#postEffects + 1] = effect
                                        effect.Enabled = false
                                     end
                                 end
                                for _, effect in ipairs(Lighting:GetChildren())do
                                     if effect:IsA('DepthOfFieldEffect') and effect.Enabled then
                                         postEffects[#postEffects + 1] = effect
                                        effect.Enabled = false
                                     end
                                 end cameraConnection = Camera.ChildAdded:Connect(function(child)
                                    if child:IsA('DepthOfFieldEffect') and child.Enabled then
                                         postEffects[#postEffects + 1] = child
                                        child.Enabled = false
                                     end
                                 end)lightingConnection = Lighting.ChildAdded:Connect(function(child)
                                    if child:IsA('DepthOfFieldEffect') and child.Enabled then
                                         postEffects[#postEffects + 1] = child
                                        child.Enabled = false
                                     end
                                 end)
                            else
                                 for _, effect in ipairs(postEffects)do
                                     if effect.Parent then
                                         effect.Enabled = true
                                     end
                                 end
                                if cameraConnection then
                                     cameraConnection:Disconnect()cameraConnection = nil
                                 end
                                if lightingConnection then
                                     lightingConnection:Disconnect()lightingConnection = nil
                                 end postEffects = {
                                }
                            end FreecamDepthOfField.Enabled = not FreecamDepthOfField.Enabled
                            resetKeys(FREECAM_DOF_TOGGLE, keyboard)
                        end
                     end
                    if FFlagUserFreecamPlayerLock then
                         if FREECAM_PLAYER_LOCK_TOGGLE[input.KeyCode] and input.UserInputState == Enum.UserInputState.Begin then
                             playerLockEnabled = not playerLockEnabled
                            if playerLockEnabled then
                                 playerLockZoom = PLAYER_LOCK_DEFAULT_ZOOM
                                rootPart = findPlayerLockRootPart()
                            end resetKeys(FREECAM_PLAYER_LOCK_TOGGLE, keyboard)
                        end
                        if FREECAM_PLAYER_LOCK_SWITCH[input.KeyCode] and input.UserInputState == Enum.UserInputState.Begin then
                             if playerLockEnabled and #playerList > 0 then
                                 currentTargetIndex = ((currentTargetIndex - 1) + (keyboard.T - keyboard.R)) % #playerList + 1
                                rootPart = findPlayerLockRootPart()
                            end resetKeys(FREECAM_PLAYER_LOCK_SWITCH, keyboard)
                        end
                     end
                    if FFlagUserFreecamCustomGui then
                         if FREECAM_CUSTOM_GUI_TOGGLE[input.keyCode] and input.UserInputState == Enum.UserInputState.Begin then
                             if freecamGui and freecamGui.Parent then
                                 freecamGui.Enabled = not freecamGui.Enabled
                             end resetKeys(FREECAM_CUSTOM_GUI_TOGGLE, keyboard)
                        end
                     end
                    return Enum.ContextActionResult.Sink
                 end
                local function GpButton(action, state, input)
                    gamepad[input.KeyCode.Name] = state == Enum.UserInputState.Begin and 1 or 0
                    if FFlagUserFreecamTiltControl then
                         if FREECAM_TILT_RESET_GP[input.KeyCode] and input.UserInputState == Enum.UserInputState.Begin then
                             handleDoubleTapReset(input.KeyCode)
                        end
                     end
                    return Enum.ContextActionResult.Sink
                 end
                local function MousePan(action, state, input)
                    local delta = input.Delta
                    mouse.Delta = Vector2.new( - delta.y, - delta.x)return Enum.ContextActionResult.Sink
                 end
                local function Thumb(action, state, input)
                    gamepad[input.KeyCode.Name] = input.Position
                    return Enum.ContextActionResult.Sink
                 end
                local function Trigger(action, state, input)
                    gamepad[input.KeyCode.Name] = input.Position.z
                    return Enum.ContextActionResult.Sink
                 end
                local function MouseWheel(action, state, input)
                    mouse[input.UserInputType.Name] = - input.Position.z
                    return Enum.ContextActionResult.Sink
                 end
                local function Zero(t)
                    for k, v in pairs(t)do
                         t[k] = v * 0
                     end
                 end function Input.StartCapture()
                    if FFlagUserFreecamControlSpeed then
                         ContextActionService:BindActionAtPriority('FreecamKeyboard', Keypress, false, INPUT_PRIORITY, Enum.KeyCode.W, Enum.KeyCode.U, Enum.KeyCode.A, Enum.KeyCode.H, Enum.KeyCode.S, Enum.KeyCode.J, Enum.KeyCode.D, Enum.KeyCode.K, Enum.KeyCode.E, Enum.KeyCode.I, Enum.KeyCode.Q, Enum.KeyCode.Y)ContextActionService:BindActionAtPriority('FreecamKeyboardControlSpeed', Keypress, false, INPUT_PRIORITY, Enum.KeyCode.Up, Enum.KeyCode.Down, Enum.KeyCode.Left, Enum.KeyCode.Right)ContextActionService:BindActionAtPriority('FreecamGamepadControlSpeed', GpButton, false, INPUT_PRIORITY, Enum.KeyCode.DPadUp, Enum.KeyCode.DPadDown, Enum.KeyCode.DPadLeft, Enum.KeyCode.DPadRight)
                    else
                         ContextActionService:BindActionAtPriority('FreecamKeyboard', Keypress, false, INPUT_PRIORITY, Enum.KeyCode.W, Enum.KeyCode.U, Enum.KeyCode.A, Enum.KeyCode.H, Enum.KeyCode.S, Enum.KeyCode.J, Enum.KeyCode.D, Enum.KeyCode.K, Enum.KeyCode.E, Enum.KeyCode.I, Enum.KeyCode.Q, Enum.KeyCode.Y, Enum.KeyCode.Up, Enum.KeyCode.Down)
                    end
                    if FFlagUserFreecamTiltControl then
                         ContextActionService:BindActionAtPriority('FreecamKeyboardTiltControl', Keypress, false, INPUT_PRIORITY, Enum.KeyCode.Z, Enum.KeyCode.C)ContextActionService:BindActionAtPriority('FreecamGamepadTiltControl', GpButton, false, INPUT_PRIORITY, Enum.KeyCode.ButtonL1, Enum.KeyCode.ButtonR1)ContextActionService:BindActionAtPriority('FreecamKeyboardTiltControlSpeed', Keypress, false, INPUT_PRIORITY, Enum.KeyCode.Comma, Enum.KeyCode.Period)if FFlagUserFreecamSmoothnessControl then
                             ContextActionService:BindActionAtPriority('FreecamKeyboardSmoothnessControl', Keypress, false, INPUT_PRIORITY, Enum.KeyCode.LeftBracket, Enum.KeyCode.RightBracket, Enum.KeyCode.Semicolon, Enum.KeyCode.Quote, Enum.KeyCode.V, Enum.KeyCode.B, Enum.KeyCode.N, Enum.KeyCode.M)
                        end
                     end
                    if FFlagUserFreecamDepthOfFieldEffect then
                         ContextActionService:BindActionAtPriority('FreecamKeyboardDoFToggle', Keypress, false, INPUT_PRIORITY, Enum.KeyCode.BackSlash)ContextActionService:BindActionAtPriority('FreecamKeyboardDoFControls', Keypress, false, INPUT_PRIORITY, Enum.KeyCode.Minus, Enum.KeyCode.Equals)
                    end
                    if FFlagUserFreecamPlayerLock then
                         ContextActionService:BindActionAtPriority('FreecamKeyboardPlayerLockToggle', Keypress, false, INPUT_PRIORITY, Enum.KeyCode.Slash)ContextActionService:BindActionAtPriority('FreecamKeyboardPlayerLockSwitch', Keypress, false, INPUT_PRIORITY, Enum.KeyCode.R, Enum.KeyCode.T)
                    end
                    if FFlagUserFreecamCustomGui then
                         ContextActionService:BindActionAtPriority('FreecamKeyboardCustomGuiToggle', Keypress, false, INPUT_PRIORITY, Enum.KeyCode.G)
                    end ContextActionService:BindActionAtPriority('FreecamMousePan', MousePan, false, INPUT_PRIORITY, Enum.UserInputType.MouseMovement)ContextActionService:BindActionAtPriority('FreecamMouseWheel', MouseWheel, false, INPUT_PRIORITY, Enum.UserInputType.MouseWheel)ContextActionService:BindActionAtPriority('FreecamGamepadButton', GpButton, false, INPUT_PRIORITY, Enum.KeyCode.ButtonX, Enum.KeyCode.ButtonY)ContextActionService:BindActionAtPriority('FreecamGamepadTrigger', Trigger, false, INPUT_PRIORITY, Enum.KeyCode.ButtonR2, Enum.KeyCode.ButtonL2)ContextActionService:BindActionAtPriority('FreecamGamepadThumbstick', Thumb, false, INPUT_PRIORITY, Enum.KeyCode.Thumbstick1, Enum.KeyCode.Thumbstick2)
                end function Input.StopCapture()
                    if not FFlagUserFreecamCustomGui then
                         navSpeed = 1
                        if FFlagUserFreecamControlSpeed then
                             fovSpeed = 1
                         end
                        if FFlagUserFreecamTiltControl then
                             rollSpeed = 1
                         end
                     end Zero(gamepad)Zero(keyboard)Zero(mouse)ContextActionService:UnbindAction('FreecamKeyboard')if FFlagUserFreecamControlSpeed then
                         ContextActionService:UnbindAction('FreecamKeyboardControlSpeed')ContextActionService:UnbindAction('FreecamGamepadControlSpeed')
                    end
                    if FFlagUserFreecamTiltControl then
                         ContextActionService:UnbindAction('FreecamKeyboardTiltControl')ContextActionService:UnbindAction('FreecamGamepadTiltControl')ContextActionService:UnbindAction('FreecamKeyboardTiltControlSpeed')if FFlagUserFreecamSmoothnessControl then
                             ContextActionService:UnbindAction('FreecamKeyboardSmoothnessControl')
                        end
                     end
                    if FFlagUserFreecamDepthOfFieldEffect then
                         ContextActionService:UnbindAction('FreecamKeyboardDoFToggle')ContextActionService:UnbindAction('FreecamKeyboardDoFControls')
                    end
                    if FFlagUserFreecamPlayerLock then
                         ContextActionService:UnbindAction('FreecamKeyboardPlayerLockToggle')ContextActionService:UnbindAction('FreecamKeyboardPlayerLockSwitch')
                    end
                    if FFlagUserFreecamCustomGui then
                         ContextActionService:UnbindAction('FreecamKeyboardCustomGuiToggle')
                    end ContextActionService:UnbindAction('FreecamMousePan')ContextActionService:UnbindAction('FreecamMouseWheel')ContextActionService:UnbindAction('FreecamGamepadButton')ContextActionService:UnbindAction('FreecamGamepadTrigger')ContextActionService:UnbindAction('FreecamGamepadThumbstick')
                end function Input.getNavSpeed()
                    return navSpeed
                 end function Input.getFovSpeed()
                    return fovSpeed
                 end function Input.getRollSpeed()
                    return rollSpeed
                 end
             end
         end
        local function StepFreecam(dt)
            if FFlagUserFreecamSmoothnessControl then
                 Input.SpringControl(dt)
            end
            if FFlagUserFreecamDepthOfFieldEffect then
                 if FreecamDepthOfField and FreecamDepthOfField.Parent then
                     Input.DoF(dt)
                end
             end
            local vel = velSpring:Update(dt, Input.Vel(dt))local pan = panSpring:Update(dt, Input.Pan(dt))local fov = fovSpring:Update(dt, Input.Fov(dt))local roll
            if FFlagUserFreecamTiltControl then
                 roll = rollSpring:Update(dt, Input.Roll(dt))
            end
            local zoomFactor = sqrt(tan(rad(70 / 2)) / tan(rad(cameraFov / 2)))cameraFov = clamp(cameraFov + fov * FOV_GAIN * (dt / zoomFactor), 1, 120)local cameraCFrame
            if FFlagUserFreecamTiltControl then
                 local panVector:Vector2 = pan * PAN_GAIN * (dt / zoomFactor)cameraRot = cameraRot + Vector3.new(panVector.X, panVector.Y, roll * ROLL_GAIN * (dt / zoomFactor))if FFlagUserFreecamSmoothnessControl then
                     cameraRot = Vector3.new(cameraRot.x % (2 * pi), cameraRot.y % (2 * pi), cameraRot.z % (2 * pi))
                else
                     cameraRot = Vector3.new(clamp(cameraRot.x, - PITCH_LIMIT, PITCH_LIMIT), cameraRot.y % (2 * pi), cameraRot.z)
                end cameraCFrame = CFrame.new(cameraPos) * CFrame.fromOrientation(cameraRot.x, cameraRot.y, cameraRot.z) * CFrame.new(vel * NAV_GAIN * dt)
            else
                 cameraRot = cameraRot + pan * PAN_GAIN * (dt / zoomFactor)cameraRot = Vector2.new(clamp(cameraRot.x, - PITCH_LIMIT, PITCH_LIMIT), cameraRot.y % (2 * pi))cameraCFrame = CFrame.new(cameraPos) * CFrame.fromOrientation(cameraRot.x, cameraRot.y, 0) * CFrame.new(vel * NAV_GAIN * dt)
            end
            if FFlagUserFreecamPlayerLock then
                 if playerLockEnabled and rootPart then
                     local zoomDelta = vel.Z * NAV_GAIN.Z * dt
                    playerLockZoom = clamp(playerLockZoom + zoomDelta, PLAYER_LOCK_MIN_ZOOM, PLAYER_LOCK_MAX_ZOOM)local targetCFrame = CFrame.new(rootPart.Position)local rotationCFrame
                    if FFlagUserFreecamTiltControl then
                         rotationCFrame = CFrame.fromOrientation(cameraRot.x, cameraRot.y, cameraRot.z)
                    else
                         rotationCFrame = CFrame.fromOrientation(cameraRot.x, cameraRot.y, 0)
                    end cameraCFrame = targetCFrame * rotationCFrame * CFrame.new(0, 0, playerLockZoom)
                end
             end
            if FFlagUserFreecamCustomGui then
                 if customGui and customGui.Parent and freecamGui and freecamGui.Parent and freecamGui.Enabled then
                     local displayText = ''
                    if dt > 0 then
                         local velocity = (cameraCFrame.p - cameraPos) / dt
                        displayText = displayText .. string.format('Velocity: (%.1f, %.1f, %.1f)\n', velocity.X, velocity.Y, velocity.Z)
                    end displayText = displayText .. string.format('FOV: %.1f\n', cameraFov)if FFlagUserFreecamTiltControl then
                         displayText = displayText .. string.format('Tilt: %.1f\u{b0}\n', math.deg(cameraRot.z))
                    end
                    if FFlagUserFreecamSmoothnessControl then
                         displayText = displayText .. string.format('Stiffness (Vel): %.1f\n', VEL_STIFFNESS)displayText = displayText .. string.format('Stiffness (Pan): %.1f\n', PAN_STIFFNESS)displayText = displayText .. string.format('Stiffness (FOV): %.1f\n', FOV_STIFFNESS)displayText = displayText .. string.format('Stiffness (Roll): %.1f\n', ROLL_STIFFNESS)
                    end
                    if FFlagUserFreecamControlSpeed then
                         displayText = displayText .. string.format('Movement Speed: %.1f\n', Input.getNavSpeed())displayText = displayText .. string.format('Zoom Speed: %.1f\n', Input.getFovSpeed())displayText = displayText .. string.format('Tilt Speed: %.1f\n', Input.getRollSpeed())
                    end
                    if FFlagUserFreecamDepthOfFieldEffect then
                         if FreecamDepthOfField and FreecamDepthOfField.Parent and FreecamDepthOfField.Enabled then
                             displayText = displayText .. string.format('Custom Depth Of Field: On\n')displayText = displayText .. string.format('Custom Depth Of Field Near Intensity: %.1f\n', FreecamDepthOfField.NearIntensity)displayText = displayText .. string.format('Custom Depth Of Field Far Intensity: %.1f\n', FreecamDepthOfField.FarIntensity)displayText = displayText .. string.format('Custom Depth Of Field Focus Distance: %.1f\n', FreecamDepthOfField.FocusDistance)displayText = displayText .. string.format('Custom Depth Of Field Focus Radius: %.1f\n', FreecamDepthOfField.InFocusRadius)
                        else
                             displayText = displayText .. string.format('Custom Depth Of Field: Off\n')
                        end
                     end
                    if FFlagUserFreecamPlayerLock then
                         if playerLockEnabled and #playerList > 0 then
                             displayText = displayText .. string.format('Player Lock: %s\n', playerList[currentTargetIndex].Name)
                        else
                             displayText = displayText .. string.format('Player Lock: Off\n')
                        end
                     end customGui.Text = displayText
                 end
             end cameraPos = cameraCFrame.p
            Camera.CFrame = cameraCFrame
            Camera.Focus = cameraCFrame
            Camera.FieldOfView = cameraFov
         end
        local function CheckMouseLockAvailability()
            local devAllowsMouseLock = Players.LocalPlayer.DevEnableMouseLock
            local devMovementModeIsScriptable = Players.LocalPlayer.DevComputerMovementMode == Enum.DevComputerMovementMode.Scriptable
            local userHasMouseLockModeEnabled = GameSettings.ControlMode == Enum.ControlMode.MouseLockSwitch
            local userHasClickToMoveEnabled = GameSettings.ComputerMovementMode == Enum.ComputerMovementMode.ClickToMove
            local MouseLockAvailable = devAllowsMouseLock and userHasMouseLockModeEnabled and not userHasClickToMoveEnabled and not devMovementModeIsScriptable
            return MouseLockAvailable
         end PlayerState = {
        }do
             local mouseBehavior
            local mouseIconEnabled
            local cameraType
            local cameraFocus
            local cameraCFrame
            local cameraFieldOfView function PlayerState.Push()
                cameraFieldOfView = Camera.FieldOfView
                Camera.FieldOfView = 70
                cameraType = Camera.CameraType
                Camera.CameraType = Enum.CameraType.Custom
                cameraCFrame = Camera.CFrame
                cameraFocus = Camera.Focus
                mouseIconEnabled = UserInputService.MouseIconEnabled
                UserInputService.MouseIconEnabled = false
                if FFlagUserExitFreecamBreaksWithShiftlock and CheckMouseLockAvailability()then
                     mouseBehavior = Enum.MouseBehavior.Default
                 else
                     mouseBehavior = UserInputService.MouseBehavior
                 end UserInputService.MouseBehavior = Enum.MouseBehavior.Default
             end function PlayerState.Pop()
                Camera.FieldOfView = cameraFieldOfView
                cameraFieldOfView = nil Camera.CameraType = cameraType
                cameraType = nil Camera.CFrame = cameraCFrame
                cameraCFrame = nil Camera.Focus = cameraFocus
                cameraFocus = nil UserInputService.MouseIconEnabled = mouseIconEnabled
                mouseIconEnabled = nil UserInputService.MouseBehavior = mouseBehavior
                mouseBehavior = nil
             end function PlayerState.getScreenGuis()
                return {
                }
            end
         end
        local function removePlayerFromList(player)
            for i, p in ipairs(playerList)do
                 if p == player then
                     table.remove(playerList, i)if currentTargetIndex == i and playerLockEnabled then
                         playerLockEnabled = false currentTargetIndex = 1
                     end
                    if currentTargetIndex > i then
                         currentTargetIndex = currentTargetIndex - 1
                     end
                    if currentTargetIndex > #playerList or currentTargetIndex < 1 then
                         currentTargetIndex = 1
                     end break
                 end
             end
         end
        local function initializePlayerList()
            playerList = Players:GetPlayers()for i, p in ipairs(playerList)do
                 if p == LocalPlayer then
                     currentTargetIndex = i break
                 end
             end playerAddedConnection = Players.PlayerAdded:Connect(function(player)
                table.insert(playerList, player)
            end)playerRemovingConnection = Players.PlayerRemoving:Connect(removePlayerFromList)
        end
        local function StartFreecam()
            if FFlagUserFreecamPlayerLock then
                 initializePlayerList()
            end
            if not FFlagUserFreecamGuiDestabilization then
                 if FFlagUserShowGuiHideToggles then
                     script:SetAttribute(FREECAM_ENABLED_ATTRIBUTE_NAME, true)
                end
             end
            local cameraCFrame = Camera.CFrame
            if FFlagUserFreecamTiltControl then
                 cameraRot = Vector3.new(cameraCFrame:toEulerAnglesYXZ())
            else
                 cameraRot = Vector2.new(cameraCFrame:toEulerAnglesYXZ())
            end cameraPos = cameraCFrame.p
            cameraFov = Camera.FieldOfView
            velSpring:Reset(Vector3.new())panSpring:Reset(Vector2.new())fovSpring:Reset(0)if FFlagUserFreecamTiltControl then
                 rollSpring:Reset(0)
            end
            if not FFlagUserFreecamCustomGui then
                 if FFlagUserFreecamSmoothnessControl then
                     VEL_STIFFNESS = 1.5
                    PAN_STIFFNESS = 1
                    FOV_STIFFNESS = 4
                    ROLL_STIFFNESS = 1
                 end
             end
            if FFlagUserFreecamCustomGui then
                 playerGui = LocalPlayer:WaitForChild('PlayerGui')freecamGui = playerGui:WaitForChild('Freecam')if not customGui or not customGui.Parent then
                     customGui = Instance.new('TextLabel')customGui.Name = 'FreecamCustomGui'
                    customGui.TextColor3 = Color3.new(1, 1, 1)customGui.Font = Enum.Font.SourceSansBold
                    customGui.TextSize = 20
                    customGui.TextStrokeTransparency = 0
                    customGui.BackgroundTransparency = 1
                    customGui.TextWrapped = true customGui.TextXAlignment = Enum.TextXAlignment.Right
                    customGui.AutomaticSize = Enum.AutomaticSize.Y
                    customGui.AnchorPoint = Vector2.new(1, 1)customGui.Position = UDim2.new(1, - 10, 1, - 10)customGui.Size = UDim2.new(0, 400, 0, 0)customGui.Parent = freecamGui
                 end
             end PlayerState.Push()if FFlagUserFreecamDepthOfFieldEffect then
                 if not FreecamDepthOfField or not FreecamDepthOfField.Parent then
                     FreecamDepthOfField = Instance.new('DepthOfFieldEffect')FreecamDepthOfField.Enabled = false FreecamDepthOfField.Name = 'FreecamDepthOfField'
                    FreecamDepthOfField.Parent = Camera
                 end
             end RunService:BindToRenderStep('Freecam', Enum.RenderPriority.Camera.Value, StepFreecam)Input.StartCapture()
        end
        local function StopFreecam()
            if not FFlagUserFreecamGuiDestabilization then
                 if FFlagUserShowGuiHideToggles then
                     script:SetAttribute(FREECAM_ENABLED_ATTRIBUTE_NAME, false)
                end
             end
            if FFlagUserFreecamPlayerLock then
                 if playerAddedConnection then
                     playerAddedConnection:Disconnect()playerAddedConnection = nil
                 end
                if playerRemovingConnection then
                     playerRemovingConnection:Disconnect()playerRemovingConnection = nil
                 end playerLockEnabled = false currentTargetIndex = 1
                playerList = {
                }
            end
            if FFlagUserFreecamDepthOfFieldEffect then
                 if FreecamDepthOfField and FreecamDepthOfField.Parent then
                     if FreecamDepthOfField.Enabled then
                         for _, effect in ipairs(postEffects)do
                             if effect.Parent then
                                 effect.Enabled = true
                             end
                         end
                        if cameraConnection then
                             cameraConnection:Disconnect()cameraConnection = nil
                         end
                        if lightingConnection then
                             lightingConnection:Disconnect()lightingConnection = nil
                         end postEffects = {
                        }
                    end FreecamDepthOfField.Enabled = false
                 end
             end
            if FFlagUserFreecamCustomGui then
                 if freecamGui and freecamGui.Parent then
                     freecamGui.Enabled = false
                 end
             end Input.StopCapture()RunService:UnbindFromRenderStep('Freecam')PlayerState.Pop()
        end
        local ToggleFreecam do
             local enabled = false ToggleFreecam = function(Value:boolean?)
                local targetEnabled
                if Value ~= nil then
                     targetEnabled = Value
                 else
                     targetEnabled = not enabled
                 end
                if targetEnabled == enabled then
                     return
                 end
                if targetEnabled then
                     StartFreecam()
                else
                     StopFreecam()
                end enabled = targetEnabled
                if FFlagUserFreecamGuiDestabilization then
                     script:SetAttribute(FREECAM_ENABLED_ATTRIBUTE_NAME, enabled)
                end
             end
            local function CheckMacro(macro)
                for i = 1, #macro - 1 do
                     if not UserInputService:IsKeyDown(macro[i])then
                         return
                     end
                 end ToggleFreecam()
            end
            local function HandleActivationInput(action, state, input)
                if state == Enum.UserInputState.Begin then
                     if input.KeyCode == FREECAM_MACRO_KB[#FREECAM_MACRO_KB]then
                         CheckMacro(FREECAM_MACRO_KB)
                    end
                 end
                return Enum.ContextActionResult.Pass
             end ContextActionService:BindActionAtPriority('FreecamToggle', HandleActivationInput, false, TOGGLE_INPUT_PRIORITY, FREECAM_MACRO_KB[#FREECAM_MACRO_KB])if FFlagUserFreecamGuiDestabilization or FFlagUserShowGuiHideToggles then
                 script:SetAttribute(FREECAM_ENABLED_ATTRIBUTE_NAME, enabled)script:GetAttributeChangedSignal(FREECAM_ENABLED_ATTRIBUTE_NAME):Connect(function()
                    local attributeValue = script:GetAttribute(FREECAM_ENABLED_ATTRIBUTE_NAME)if typeof(attributeValue) ~= 'boolean' then
                         script:SetAttribute(FREECAM_ENABLED_ATTRIBUTE_NAME, enabled)return
                     end
                    if attributeValue ~= enabled then
                         if attributeValue then
                             StartFreecam()enabled = true
                         else
                             StopFreecam()enabled = false
                         end
                     end
                 end)
            end
         end
        return ToggleFreecam
     end)()
end function __DARKLUA_BUNDLE_MODULES.o()
    if not LPH_OBFUSCATED then
         LPH_ENCNUM = function(toEncrypt, ...)
            assert(type(toEncrypt) == 'number' and #{
                ...
            } == 0, [[LPH_ENCNUM only accepts a single constant double or integer as an argument.]])
            return toEncrypt
         end LPH_NUMENC = LPH_ENCNUM
        LPH_ENCSTR = function(toEncrypt, ...)
            assert(type(toEncrypt) == 'string' and #{
                ...
            } == 0, [[LPH_ENCSTR only accepts a single constant string as an argument.]])
            return toEncrypt
         end LPH_STRENC = LPH_ENCSTR
        LPH_ENCFUNC = function(toEncrypt, encKey, decKey, ...)
            assert(type(toEncrypt) == 'function' and type(encKey) == 'string' and #{
                ...
            } == 0, [[LPH_ENCFUNC accepts a constant function, constant string, and string variable as arguments.]])
            return toEncrypt
         end LPH_FUNCENC = LPH_ENCFUNC
        LPH_JIT = function(f, ...)
            assert(type(f) == 'function' and #{
                ...
            } == 0, [[LPH_JIT only accepts a single constant function as an argument.]])
            return f
         end LPH_JIT_MAX = LPH_JIT
        LPH_NO_VIRTUALIZE = function(f, ...)
            assert(type(f) == 'function' and #{
                ...
            } == 0, [[LPH_NO_VIRTUALIZE only accepts a single constant function as an argument.]])
            return f
         end LPH_NO_UPVALUES = function(f, ...)
            assert(type(setfenv) == 'function', [[LPH_NO_UPVALUES can only be used on Lua versions with getfenv & setfenv]])
            assert(type(f) == 'function' and #{
                ...
            } == 0, [[LPH_NO_UPVALUES only accepts a single constant function as an argument.]])
            return f
         end LPH_CRASH = function(...)
            warn('LPH_CRASH INVOKED')
            assert(#{
                ...
            } == 0, 'LPH_CRASH does not accept any arguments.')
        end
     end
    return LPH_NO_VIRTUALIZE(function()
        local function ValidatePart(Part:BasePart?)
            return Part and Part.Parent and Part:IsDescendantOf(workspace)
        end
        local Prediction = {
            Connections = {
            },
            TrackedParts = {
            },
            TrackedCharacters = {
            },
            Configuration = {
                AccelerationWindowSize = 2,
                PredictPhysics = true
            },
            ModelSettings = {
                SimplifiedNetworkTime = false,
                AddAccelerationComponent = true,
                UseCustomVelocityResolver = false
            },
            VelocityResolver = {
                TrackedRoots = {
                }
            }
        }
        local function GetCharacterFromPart(Part:BasePart)
            for Character, Data in next, Prediction.TrackedCharacters do
                 if Part:IsDescendantOf(Character)then
                     return Character, Data
                 end
             end
            return nil
         end
        local RunService = game:GetService('RunService')local Heartbeat = RunService.Heartbeat
        local os_clock = os.clock
        local function GetResolvedVelocity(RootPart:BasePart)
            :Vector3
            if not Prediction.ModelSettings.UseCustomVelocityResolver then
                 return RootPart.AssemblyLinearVelocity
             end
            local resolverData = Prediction.VelocityResolver.TrackedRoots[RootPart]if resolverData and resolverData.ResolvedVelocity then
                 return resolverData.ResolvedVelocity
             end
            return RootPart.AssemblyLinearVelocity
         end
        local function UpdateVelocityResolver(DeltaTime:number)
            if not Prediction.ModelSettings.UseCustomVelocityResolver then
                 return
             end
            local currentTime = os_clock()for Character, CharData in next, Prediction.TrackedCharacters do
                 local RootPart = CharData.Root
                if RootPart and RootPart.Parent then
                     local currentPos = RootPart.Position
                    local resolverData = Prediction.VelocityResolver.TrackedRoots[RootPart]if resolverData then
                         local timeDelta = currentTime - resolverData.LastTime
                        if timeDelta > 0 then
                             local posDelta = currentPos - resolverData.LastPosition
                            resolverData.ResolvedVelocity = posDelta / timeDelta
                         end resolverData.LastPosition = currentPos
                        resolverData.LastTime = currentTime
                     else
                         Prediction.VelocityResolver.TrackedRoots[RootPart] = {
                            LastPosition = currentPos,
                            LastTime = currentTime,
                            ResolvedVelocity = RootPart.AssemblyLinearVelocity
                        }
                    end
                 else
                     Prediction.VelocityResolver.TrackedRoots[RootPart] = nil
                 end
             end
         end function Prediction:Register(Part:BasePart)
            assert(Part:IsA('BasePart'), string.format('Invalid part class: %s', Part.ClassName))assert(not self.TrackedParts[Part], string.format('Part %s is already registered', Part.Name))self.TrackedParts[Part] = {
                LastVelocity = Vector3.new(0,
                0,
                0),
                PredictedPosition = Part.Position
            }
        end function Prediction:RegisterCharacter(Model:Model)
            assert(Model:IsA('Model'), string.format('Invalid model class: %s', Model.ClassName))assert(Model:FindFirstChild('Humanoid'), 'Model must have a Humanoid')assert(Model:FindFirstChild('HumanoidRootPart'), 'Model must have a HumanoidRootPart')if self.TrackedCharacters[Model]then
                 self:UnregisterCharacter(Model)
            end Prediction:Register(Model:FindFirstChild('HumanoidRootPart') :: BasePart)self.TrackedCharacters[Model] = {
                Root = Model:FindFirstChild('HumanoidRootPart') :: BasePart
            }
            print('Registered character:', Model.Name)
        end function Prediction:UnregisterCharacter(Model:Model)
            if self.TrackedCharacters[Model]then
                 local RootPart = self.TrackedCharacters[Model].Root
                if RootPart and self.TrackedParts[RootPart]then
                     self.TrackedParts[RootPart] = nil
                 end self.TrackedCharacters[Model] = nil print('Unregistered character:', Model.Name)return true
             end
            return false
         end function Prediction:GetPredictedPosition(Part:BasePart)
            assert(Part:IsA('BasePart'), string.format('Invalid part class: %s', Part.ClassName))if not self.TrackedParts[Part]then
                 local Character, Data = GetCharacterFromPart(Part)if Character then
                     if Part == Data.Root then
                         return self.TrackedParts[Data.Root].PredictedPosition
                     else
                         local Offset = Part.Position - Data.Root.Position
                        return self.TrackedParts[Data.Root].PredictedPosition + Offset
                     end
                 else
                     warn(string.format('Part %s is not registered', Part.Name))return Part.Position
                 end
             end
            return self.TrackedParts[Part].PredictedPosition
         end Prediction.Connections.Heartbeat = Heartbeat:Connect(function(DeltaTime)
            UpdateVelocityResolver(DeltaTime)local Ping = game:GetService('Players').LocalPlayer:GetNetworkPing()local NetworkTime = Ping
            if Prediction.ModelSettings.SimplifiedNetworkTime then
                 NetworkTime*=1.15
             else
                 NetworkTime+=DeltaTime + (1 / 60)
            end
            for Part, Data in next, Prediction.TrackedParts do
                 if ValidatePart(Part)then
                     local CurrentVelocity = GetResolvedVelocity(Part)local Acceleration = Vector3.new(0, 0, 0)if DeltaTime > 0 then
                         Acceleration = (CurrentVelocity - Data.LastVelocity) / DeltaTime
                     end Data.LastVelocity = CurrentVelocity
                    Data.PredictedPosition = Part.Position + (CurrentVelocity * NetworkTime)if Prediction.ModelSettings.AddAccelerationComponent then
                         Data.PredictedPosition = Data.PredictedPosition + (Acceleration * 0.5 * (NetworkTime ^ 2))
                    end
                 else
                     Prediction.TrackedParts[Part] = nil Prediction.VelocityResolver.TrackedRoots[Part] = nil
                    for Character, CharData in next, Prediction.TrackedCharacters do
                         if CharData.Root == Part then
                             Prediction.TrackedCharacters[Character] = nil print('Removed invalid tracked character:', Character.Name)break
                         end
                     end
                 end
             end
         end)function Prediction:Cleanup()
            for _, Connection in next, self.Connections do
                 if typeof(Connection) == 'RBXScriptConnection' and Connection.Connected then
                     Connection:Disconnect()
                end
             end self.Connections = {
            }
            self.TrackedParts = {
            }
            self.TrackedCharacters = {
            }
            self.VelocityResolver.TrackedRoots = {
            }
            print('Prediction module cleaned up')
        end function Prediction:GetVelocity(Part:BasePart)
            :Vector3
            return GetResolvedVelocity(Part)
        end
        return Prediction
     end)()
end function __DARKLUA_BUNDLE_MODULES.p()
    local Gizmo = {
    }
    Gizmo.__index = Gizmo function Gizmo.Init(Ceive, Propertys, Request, Release, Retain)
        local self = setmetatable({
        }, Gizmo)
        self.Ceive = Ceive
        self.Propertys = Propertys
        self.Request = Request
        self.Release = Release
        self.Retain = Retain
        return self
     end function Gizmo:Draw(Origin:Vector3, End:Vector3, Radius:number, Length:number, Subdivisions:number)
        local Ceive = self.Ceive
        if not Ceive.Enabled then
             return
         end Ceive.Ray:Draw(Origin, End)
        local ArrowCFrame = CFrame.lookAt(End + ((Origin - End).Unit * (Length / 2)), End)
        Ceive.Cone:Draw(ArrowCFrame, Radius, Length, Subdivisions)
    end function Gizmo:Create(Origin:Vector3, End:Vector3, Radius:number, Length:number, Subdivisions:number)
        local PropertyTable = {
            Origin = Origin,
            End = End,
            Radius = Radius,
            Length = Length,
            Subdivisions = Subdivisions,
            AlwaysOnTop = self.Propertys.AlwaysOnTop,
            Transparency = self.Propertys.Transparency,
            Color3 = self.Propertys.Color3,
            Enabled = true,
            Destroy = false
        }
        self.Retain(self, PropertyTable)
        return PropertyTable
     end function Gizmo:Update(PropertyTable)
        local Ceive = self.Ceive
        Ceive.PushProperty('AlwaysOnTop', PropertyTable.AlwaysOnTop)
        Ceive.PushProperty('Transparency', PropertyTable.Transparency)
        Ceive.PushProperty('Color3', PropertyTable.Color3)
        self:Draw(PropertyTable.Origin, PropertyTable.End, PropertyTable.Radius, PropertyTable.Length, PropertyTable.Subdivisions)
    end
    return Gizmo
 end function __DARKLUA_BUNDLE_MODULES.q()
    local Gizmo = {
    }
    Gizmo.__index = Gizmo function Gizmo.Init(Ceive, Propertys, Request, Release, Retain)
        local self = setmetatable({
        }, Gizmo)
        self.Ceive = Ceive
        self.Propertys = Propertys
        self.Request = Request
        self.Release = Release
        self.Retain = Retain
        return self
     end function Gizmo:Draw(Transform:CFrame, Size:Vector3, DrawTriangles:boolean)
        local Ceive = self.Ceive
        if not Ceive.Enabled then
             return
         end
        local Position = Transform.Position
        local Uv = Transform.UpVector
        local Rv = Transform.RightVector
        local Lv = Transform.LookVector
        local sO2 = Size / 2
        local sUv = Uv * sO2.Y
        local sRv = Rv * sO2.X
        local sLv = Lv * sO2.Z
        local function CalculateYFace(lUv, lRv, lLv)
            local TopLeft = Position + (lUv - lRv + lLv)
            local TopRight = Position + (lUv + lRv + lLv)
            local BottomLeft = Position + (lUv - lRv - lLv)
            local BottomRight = Position + (lUv + lRv - lLv)
            Ceive.Ray:Draw(TopLeft, TopRight)
            Ceive.Ray:Draw(TopLeft, BottomLeft)
            Ceive.Ray:Draw(TopRight, BottomRight)
            if DrawTriangles ~= false then
                 Ceive.Ray:Draw(TopRight, BottomLeft)
            end Ceive.Ray:Draw(BottomLeft, BottomRight)
        end
        local function CalculateZFace(lUv, lRv, lLv)
            local TopLeft = Position + (lUv - lRv + lLv)
            local TopRight = Position + (lUv + lRv + lLv)
            local BottomLeft = Position + ( - lUv - lRv + lLv)
            local BottomRight = Position + ( - lUv + lRv + lLv)
            Ceive.Ray:Draw(TopLeft, TopRight)
            Ceive.Ray:Draw(TopLeft, BottomLeft)
            Ceive.Ray:Draw(TopRight, BottomRight)
            if DrawTriangles ~= false then
                 Ceive.Ray:Draw(TopRight, BottomLeft)
            end Ceive.Ray:Draw(BottomLeft, BottomRight)
        end
        local function CalculateXFace(lUv, lRv, lLv)
            local TopLeft = Position + (lUv - lRv - lLv)
            local TopRight = Position + (lUv - lRv + lLv)
            local BottomLeft = Position + ( - lUv - lRv - lLv)
            local BottomRight = Position + ( - lUv - lRv + lLv)
            Ceive.Ray:Draw(TopLeft, TopRight)
            Ceive.Ray:Draw(TopLeft, BottomLeft)
            Ceive.Ray:Draw(TopRight, BottomRight)
            if DrawTriangles ~= false then
                 Ceive.Ray:Draw(TopRight, BottomLeft)
            end Ceive.Ray:Draw(BottomLeft, BottomRight)
        end CalculateXFace(sUv, sRv, sLv)
        CalculateXFace(sUv, - sRv, sLv)
        CalculateYFace(sUv, sRv, sLv)
        CalculateYFace( - sUv, sRv, sLv)
        CalculateZFace(sUv, sRv, sLv)
        CalculateZFace(sUv, sRv, - sLv)
    end function Gizmo:Create(Transform:CFrame, Size:Vector3, DrawTriangles:boolean)
        local PropertyTable = {
            Transform = Transform,
            Size = Size,
            DrawTriangles = DrawTriangles,
            AlwaysOnTop = self.Propertys.AlwaysOnTop,
            Transparency = self.Propertys.Transparency,
            Color3 = self.Propertys.Color3,
            Enabled = true,
            Destroy = false
        }
        self.Retain(self, PropertyTable)
        return PropertyTable
     end function Gizmo:Update(PropertyTable)
        local Ceive = self.Ceive
        Ceive.PushProperty('AlwaysOnTop', PropertyTable.AlwaysOnTop)
        Ceive.PushProperty('Transparency', PropertyTable.Transparency)
        Ceive.PushProperty('Color3', PropertyTable.Color3)
        self:Draw(PropertyTable.Transform, PropertyTable.Size, PropertyTable.DrawTriangles)
    end
    return Gizmo
 end function __DARKLUA_BUNDLE_MODULES.r()
    local Rad180D = math.rad(180)
    local Gizmo = {
    }
    Gizmo.__index = Gizmo function Gizmo.Init(Ceive, Propertys, Request, Release, Retain)
        local self = setmetatable({
        }, Gizmo)
        self.Ceive = Ceive
        self.Propertys = Propertys
        self.Request = Request
        self.Release = Release
        self.Retain = Retain
        return self
     end function Gizmo:Draw(Transform:CFrame, Radius:number, Length:number, Subdivisions:number)
        local Ceive = self.Ceive
        if not Ceive.Enabled then
             return
         end
        local TopOfCylinder = Transform.Position + (Transform.UpVector * (Length / 2))
        local BottomOfCylinder = Transform.Position - (Transform.UpVector * (Length / 2))
        TopOfCylinder = CFrame.lookAt(TopOfCylinder, TopOfCylinder + Transform.UpVector)
        BottomOfCylinder = CFrame.lookAt(BottomOfCylinder, BottomOfCylinder - Transform.UpVector)
        local AnglePerChunk = math.floor(360 / Subdivisions)
        local LastTop
        local LastBottom
        local FirstTop
        local FirstBottom
        for i = 0, 360, AnglePerChunk do
             local XMagnitude = math.sin(math.rad(i)) * Radius
            local YMagnitude = math.cos(math.rad(i)) * Radius
            local VertexOffset = (Transform.LookVector * YMagnitude) + (Transform.RightVector * XMagnitude)
            local TopVertexPosition = TopOfCylinder.Position + VertexOffset
            local BottomVertexPosition = BottomOfCylinder.Position + VertexOffset
            Ceive.Ray:Draw(TopVertexPosition, BottomVertexPosition)
            Ceive.Circle:Draw(CFrame.new(TopOfCylinder.Position) * Transform.Rotation * CFrame.Angles(0, math.rad(i), 0), Radius, Subdivisions / 2, 90, false)
            Ceive.Circle:Draw(CFrame.new(BottomOfCylinder.Position) * Transform.Rotation * CFrame.Angles(Rad180D, math.rad(i), 0), Radius, Subdivisions / 2, 90, false)
            if not LastTop then
                 LastTop = TopVertexPosition
                LastBottom = BottomVertexPosition
                FirstTop = TopVertexPosition
                FirstBottom = BottomVertexPosition continue
             end Ceive.Ray:Draw(LastTop, TopVertexPosition)
            Ceive.Ray:Draw(LastBottom, BottomVertexPosition)
            LastTop = TopVertexPosition
            LastBottom = BottomVertexPosition
         end Ceive.Ray:Draw(LastTop, FirstTop)
        Ceive.Ray:Draw(LastBottom, FirstBottom)
    end function Gizmo:Create(Transform:CFrame, Radius:number, Length:number, Subdivisions:number)
        local PropertyTable = {
            Transform = Transform,
            Radius = Radius,
            Length = Length,
            Subdivisions = Subdivisions,
            AlwaysOnTop = self.Propertys.AlwaysOnTop,
            Transparency = self.Propertys.Transparency,
            Color3 = self.Propertys.Color3,
            Enabled = true,
            Destroy = false
        }
        self.Retain(self, PropertyTable)
        return PropertyTable
     end function Gizmo:Update(PropertyTable)
        local Ceive = self.Ceive
        Ceive.PushProperty('AlwaysOnTop', PropertyTable.AlwaysOnTop)
        Ceive.PushProperty('Transparency', PropertyTable.Transparency)
        Ceive.PushProperty('Color3', PropertyTable.Color3)
        self:Draw(PropertyTable.Transform, PropertyTable.Radius, PropertyTable.Length, PropertyTable.Subdivisions)
    end
    return Gizmo
 end function __DARKLUA_BUNDLE_MODULES.s()
    local Gizmo = {
    }
    Gizmo.__index = Gizmo function Gizmo.Init(Ceive, Propertys, Request, Release, Retain)
        local self = setmetatable({
        }, Gizmo)
        self.Ceive = Ceive
        self.Propertys = Propertys
        self.Request = Request
        self.Release = Release
        self.Retain = Retain
        return self
     end function Gizmo:Draw(Transform:CFrame, Scale:number)
        local Ceive = self.Ceive
        if not Ceive.Enabled then
             return
         end
        local FORWARD_COLOR = Color3.new(0, 0, 1)
        local UP_COLOR = Color3.new(0, 1, 0)
        local RIGHT_COLOR = Color3.new(1, 0, 0)
        local Origin = Transform.Position
        local Up = Transform.UpVector
        local Right = Transform.RightVector
        local Forward = Transform.LookVector
        local PreviousColor = self.Ceive.PopProperty('Color3')
        self.Ceive.PushProperty('Color3', UP_COLOR)
        self.Ceive.Arrow:Draw(Origin, Origin + Up * Scale, 0.05, 0.15, 3)
        self.Ceive.PushProperty('Color3', RIGHT_COLOR)
        self.Ceive.Arrow:Draw(Origin, Origin + Right * Scale, 0.05, 0.15, 3)
        self.Ceive.PushProperty('Color3', FORWARD_COLOR)
        self.Ceive.Arrow:Draw(Origin, Origin + Forward * Scale, 0.05, 0.15, 3)
        self.Ceive.PushProperty('Color3', PreviousColor)
    end function Gizmo:Create(Transform:CFrame, Scale:number)
        local PropertyTable = {
            Transform = Transform,
            Scale = Scale,
            AlwaysOnTop = self.Propertys.AlwaysOnTop,
            Transparency = self.Propertys.Transparency,
            Enabled = true,
            Destroy = false
        }
        self.Retain(self, PropertyTable)
        return PropertyTable
     end function Gizmo:Update(PropertyTable)
        local Ceive = self.Ceive
        Ceive.PushProperty('AlwaysOnTop', PropertyTable.AlwaysOnTop)
        Ceive.PushProperty('Transparency', PropertyTable.Transparency)
        self:Draw(PropertyTable.Origin, PropertyTable.End)
    end
    return Gizmo
 end function __DARKLUA_BUNDLE_MODULES.t()
    local Gizmo = {
    }
    Gizmo.__index = Gizmo function Gizmo.Init(Ceive, Propertys, Request, Release, Retain)
        local self = setmetatable({
        }, Gizmo)
        self.Ceive = Ceive
        self.Propertys = Propertys
        self.Request = Request
        self.Release = Release
        self.Retain = Retain
        return self
     end function Gizmo:Draw(Transform:CFrame, Radius:number, Subdivisions:number, Angle:number, ConnectToStart:boolean?)
        local Ceive = self.Ceive
        if not Ceive.Enabled then
             return
         end
        local AnglePerChunk = math.floor(Angle / Subdivisions)
        local PreviousVertex = nil
        local FirstVertex = nil
        local FinishingAngle = 0
        for i = 0, Angle, AnglePerChunk do
             local XMagnitude = math.sin(math.rad(i)) * Radius
            local YMagnitude = math.cos(math.rad(i)) * Radius
            local VertexPosition = Transform.Position + ((Transform.UpVector * YMagnitude) + (Transform.RightVector * XMagnitude))
            if PreviousVertex == nil then
                 PreviousVertex = VertexPosition
                FirstVertex = VertexPosition
                FinishingAngle = i continue
             end Ceive.Ray:Draw(PreviousVertex, VertexPosition)
            PreviousVertex = VertexPosition
            FinishingAngle = i
         end
        if FinishingAngle ~= Angle then
             local XMagnitude = math.sin(math.rad(Angle)) * Radius
            local YMagnitude = math.cos(math.rad(Angle)) * Radius
            local VertexPosition = Transform.Position + ((Transform.UpVector * YMagnitude) + (Transform.RightVector * XMagnitude))
            Ceive.Ray:Draw(PreviousVertex, VertexPosition)
        end
        if ConnectToStart ~= false then
             Ceive.Ray:Draw(PreviousVertex, FirstVertex)
        end
        return PreviousVertex
     end function Gizmo:Create(Transform:CFrame, Radius:number, Subdivisions:number, Angle:number, ConnectToStart:boolean?)
        local PropertyTable = {
            Transform = Transform,
            Radius = Radius,
            Subdivisions = Subdivisions,
            Angle = Angle,
            ConnectToStart = ConnectToStart,
            AlwaysOnTop = self.Propertys.AlwaysOnTop,
            Transparency = self.Propertys.Transparency,
            Color3 = self.Propertys.Color3,
            Enabled = true,
            Destroy = false
        }
        self.Retain(self, PropertyTable)
        return PropertyTable
     end function Gizmo:Update(PropertyTable)
        local Ceive = self.Ceive
        Ceive.PushProperty('AlwaysOnTop', PropertyTable.AlwaysOnTop)
        Ceive.PushProperty('Transparency', PropertyTable.Transparency)
        Ceive.PushProperty('Color3', PropertyTable.Color3)
        self:Draw(PropertyTable.Transform, PropertyTable.Radius, PropertyTable.Subdivisions, PropertyTable.Angle, PropertyTable.ConnectToStart)
    end
    return Gizmo
 end function __DARKLUA_BUNDLE_MODULES.u()
    local Rad90D = math.rad(90)
    local Gizmo = {
    }
    Gizmo.__index = Gizmo function Gizmo.Init(Ceive, Propertys, Request, Release, Retain)
        local self = setmetatable({
        }, Gizmo)
        self.Ceive = Ceive
        self.Propertys = Propertys
        self.Request = Request
        self.Release = Release
        self.Retain = Retain
        return self
     end function Gizmo:Draw(Transform:CFrame, Radius:number, Length:number, Subdivisions:number)
        local Ceive = self.Ceive
        if not Ceive.Enabled then
             return
         end Transform*=CFrame.Angles( - Rad90D, 0, 0)
        local TopOfCone = Transform.Position + Transform.UpVector * (Length / 2)
        local BottomOfCone = Transform.Position + - Transform.UpVector * (Length / 2)
        TopOfCone = CFrame.lookAt(TopOfCone, TopOfCone + Transform.UpVector)
        BottomOfCone = CFrame.lookAt(BottomOfCone, BottomOfCone - Transform.UpVector)
        local AnglePerChunk = math.floor(360 / Subdivisions)
        local Last
        local First
        for i = 0, 360, AnglePerChunk do
             local XMagnitude = math.sin(math.rad(i)) * Radius
            local YMagnitude = math.cos(math.rad(i)) * Radius
            local VertexOffset = (Transform.LookVector * YMagnitude) + (Transform.RightVector * XMagnitude)
            local VertexPosition = BottomOfCone.Position + VertexOffset
            if not Last then
                 Last = VertexPosition
                First = VertexPosition
                Ceive.Ray:Draw(VertexPosition, TopOfCone.Position)continue
             end Ceive.Ray:Draw(VertexPosition, TopOfCone.Position)
            Ceive.Ray:Draw(Last, VertexPosition)
            Last = VertexPosition
         end Ceive.Ray:Draw(Last, First)
    end function Gizmo:Create(Transform:CFrame, Radius:number, Length:number, Subdivisions:number)
        local PropertyTable = {
            Transform = Transform,
            Radius = Radius,
            Length = Length,
            Subdivisions = Subdivisions,
            AlwaysOnTop = self.Propertys.AlwaysOnTop,
            Transparency = self.Propertys.Transparency,
            Color3 = self.Propertys.Color3,
            Enabled = true,
            Destroy = false
        }
        self.Retain(self, PropertyTable)
        return PropertyTable
     end function Gizmo:Update(PropertyTable)
        local Ceive = self.Ceive
        Ceive.PushProperty('AlwaysOnTop', PropertyTable.AlwaysOnTop)
        Ceive.PushProperty('Transparency', PropertyTable.Transparency)
        Ceive.PushProperty('Color3', PropertyTable.Color3)
        self:Draw(PropertyTable.Transform, PropertyTable.Radius, PropertyTable.Length, PropertyTable.Subdivisions)
    end
    return Gizmo
 end function __DARKLUA_BUNDLE_MODULES.v()
    local Gizmo = {
    }
    Gizmo.__index = Gizmo function Gizmo.Init(Ceive, Propertys, Request, Release, Retain)
        local self = setmetatable({
        }, Gizmo)
        self.Ceive = Ceive
        self.Propertys = Propertys
        self.Request = Request
        self.Release = Release
        self.Retain = Retain
        return self
     end function Gizmo:Draw(Transform:CFrame, Radius:number, Length:number, Subdivisions:number)
        local Ceive = self.Ceive
        if not Ceive.Enabled then
             return
         end
        local TopOfCylinder = Transform.Position + (Transform.UpVector * (Length / 2))
        local BottomOfCylinder = Transform.Position - (Transform.UpVector * (Length / 2))
        TopOfCylinder = CFrame.lookAt(TopOfCylinder, TopOfCylinder + Transform.UpVector)
        BottomOfCylinder = CFrame.lookAt(BottomOfCylinder, BottomOfCylinder - Transform.UpVector)
        local AnglePerChunk = math.floor(360 / Subdivisions)
        local LastTop
        local LastBottom
        local FirstTop
        local FirstBottom
        for i = 0, 360, AnglePerChunk do
             local XMagnitude = math.sin(math.rad(i)) * Radius
            local YMagnitude = math.cos(math.rad(i)) * Radius
            local VertexOffset = (Transform.LookVector * YMagnitude) + (Transform.RightVector * XMagnitude)
            local TopVertexPosition = TopOfCylinder.Position + VertexOffset
            local BottomVertexPosition = BottomOfCylinder.Position + VertexOffset
            Ceive.Ray:Draw(TopVertexPosition, BottomVertexPosition)
            if not LastTop then
                 LastTop = TopVertexPosition
                LastBottom = BottomVertexPosition
                FirstTop = TopVertexPosition
                FirstBottom = BottomVertexPosition continue
             end Ceive.Ray:Draw(LastTop, TopVertexPosition)
            Ceive.Ray:Draw(LastBottom, BottomVertexPosition)
            LastTop = TopVertexPosition
            LastBottom = BottomVertexPosition
         end Ceive.Ray:Draw(LastTop, FirstTop)
        Ceive.Ray:Draw(LastBottom, FirstBottom)
    end function Gizmo:Create(Transform:CFrame, Radius:number, Length:number, Subdivisions:number)
        local PropertyTable = {
            Transform = Transform,
            Radius = Radius,
            Length = Length,
            Subdivisions = Subdivisions,
            AlwaysOnTop = self.Propertys.AlwaysOnTop,
            Transparency = self.Propertys.Transparency,
            Color3 = self.Propertys.Color3,
            Enabled = true,
            Destroy = false
        }
        self.Retain(self, PropertyTable)
        return PropertyTable
     end function Gizmo:Update(PropertyTable)
        local Ceive = self.Ceive
        Ceive.PushProperty('AlwaysOnTop', PropertyTable.AlwaysOnTop)
        Ceive.PushProperty('Transparency', PropertyTable.Transparency)
        Ceive.PushProperty('Color3', PropertyTable.Color3)
        self:Draw(PropertyTable.Transform, PropertyTable.Radius, PropertyTable.Length, PropertyTable.Subdivisions)
    end
    return Gizmo
 end function __DARKLUA_BUNDLE_MODULES.w()
    local Gizmo = {
    }
    Gizmo.__index = Gizmo function Gizmo.Init(Ceive, Propertys, Request, Release, Retain)
        local self = setmetatable({
        }, Gizmo)
        self.Ceive = Ceive
        self.Propertys = Propertys
        self.Request = Request
        self.Release = Release
        self.Retain = Retain
        return self
     end function Gizmo:Draw(Transform:CFrame, Length:number)
        local Ceive = self.Ceive
        if not Ceive.Enabled then
             return
         end
        local Origin = Transform.Position + (Transform.LookVector * ( - Length / 2))
        local End = Transform.Position + (Transform.LookVector * (Length / 2))
        Ceive.Ray:Draw(Origin, End)
    end function Gizmo:Create(Transform:CFrame, Length:number)
        local PropertyTable = {
            Transform = Transform,
            Length = Length,
            AlwaysOnTop = self.Propertys.AlwaysOnTop,
            Transparency = self.Propertys.Transparency,
            Color3 = self.Propertys.Color3,
            Enabled = true,
            Destroy = false
        }
        self.Retain(self, PropertyTable)
        return PropertyTable
     end function Gizmo:Update(PropertyTable)
        local Ceive = self.Ceive
        Ceive.PushProperty('AlwaysOnTop', PropertyTable.AlwaysOnTop)
        Ceive.PushProperty('Transparency', PropertyTable.Transparency)
        Ceive.PushProperty('Color3', PropertyTable.Color3)
        self:Draw(PropertyTable.Transform, PropertyTable.Length)
    end
    return Gizmo
 end function __DARKLUA_BUNDLE_MODULES.x()
    local function Map(n, start, stop, newStart, newStop)
        return ((n - start) / (stop - start)) * (newStop - newStart) + newStart
     end
    local Gizmo = {
    }
    Gizmo.__index = Gizmo function Gizmo.Init(Ceive, Propertys, Request, Release, Retain)
        local self = setmetatable({
        }, Gizmo)
        self.Ceive = Ceive
        self.Propertys = Propertys
        self.Request = Request
        self.Release = Release
        self.Retain = Retain
        return self
     end function Gizmo:Draw(Transform:CFrame, Size:Vector3, Vertices, Faces)
        local Ceive = self.Ceive
        if not Ceive.Enabled then
             return
         end
        local maxX = - math.huge
        local maxY = - math.huge
        local maxZ = - math.huge
        local minX = math.huge
        local minY = math.huge
        local minZ = math.huge
        for _, vertex in Vertices do
             maxX = math.max(maxX, vertex.x)
            maxY = math.max(maxY, vertex.y)
            maxZ = math.max(maxZ, vertex.z)
            minX = math.min(minX, vertex.x)
            minY = math.min(minY, vertex.y)
            minZ = math.min(minZ, vertex.z)
        end
        for i, vertex in Vertices do
             local vX = Map(vertex.x, minX, maxX, - 0.5, 0.5)
            local vY = Map(vertex.y, minY, maxY, - 0.5, 0.5)
            local vZ = Map(vertex.z, minZ, maxZ, - 0.5, 0.5)
            local vertexCFrame = Transform * CFrame.new(Vector3.new(vX, vY, vZ) * Size)
            Vertices[i] = vertexCFrame
         end
        for _, face in Faces do
             if#face == 3 then
                 local vCF1 = Vertices[face[1].v]local vCF2 = Vertices[face[2].v]local vCF3 = Vertices[face[3].v]Ceive.Ray:Draw(vCF1.Position, vCF2.Position)
                Ceive.Ray:Draw(vCF2.Position, vCF3.Position)
                Ceive.Ray:Draw(vCF3.Position, vCF1.Position)
            else
                 local vCF1 = Vertices[face[1].v]local vCF2 = Vertices[face[2].v]local vCF3 = Vertices[face[3].v]local vCF4 = Vertices[face[4].v]Ceive.Ray:Draw(vCF1.Position, vCF2.Position)
                Ceive.Ray:Draw(vCF1.Position, vCF4.Position)
                Ceive.Ray:Draw(vCF4.Position, vCF2.Position)
                Ceive.Ray:Draw(vCF3.Position, vCF4.Position)
                Ceive.Ray:Draw(vCF2.Position, vCF3.Position)
            end
         end
     end function Gizmo:Create(Transform:CFrame, Size:Vector3, Vertices, Faces)
        local PropertyTable = {
            Transform = Transform,
            Size = Size,
            Vertices = Vertices,
            Faces = Faces,
            AlwaysOnTop = self.Propertys.AlwaysOnTop,
            Transparency = self.Propertys.Transparency,
            Color3 = self.Propertys.Color3,
            Enabled = true,
            Destroy = false
        }
        self.Retain(self, PropertyTable)
        return PropertyTable
     end function Gizmo:Update(PropertyTable)
        local Ceive = self.Ceive
        Ceive.PushProperty('AlwaysOnTop', PropertyTable.AlwaysOnTop)
        Ceive.PushProperty('Transparency', PropertyTable.Transparency)
        Ceive.PushProperty('Color3', PropertyTable.Color3)
        self:Draw(PropertyTable.Transform, PropertyTable.Size, PropertyTable.Vertices, PropertyTable.Faces)
    end
    return Gizmo
 end function __DARKLUA_BUNDLE_MODULES.y()
    local Gizmo = {
    }
    Gizmo.__index = Gizmo function Gizmo.Init(Ceive, Propertys, Request, Release, Retain)
        local self = setmetatable({
        }, Gizmo)
        self.Ceive = Ceive
        self.Propertys = Propertys
        self.Request = Request
        self.Release = Release
        self.Retain = Retain
        return self
     end function Gizmo:Draw(Position:Vector3, Normal:Vector3, Size:Vector3)
        local Ceive = self.Ceive
        if not Ceive.Enabled then
             return
         end Size*=Vector3.new(1, 1, 0)
        local Transform = CFrame.lookAt(Position, Position + Normal)
        local Uv = Transform.UpVector
        local Rv = Transform.RightVector
        local Lv = Transform.LookVector
        local sO2 = Size / 2
        local sUv = Uv * sO2.Y
        local sRv = Rv * sO2.X
        local sLv = Lv * sO2.Z
        local function CalculateZFace(lUv, lRv, lLv)
            local TopLeft = Position + (lUv - lRv + lLv)
            local TopRight = Position + (lUv + lRv + lLv)
            local BottomLeft = Position + ( - lUv - lRv + lLv)
            local BottomRight = Position + ( - lUv + lRv + lLv)
            Ceive.Ray:Draw(TopLeft, TopRight)
            Ceive.Ray:Draw(TopLeft, BottomLeft)
            Ceive.Ray:Draw(TopRight, BottomRight)
            Ceive.Ray:Draw(TopRight, BottomLeft)
            Ceive.Ray:Draw(BottomLeft, BottomRight)
        end CalculateZFace(sUv, sRv, sLv)
    end function Gizmo:Create(Position:Vector3, Normal:Vector3, Size:Vector3)
        local PropertyTable = {
            Position = Position,
            Normal = Normal,
            Size = Size,
            AlwaysOnTop = self.Propertys.AlwaysOnTop,
            Transparency = self.Propertys.Transparency,
            Color3 = self.Propertys.Color3,
            Enabled = true,
            Destroy = false
        }
        self.Retain(self, PropertyTable)
        return PropertyTable
     end function Gizmo:Update(PropertyTable)
        local Ceive = self.Ceive
        Ceive.PushProperty('AlwaysOnTop', PropertyTable.AlwaysOnTop)
        Ceive.PushProperty('Transparency', PropertyTable.Transparency)
        Ceive.PushProperty('Color3', PropertyTable.Color3)
        self:Draw(PropertyTable.Position, PropertyTable.Normal, PropertyTable.Size)
    end
    return Gizmo
 end function __DARKLUA_BUNDLE_MODULES.z()
    local Gizmo = {
    }
    Gizmo.__index = Gizmo function Gizmo.Init(Ceive, Propertys, Request, Release, Retain)
        local self = setmetatable({
        }, Gizmo)
        self.Ceive = Ceive
        self.Propertys = Propertys
        self.Request = Request
        self.Release = Release
        self.Retain = Retain
        return self
     end function Gizmo:Draw(Origin:Vector3, End:Vector3)
        local Ceive = self.Ceive
        if not Ceive.Enabled then
             return
         end
        if self.Propertys.AlwaysOnTop then
             Ceive.AOTWireframeHandle:AddLine(Origin, End)
        else
             Ceive.WireframeHandle:AddLine(Origin, End)
        end self.Ceive.ActiveRays+=1
        self.Ceive.ScheduleCleaning()
    end function Gizmo:Create(Origin:Vector3, End:Vector3)
        local PropertyTable = {
            Origin = Origin,
            End = End,
            AlwaysOnTop = self.Propertys.AlwaysOnTop,
            Transparency = self.Propertys.Transparency,
            Color3 = self.Propertys.Color3,
            Enabled = true,
            Destroy = false
        }
        self.Retain(self, PropertyTable)
        return PropertyTable
     end function Gizmo:Update(PropertyTable)
        local Ceive = self.Ceive
        Ceive.PushProperty('AlwaysOnTop', PropertyTable.AlwaysOnTop)
        Ceive.PushProperty('Transparency', PropertyTable.Transparency)
        Ceive.PushProperty('Color3', PropertyTable.Color3)
        self:Draw(PropertyTable.Origin, PropertyTable.End)
    end
    return Gizmo
 end function __DARKLUA_BUNDLE_MODULES.A()
    local Rad180D = math.rad(180)
    local Gizmo = {
    }
    Gizmo.__index = Gizmo function Gizmo.Init(Ceive, Propertys, Request, Release, Retain)
        local self = setmetatable({
        }, Gizmo)
        self.Ceive = Ceive
        self.Propertys = Propertys
        self.Request = Request
        self.Release = Release
        self.Retain = Retain
        return self
     end function Gizmo:Draw(Transform:CFrame, Radius0:number, Radius1:number, Length:number, Subdivisions:number)
        local Ceive = self.Ceive
        if not Ceive.Enabled then
             return
         end
        local TopOfCylinder = Transform.Position + (Transform.UpVector * (Length / 2))
        local BottomOfCylinder = Transform.Position - (Transform.UpVector * (Length / 2))
        TopOfCylinder = CFrame.lookAt(TopOfCylinder, TopOfCylinder + Transform.UpVector)
        BottomOfCylinder = CFrame.lookAt(BottomOfCylinder, BottomOfCylinder - Transform.UpVector)
        local AnglePerChunk = math.floor(360 / Subdivisions)
        local LastTop
        local LastBottom
        local FirstTop
        local FirstBottom
        for i = 0, 360, AnglePerChunk do
             local XMagnitude0 = math.sin(math.rad(i)) * Radius0
            local YMagnitude0 = math.cos(math.rad(i)) * Radius0
            local XMagnitude1 = math.sin(math.rad(i)) * Radius1
            local YMagnitude1 = math.cos(math.rad(i)) * Radius1
            local TopVertexOffset = (Transform.LookVector * YMagnitude1) + (Transform.RightVector * XMagnitude1)
            local BottomVertexOffset = (Transform.LookVector * YMagnitude0) + (Transform.RightVector * XMagnitude0)
            local TopVertexPosition = TopOfCylinder.Position + TopVertexOffset
            local BottomVertexPosition = BottomOfCylinder.Position + BottomVertexOffset
            Ceive.Ray:Draw(TopVertexPosition, BottomVertexPosition)
            Ceive.Circle:Draw(CFrame.new(TopOfCylinder.Position) * Transform.Rotation * CFrame.Angles(0, math.rad(i), 0), Radius1, Subdivisions / 2, 90, false)
            Ceive.Circle:Draw(CFrame.new(BottomOfCylinder.Position) * Transform.Rotation * CFrame.Angles(Rad180D, math.rad(i), 0), Radius0, Subdivisions / 2, 90, false)
            if not LastTop then
                 LastTop = TopVertexPosition
                LastBottom = BottomVertexPosition
                FirstTop = TopVertexPosition
                FirstBottom = BottomVertexPosition continue
             end Ceive.Ray:Draw(LastTop, TopVertexPosition)
            Ceive.Ray:Draw(LastBottom, BottomVertexPosition)
            LastTop = TopVertexPosition
            LastBottom = BottomVertexPosition
         end Ceive.Ray:Draw(LastTop, FirstTop)
        Ceive.Ray:Draw(LastBottom, FirstBottom)
    end function Gizmo:Create(Transform:CFrame, Radius0:number, Radius1:number, Length:number, Subdivisions:number)
        local PropertyTable = {
            Transform = Transform,
            Radius0 = Radius0,
            Radius1 = Radius1,
            Length = Length,
            Subdivisions = Subdivisions,
            AlwaysOnTop = self.Propertys.AlwaysOnTop,
            Transparency = self.Propertys.Transparency,
            Color3 = self.Propertys.Color3,
            Enabled = true,
            Destroy = false
        }
        self.Retain(self, PropertyTable)
        return PropertyTable
     end function Gizmo:Update(PropertyTable)
        local Ceive = self.Ceive
        Ceive.PushProperty('AlwaysOnTop', PropertyTable.AlwaysOnTop)
        Ceive.PushProperty('Transparency', PropertyTable.Transparency)
        Ceive.PushProperty('Color3', PropertyTable.Color3)
        self:Draw(PropertyTable.Transform, PropertyTable.Radius, PropertyTable.Length, PropertyTable.Subdivisions)
    end
    return Gizmo
 end function __DARKLUA_BUNDLE_MODULES.B()
    local Rad90D = math.rad(90)
    local Gizmo = {
    }
    Gizmo.__index = Gizmo function Gizmo.Init(Ceive, Propertys, Request, Release, Retain)
        local self = setmetatable({
        }, Gizmo)
        self.Ceive = Ceive
        self.Propertys = Propertys
        self.Request = Request
        self.Release = Release
        self.Retain = Retain
        return self
     end function Gizmo:Draw(Transform:CFrame, Radius:number, Subdivisions:number, Angle:number)
        local Ceive = self.Ceive
        if not Ceive.Enabled then
             return
         end Ceive.Circle:Draw(Transform, Radius, Subdivisions, Angle)
        Ceive.Circle:Draw(Transform * CFrame.Angles(0, Rad90D, 0), Radius, Subdivisions, Angle)
        Ceive.Circle:Draw(Transform * CFrame.Angles(Rad90D, 0, 0), Radius, Subdivisions, Angle)
    end function Gizmo:Create(Transform:CFrame, Radius:number, Subdivisions:number, Angle:number)
        local PropertyTable = {
            Transform = Transform,
            Radius = Radius,
            Subdivisions = Subdivisions,
            Angle = Angle,
            AlwaysOnTop = self.Propertys.AlwaysOnTop,
            Transparency = self.Propertys.Transparency,
            Color3 = self.Propertys.Color3,
            Enabled = true,
            Destroy = false
        }
        self.Retain(self, PropertyTable)
        return PropertyTable
     end function Gizmo:Update(PropertyTable)
        local Ceive = self.Ceive
        Ceive.PushProperty('AlwaysOnTop', PropertyTable.AlwaysOnTop)
        Ceive.PushProperty('Transparency', PropertyTable.Transparency)
        Ceive.PushProperty('Color3', PropertyTable.Color3)
        self:Draw(PropertyTable.Transform, PropertyTable.Radius, PropertyTable.Subdivisions, PropertyTable.Angle)
    end
    return Gizmo
 end function __DARKLUA_BUNDLE_MODULES.C()
    local DROP_SHADOW = true
    local OFFSET_PERCENTAGE = 0.00175
    local Camera = workspace.CurrentCamera
    local Gizmo = {
    }
    Gizmo.__index = Gizmo function Gizmo.Init(Ceive, Propertys, Request, Release, Retain)
        local self = setmetatable({
        }, Gizmo)
        self.Ceive = Ceive
        self.Propertys = Propertys
        self.Request = Request
        self.Release = Release
        self.Retain = Retain
        return self
     end function Gizmo:Draw(Origin:Vector3, Text:string, Size:number?)
        local Ceive = self.Ceive
        if not Ceive.Enabled then
             return
         end
        if self.Propertys.AlwaysOnTop then
             if DROP_SHADOW then
                 local DistanceToCamera = (Origin - Camera.CFrame.Position).Magnitude
                local PrevColor = Ceive.PopProperty('Color3')
                Ceive.PushProperty('Color3', Color3.new())
                local Offset = - (Vector3.xAxis + Vector3.yAxis).Unit
                Ceive.AOTWireframeHandle:AddText(Origin + Offset * (DistanceToCamera * OFFSET_PERCENTAGE), Text, Size)
                Ceive.PushProperty('Color3', PrevColor)
            end Ceive.AOTWireframeHandle:AddText(Origin, Text, Size)
        else
             if DROP_SHADOW then
                 local DistanceToCamera = (Origin - Camera.CFrame.Position).Magnitude
                local PrevColor = Ceive.PopProperty('Color3')
                Ceive.PushProperty('Color3', Color3.new())
                local Offset = - (Vector3.xAxis + Vector3.yAxis).Unit
                Ceive.WireframeHandle:AddText(Origin + Offset * (DistanceToCamera * OFFSET_PERCENTAGE), Text, Size)
                Ceive.PushProperty('Color3', PrevColor)
            end Ceive.WireframeHandle:AddText(Origin, Text, Size)
        end self.Ceive.ScheduleCleaning()
    end function Gizmo:Create(Origin:Vector3, Text:string, Size:number?)
        local PropertyTable = {
            Origin = Origin,
            Text = Text,
            Size = Size,
            AlwaysOnTop = self.Propertys.AlwaysOnTop,
            Transparency = self.Propertys.Transparency,
            Color3 = self.Propertys.Color3,
            Enabled = true,
            Destroy = false
        }
        self.Retain(self, PropertyTable)
        return PropertyTable
     end function Gizmo:Update(PropertyTable)
        local Ceive = self.Ceive
        Ceive.PushProperty('AlwaysOnTop', PropertyTable.AlwaysOnTop)
        Ceive.PushProperty('Transparency', PropertyTable.Transparency)
        Ceive.PushProperty('Color3', PropertyTable.Color3)
        self:Draw(PropertyTable.Origin, PropertyTable.Text, PropertyTable.Size)
    end
    return Gizmo
 end function __DARKLUA_BUNDLE_MODULES.D()
    local Gizmo = {
    }
    Gizmo.__index = Gizmo function Gizmo.Init(Ceive, Propertys, Request, Release, Retain, Register)
        local self = setmetatable({
        }, Gizmo)
        self.Ceive = Ceive
        self.Propertys = Propertys
        self.Request = Request
        self.Release = Release
        self.Retain = Retain
        self.Register = Register
        return self
     end function Gizmo:Draw(Origin:Vector3, End:Vector3, CylinderRadius:number, ConeRadius:number, Length:number, UseCylinder:boolean?)
        local Ceive = self.Ceive
        if not Ceive.Enabled then
             return
         end
        local ArrowCFrame = CFrame.lookAt(End - (End - Origin).Unit * (Length / 2), End)
        if UseCylinder == true then
             local BottomCone = ArrowCFrame.Position
            local CylinderLength = (BottomCone - Origin).Magnitude
            local CylinderCFrame = CFrame.lookAt((Origin + BottomCone) / 2, End)
            Ceive.VolumeCylinder:Draw(CylinderCFrame, CylinderRadius, CylinderLength)
        else
             Ceive.Ray:Draw(Origin, End)
        end Ceive.VolumeCone:Draw(ArrowCFrame, ConeRadius, Length)
        self.Ceive.ScheduleCleaning()
    end function Gizmo:Create(Origin:Vector3, End:Vector3, CylinderRadius:number, ConeRadius:number, Length:number, UseCylinder:boolean?)
        local PropertyTable = {
            Origin = Origin,
            End = End,
            CylinderRadius = CylinderRadius,
            ConeRadius = ConeRadius,
            Length = Length,
            UseCylinder = UseCylinder,
            AlwaysOnTop = self.Propertys.AlwaysOnTop,
            Transparency = self.Propertys.Transparency,
            Color3 = self.Propertys.Color3,
            Enabled = true,
            Destroy = false
        }
        self.Retain(self, PropertyTable)
        return PropertyTable
     end function Gizmo:Update(PropertyTable)
        local Ceive = self.Ceive
        Ceive.PushProperty('AlwaysOnTop', PropertyTable.AlwaysOnTop)
        Ceive.PushProperty('Transparency', PropertyTable.Transparency)
        Ceive.PushProperty('Color3', PropertyTable.Color3)
        self:Draw(PropertyTable.Origin, PropertyTable.End, PropertyTable.Radius, PropertyTable.Length, PropertyTable.UseCylinder)
    end
    return Gizmo
 end function __DARKLUA_BUNDLE_MODULES.E()
    local Terrain = workspace.Terrain
    local Gizmo = {
    }
    Gizmo.__index = Gizmo function Gizmo.Init(Ceive, Propertys, Request, Release, Retain, Register)
        local self = setmetatable({
        }, Gizmo)
        self.Ceive = Ceive
        self.Propertys = Propertys
        self.Request = Request
        self.Release = Release
        self.Retain = Retain
        self.Register = Register
        return self
     end function Gizmo:Draw(Transform:CFrame, Size:Vector3)
        local Ceive = self.Ceive
        if not Ceive.Enabled then
             return
         end
        local Box = self.Request('BoxHandleAdornment')
        Box.Color3 = self.Propertys.Color3
        Box.Transparency = self.Propertys.Transparency
        Box.CFrame = Transform
        Box.Size = Size
        Box.AlwaysOnTop = self.Propertys.AlwaysOnTop
        Box.ZIndex = 1
        Box.Adornee = Terrain
        Box.Parent = Terrain
        Ceive.ActiveInstances+=1
        self.Register(Box)
        self.Ceive.ScheduleCleaning()
    end function Gizmo:Create(Transform:CFrame, Size:Vector3)
        local PropertyTable = {
            Transform = Transform,
            Size = Size,
            AlwaysOnTop = self.Propertys.AlwaysOnTop,
            Transparency = self.Propertys.Transparency,
            Color3 = self.Propertys.Color3,
            Enabled = true,
            Destroy = false
        }
        self.Retain(self, PropertyTable)
        return PropertyTable
     end function Gizmo:Update(PropertyTable)
        local Ceive = self.Ceive
        Ceive.PushProperty('AlwaysOnTop', PropertyTable.AlwaysOnTop)
        Ceive.PushProperty('Transparency', PropertyTable.Transparency)
        Ceive.PushProperty('Color3', PropertyTable.Color3)
        self:Draw(PropertyTable.Transform, PropertyTable.Size)
    end
    return Gizmo
 end function __DARKLUA_BUNDLE_MODULES.F()
    local Terrain = workspace.Terrain
    local Gizmo = {
    }
    Gizmo.__index = Gizmo function Gizmo.Init(Ceive, Propertys, Request, Release, Retain, Register)
        local self = setmetatable({
        }, Gizmo)
        self.Ceive = Ceive
        self.Propertys = Propertys
        self.Request = Request
        self.Release = Release
        self.Retain = Retain
        self.Register = Register
        return self
     end function Gizmo:Draw(Transform:CFrame, Radius:number, Length:number)
        local Ceive = self.Ceive
        if not Ceive.Enabled then
             return
         end
        local Cone = self.Request('ConeHandleAdornment')
        Cone.Color3 = self.Propertys.Color3
        Cone.Transparency = self.Propertys.Transparency
        Cone.CFrame = Transform
        Cone.AlwaysOnTop = self.Propertys.AlwaysOnTop
        Cone.ZIndex = 1
        Cone.Height = Length
        Cone.Radius = Radius
        Cone.Adornee = Terrain
        Cone.Parent = Terrain
        Ceive.ActiveInstances+=1
        self.Register(Cone)
        self.Ceive.ScheduleCleaning()
    end function Gizmo:Create(Transform:CFrame, Radius:number, Length:number)
        local PropertyTable = {
            Transform = Transform,
            Radius = Radius,
            Length = Length,
            AlwaysOnTop = self.Propertys.AlwaysOnTop,
            Transparency = self.Propertys.Transparency,
            Color3 = self.Propertys.Color3,
            Enabled = true,
            Destroy = false
        }
        self.Retain(self, PropertyTable)
        return PropertyTable
     end function Gizmo:Update(PropertyTable)
        local Ceive = self.Ceive
        Ceive.PushProperty('AlwaysOnTop', PropertyTable.AlwaysOnTop)
        Ceive.PushProperty('Transparency', PropertyTable.Transparency)
        Ceive.PushProperty('Color3', PropertyTable.Color3)
        self:Draw(PropertyTable.Transform, PropertyTable.Radius, PropertyTable.Length)
    end
    return Gizmo
 end function __DARKLUA_BUNDLE_MODULES.G()
    local Terrain = workspace.Terrain
    local Gizmo = {
    }
    Gizmo.__index = Gizmo function Gizmo.Init(Ceive, Propertys, Request, Release, Retain, Register)
        local self = setmetatable({
        }, Gizmo)
        self.Ceive = Ceive
        self.Propertys = Propertys
        self.Request = Request
        self.Release = Release
        self.Retain = Retain
        self.Register = Register
        return self
     end function Gizmo:Draw(Transform:CFrame, Radius:number, Length:number, InnerRadius:number?, Angle:number?)
        local Ceive = self.Ceive
        if not Ceive.Enabled then
             return
         end
        local Cylinder = self.Request('CylinderHandleAdornment')
        Cylinder.Color3 = self.Propertys.Color3
        Cylinder.Transparency = self.Propertys.Transparency
        Cylinder.CFrame = Transform
        Cylinder.Height = Length
        Cylinder.Radius = Radius
        Cylinder.InnerRadius = InnerRadius or 0
        Cylinder.Angle = Angle or 360
        Cylinder.AlwaysOnTop = self.Propertys.AlwaysOnTop
        Cylinder.ZIndex = 1
        Cylinder.Adornee = Terrain
        Cylinder.Parent = Terrain
        Ceive.ActiveInstances+=1
        self.Register(Cylinder)
        self.Ceive.ScheduleCleaning()
    end function Gizmo:Create(Transform:CFrame, Radius:number, Length:number, InnerRadius:number?, Angle:number?)
        local PropertyTable = {
            Transform = Transform,
            Radius = Radius,
            Length = Length,
            InnerRadius = InnerRadius or 0,
            Angle = Angle or 360,
            AlwaysOnTop = self.Propertys.AlwaysOnTop,
            Transparency = self.Propertys.Transparency,
            Color3 = self.Propertys.Color3,
            Enabled = true,
            Destroy = false
        }
        self.Retain(self, PropertyTable)
        return PropertyTable
     end function Gizmo:Update(PropertyTable)
        local Ceive = self.Ceive
        Ceive.PushProperty('AlwaysOnTop', PropertyTable.AlwaysOnTop)
        Ceive.PushProperty('Transparency', PropertyTable.Transparency)
        Ceive.PushProperty('Color3', PropertyTable.Color3)
        self:Draw(PropertyTable.Transform, PropertyTable.Radius, PropertyTable.Length, PropertyTable.InnerRadius, PropertyTable.Angle)
    end
    return Gizmo
 end function __DARKLUA_BUNDLE_MODULES.H()
    local Terrain = workspace.Terrain
    local Gizmo = {
    }
    Gizmo.__index = Gizmo function Gizmo.Init(Ceive, Propertys, Request, Release, Retain, Register)
        local self = setmetatable({
        }, Gizmo)
        self.Ceive = Ceive
        self.Propertys = Propertys
        self.Request = Request
        self.Release = Release
        self.Retain = Retain
        self.Register = Register
        return self
     end function Gizmo:Draw(Transform:CFrame, Radius:number)
        local Ceive = self.Ceive
        if not Ceive.Enabled then
             return
         end
        local Sphere = self.Request('SphereHandleAdornment')
        Sphere.Color3 = self.Propertys.Color3
        Sphere.Transparency = self.Propertys.Transparency
        Sphere.CFrame = Transform
        Sphere.Radius = Radius
        Sphere.AlwaysOnTop = self.Propertys.AlwaysOnTop
        Sphere.ZIndex = 1
        Sphere.Adornee = Terrain
        Sphere.Parent = Terrain
        Ceive.ActiveInstances+=1
        self.Register(Sphere)
        self.Ceive.ScheduleCleaning()
    end function Gizmo:Create(Transform:CFrame, Radius:number)
        local PropertyTable = {
            Transform = Transform,
            Radius = Radius,
            AlwaysOnTop = self.Propertys.AlwaysOnTop,
            Transparency = self.Propertys.Transparency,
            Color3 = self.Propertys.Color3,
            Enabled = true,
            Destroy = false
        }
        self.Retain(self, PropertyTable)
        return PropertyTable
     end function Gizmo:Update(PropertyTable)
        local Ceive = self.Ceive
        Ceive.PushProperty('AlwaysOnTop', PropertyTable.AlwaysOnTop)
        Ceive.PushProperty('Transparency', PropertyTable.Transparency)
        Ceive.PushProperty('Color3', PropertyTable.Color3)
        self:Draw(PropertyTable.Transform, PropertyTable.Radius)
    end
    return Gizmo
 end function __DARKLUA_BUNDLE_MODULES.I()
    local Gizmo = {
    }
    Gizmo.__index = Gizmo function Gizmo.Init(Ceive, Propertys, Request, Release, Retain)
        local self = setmetatable({
        }, Gizmo)
        self.Ceive = Ceive
        self.Propertys = Propertys
        self.Request = Request
        self.Release = Release
        self.Retain = Retain
        return self
     end function Gizmo:Draw(Transform:CFrame, Size:Vector3, DrawTriangles:boolean)
        local Ceive = self.Ceive
        if not Ceive.Enabled then
             return
         end
        local Position = Transform.Position
        local Uv = Transform.UpVector
        local Rv = Transform.RightVector
        local Lv = Transform.LookVector
        local sO2 = Size / 2
        local sUv = Uv * sO2.Y
        local sRv = Rv * sO2.X
        local sLv = Lv * sO2.Z
        local YTopLeft
        local YTopRight
        local ZBottomLeft
        local ZBottomRight
        local function CalculateYFace(lUv, lRv, lLv)
            local TopLeft = Position + (lUv - lRv + lLv)
            local TopRight = Position + (lUv + lRv + lLv)
            local BottomLeft = Position + (lUv - lRv - lLv)
            local BottomRight = Position + (lUv + lRv - lLv)
            YTopLeft = TopLeft
            YTopRight = TopRight
            Ceive.Ray:Draw(TopLeft, TopRight)
            Ceive.Ray:Draw(TopLeft, BottomLeft)
            Ceive.Ray:Draw(TopRight, BottomRight)
            if DrawTriangles ~= false then
                 Ceive.Ray:Draw(TopRight, BottomLeft)
            end Ceive.Ray:Draw(BottomLeft, BottomRight)
        end
        local function CalculateZFace(lUv, lRv, lLv)
            local TopLeft = Position + (lUv - lRv + lLv)
            local TopRight = Position + (lUv + lRv + lLv)
            local BottomLeft = Position + ( - lUv - lRv + lLv)
            local BottomRight = Position + ( - lUv + lRv + lLv)
            ZBottomLeft = TopLeft
            ZBottomRight = TopRight
            Ceive.Ray:Draw(TopLeft, TopRight)
            Ceive.Ray:Draw(TopLeft, BottomLeft)
            Ceive.Ray:Draw(TopRight, BottomRight)
            if DrawTriangles ~= false then
                 Ceive.Ray:Draw(TopRight, BottomLeft)
            end Ceive.Ray:Draw(BottomLeft, BottomRight)
        end CalculateYFace( - sUv, sRv, sLv)
        CalculateZFace(sUv, sRv, - sLv)
        Ceive.Ray:Draw(YTopLeft, ZBottomLeft)
        Ceive.Ray:Draw(YTopRight, ZBottomRight)
        if DrawTriangles ~= false then
             Ceive.Ray:Draw(YTopRight, ZBottomLeft)
        end
     end function Gizmo:Create(Transform:CFrame, Size:Vector3, DrawTriangles:boolean)
        local PropertyTable = {
            Transform = Transform,
            Size = Size,
            DrawTriangles = DrawTriangles,
            AlwaysOnTop = self.Propertys.AlwaysOnTop,
            Transparency = self.Propertys.Transparency,
            Color3 = self.Propertys.Color3,
            Enabled = true,
            Destroy = false
        }
        self.Retain(self, PropertyTable)
        return PropertyTable
     end function Gizmo:Update(PropertyTable)
        local Ceive = self.Ceive
        Ceive.PushProperty('AlwaysOnTop', PropertyTable.AlwaysOnTop)
        Ceive.PushProperty('Transparency', PropertyTable.Transparency)
        Ceive.PushProperty('Color3', PropertyTable.Color3)
        self:Draw(PropertyTable.Transform, PropertyTable.Size, PropertyTable.DrawTriangles)
    end
    return Gizmo
 end function __DARKLUA_BUNDLE_MODULES.J()
    if not LPH_OBFUSCATED then
         LPH_ENCNUM = function(toEncrypt, ...)
            assert(type(toEncrypt) == 'number' and #{
                ...
            } == 0, [[LPH_ENCNUM only accepts a single constant double or integer as an argument.]])
            return toEncrypt
         end LPH_NUMENC = LPH_ENCNUM
        LPH_ENCSTR = function(toEncrypt, ...)
            assert(type(toEncrypt) == 'string' and #{
                ...
            } == 0, [[LPH_ENCSTR only accepts a single constant string as an argument.]])
            return toEncrypt
         end LPH_STRENC = LPH_ENCSTR
        LPH_ENCFUNC = function(toEncrypt, encKey, decKey, ...)
            assert(type(toEncrypt) == 'function' and type(encKey) == 'string' and #{
                ...
            } == 0, [[LPH_ENCFUNC accepts a constant function, constant string, and string variable as arguments.]])
            return toEncrypt
         end LPH_FUNCENC = LPH_ENCFUNC
        LPH_JIT = function(f, ...)
            assert(type(f) == 'function' and #{
                ...
            } == 0, [[LPH_JIT only accepts a single constant function as an argument.]])
            return f
         end LPH_JIT_MAX = LPH_JIT
        LPH_NO_VIRTUALIZE = function(f, ...)
            assert(type(f) == 'function' and #{
                ...
            } == 0, [[LPH_NO_VIRTUALIZE only accepts a single constant function as an argument.]])
            return f
         end LPH_NO_UPVALUES = function(f, ...)
            assert(type(setfenv) == 'function', [[LPH_NO_UPVALUES can only be used on Lua versions with getfenv & setfenv]])
            assert(type(f) == 'function' and #{
                ...
            } == 0, [[LPH_NO_UPVALUES only accepts a single constant function as an argument.]])
            return f
         end LPH_CRASH = function(...)
            warn('LPH_CRASH INVOKED')
            assert(#{
                ...
            } == 0, 'LPH_CRASH does not accept any arguments.')
        end
     end
    return LPH_NO_VIRTUALIZE(function()
        local RunService = game:GetService('RunService')local TweenService = game:GetService('TweenService')local Terrain = workspace:WaitForChild('Terrain')local TargetParent = Terrain
        assert(Terrain, 'No terrain object found under workspace')assert(TargetParent, 'No target parent found.')local AOTWireframeHandle:WireframeHandleAdornment = TargetParent:FindFirstChild('AOTGizmoAdornment')local WireframeHandle:WireframeHandleAdornment = TargetParent:FindFirstChild('GizmoAdornment')if not AOTWireframeHandle then
             AOTWireframeHandle = Instance.new('WireframeHandleAdornment')AOTWireframeHandle.Adornee = Terrain
            AOTWireframeHandle.ZIndex = 1
            AOTWireframeHandle.AlwaysOnTop = true AOTWireframeHandle.Name = 'AOTGizmoAdornment'
            AOTWireframeHandle.Parent = TargetParent
         end
        if not WireframeHandle then
             WireframeHandle = Instance.new('WireframeHandleAdornment')WireframeHandle.Adornee = Terrain
            WireframeHandle.ZIndex = 1
            WireframeHandle.AlwaysOnTop = false WireframeHandle.Name = 'GizmoAdornment'
            WireframeHandle.Parent = TargetParent
         end
        local ActiveObjects = {
        }
        local RetainObjects = {
        }
        local Debris = {
        }
        local Tweens = {
        }
        local PropertyTable = {
            AlwaysOnTop = true,
            Color3 = Color3.fromRGB(13,
            105,
            172),
            Transparency = 0
        }
        local Pool = {
        }
        local CleanerScheduled = false
        local function Retain(Gizmo, GizmoProperties)
            table.insert(RetainObjects, {
                Gizmo,
                GizmoProperties
            })
        end
        local function Register(object)
            object.Parent = TargetParent
            table.insert(ActiveObjects, object)
        end
        local function Release(object)
            local ClassName = object.ClassName
            if not Pool[ClassName]then
                 Pool[ClassName] = {
                }
            end object:Remove()table.insert(Pool[ClassName], object)
        end
        local function Request(ClassName)
            if not Pool[ClassName]then
                 return Instance.new(ClassName)
            end
            local Object = table.remove(Pool[ClassName])if not Object then
                 return Instance.new(ClassName)
            end
            return Object
         end
        local function Lerp(a, b, t)
            return a + (b - a) * t
         end
        local function deepCopy(original)
            local copy = {
            }
            for k, v in pairs(original)do
                 if type(v) == 'table' then
                     v = deepCopy(v)
                end copy[k] = v
             end
            return copy
         end
        local Styles = {
            Color = 'Color3',
            Transparency = 'Transparency',
            AlwaysOnTop = 'AlwaysOnTop'
        }
        local Ceive:ICeive__DARKLUA_TYPE_R = {
            Enabled = true,
            ActiveRays = 0,
            ActiveInstances = 0,
            Styles = Styles,
            AOTWireframeHandle = AOTWireframeHandle,
            WireframeHandle = WireframeHandle
        }
        function Ceive.GetPoolSize()
            :number
            local n = 0
            for _, t in Pool do
                 n+=#t
             end
            return n
         end function Ceive.PushProperty(Property, Value)
            PropertyTable[Property] = Value
            if Property == 'AlwaysOnTop' then
                 return
             end pcall(function()
                AOTWireframeHandle[Property] = Value
                WireframeHandle[Property] = Value
             end)
        end function Ceive.PopProperty(Property)
            if PropertyTable[Property]then
                 return PropertyTable[Property]
            end
            return AOTWireframeHandle[Property]
        end function Ceive.SetStyle(Color, Transparency, AlwaysOnTop)
            if Color ~= nil and typeof(Color) == 'Color3' then
                 Ceive.PushProperty('Color3', Color)
            end
            if Transparency ~= nil and typeof(Transparency) == 'number' then
                 Ceive.PushProperty('Transparency', Transparency)
            end
            if AlwaysOnTop ~= nil and typeof(AlwaysOnTop) == 'boolean' then
                 Ceive.PushProperty('AlwaysOnTop', AlwaysOnTop)
            end
         end function Ceive.DoCleaning()
            AOTWireframeHandle:Clear()WireframeHandle:Clear()for _, Object in ActiveObjects do
                 Release(Object)
            end ActiveObjects = {
            }
            Ceive.ActiveRays = 0
            Ceive.ActiveInstances = 0
         end function Ceive.ScheduleCleaning()
            if CleanerScheduled then
                 return
             end CleanerScheduled = true task.delay(0, function()
                Ceive.DoCleaning()CleanerScheduled = false
             end)
        end function Ceive.AddDebrisInSeconds(Seconds:number, Callback)
            table.insert(Debris, {
                'Seconds',
                Seconds,
                os.clock(),
                Callback
            })
        end function Ceive.AddDebrisInFrames(Frames:number, Callback)
            table.insert(Debris, {
                'Frames',
                Frames,
                0,
                Callback
            })
        end function Ceive.TweenProperties(Properties:{
            }, Goal:{
            }, TweenInfo:TweenInfo)
            :()->()local p_Properties = Properties
            local c_Properties = deepCopy(Properties)local Tween = {
                p_Properties = p_Properties,
                Properties = c_Properties,
                Goal = Goal,
                TweenInfo = TweenInfo,
                Time = 0
            }
            Tweens[Tween] = true
            return function()
                Tweens[Tween] = nil
             end
         end function Ceive.Init()
            RunService.RenderStepped:Connect(function(dt)
                setthreadcontext(8)if Ceive.Enabled then
                     if not TargetParent:FindFirstChild('AOTGizmoAdornment')then
                         AOTWireframeHandle = Instance.new('WireframeHandleAdornment')AOTWireframeHandle.Adornee = Terrain
                        AOTWireframeHandle.ZIndex = 1
                        AOTWireframeHandle.AlwaysOnTop = true AOTWireframeHandle.Name = 'AOTGizmoAdornment'
                        AOTWireframeHandle.Parent = TargetParent
                        Ceive.AOTWireframeHandle = AOTWireframeHandle
                     end
                    if not TargetParent:FindFirstChild('GizmoAdornment')then
                         WireframeHandle = Instance.new('WireframeHandleAdornment')WireframeHandle.Adornee = Terrain
                        WireframeHandle.ZIndex = 1
                        WireframeHandle.AlwaysOnTop = false WireframeHandle.Name = 'GizmoAdornment'
                        WireframeHandle.Parent = TargetParent
                        Ceive.WireframeHandle = WireframeHandle
                     end
                 end
                for Tween in Tweens do
                     Tween.Time+=dt
                    local Alpha = Tween.Time / Tween.TweenInfo.Time
                    if Alpha > 1 then
                         Alpha = 1
                     end
                    local function LerpProperty(Start, End, Time)
                        if type(Start) == 'number' then
                             return Lerp(Start, End, Time)
                        end
                        return Start:Lerp(End, Time)
                    end
                    for k, v in Tween.Properties do
                         if not Tween.Goal[k]then
                             continue
                         end
                        local TweenAlpha = TweenService:GetValue(Alpha, Tween.TweenInfo.EasingStyle, Tween.TweenInfo.EasingDirection)local PropertyValue = LerpProperty(v, Tween.Goal[k], TweenAlpha)Tween.p_Properties[k] = PropertyValue
                     end
                    if Alpha == 1 then
                         Tweens[Tween] = nil
                     end
                 end
                for i = #Debris, 1, - 1 do
                     local DebrisObject = Debris[i]local DebrisType = DebrisObject[1]local DebrisLifetime = DebrisObject[2]local DebrisBirth = DebrisObject[3]local DebrisCallback = DebrisObject[4]if DebrisType == 'Seconds' then
                         if os.clock() - DebrisBirth > DebrisLifetime then
                             table.remove(Debris, i)continue
                         end DebrisCallback()continue
                     end
                    if DebrisBirth > DebrisLifetime then
                         table.remove(Debris, i)continue
                     end DebrisObject[2]+=1
                    DebrisCallback()
                end
                for i = #RetainObjects, 1, - 1 do
                     local Gizmo = RetainObjects[i]local GizmoPropertys = Gizmo[2]if not GizmoPropertys.Enabled then
                         continue
                     end
                    if GizmoPropertys.Destroy then
                         table.remove(RetainObjects, i)
                    end Gizmo[1]:Update(GizmoPropertys)
                end
             end)
        end function Ceive.SetEnabled(Value)
            Ceive.Enabled = Value
            if Value == false then
                 Ceive.DoCleaning()
            end
         end function Ceive.RemoveAdornments()
            if TargetParent:FindFirstChild('AOTGizmoAdornment')then
                 TargetParent:FindFirstChild('AOTGizmoAdornment'):Destroy()
            end
            if TargetParent:FindFirstChild('GizmoAdornment')then
                 TargetParent:FindFirstChild('GizmoAdornment'):Destroy()
            end
         end Ceive['Arrow'] = __DARKLUA_BUNDLE_MODULES.load('p').Init(Ceive, PropertyTable, Request, Release, Retain, Register)Ceive['Box'] = __DARKLUA_BUNDLE_MODULES.load('q').Init(Ceive, PropertyTable, Request, Release, Retain, Register)Ceive['Capsule'] = __DARKLUA_BUNDLE_MODULES.load('r').Init(Ceive, PropertyTable, Request, Release, Retain, Register)Ceive['CFrame'] = __DARKLUA_BUNDLE_MODULES.load('s').Init(Ceive, PropertyTable, Request, Release, Retain, Register)Ceive['Circle'] = __DARKLUA_BUNDLE_MODULES.load('t').Init(Ceive, PropertyTable, Request, Release, Retain, Register)Ceive['Cone'] = __DARKLUA_BUNDLE_MODULES.load('u').Init(Ceive, PropertyTable, Request, Release, Retain, Register)Ceive['Cylinder'] = __DARKLUA_BUNDLE_MODULES.load('v').Init(Ceive, PropertyTable, Request, Release, Retain, Register)Ceive['Line'] = __DARKLUA_BUNDLE_MODULES.load('w').Init(Ceive, PropertyTable, Request, Release, Retain, Register)Ceive['Mesh'] = __DARKLUA_BUNDLE_MODULES.load('x').Init(Ceive, PropertyTable, Request, Release, Retain, Register)Ceive['Plane'] = __DARKLUA_BUNDLE_MODULES.load('y').Init(Ceive, PropertyTable, Request, Release, Retain, Register)Ceive['Ray'] = __DARKLUA_BUNDLE_MODULES.load('z').Init(Ceive, PropertyTable, Request, Release, Retain, Register)Ceive['RoundedFrustum'] = __DARKLUA_BUNDLE_MODULES.load('A').Init(Ceive, PropertyTable, Request, Release, Retain, Register)Ceive['Sphere'] = __DARKLUA_BUNDLE_MODULES.load('B').Init(Ceive, PropertyTable, Request, Release, Retain, Register)Ceive['Text'] = __DARKLUA_BUNDLE_MODULES.load('C').Init(Ceive, PropertyTable, Request, Release, Retain, Register)Ceive['VolumeArrow'] = __DARKLUA_BUNDLE_MODULES.load('D').Init(Ceive, PropertyTable, Request, Release, Retain, Register)Ceive['VolumeBox'] = __DARKLUA_BUNDLE_MODULES.load('E').Init(Ceive, PropertyTable, Request, Release, Retain, Register)Ceive['VolumeCone'] = __DARKLUA_BUNDLE_MODULES.load('F').Init(Ceive, PropertyTable, Request, Release, Retain, Register)Ceive['VolumeCylinder'] = __DARKLUA_BUNDLE_MODULES.load('G').Init(Ceive, PropertyTable, Request, Release, Retain, Register)Ceive['VolumeSphere'] = __DARKLUA_BUNDLE_MODULES.load('H').Init(Ceive, PropertyTable, Request, Release, Retain, Register)Ceive['Wedge'] = __DARKLUA_BUNDLE_MODULES.load('I').Init(Ceive, PropertyTable, Request, Release, Retain, Register)return Ceive
     end)()
end function __DARKLUA_BUNDLE_MODULES.K()
    if not LPH_OBFUSCATED then
         LPH_ENCNUM = function(toEncrypt, ...)
            assert(type(toEncrypt) == 'number' and #{
                ...
            } == 0, [[LPH_ENCNUM only accepts a single constant double or integer as an argument.]])
            return toEncrypt
         end LPH_NUMENC = LPH_ENCNUM
        LPH_ENCSTR = function(toEncrypt, ...)
            assert(type(toEncrypt) == 'string' and #{
                ...
            } == 0, [[LPH_ENCSTR only accepts a single constant string as an argument.]])
            return toEncrypt
         end LPH_STRENC = LPH_ENCSTR
        LPH_ENCFUNC = function(toEncrypt, encKey, decKey, ...)
            assert(type(toEncrypt) == 'function' and type(encKey) == 'string' and #{
                ...
            } == 0, [[LPH_ENCFUNC accepts a constant function, constant string, and string variable as arguments.]])
            return toEncrypt
         end LPH_FUNCENC = LPH_ENCFUNC
        LPH_JIT = function(f, ...)
            assert(type(f) == 'function' and #{
                ...
            } == 0, [[LPH_JIT only accepts a single constant function as an argument.]])
            return f
         end LPH_JIT_MAX = LPH_JIT
        LPH_NO_VIRTUALIZE = function(f, ...)
            assert(type(f) == 'function' and #{
                ...
            } == 0, [[LPH_NO_VIRTUALIZE only accepts a single constant function as an argument.]])
            return f
         end LPH_NO_UPVALUES = function(f, ...)
            assert(type(setfenv) == 'function', [[LPH_NO_UPVALUES can only be used on Lua versions with getfenv & setfenv]])
            assert(type(f) == 'function' and #{
                ...
            } == 0, [[LPH_NO_UPVALUES only accepts a single constant function as an argument.]])
            return f
         end LPH_CRASH = function(...)
            warn('LPH_CRASH INVOKED')
            assert(#{
                ...
            } == 0, 'LPH_CRASH does not accept any arguments.')
        end
     end
    local secure_call = function(Function:(...any)->any, ...)
        local fenv = getfenv(Function)
        return coroutine.wrap(function(...)
            setidentity(2)setfenv(0, fenv)setfenv(1, fenv)return Function(...)
        end)(...)
    end
    return secure_call
 end function __DARKLUA_BUNDLE_MODULES.L()
    local function flen(Table)
        :number
        local Count = 0
        for _ in next, Table do
             Count+=1
         end
        return Count
     end
    local Cleaner = {
        Registry = {
        },
        AllowedTypes = {
            ['RBXScriptConnection'] = true,
            ['Instance'] = true,
            ['table'] = true,
            ['function'] = true,
            ['thread'] = true
        },
        CleanEvent = Instance.new('BindableEvent')
    }
    local function _autoRegisterWithStorage(Object:any)
        local ok, getg = pcall(function()
            return getgenv
         end)
        if not ok or type(getg) ~= 'function' then
             return
         end
        local env = getg()
        local Storage = env and env.BS_Storage
        local optIn = env and env.BS_AutoRegisterStorage
        if not Storage or not optIn then
             return
         end
        local function nextKey(map, base)
            map.__auto_index = map.__auto_index or {
            }
            local counters = map.__auto_index
            local n = (counters[base] or 0) + 1
            local key = base
            if rawget(map, base) ~= nil then
                 key = string.format('%s#%d', base, n)
            end
            while rawget(map, key) ~= nil do
                 n+=1
                key = string.format('%s#%d', base, n)
            end counters[base] = n
            return key
         end
        local t = typeof(Object)
        if t == 'RBXScriptConnection' then
             local key = nextKey(Storage.Connections, 'AutoConnection')
            Storage.Connections[key] = Object
         elseif  t == 'thread' then
             local key = nextKey(Storage.Routines, 'AutoRoutine')
            Storage.Routines[key] = Object
         end
     end function Cleaner.Register(Object:any)
        if not Cleaner.AllowedTypes[typeof(Object)]then
             warn('Attempted to register an invalid object type:', typeof(Object))
            warn(debug.traceback())
            return
         end
        if Cleaner.Registry[Object]then
             warn('Object is already registered for cleanup:', Object)
            return
         end Cleaner.Registry[Object] = true
        if typeof(Object) == 'RBXScriptConnection' or typeof(Object) == 'thread' then
             _autoRegisterWithStorage(Object)
        end
        return {
            Clean = function()
                Cleaner.CleanOne(Object)
            end
        }
    end function Cleaner.Clean()
        print('Cleaning up', flen(Cleaner.Registry), 'objects.')
        for Object, _ in next, Cleaner.Registry do
             if typeof(Object) == 'RBXScriptConnection' then
                 Object:Disconnect()
            elseif  typeof(Object) == 'Instance' then
                 Object:Destroy()
            elseif  type(Object) == 'table' then
                 for Index, Value in next, Object do
                     Object[Index] = nil
                 end
             elseif  type(Object) == 'function' then
                 Object()
            elseif  type(Object) == 'thread' then
                 coroutine.close(Object)
            end Cleaner.Registry[Object] = nil
         end Cleaner.CleanEvent:Fire()
    end function Cleaner.CleanOne(Object:any)
        if not Cleaner.AllowedTypes[typeof(Object)]then
             warn('Attempted to clean an invalid object type:', typeof(Object))
            return
         end
        if not Cleaner.Registry[Object]then
             warn('Object is not registered for cleanup:', Object)
            return
         end
        if typeof(Object) == 'RBXScriptConnection' then
             Object:Disconnect()
        elseif  typeof(Object) == 'Instance' then
             Object:Destroy()
        elseif  type(Object) == 'table' then
             for Index, Value in next, Object do
                 Object[Index] = nil
             end
         elseif  type(Object) == 'function' then
             Object()
        elseif  type(Object) == 'thread' then
             coroutine.close(Object)
        end Cleaner.Registry[Object] = nil
     end function Cleaner.GetCleanEvent()
        return Cleaner.CleanEvent.Event
     end setmetatable(Cleaner, {
        __call = function(self,
            Object:any)
            self.Register(Object)return Object
         end
    })
    return Cleaner
 end function __DARKLUA_BUNDLE_MODULES.M()
    local function flen(Table)
        :number
        local Count = 0
        for _ in next, Table do
             Count+=1
         end
        return Count
     end
    local HookMgr = {
        Registry = {
        },
        GameMT = {
            __namecall = function(self,
                ...)
            end,
            __index = function(self,
                Index:string)
            end,
            __newindex = function(self,
                Index:string,
                Value:any)
            end
        }
    }
    if getrawmetatable then
         HookMgr.GameMT = getrawmetatable(game)
    end HookMgr.RegisterHook = function(HookName:string, FunctionReference:(...any)->...any, Hook:(Original:(...any)->...any, ...any)->...any)
        :{
            Original:(...any)->...any,
            Reference:(...any)->...any
        }
        local OriginalFunction:(...any)->...any
        if shared.HOOKING_ENABLED then
             local HookKey = 'HookMgr_Hook_' .. HookName
            local OriginalKey = 'HookMgr_Original_' .. HookName
            shared.HookRegistry = shared.HookRegistry or {
            }
            shared.HookRegistry[HookKey] = Hook
            local Success, Error = pcall(function()
                OriginalFunction = hookfunction(FunctionReference, loadstring(`return function(...) return shared.HookRegistry["{HookKey}"](shared.HookRegistry["{ OriginalKey}"], ...) end`)())
            end)
            if not Success then
                 warn('Failed to hook function:', HookName, 'Error:', Error)
            end
            local RegistryEntry = HookMgr.Registry[HookName]if RegistryEntry then
                 restorefunction(RegistryEntry.Reference)
                warn('Hook for function', HookName, 'already exists. Overriding.')
            end shared.HookRegistry[OriginalKey] = OriginalFunction
         else
             warn('Hooking is disabled. Skipping hook for function:', HookName)
        end HookMgr.Registry[HookName] = {
            Original = OriginalFunction or FunctionReference,
            Reference = FunctionReference
        }
        return HookMgr.Registry[HookName]
    end HookMgr.UnregisterHook = function(HookName:string)
        if shared.HOOKING_ENABLED then
             local RegistryEntry = HookMgr.Registry[HookName]if RegistryEntry then
                 local Success, Error = pcall(function()
                    restorefunction(RegistryEntry.Reference)
                end)
                if not Success then
                     warn('Failed to unhook function:', HookName, 'Error:', Error)
                end
             else
                 warn('Hook for function', HookName, 'does not exist.')
            end
         else
             warn('Hooking is disabled. Skipping unhook for function:', HookName)
        end HookMgr.Registry[HookName] = nil
     end HookMgr.ClearHooks = function()
        if shared.HOOKING_ENABLED then
             print('Clearing', flen(HookMgr.Registry), 'hooks.')
            for HookName, RegistryEntry in next, HookMgr.Registry do
                 local Success, Error = pcall(function()
                    restorefunction(RegistryEntry.Reference)
                end)
                if not Success then
                     warn('Failed to unhook function:', HookName, 'Error:', Error)
                end
             end
         else
             warn('Hooking is disabled. Skipping clearing hooks.')
        end HookMgr.Registry = {
        }
    end
    return HookMgr
 end function __DARKLUA_BUNDLE_MODULES.N()
    if not LPH_OBFUSCATED then
         LPH_ENCNUM = function(toEncrypt, ...)
            assert(type(toEncrypt) == 'number' and #{
                ...
            } == 0, [[LPH_ENCNUM only accepts a single constant double or integer as an argument.]])
            return toEncrypt
         end LPH_NUMENC = LPH_ENCNUM
        LPH_ENCSTR = function(toEncrypt, ...)
            assert(type(toEncrypt) == 'string' and #{
                ...
            } == 0, [[LPH_ENCSTR only accepts a single constant string as an argument.]])
            return toEncrypt
         end LPH_STRENC = LPH_ENCSTR
        LPH_ENCFUNC = function(toEncrypt, encKey, decKey, ...)
            assert(type(toEncrypt) == 'function' and type(encKey) == 'string' and #{
                ...
            } == 0, [[LPH_ENCFUNC accepts a constant function, constant string, and string variable as arguments.]])
            return toEncrypt
         end LPH_FUNCENC = LPH_ENCFUNC
        LPH_JIT = function(f, ...)
            assert(type(f) == 'function' and #{
                ...
            } == 0, [[LPH_JIT only accepts a single constant function as an argument.]])
            return f
         end LPH_JIT_MAX = LPH_JIT
        LPH_NO_VIRTUALIZE = function(f, ...)
            assert(type(f) == 'function' and #{
                ...
            } == 0, [[LPH_NO_VIRTUALIZE only accepts a single constant function as an argument.]])
            return f
         end LPH_NO_UPVALUES = function(f, ...)
            assert(type(setfenv) == 'function', [[LPH_NO_UPVALUES can only be used on Lua versions with getfenv & setfenv]])
            assert(type(f) == 'function' and #{
                ...
            } == 0, [[LPH_NO_UPVALUES only accepts a single constant function as an argument.]])
            return f
         end LPH_CRASH = function(...)
            warn('LPH_CRASH INVOKED')
            assert(#{
                ...
            } == 0, 'LPH_CRASH does not accept any arguments.')
        end
     end
    local ArgumentCheck = {
    }
    local function sprint(...)
        return
     end
    local function _swarn(...)
        return
     end
    local function flen(Table)
        :number
        local Count = 0
        for _ in next, Table do
             Count+=1
         end
        return Count
     end
    local T = __DARKLUA_BUNDLE_MODULES.load('e').translate
    local Checks = {
        Purchase_Consumable = {
            Match = 'purchase_consumable',
            Last_Constant = 'get',
            Value = 'purchase_consumable',
            Found = false,
            SourceString = 'ReplicatedStorage.Modules.Game.UI.ConsumableBuyUI'
        },
        Win = {
            Match = 'atm_win',
            Last_Constant = 'send',
            Value = 'atm_win_2',
            Found = false,
            SourceString = 'ReplicatedStorage.Modules.Game.ATM.ATM'
        },
        Request = {
            Match = 'request_begin_hacking',
            Last_Constant = 'send',
            Value = 'request_begin_hacking_2',
            Found = false,
            SourceString = 'ReplicatedStorage.Modules.Game.ATM.ATM'
        },
        Sprint = {
            Match = 'set_sprinting',
            Last_Constant = 'send',
            Value = 'set_sprinting_1',
            Found = false,
            SourceString = 'ReplicatedStorage.Modules.Game.Sprint'
        },
        Start_Grilling = {
            Match = 'start_grilling',
            Last_Constant = 'send',
            Value = 'start_grilling_2',
            Found = false,
            SourceString = 'ReplicatedStorage.Modules.Game.Jobs.SteakhouseCook'
        },
        Finish_Grilling = {
            Match = 'finish_grilling',
            Last_Constant = 'send',
            Value = 'finish_grilling_2',
            Found = false,
            SourceString = 'ReplicatedStorage.Modules.Game.Jobs.SteakhouseCook'
        },
        ATM_Transfer = {
            Match = 'transfer_funds',
            Last_Constant = 'get',
            Value = 'transfer_funds',
            Found = false,
            SourceString = 'ReplicatedStorage.Modules.Game.ATM.ATMUI'
        },
        Respawn = {
            Match = 'death_screen_request_respawn',
            Last_Constant = 'send',
            Value = 'death_screen_request_respawn',
            Found = false,
            SourceString = 'ReplicatedStorage.Modules.Game.DeathScreen'
        },
        Request_Respawn = {
            Match = 'request_respawn',
            Last_Constant = 'send',
            Value = 'request_respawn',
            Found = false,
            SourceString = 'ReplicatedStorage.Modules.Game.ResetCallback'
        },
        Toggle_Equip_Item = {
            Match = 'toggle_equip_item',
            Last_Constant = 'format',
            Value = 'toggle_equip_item_1',
            Found = false,
            SourceString = 'ReplicatedStorage.Modules.Game.Inventory.ItemsUI'
        },
        Apply_For_Job = {
            Match = 'apply_for_job',
            Last_Constant = 'send',
            Value = 'apply_for_job',
            Found = false,
            SourceString = 'ReplicatedStorage.Modules.Game.Jobs.JobApplicationBeacon'
        },
        Leave_Character_Creator = {
            Match = 'leave_character_creator',
            Last_Constant = 'send',
            Value = 'leave_character_creator',
            Found = false,
            SourceString = [[ReplicatedStorage.Modules.Game.CharacterCreator.CharacterCreator]]
        },
        Enter_Character_Creator = {
            Match = 'enter_character_creator',
            Last_Constant = 'send',
            Value = 'enter_character_creator',
            Found = false,
            SourceString = [[ReplicatedStorage.Modules.Game.CharacterCreator.CharacterCreator]]
        },
        End_Ragdoll_Early = {
            Match = 'end_ragdoll_early',
            Last_Constant = 'send',
            Value = 'end_ragdoll_early',
            Found = false,
            SourceString = 'ReplicatedStorage.Modules.Game.Ragdoll'
        },
        Player_Started_Stocking_Shelf = {
            Match = 'player_started_stocking_shelf',
            Last_Constant = 'get',
            Value = 'player_started_stocking_shelf',
            Found = false,
            SourceString = 'ReplicatedStorage.Modules.Game.Jobs.ShelfStocking'
        },
        Player_Stocked_Shelf = {
            Match = 'player_stocked_shelf',
            Last_Constant = 'get',
            Value = 'player_stocked_shelf',
            Found = false,
            SourceString = 'ReplicatedStorage.Modules.Game.Jobs.ShelfStocking'
        },
        Pickup_Dropped_Item = {
            Match = 'pickup_dropped_item',
            Last_Constant = 'get',
            Value = 'pickup_dropped_item',
            Found = false,
            SourceString = 'ReplicatedStorage.Modules.Game.DroppedItem'
        },
        Get_Random_Free_Grill = {
            Match = 'get_random_free_grill',
            Last_Constant = 'get',
            Value = 'get_random_free_grill',
            Found = false,
            SourceString = 'ReplicatedStorage.Modules.Game.Jobs.SteakhouseCook'
        },
        Claim_Quest = {
            Match = 'claim_quest',
            Last_Constant = 'get',
            Value = 'claim_quest',
            Found = false,
            SourceString = 'ReplicatedStorage.Modules.Game.Quests.QuestsUI'
        },
        Melee_Attack = {
            Match = 'melee_attack',
            Last_Constant = 'send',
            Value = 'melee_attack',
            Found = false,
            SourceString = 'ReplicatedStorage.Modules.Game.ItemTypes.Melee'
        },
        Lock_Vehicle = {
            Match = 'lock_vehicle',
            Last_Constant = 'send',
            Value = 'lock_vehicle',
            Found = false,
            SourceString = 'ReplicatedStorage.Modules.Game.VehicleSystem.VehicleGui'
        },
        Drop_Item = {
            Match = 'drop_item',
            Last_Constant = 'send',
            Value = 'drop_item',
            Found = false,
            SourceString = 'ReplicatedStorage.Modules.Game.Inventory.ItemsUI'
        },
        Reel_Ended = {
            Match = 'reel_ended',
            Last_Constant = 'send',
            Value = 'reel_ended',
            Found = false,
            SourceString = 'ReplicatedStorage.Modules.Game.ItemTypes.FishingRod'
        },
        Change_Accessory = {
            Match = 'change_accessory',
            Last_Constant = 'get',
            Value = 'change_accessory',
            Found = false,
            SourceString = [[ReplicatedStorage.Modules.Game.CharacterCreator.CharacterCreator.Items.HatAccessories]]
        },
        Throw_Item = {
            Match = 'throw_item',
            Last_Constant = 'send',
            Value = 'throw_item',
            Found = false,
            SourceString = 'ReplicatedStorage.Modules.Game.ItemTypes.Throwable'
        },
        Throw_Hit = {
            Match = 'throw_hit',
            Last_Constant = 'send',
            Value = 'throw_hit',
            Found = false,
            SourceString = 'ReplicatedStorage.Modules.Game.ItemTypes.Throwable'
        },
        Throw_Rod = {
            Match = 'throw_rod',
            Last_Constant = 'send',
            Value = 'throw_rod',
            Found = false,
            SourceString = 'ReplicatedStorage.Modules.Game.ItemTypes.FishingRod'
        },
        Fix_Desync_Hip_Height = {
            Match = 'fix_desync_hip_height',
            Last_Constant = 'get',
            Value = 'fix_desync_hip_height',
            Found = false,
            SourceString = [[ReplicatedStorage.Modules.Game.Character.AutomaticScalingEnabled]]
        },
        Redeem_Referral_Code = {
            Match = 'redeem_referral_code',
            Last_Constant = 'get',
            Value = 'redeem_referral_code',
            Found = false,
            SourceString = 'ReplicatedStorage.Modules.Game.Referral.ReferralUI'
        },
        Run_Over = {
            Math = 'run_over',
            Last_Constant = 'send',
            Value = 'run_over',
            Found = false,
            SourceString = [[ReplicatedStorage.Modules.Game.VehicleSystem.Vehicle.VehicleTypes.car]]
        }
    }
    local function dbgprint(...)
    end
    local function dbgwarn(...)
    end
    local function IsASCII(char)
        return char:byte() >= 32 and char:byte() <= 127
     end function ParseBytecode(data)
        local Constants = {
        }
        local Constant = {
        }
        local NAIaR = 0
        local CanAbort = false
        for i = 1, #data do
             local char = data:sub(i, i)
            if IsASCII(char)then
                 NAIaR = 0
                table.insert(Constant, char)
            else
                 NAIaR+=1
                if#Constant > 0 then
                     table.insert(Constants, table.concat(Constant, ''))
                    table.clear(Constant)
                    CanAbort = true
                 end
             end
            if NAIaR > 10 and CanAbort then
                 break
             end
         end
        return Constants
     end
    local Arguments = flen(Checks)
    local Threads = {
    }
    local CompletedCount = 0
    local DumpCache = {
    }
    local DumpScript = LPH_JIT_MAX(function(Script:BaseScript)
        if not DumpCache[Script]then
             DumpCache[Script] = ParseBytecode(getscriptbytecode(Script))
        end
        return DumpCache[Script]
    end)
    local function GetScriptInstanceFromSourceString(SourceString:string)
        :Instance?local Current = game
        local Segments = {
        }
        for Segment in string.gmatch(SourceString, '[^%.]+')do
             table.insert(Segments, Segment)
        end
        for i = 1, #Segments do
             Current = Current:FindFirstChild(Segments[i])
            if not Current then
                 warn('Failed to find segment', Segments[i], 'in path', SourceString)
                return nil
             end
         end
        return Current
     end
    for Argument, Data in next, Checks do
         local Thread = task.spawn(function()
            local CurrentIndex = #Threads + 1
            sprint(T(`Performing integrity check{ CurrentIndex } / { Arguments } for '{Argument}'...`))dbgprint(T(`------------------------------------------------------`
            ))dbgprint(T(`[ArgCheck]Starting check for:{ Argument }`))dbgprint(T(`[ArgCheck]Expected Value:'{ Data.Value}', Match Pattern:'{Data.Match}', Source:'{Data.SourceString}'`))local Constants = DumpScript(GetScriptInstanceFromSourceString(Data.SourceString))dbgprint(`[ArgCheck]Attempting exact match...`)for _, Constant in next, Constants do
                 if type(Constant) == 'string' and Constant == Data.Value then
                     dbgprint(`[ArgCheck]SUCCESS:Exact match found for '{ Argument}' with value '{Constant}'.`)Checks[Argument].Found = true break
                 end
             end
            if Checks[Argument].Found then
                 sprint(`Integrity check{ CurrentIndex } / { Arguments } passed.('{Argument}' is up - to - date)`)
            else
                 dbgwarn(`[ArgCheck]INFO:Exact match for '{ Argument}' failed.Attempting fuzzy match to find new value...`)for i, Constant in ipairs(Constants)do
                     local constantStr = tostring(Constant)local pattern = tostring(Data.Match)if string.match(constantStr, pattern)then
                         dbgprint(`[ArgCheck]SUCCESS:Fuzzy match found.Updating '{ Argument}' to new value '{Constant}'.`)Checks[Argument].Found = true Checks[Argument].Value = Constant break
                     end
                 end
                if Checks[Argument].Found then
                     sprint(`Integrity check{ CurrentIndex } / { Arguments } passed.('{Argument}' was updated to '{Data.Value}')`)
                else
                     warn(`[ArgCheck]CRITICAL:All checks for '{Argument}' failed.Feature may be broken.`)sprint(`Integrity check{ CurrentIndex } / { Arguments } FAILED.('{Argument}' could not be found)`)
                end
             end dbgprint(`------------------------------------------------------`)
            CompletedCount+=1
         end)table.insert(Threads, Thread)
    end
    while CompletedCount < Arguments do
         task.wait()
    end ArgumentCheck.Results = Checks
    ArgumentCheck.AllFound = true
    for Argument, Data in next, Checks do
         if not Data.Found then
             warn(`[ArgCheck]CRITICAL:'{ Argument}' was not found.Feature may be broken.`)ArgumentCheck.AllFound = false
         end
     end
    return ArgumentCheck
 end function __DARKLUA_BUNDLE_MODULES.O()
    if not LPH_OBFUSCATED then
         LPH_ENCNUM = function(toEncrypt, ...)
            assert(type(toEncrypt) == 'number' and #{
                ...
            } == 0, [[LPH_ENCNUM only accepts a single constant double or integer as an argument.]])return toEncrypt
         end LPH_NUMENC = LPH_ENCNUM
        LPH_ENCSTR = function(toEncrypt, ...)
            assert(type(toEncrypt) == 'string' and #{
                ...
            } == 0, [[LPH_ENCSTR only accepts a single constant string as an argument.]])return toEncrypt
         end LPH_STRENC = LPH_ENCSTR
        LPH_ENCFUNC = function(toEncrypt, encKey, decKey, ...)
            assert(type(toEncrypt) == 'function' and type(encKey) == 'string' and #{
                ...
            } == 0, [[LPH_ENCFUNC accepts a constant function, constant string, and string variable as arguments.]])return toEncrypt
         end LPH_FUNCENC = LPH_ENCFUNC
        LPH_JIT = function(f, ...)
            assert(type(f) == 'function' and #{
                ...
            } == 0, [[LPH_JIT only accepts a single constant function as an argument.]])return f
         end LPH_JIT_MAX = LPH_JIT
        LPH_NO_VIRTUALIZE = function(f, ...)
            assert(type(f) == 'function' and #{
                ...
            } == 0, [[LPH_NO_VIRTUALIZE only accepts a single constant function as an argument.]])return f
         end LPH_NO_UPVALUES = function(f, ...)
            assert(type(setfenv) == 'function', [[LPH_NO_UPVALUES can only be used on Lua versions with getfenv & setfenv]])assert(type(f) == 'function' and #{
                ...
            } == 0, [[LPH_NO_UPVALUES only accepts a single constant function as an argument.]])return f
         end LPH_CRASH = function(...)
            warn('LPH_CRASH INVOKED')assert(#{
                ...
            } == 0, 'LPH_CRASH does not accept any arguments.')
        end
     end
    local function Initialize(Storage, SafeRequire, Core, UpdateStatus, T)
        local Net = SafeRequire(Core:WaitForChild('Net') :: ModuleScript)xpcall(function()
            if Storage.SecurityCheckPatched == true then
                 return
             end
            local function findSecurityCheck()
                local Ok, Value = pcall(debug.getupvalue, Net.send, 2)if Ok and Value and type(Value) == 'function' then
                     local ConstantsToFind = {
                        ['getfenv'] = false,
                        ['identifyexecutor'] = false
                    }
                    for Constant, _ in next, ConstantsToFind do
                         local Found = false
                        for _, Const in next, debug.getconstants(Value)do
                             if Const == Constant then
                                 Found = true break
                             end
                         end
                        if not Found then
                             return nil
                         end ConstantsToFind[Constant] = true
                     end
                    if not(ConstantsToFind['getfenv'] and ConstantsToFind['identifyexecutor'])then
                         return nil
                     end
                    return Value
                 end
                return nil
             end
            local SecurityCheck = findSecurityCheck()if not SecurityCheck then
                 if Storage.SecurityCheckPatched ~= false then
                     warn([[Security check signature was not found on Net.send. It may have changed or been patched already.]])
                end Storage.SecurityCheckPatched = false
                return
             end replaceclosure(SecurityCheck, LPH_NO_UPVALUES(function(p12, p13, p14, p15, ...)
                return p12(p13, p14, p15, ...)
            end))Storage.SecurityCheckPatched = true
         end, function(err)
            local traceback
            local success, trace = pcall(debug.traceback, err, 2)if success and type(trace) == 'string' then
                 traceback = trace
             else
                 traceback = tostring(err)
            end
            local message = 'Network security check failed!'
            warn(message)print(traceback)if typeof(setclipboard) == 'function' then
                 local clipboardOk, clipboardErr = pcall(setclipboard, traceback)if clipboardOk then
                     warn('Stack trace copied to clipboard.')
                else
                     warn('Failed to copy stack trace to clipboard:', clipboardErr)
                end
             else
                 warn('setclipboard is not available in this environment.')
            end coroutine.yield()
        end)local SecureNet = {
            Send2 = clonefunction(Net.send),
            Get2 = clonefunction(Net.get)
        }
        UpdateStatus(T('Updating arguments...'))local ArgCheck = __DARKLUA_BUNDLE_MODULES.load('N')local ArgumentChecks = ArgCheck.Results
        assert(ArgCheck.AllFound, 'Not all argument checks were found!')function SecureNet.Send(...)
            local FirstArg = select(1, ...)if type(FirstArg) == 'string' then
                 local Found = false
                for _, Data in pairs(ArgumentChecks)do
                     if Data.Value == FirstArg and Data.Found then
                         Found = true break
                     end
                 end
                if not Found then
                     if Storage.Blacklisted_Network_Calls[FirstArg]then
                         warn('Network call to', FirstArg, 'is blacklisted. Call blocked.')return
                     else
                         warn('First argument', FirstArg, [[not found in argument checks or not verified. Network call blocked.]])return
                     end
                 end
             else
                 warn('First argument is not a string. Network call blocked.')return
             end
            return SecureNet.Send2(...)
        end function SecureNet.Get(...)
            local FirstArg = select(1, ...)if type(FirstArg) == 'string' then
                 local Found = false
                for _, Data in pairs(ArgumentChecks)do
                     if Data.Value == FirstArg and Data.Found then
                         Found = true break
                     end
                 end
                if not Found then
                     if Storage.Blacklisted_Network_Calls[FirstArg]then
                         warn('Network call to', FirstArg, 'is blacklisted. Call blocked.')return
                     else
                         warn('First argument', FirstArg, [[not found in argument checks or not verified. Network call blocked.]])return
                     end
                 end
             else
                 warn('First argument is not a string. Network call blocked.')return
             end
            return SecureNet.Get2(...)
        end
        return SecureNet
     end
    return Initialize
 end function __DARKLUA_BUNDLE_MODULES.P()
    if not LPH_OBFUSCATED then
         LPH_ENCNUM = function(toEncrypt, ...)
            assert(type(toEncrypt) == 'number' and #{
                ...
            } == 0, [[LPH_ENCNUM only accepts a single constant double or integer as an argument.]])return toEncrypt
         end LPH_NUMENC = LPH_ENCNUM
        LPH_ENCSTR = function(toEncrypt, ...)
            assert(type(toEncrypt) == 'string' and #{
                ...
            } == 0, [[LPH_ENCSTR only accepts a single constant string as an argument.]])return toEncrypt
         end LPH_STRENC = LPH_ENCSTR
        LPH_ENCFUNC = function(toEncrypt, encKey, decKey, ...)
            assert(type(toEncrypt) == 'function' and type(encKey) == 'string' and #{
                ...
            } == 0, [[LPH_ENCFUNC accepts a constant function, constant string, and string variable as arguments.]])return toEncrypt
         end LPH_FUNCENC = LPH_ENCFUNC
        LPH_JIT = function(f, ...)
            assert(type(f) == 'function' and #{
                ...
            } == 0, [[LPH_JIT only accepts a single constant function as an argument.]])return f
         end LPH_JIT_MAX = LPH_JIT
        LPH_NO_VIRTUALIZE = function(f, ...)
            assert(type(f) == 'function' and #{
                ...
            } == 0, [[LPH_NO_VIRTUALIZE only accepts a single constant function as an argument.]])return f
         end LPH_NO_UPVALUES = function(f, ...)
            assert(type(setfenv) == 'function', [[LPH_NO_UPVALUES can only be used on Lua versions with getfenv & setfenv]])assert(type(f) == 'function' and #{
                ...
            } == 0, [[LPH_NO_UPVALUES only accepts a single constant function as an argument.]])return f
         end LPH_CRASH = function(...)
            warn('LPH_CRASH INVOKED')assert(#{
                ...
            } == 0, 'LPH_CRASH does not accept any arguments.')
        end
     end
    local function Initialize(...)
        local Cleaner = __DARKLUA_BUNDLE_MODULES.load('L')local SecureNet = __DARKLUA_BUNDLE_MODULES.load('O')(...)local ArgumentChecks = __DARKLUA_BUNDLE_MODULES.load('N').Results
        local LocalPlayer = game:GetService('Players').LocalPlayer
        local RunService = game:GetService('RunService')local Utils = {
        }
        function Utils.GetJoinCode()
            :string
            local JobId = game.JobId
            local PlaceId = game.PlaceId
            if not JobId or type(JobId) ~= 'string' or #JobId < 1 then
                 return ''
             end
            local function rot13(str)
                return str:gsub('%a', function(c)
                    local byte = string.byte(c)local base
                    if byte >= string.byte('a') and byte <= string.byte('z')then
                         base = string.byte('a')
                    elseif  byte >= string.byte('A') and byte <= string.byte('Z')then
                         base = string.byte('A')
                    else
                         return c
                     end
                    return string.char((byte - base + 13) % 26 + base)
                end)
            end
            local function toBase36(n)
                if type(n) ~= 'number' or n < 0 then
                     return ''
                 end
                if n == 0 then
                     return '0'
                 end
                local chars = '0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ'
                local out = {
                }
                while n > 0 do
                     local rem = n % 36
                    n = math.floor(n / 36)table.insert(out, 1, chars:sub(rem + 1, rem + 1))
                end
                return table.concat(out)
            end
            local RotatedJobId = rot13(JobId):gsub('-', '.')local EncodedPlace = toBase36(PlaceId)return RotatedJobId .. '|' .. EncodedPlace
         end function Utils.JoinCodeToJoinData(JoinCode:string)
            :{
                JobId:string,
                PlaceId:number
            }
            if not JoinCode or type(JoinCode) ~= 'string' or #JoinCode < 1 then
                 return {
                    JobId = '',
                    PlaceId = 0
                }
            end
            local function rot13(str)
                return str:gsub('%a', function(c)
                    local byte = string.byte(c)local base
                    if byte >= string.byte('a') and byte <= string.byte('z')then
                         base = string.byte('a')
                    elseif  byte >= string.byte('A') and byte <= string.byte('Z')then
                         base = string.byte('A')
                    else
                         return c
                     end
                    return string.char((byte - base + 13) % 26 + base)
                end)
            end
            local function fromBase36(s)
                if not s or s == '' then
                     return 0
                 end s = s:upper()local value = 0
                for i = 1, #s do
                     local c = s:sub(i, i)local digit = tonumber(c)if not digit then
                         digit = string.byte(c) - string.byte('A') + 10
                     end value = value * 36 + digit
                 end
                return value
             end
            local sep = JoinCode:find('|', 1, true)local rotatedPart, placePart
            if sep then
                 rotatedPart = JoinCode:sub(1, sep - 1)placePart = JoinCode:sub(sep + 1)
            else
                 rotatedPart = JoinCode
                placePart = nil
             end rotatedPart = rotatedPart:match('^%s*(.-)%s*$') or rotatedPart
            local restoredJobRot = rotatedPart:gsub('%.', '-')local JobId = rot13(restoredJobRot)local PlaceId = 0
            if placePart and #placePart > 0 then
                 PlaceId = fromBase36(placePart)
            else
                 PlaceId = game.PlaceId or 0
             end
            return {
                JobId = JobId,
                PlaceId = PlaceId
            }
        end Utils.TP = LPH_NO_VIRTUALIZE(function(Target:Vector3 | CFrame | PVInstance)
            :boolean
            local Pivot:CFrame
            if typeof(Target) == 'CFrame' then
                 Pivot = Target :: CFrame
             elseif  typeof(Target) == 'Vector3' then
                 Pivot = CFrame.new(Target :: Vector3)
            elseif  typeof(Target) == 'PVInstance' then
                 Pivot = (Target :: PVInstance):GetPivot()
            elseif  typeof(Target) == 'BasePart' then
                 Pivot = (Target :: BasePart):GetPivot()
            elseif  typeof(Target) == 'Model' then
                 Pivot = (Target :: Model):GetPivot()
            end
            local Character = LocalPlayer.Character
            if Character then
                 Character:PivotTo(Pivot)return true
             end
            return false
         end)Utils.TPRoot = LPH_NO_VIRTUALIZE(function(Target:Vector3 | CFrame | PVInstance)
            :boolean
            local Pivot:CFrame
            if typeof(Target) == 'CFrame' then
                 Pivot = Target :: CFrame
             elseif  typeof(Target) == 'Vector3' then
                 Pivot = CFrame.new(Target :: Vector3)
            elseif  typeof(Target) == 'PVInstance' then
                 Pivot = (Target :: PVInstance):GetPivot()
            elseif  typeof(Target) == 'BasePart' then
                 Pivot = (Target :: BasePart):GetPivot()
            elseif  typeof(Target) == 'Model' then
                 Pivot = (Target :: Model):GetPivot()
            end
            local Character = LocalPlayer.Character
            if Character then
                 Character.HumanoidRootPart.CFrame = Pivot
                return true
             end
            return false
         end)Utils.LockPosition = LPH_NO_VIRTUALIZE(function(Target:Vector3 | CFrame | PVInstance)
            :RBXScriptConnection?local Character = LocalPlayer.Character
            if Character then
                 local Connection = Cleaner(RunService.Heartbeat:Connect(function()
                    Utils.TP(Target)
                end))task.delay(30, function()
                    if Connection and Connection.Connected then
                         warn([[LockPosition connection not properly cleaned up after 30 seconds!]])Connection:Disconnect()
                    end
                 end)return Connection
             end
            return nil
         end)Utils.LerpTP = LPH_NO_VIRTUALIZE(function(Target:Vector3 | CFrame | PVInstance, Duration:number)
            :boolean
            local Pivot:CFrame
            if typeof(Target) == 'CFrame' then
                 Pivot = Target :: CFrame
             elseif  typeof(Target) == 'Vector3' then
                 Pivot = CFrame.new(Target :: Vector3)
            elseif  typeof(Target) == 'PVInstance' then
                 Pivot = (Target :: PVInstance):GetPivot()
            elseif  typeof(Target) == 'BasePart' then
                 Pivot = (Target :: BasePart):GetPivot()
            elseif  typeof(Target) == 'Model' then
                 Pivot = (Target :: Model):GetPivot()
            end
            local Character = LocalPlayer.Character
            if Character then
                 local Humanoid = Character:FindFirstChildOfClass('Humanoid')local VehicleSeat = Humanoid and Humanoid.SeatPart
                local IsInVehicle = VehicleSeat and VehicleSeat:IsA('VehicleSeat')local ObjectToMove = (IsInVehicle and VehicleSeat.Parent) or Character
                if not(ObjectToMove and ObjectToMove:IsA('PVInstance'))then
                     ObjectToMove = Character
                 end
                local Start = os.clock()local StartPosition = ObjectToMove:GetPivot()local EndPosition = Pivot
                local LastSprintCall = 0
                while true do
                     RunService.PreSimulation:Wait()for _, Descendant in next, ObjectToMove:GetDescendants()do
                         if Descendant:IsA('BasePart')then
                             Descendant.AssemblyLinearVelocity = Vector3.zero
                            Descendant.AssemblyAngularVelocity = Vector3.zero
                         end
                     end
                    local Elapsed = os.clock() - Start
                    local Alpha = math.clamp(Elapsed / Duration, 0, 1)local NewPosition = StartPosition:Lerp(EndPosition, Alpha)if os.clock() - LastSprintCall > 1 then
                         LastSprintCall = os.clock()SecureNet.Send(ArgumentChecks.Sprint.Value, true)
                    end ObjectToMove:PivotTo(NewPosition)if Alpha >= 1 then
                         break
                     end
                 end
                if ObjectToMove then
                     ObjectToMove:PivotTo(Pivot)return true
                 else
                     warn('ObjectToMove not found during end of LerpTP.')return false
                 end
             end
            return false
         end)Utils.LerpTPWithHeight = LPH_NO_VIRTUALIZE(function(Target:Vector3 | CFrame | PVInstance, Duration:number)
            :boolean
            local Pivot:CFrame
            if typeof(Target) == 'CFrame' then
                 Pivot = Target :: CFrame
             elseif  typeof(Target) == 'Vector3' then
                 Pivot = CFrame.new(Target :: Vector3)
            elseif  typeof(Target) == 'PVInstance' then
                 Pivot = (Target :: PVInstance):GetPivot()
            elseif  typeof(Target) == 'BasePart' then
                 Pivot = (Target :: BasePart):GetPivot()
            elseif  typeof(Target) == 'Model' then
                 Pivot = (Target :: Model):GetPivot()
            end
            local Params = RaycastParams.new()Params.FilterType = Enum.RaycastFilterType.Exclude
            Params.FilterDescendantsInstances = {
                LocalPlayer.Character,
                workspace:WaitForChild('Vehicles'),
                workspace:WaitForChild('Map'):WaitForChild('BoundaryWalls'),
                workspace:WaitForChild('Map'):WaitForChild('Vegetation'):WaitForChild('Trees'),
                workspace:WaitForChild('Map'):WaitForChild('Props'):WaitForChild('PowerLines'),
                workspace:WaitForChild('Map'):WaitForChild('Props'):WaitForChild('PrestigeMotorsLargeSign')
            }
            Params.RespectCanCollide = true
            local function ShapecastDown(Position:Vector3)
                :RaycastResult?local Result = workspace:Spherecast(Position + Vector3.yAxis * 7, 5, Vector3.yAxis * - 200, Params)return Result
             end
            local function lerp(a:number, b:number, alpha:number)
                :number
                return a + (b - a) * alpha
             end
            local Character = LocalPlayer.Character
            if Character then
                 local Humanoid = Character:FindFirstChildOfClass('Humanoid')local VehicleSeat = Humanoid and Humanoid.SeatPart
                local IsInVehicle = VehicleSeat and VehicleSeat:IsA('VehicleSeat')local ObjectToMove = (IsInVehicle and VehicleSeat.Parent) or Character
                if not(ObjectToMove and ObjectToMove:IsA('PVInstance'))then
                     ObjectToMove = Character
                 end
                local Start = os.clock()local StartPosition = ObjectToMove:GetPivot()local EndPosition = Pivot
                local Height = StartPosition.Position.Y
                local Rotation = CFrame.lookAt(StartPosition.Position, EndPosition.Position).Rotation
                while true do
                     RunService.PreSimulation:Wait()for _, Descendant in next, ObjectToMove:GetDescendants()do
                         if Descendant:IsA('BasePart')then
                             Descendant.AssemblyLinearVelocity = Vector3.zero
                            Descendant.AssemblyAngularVelocity = Vector3.zero
                         end
                     end
                    local Elapsed = os.clock() - Start
                    local Alpha = math.clamp(Elapsed / Duration, 0, 1)local NewPosition = StartPosition:Lerp(EndPosition, Alpha)local RaycastResult = ShapecastDown(NewPosition.Position)local PivotTarget = CFrame.new(NewPosition.Position)if RaycastResult then
                         Height = lerp(Height, RaycastResult.Position.Y + 3, 0.1)PivotTarget = CFrame.new(NewPosition.Position.X, NewPosition.Position.Y, NewPosition.Position.Z)
                    end ObjectToMove:PivotTo(PivotTarget * Rotation)if Alpha >= 1 then
                         break
                     end
                 end
                if ObjectToMove then
                     ObjectToMove:PivotTo(Pivot * Rotation)return true
                 else
                     warn('ObjectToMove not found during end of LerpTP.')return false
                 end
             end
            return false
         end)Utils.MergeTables = LPH_NO_VIRTUALIZE(function(...)
            local Merged = {
            }
            for _, Table in ipairs({
                ...
            })
do
                 if type(Table) == 'table' then
                     for Key, Value in pairs(Table)do
                         Merged[Key] = Value
                     end
                 end
             end
            return Merged
         end)Utils.InsertMergeTables = LPH_NO_VIRTUALIZE(function(...)
            local Merged = {
            }
            for _, t in ipairs({
                ...
            })
do
                 if type(t) == 'table' then
                     for _, v in ipairs(t)do
                         table.insert(Merged, v)
                    end
                 end
             end
            return Merged
         end)function Utils.UnifiedTeleportHandler(options:{
                PlaceId:number,
                JobId:string?,
                Bypass:boolean?
            })
            local PlaceId = options.PlaceId
            local JobId = options.JobId
            local Bypass = options.Bypass
            print('Teleport requested', PlaceId, JobId, Bypass)setclipboard(JobId)if not PlaceId or type(PlaceId) ~= 'number' or PlaceId <= 0 then
                 error('Invalid PlaceId provided for teleport.')return
             end
            local TeleportService = game:GetService('TeleportService')local Players = game:GetService('Players')local LocalPlayer = Players.LocalPlayer
            local PAID_PLACE = 95898900045000
            local finalLoadScript = '\r\n    print("[Sasware] Loading main script...")\r\n    --game:GetService("TeleportService"):SetLocalPlayerTeleportData({ teleport_reason = "Sasware Teleport Success" })\r\n    if getgenv().Key ~= "BLACKLISTED" then\r\n        task_wait(5)\r\n        loadstring(game:HttpGet("https://example.com/script/Blockspin_Paid_Loader.luau"))()\r\n    end\r\n'
            local AppendString = 'getgenv().Key = "NoKey"\n'
            if getgenv().Key then
                 AppendString = `getgenv().Key = "{getgenv().Key}"\n`
            end
            if Bypass == false then
                 queue_on_teleport(AppendString .. finalLoadScript)local success, err = pcall(function()
                    if JobId then
                         TeleportService:TeleportToPlaceInstance(PlaceId, JobId, LocalPlayer)
                    else
                         TeleportService:Teleport(PlaceId, LocalPlayer)
                    end
                 end)if not success then
                     warn('Teleport error:', err)
                end
                return
             end
            if PlaceId == PAID_PLACE then
                 queue_on_teleport(AppendString .. finalLoadScript)local success, err = pcall(function()
                    if JobId then
                         TeleportService:TeleportToPlaceInstance(PlaceId, JobId, LocalPlayer)
                    else
                         TeleportService:Teleport(PlaceId, LocalPlayer)
                    end
                 end)if not success then
                     warn('Teleport error:', err)
                end
                return
             end
            local teleportCall
            if JobId then
                 teleportCall = string.format('\r\n    local TeleportService = game:GetService("TeleportService")\r\n    local Players = game:GetService("Players")\r\n    local LocalPlayer = Players.LocalPlayer\r\n    pcall(function()\r\n        TeleportService:TeleportToPlaceInstance(%d, %q, LocalPlayer)\r\n    end)\r\n', PlaceId, JobId)
            else
                 teleportCall = ''
             end
            local paidRedirectScript = string.format('\r\n    local final = %q\r\n    local append = %q\r\n    -- Ensure the final loader is queued so it runs on arrival to the target server.\r\n    queue_on_teleport(append .. final)\r\n    -- Perform authenticated teleport to the actual destination.\r\n    %s\r\n', finalLoadScript, AppendString, teleportCall)queue_on_teleport(AppendString .. paidRedirectScript)local success, err = pcall(function()
                TeleportService:Teleport(PAID_PLACE, LocalPlayer)
            end)if not success then
                 warn('Teleport error:', err)
            end
         end
        return Utils
     end
    return Initialize
 end function __DARKLUA_BUNDLE_MODULES.Q()
    local ConnectionProxyMgr = {
        Registry = {
        },
        Id = 0
    }
    function ConnectionProxyMgr._requestId()
        ConnectionProxyMgr.Id+=1
        return ConnectionProxyMgr.Id
     end function ConnectionProxyMgr._newProxyHandler(ConnectionProxy)
        local Id = ConnectionProxyMgr._requestId()local Handler = {
            Proxy = ConnectionProxy,
            Enabled = true,
            ClearSignal = Instance.new('BindableEvent')
        }
        function Handler:Disable()
            self.Enabled = false self.Proxy:Disable()
        end function Handler:Enable()
            self.Enabled = true self.Proxy:Enable()
        end Handler.ClearSignal.Event:Once(function()
            pcall(function()
                Handler.Proxy:Enable()ConnectionProxyMgr.Registry[Id] = nil
             end)
        end)ConnectionProxyMgr.Registry[Id] = Handler
        return Handler
     end function ConnectionProxyMgr:Register(ConnectionProxy)
        return ConnectionProxyMgr._newProxyHandler(ConnectionProxy)
    end function ConnectionProxyMgr:Clear()
        for _, Handler in next, ConnectionProxyMgr.Registry do
             Handler.ClearSignal:Fire()
        end
     end function ConnectionProxyMgr:YieldForConnection(Signal:RBXScriptSignal, SourceNeedle:string, Timeout:number?)
        local Start = os.clock()while task.wait()do
             local Connections = getconnections(Signal) :: {
                any
            }
            for _, Connection in next, Connections do
                 local Function = Connection.Function
                if Function and type(Function) == 'function' then
                     if not pcall(debug.info, Function, 's')then
                         warn('Failed to get function source:', Function)continue
                     end
                    if debug.info(Function, 's'):match(SourceNeedle)then
                         return Connection
                     end
                 end
             end
            if Timeout and os.clock() - Start >= Timeout then
                 return nil
             end
         end
        return nil
     end
    return ConnectionProxyMgr
 end function __DARKLUA_BUNDLE_MODULES.R()
    local Webhooks = __DARKLUA_BUNDLE_MODULES.load('b')local HttpService = game:GetService('HttpService')local Players = game:GetService('Players')local REPORT_URL = [[https://discord.com/api/webhooks/REDACTED/REDACTED]]
    local MAX_FIELD_LENGTH = 1024
    local MAX_DESCRIPTION_LENGTH = 2048
    local ErrorReporter = {
    }
    local function toString(value)
        if value == nil then
             return 'nil'
         end
        if type(value) == 'string' then
             return value
         end
        if type(value) == 'table' then
             local success, encoded = pcall(function()
                return HttpService:JSONEncode(value)
            end)if success then
                 return encoded
             end
         end
        return tostring(value)
    end
    local function truncate(value, limit)
        local text = toString(value)if limit and #text > limit then
             return string.sub(text, 1, limit - 3) .. '...'
         end
        return text
     end
    local function getEnvValue(key)
        if type(getgenv) ~= 'function' then
             return nil
         end
        local success, env = pcall(getgenv)if success and type(env) == 'table' then
             return env[key]
        end
        return nil
     end
    local function getExecutorInfo()
        if type(identifyexecutor) == 'function' then
             local success, name, version = pcall(identifyexecutor)if success then
                 if type(name) == 'table' then
                     local encoded = toString(name)return truncate(encoded, MAX_FIELD_LENGTH)
                end
                local label = tostring(name or 'Unknown')if version and version ~= '' then
                     label = label .. '' .. tostring(version)
                end
                return truncate(label, MAX_FIELD_LENGTH)
            end
         end
        return 'Unavailable'
     end
    local function getLicenseKey()
        local key = getEnvValue('Key')if key == nil or key == '' then
             return 'No Key'
         end
        return truncate(toString(key), MAX_FIELD_LENGTH)
    end
    local function resolveFreeBuild()
        local value = getEnvValue('FREE_BUILD')if value ~= nil then
             return value and 'Yes' or 'No'
         end
        local success, fallback = pcall(function()
            return false
         end)if success and fallback ~= nil then
             return fallback and 'Yes' or 'No'
         end
        return 'Unknown'
     end
    local function getLocalPlayer()
        local success, player = pcall(function()
            return Players.LocalPlayer
         end)if success and player then
             return player
         end
        return nil
     end
    local function resolveTraceback(raw, depth)
        if raw and raw ~= '' then
             return truncate(toString(raw), MAX_FIELD_LENGTH)
        end
        if type(debug) == 'table' and type(debug.traceback) == 'function' then
             local success, trace = pcall(function()
                return debug.traceback(nil, depth or 4)
            end)if success and trace and trace ~= '' then
                 return truncate(trace, MAX_FIELD_LENGTH)
            end
         end
        return 'Unavailable'
     end function ErrorReporter.ReportPopup(data)
        if type(data) ~= 'table' then
             return
         end task.spawn(function()
            local player = getLocalPlayer()local playerLabel = 'Unknown'
            local userId = '0'
            if player then
                 local display = player.DisplayName or player.Name
                playerLabel = string.format('%s (%s)', player.Name, display)userId = tostring(player.UserId)
            end
            local message = truncate(data.message or 'No message provided.', MAX_DESCRIPTION_LENGTH)local trace = resolveTraceback(data.traceback, data.tracebackDepth)local executorInfo = getExecutorInfo()local licenseKey = getLicenseKey()local freeBuild = resolveFreeBuild()local recoverableText = 'Unknown'
            if data.recoverable ~= nil then
                 recoverableText = data.recoverable and 'Yes' or 'No'
             end
            local embed = {
                title = data.title or 'Sasware Error Report',
                description = message,
                color = data.color or 0xff5555,
                fields = {
                    {
                        name = 'Error Code',
                        value = truncate(data.code or 'N/A',
                        256),
                        inline = true
                    },
                    {
                        name = 'Recoverable',
                        value = recoverableText,
                        inline = true
                    },
                    {
                        name = 'Source',
                        value = truncate(data.source or 'Unknown',
                        MAX_FIELD_LENGTH),
                        inline = true
                    },
                    {
                        name = 'Executor',
                        value = executorInfo,
                        inline = true
                    },
                    {
                        name = 'Free Build',
                        value = freeBuild,
                        inline = true
                    },
                    {
                        name = 'License Key',
                        value = licenseKey,
                        inline = false
                    },
                    {
                        name = 'Player',
                        value = truncate(playerLabel,
                        MAX_FIELD_LENGTH),
                        inline = true
                    },
                    {
                        name = 'UserId',
                        value = userId,
                        inline = true
                    },
                    {
                        name = 'PlaceId',
                        value = tostring(game.PlaceId),
                        inline = true
                    },
                    {
                        name = 'Traceback',
                        value = trace,
                        inline = false
                    }
                },
                footer = {
                    text = string.format('Timestamp: %s',
                    os.date('%Y-%m-%d %H:%M:%S'))
                }
            }
            if type(data.extraFields) == 'table' then
                 for _, field in ipairs(data.extraFields)do
                     if type(field) == 'table' then
                         table.insert(embed.fields, {
                            name = truncate(field.name or 'Extra',
                            256),
                            value = truncate(field.value or 'N/A',
                            MAX_FIELD_LENGTH),
                            inline = field.inline or false
                        })
                    end
                 end
             end
            local payload = {
                url = REPORT_URL,
                embeds = {
                    embed
                },
                username = data.username or 'Sasware Error Reporter'
            }
            if data.content then
                 payload.content = truncate(data.content, 2000)
            end
            local success = Webhooks.SendWebhook(payload)if not success then
                 warn('[ErrorReporter] Failed to send error webhook')
            end
         end)
    end
    return ErrorReporter
 end function __DARKLUA_BUNDLE_MODULES.S()
    local function InteractiveToast(HeaderText:string, ContentText:string, Button1Text:string, Button2Text:string)
        :(ScreenGui, ImageButton, ImageButton)local ActiveToastObject = Instance.new('ScreenGui')ActiveToastObject.Parent = nil ActiveToastObject.Enabled = true ActiveToastObject.SafeAreaCompatibility = Enum.SafeAreaCompatibility.FullscreenExtension
        ActiveToastObject.ResetOnSpawn = false ActiveToastObject.IgnoreGuiInset = false ActiveToastObject.Name = 'InteractiveToast'
        ActiveToastObject.DisplayOrder = 0
        ActiveToastObject.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
        ActiveToastObject.ScreenInsets = Enum.ScreenInsets.CoreUISafeInsets
        ActiveToastObject.ClipToDeviceSafeArea = true
        local Frame_2241 = Instance.new('Frame')Frame_2241.Parent = ActiveToastObject
        Frame_2241.LayoutOrder = 0
        Frame_2241.BorderMode = Enum.BorderMode.Outline
        Frame_2241.Interactable = true Frame_2241.AnchorPoint = Vector2.new(0, 0)Frame_2241.BorderColor = BrickColor.new('Black')Frame_2241.SizeConstraint = Enum.SizeConstraint.RelativeXY
        Frame_2241.ZIndex = 1
        Frame_2241.AutomaticSize = Enum.AutomaticSize.Y
        Frame_2241.Size = UDim2.new(1, 0, 1, 0)Frame_2241.Draggable = false Frame_2241.Visible = true Frame_2241.ClipsDescendants = false Frame_2241.BorderColor3 = Color3.fromRGB(27, 42, 53)Frame_2241.Selectable = false Frame_2241.Style = Enum.FrameStyle.Custom
        Frame_2241.SelectionOrder = 0
        Frame_2241.Rotation = 0
        Frame_2241.Transparency = 1
        Frame_2241.BackgroundTransparency = 1
        Frame_2241.Position = UDim2.new(0, 0, 0, 0)Frame_2241.Active = false Frame_2241.Name = '1'
        Frame_2241.BorderSizePixel = 1
        Frame_2241.BackgroundColor3 = Color3.fromRGB(163, 162, 165)local Child = Instance.new('Frame')Child.Parent = Frame_2241
        Child.LayoutOrder = 0
        Child.BorderMode = Enum.BorderMode.Outline
        Child.Interactable = true Child.AnchorPoint = Vector2.new(0.5, 0.5)Child.BorderColor = BrickColor.new('Black')Child.SizeConstraint = Enum.SizeConstraint.RelativeXY
        Child.ZIndex = 1
        Child.AutomaticSize = Enum.AutomaticSize.Y
        Child.Size = UDim2.new(0, 360, 0, 0)Child.Draggable = false Child.Visible = true Child.ClipsDescendants = false Child.BorderColor3 = Color3.fromRGB(27, 42, 53)Child.Selectable = false Child.Style = Enum.FrameStyle.Custom
        Child.SelectionOrder = 0
        Child.Rotation = 0
        Child.Transparency = 0.30000001192092896
        Child.BackgroundTransparency = 0.30000001192092896
        Child.Position = UDim2.new(0.5, 0, 0.5, 0)Child.Active = false Child.Name = 'Child'
        Child.BorderSizePixel = 0
        Child.BackgroundColor3 = Color3.fromRGB(0, 0, 0)local ListLayout = Instance.new('UIListLayout')ListLayout.Parent = Child
        ListLayout.FillDirection = Enum.FillDirection.Horizontal
        ListLayout.HorizontalAlignment = Enum.HorizontalAlignment.Left
        ListLayout.HorizontalFlex = Enum.UIFlexAlignment.None
        ListLayout.VerticalAlignment = Enum.VerticalAlignment.Top
        ListLayout.SortOrder = Enum.SortOrder.LayoutOrder
        ListLayout.Name = 'ListLayout'
        ListLayout.Wraps = false ListLayout.Padding = UDim.new(0, 8)ListLayout.ItemLineAlignment = Enum.ItemLineAlignment.Automatic
        ListLayout.VerticalFlex = Enum.UIFlexAlignment.None
        local Padding = Instance.new('UIPadding')Padding.Parent = Child
        Padding.PaddingTop = UDim.new(0, 12)Padding.Name = 'Padding'
        Padding.PaddingBottom = UDim.new(0, 12)Padding.PaddingLeft = UDim.new(0, 12)Padding.PaddingRight = UDim.new(0, 12)local Content = Instance.new('Frame')Content.Parent = Child
        Content.LayoutOrder = 2
        Content.BorderMode = Enum.BorderMode.Outline
        Content.Interactable = true Content.AnchorPoint = Vector2.new(0, 0)Content.BorderColor = BrickColor.new('Black')Content.SizeConstraint = Enum.SizeConstraint.RelativeXY
        Content.ZIndex = 1
        Content.AutomaticSize = Enum.AutomaticSize.Y
        Content.Size = UDim2.new(0, 0, 0, 0)Content.Draggable = false Content.Visible = true Content.ClipsDescendants = false Content.BorderColor3 = Color3.fromRGB(27, 42, 53)Content.Selectable = false Content.Style = Enum.FrameStyle.Custom
        Content.SelectionOrder = 0
        Content.Rotation = 0
        Content.Transparency = 1
        Content.BackgroundTransparency = 1
        Content.Position = UDim2.new(0, 0, 0, 0)Content.Active = false Content.Name = 'Content'
        Content.BorderSizePixel = 0
        Content.BackgroundColor3 = Color3.fromRGB(163, 162, 165)local FlexItem = Instance.new('UIFlexItem')FlexItem.Parent = Content
        FlexItem.Name = 'FlexItem'
        FlexItem.FlexMode = Enum.UIFlexMode.Fill
        FlexItem.ShrinkRatio = 0
        FlexItem.GrowRatio = 0
        FlexItem.ItemLineAlignment = Enum.ItemLineAlignment.Center
        local ListLayout = Instance.new('UIListLayout')ListLayout.Parent = Content
        ListLayout.FillDirection = Enum.FillDirection.Vertical
        ListLayout.HorizontalAlignment = Enum.HorizontalAlignment.Left
        ListLayout.HorizontalFlex = Enum.UIFlexAlignment.None
        ListLayout.VerticalAlignment = Enum.VerticalAlignment.Top
        ListLayout.SortOrder = Enum.SortOrder.LayoutOrder
        ListLayout.Name = 'ListLayout'
        ListLayout.Wraps = false ListLayout.Padding = UDim.new(0, 2)ListLayout.ItemLineAlignment = Enum.ItemLineAlignment.Automatic
        ListLayout.VerticalFlex = Enum.UIFlexAlignment.None
        local Actions = Instance.new('Frame')Actions.Parent = Content
        Actions.LayoutOrder = 3
        Actions.BorderMode = Enum.BorderMode.Outline
        Actions.Interactable = true Actions.AnchorPoint = Vector2.new(0, 0)Actions.BorderColor = BrickColor.new('Black')Actions.SizeConstraint = Enum.SizeConstraint.RelativeXY
        Actions.ZIndex = 1
        Actions.AutomaticSize = Enum.AutomaticSize.Y
        Actions.Size = UDim2.new(1, 0, 0, 0)Actions.Draggable = false Actions.Visible = true Actions.ClipsDescendants = false Actions.BorderColor3 = Color3.fromRGB(27, 42, 53)Actions.Selectable = false Actions.Style = Enum.FrameStyle.Custom
        Actions.SelectionOrder = 0
        Actions.Rotation = 0
        Actions.Transparency = 1
        Actions.BackgroundTransparency = 1
        Actions.Position = UDim2.new(0, 0, 0, 0)Actions.Active = false Actions.Name = 'Actions'
        Actions.BorderSizePixel = 0
        Actions.BackgroundColor3 = Color3.fromRGB(163, 162, 165)local ListLayout = Instance.new('UIListLayout')ListLayout.Parent = Actions
        ListLayout.FillDirection = Enum.FillDirection.Horizontal
        ListLayout.HorizontalAlignment = Enum.HorizontalAlignment.Center
        ListLayout.HorizontalFlex = Enum.UIFlexAlignment.Fill
        ListLayout.VerticalAlignment = Enum.VerticalAlignment.Top
        ListLayout.SortOrder = Enum.SortOrder.LayoutOrder
        ListLayout.Name = 'ListLayout'
        ListLayout.Wraps = false ListLayout.Padding = UDim.new(0, 8)ListLayout.ItemLineAlignment = Enum.ItemLineAlignment.Automatic
        ListLayout.VerticalFlex = Enum.UIFlexAlignment.None
        local ToastButton1 = Instance.new('ImageButton')ToastButton1.Parent = Actions
        ToastButton1.LayoutOrder = 1
        ToastButton1.Active = true ToastButton1.Interactable = true ToastButton1.SizeConstraint = Enum.SizeConstraint.RelativeXY
        ToastButton1.ZIndex = 1
        ToastButton1.BorderSizePixel = 0
        ToastButton1.SliceCenter = Rect.new(0, 0, 0, 0)ToastButton1.Draggable = false ToastButton1.ScaleType = Enum.ScaleType.Stretch
        ToastButton1.Modal = false ToastButton1.AutoButtonColor = false ToastButton1.Transparency = 1
        ToastButton1.SelectionOrder = 0
        ToastButton1.BackgroundColor3 = Color3.fromRGB(0, 0, 0)ToastButton1.ImageTransparency = 0
        ToastButton1.Selectable = true ToastButton1.AnchorPoint = Vector2.new(0, 0)ToastButton1.Image = ''
        ToastButton1.TileSize = UDim2.new(1, 0, 1, 0)ToastButton1.ImageRectSize = Vector2.new(0, 0)ToastButton1.Selected = false ToastButton1.AutomaticSize = Enum.AutomaticSize.X
        ToastButton1.Size = UDim2.new(1, 0, 0, 36)ToastButton1.Visible = true ToastButton1.HoverImage = ''
        ToastButton1.Style = Enum.ButtonStyle.Custom
        ToastButton1.ClipsDescendants = true ToastButton1.BorderColor3 = Color3.fromRGB(27, 42, 53)ToastButton1.BorderMode = Enum.BorderMode.Outline
        ToastButton1.ImageColor3 = Color3.fromRGB(255, 255, 255)ToastButton1.PressedImage = ''
        ToastButton1.Rotation = 0
        ToastButton1.ImageRectOffset = Vector2.new(0, 0)ToastButton1.BackgroundTransparency = 1
        ToastButton1.Position = UDim2.new(0, 0, 0, 0)ToastButton1.SliceScale = 1
        ToastButton1.ResampleMode = Enum.ResamplerMode.Default
        ToastButton1.BorderColor = BrickColor.new('Black')ToastButton1.Name = 'ToastButton1'
        local Stroke = Instance.new('UIStroke')Stroke.Parent = ToastButton1
        Stroke.ApplyStrokeMode = Enum.ApplyStrokeMode.Contextual
        Stroke.LineJoinMode = Enum.LineJoinMode.Round
        Stroke.Name = 'Stroke'
        Stroke.Color = Color3.fromRGB(255, 255, 255)Stroke.Transparency = 0
        Stroke.Thickness = 1
        Stroke.Enabled = true
        local Text = Instance.new('TextLabel')Text.Parent = ToastButton1
        Text.LayoutOrder = 2
        Text.FontSize = Enum.FontSize.Size24
        Text.TextDirection = Enum.TextDirection.Auto
        Text.Active = false Text.Interactable = true Text.TextStrokeTransparency = 1
        Text.TextTruncate = Enum.TextTruncate.AtEnd
        Text.SizeConstraint = Enum.SizeConstraint.RelativeXY
        Text.ZIndex = 1
        Text.BorderSizePixel = 0
        Text.Draggable = false Text.RichText = true Text.SelectionOrder = 0
        Text.TextYAlignment = Enum.TextYAlignment.Center
        Text.TextScaled = false Text.BackgroundColor3 = Color3.fromRGB(163, 162, 165)Text.FontFace = Font.new('rbxasset://fonts/families/BuilderSans.json', Enum.FontWeight.Bold, Enum.FontStyle.Normal)Text.BorderMode = Enum.BorderMode.Outline
        Text.Selectable = false Text.OpenTypeFeatures = ''
        Text.AnchorPoint = Vector2.new(0, 0)Text.BorderColor = BrickColor.new('Black')Text.Visible = true Text.TextXAlignment = Enum.TextXAlignment.Center
        Text.AutomaticSize = Enum.AutomaticSize.X
        Text.Size = UDim2.new(1, 0, 1, 0)Text.TextWrapped = true Text.TextWrap = true Text.TextTransparency = 0
        Text.ClipsDescendants = false Text.BorderColor3 = Color3.fromRGB(27, 42, 53)Text.Text = Button1Text
        Text.TextStrokeColor3 = Color3.fromRGB(0, 0, 0)Text.LineHeight = 1
        Text.Rotation = 0
        Text.Font = Enum.Font.BuilderSansBold
        Text.BackgroundTransparency = 1
        Text.Position = UDim2.new(0, 0, 0, 0)Text.TextSize = 20
        Text.MaxVisibleGraphemes = - 1
        Text.TextColor3 = Color3.fromRGB(255, 255, 255)Text.Name = 'Text'
        local CornerRadius = Instance.new('UICorner')CornerRadius.Parent = ToastButton1
        CornerRadius.Name = 'CornerRadius'
        CornerRadius.CornerRadius = UDim.new(0, 8)local ListLayout = Instance.new('UIListLayout')ListLayout.Parent = ToastButton1
        ListLayout.FillDirection = Enum.FillDirection.Horizontal
        ListLayout.HorizontalAlignment = Enum.HorizontalAlignment.Center
        ListLayout.HorizontalFlex = Enum.UIFlexAlignment.None
        ListLayout.VerticalAlignment = Enum.VerticalAlignment.Center
        ListLayout.SortOrder = Enum.SortOrder.LayoutOrder
        ListLayout.Name = 'ListLayout'
        ListLayout.Wraps = false ListLayout.Padding = UDim.new(0, 4)ListLayout.ItemLineAlignment = Enum.ItemLineAlignment.Automatic
        ListLayout.VerticalFlex = Enum.UIFlexAlignment.None
        local ToastButton2 = Instance.new('ImageButton')ToastButton2.Parent = Actions
        ToastButton2.LayoutOrder = 2
        ToastButton2.Active = true ToastButton2.Interactable = true ToastButton2.SizeConstraint = Enum.SizeConstraint.RelativeXY
        ToastButton2.ZIndex = 1
        ToastButton2.BorderSizePixel = 0
        ToastButton2.SliceCenter = Rect.new(0, 0, 0, 0)ToastButton2.Draggable = false ToastButton2.ScaleType = Enum.ScaleType.Stretch
        ToastButton2.Modal = false ToastButton2.AutoButtonColor = false ToastButton2.Transparency = 0
        ToastButton2.SelectionOrder = 0
        ToastButton2.BackgroundColor3 = Color3.fromRGB(0, 179, 108)ToastButton2.ImageTransparency = 0
        ToastButton2.Selectable = true ToastButton2.AnchorPoint = Vector2.new(0, 0)ToastButton2.Image = ''
        ToastButton2.TileSize = UDim2.new(1, 0, 1, 0)ToastButton2.ImageRectSize = Vector2.new(0, 0)ToastButton2.Selected = false ToastButton2.AutomaticSize = Enum.AutomaticSize.X
        ToastButton2.Size = UDim2.new(1, 0, 0, 36)ToastButton2.Visible = true ToastButton2.HoverImage = ''
        ToastButton2.Style = Enum.ButtonStyle.Custom
        ToastButton2.ClipsDescendants = true ToastButton2.BorderColor3 = Color3.fromRGB(27, 42, 53)ToastButton2.BorderMode = Enum.BorderMode.Outline
        ToastButton2.ImageColor3 = Color3.fromRGB(255, 255, 255)ToastButton2.PressedImage = ''
        ToastButton2.Rotation = 0
        ToastButton2.ImageRectOffset = Vector2.new(0, 0)ToastButton2.BackgroundTransparency = 0
        ToastButton2.Position = UDim2.new(0, 0, 0, 0)ToastButton2.SliceScale = 1
        ToastButton2.ResampleMode = Enum.ResamplerMode.Default
        ToastButton2.BorderColor = BrickColor.new('Black')ToastButton2.Name = 'ToastButton2'
        local Stroke = Instance.new('UIStroke')Stroke.Parent = ToastButton2
        Stroke.ApplyStrokeMode = Enum.ApplyStrokeMode.Contextual
        Stroke.LineJoinMode = Enum.LineJoinMode.Round
        Stroke.Name = 'Stroke'
        Stroke.Color = Color3.fromRGB(0, 0, 0)Stroke.Transparency = 1
        Stroke.Thickness = 1
        Stroke.Enabled = true
        local Text = Instance.new('TextLabel')Text.Parent = ToastButton2
        Text.LayoutOrder = 2
        Text.FontSize = Enum.FontSize.Size24
        Text.TextDirection = Enum.TextDirection.Auto
        Text.Active = false Text.Interactable = true Text.TextStrokeTransparency = 1
        Text.TextTruncate = Enum.TextTruncate.AtEnd
        Text.SizeConstraint = Enum.SizeConstraint.RelativeXY
        Text.ZIndex = 1
        Text.BorderSizePixel = 0
        Text.Draggable = false Text.RichText = true Text.SelectionOrder = 0
        Text.TextYAlignment = Enum.TextYAlignment.Center
        Text.TextScaled = false Text.BackgroundColor3 = Color3.fromRGB(163, 162, 165)Text.FontFace = Font.new('rbxasset://fonts/families/BuilderSans.json', Enum.FontWeight.Bold, Enum.FontStyle.Normal)Text.BorderMode = Enum.BorderMode.Outline
        Text.Selectable = false Text.OpenTypeFeatures = ''
        Text.AnchorPoint = Vector2.new(0, 0)Text.BorderColor = BrickColor.new('Black')Text.Visible = true Text.TextXAlignment = Enum.TextXAlignment.Center
        Text.AutomaticSize = Enum.AutomaticSize.X
        Text.Size = UDim2.new(1, 0, 1, 0)Text.TextWrapped = true Text.TextWrap = true Text.TextTransparency = 0
        Text.ClipsDescendants = false Text.BorderColor3 = Color3.fromRGB(27, 42, 53)Text.Text = Button2Text
        Text.TextStrokeColor3 = Color3.fromRGB(0, 0, 0)Text.LineHeight = 1
        Text.Rotation = 0
        Text.Font = Enum.Font.BuilderSansBold
        Text.BackgroundTransparency = 1
        Text.Position = UDim2.new(0, 0, 0, 0)Text.TextSize = 20
        Text.MaxVisibleGraphemes = - 1
        Text.TextColor3 = Color3.fromRGB(255, 255, 255)Text.Name = 'Text'
        local CornerRadius = Instance.new('UICorner')CornerRadius.Parent = ToastButton2
        CornerRadius.Name = 'CornerRadius'
        CornerRadius.CornerRadius = UDim.new(0, 8)local ListLayout = Instance.new('UIListLayout')ListLayout.Parent = ToastButton2
        ListLayout.FillDirection = Enum.FillDirection.Horizontal
        ListLayout.HorizontalAlignment = Enum.HorizontalAlignment.Center
        ListLayout.HorizontalFlex = Enum.UIFlexAlignment.None
        ListLayout.VerticalAlignment = Enum.VerticalAlignment.Center
        ListLayout.SortOrder = Enum.SortOrder.LayoutOrder
        ListLayout.Name = 'ListLayout'
        ListLayout.Wraps = false ListLayout.Padding = UDim.new(0, 4)ListLayout.ItemLineAlignment = Enum.ItemLineAlignment.Automatic
        ListLayout.VerticalFlex = Enum.UIFlexAlignment.None
        local Padding = Instance.new('UIPadding')Padding.Parent = Actions
        Padding.PaddingTop = UDim.new(0, 8)Padding.Name = 'Padding'
        Padding.PaddingBottom = UDim.new(0, 0)Padding.PaddingLeft = UDim.new(0, 0)Padding.PaddingRight = UDim.new(0, 0)local Body = Instance.new('TextLabel')Body.Parent = Content
        Body.LayoutOrder = 2
        Body.FontSize = Enum.FontSize.Size18
        Body.TextDirection = Enum.TextDirection.Auto
        Body.Active = false Body.Interactable = true Body.TextStrokeTransparency = 1
        Body.TextTruncate = Enum.TextTruncate.None
        Body.SizeConstraint = Enum.SizeConstraint.RelativeXY
        Body.ZIndex = 1
        Body.BorderSizePixel = 0
        Body.Draggable = false Body.RichText = true Body.SelectionOrder = 0
        Body.TextYAlignment = Enum.TextYAlignment.Center
        Body.TextScaled = false Body.BackgroundColor3 = Color3.fromRGB(163, 162, 165)Body.FontFace = Font.new('rbxasset://fonts/families/BuilderSans.json', Enum.FontWeight.Regular, Enum.FontStyle.Normal)Body.BorderMode = Enum.BorderMode.Outline
        Body.Selectable = false Body.OpenTypeFeatures = ''
        Body.AnchorPoint = Vector2.new(0, 0)Body.BorderColor = BrickColor.new('Black')Body.Visible = true Body.TextXAlignment = Enum.TextXAlignment.Left
        Body.AutomaticSize = Enum.AutomaticSize.Y
        Body.Size = UDim2.new(1, 0, 0, 0)Body.TextWrapped = true Body.TextWrap = true Body.TextTransparency = 0
        Body.ClipsDescendants = false Body.BorderColor3 = Color3.fromRGB(27, 42, 53)Body.Text = ContentText
        Body.TextStrokeColor3 = Color3.fromRGB(0, 0, 0)Body.LineHeight = 1.031999945640564
        Body.Rotation = 0
        Body.Font = Enum.Font.BuilderSans
        Body.BackgroundTransparency = 1
        Body.Position = UDim2.new(0, 0, 0, 0)Body.TextSize = 15
        Body.MaxVisibleGraphemes = - 1
        Body.TextColor3 = Color3.fromRGB(189, 190, 190)Body.Name = 'Body'
        local Padding = Instance.new('UIPadding')Padding.Parent = Body
        Padding.PaddingTop = UDim.new(0, 0)Padding.Name = 'Padding'
        Padding.PaddingBottom = UDim.new(0, 0)Padding.PaddingLeft = UDim.new(0, 0)Padding.PaddingRight = UDim.new(0, 0)local Header = Instance.new('TextLabel')Header.Parent = Content
        Header.LayoutOrder = 1
        Header.FontSize = Enum.FontSize.Size32
        Header.TextDirection = Enum.TextDirection.Auto
        Header.Active = false Header.Interactable = true Header.TextStrokeTransparency = 1
        Header.TextTruncate = Enum.TextTruncate.AtEnd
        Header.SizeConstraint = Enum.SizeConstraint.RelativeXY
        Header.ZIndex = 1
        Header.BorderSizePixel = 0
        Header.Draggable = false Header.RichText = true Header.SelectionOrder = 0
        Header.TextYAlignment = Enum.TextYAlignment.Center
        Header.TextScaled = false Header.BackgroundColor3 = Color3.fromRGB(163, 162, 165)Header.FontFace = Font.new('rbxasset://fonts/families/BuilderSans.json', Enum.FontWeight.Bold, Enum.FontStyle.Normal)Header.BorderMode = Enum.BorderMode.Outline
        Header.Selectable = false Header.OpenTypeFeatures = ''
        Header.AnchorPoint = Vector2.new(0, 0)Header.BorderColor = BrickColor.new('Black')Header.Visible = true Header.TextXAlignment = Enum.TextXAlignment.Center
        Header.AutomaticSize = Enum.AutomaticSize.Y
        Header.Size = UDim2.new(1, 0, 0, 0)Header.TextWrapped = false Header.TextWrap = false Header.TextTransparency = 0
        Header.ClipsDescendants = false Header.BorderColor3 = Color3.fromRGB(27, 42, 53)Header.Text = HeaderText
        Header.TextStrokeColor3 = Color3.fromRGB(0, 0, 0)Header.LineHeight = 1
        Header.Rotation = 0
        Header.Font = Enum.Font.BuilderSansBold
        Header.BackgroundTransparency = 1
        Header.Position = UDim2.new(0, 0, 0, 0)Header.TextSize = 30
        Header.MaxVisibleGraphemes = - 1
        Header.TextColor3 = Color3.fromRGB(255, 255, 255)Header.Name = 'Header'
        local Padding = Instance.new('UIPadding')Padding.Parent = Header
        Padding.PaddingTop = UDim.new(0, 0)Padding.Name = 'Padding'
        Padding.PaddingBottom = UDim.new(0, 5)Padding.PaddingLeft = UDim.new(0, 0)Padding.PaddingRight = UDim.new(0, 0)local CornerRadius = Instance.new('UICorner')CornerRadius.Parent = Child
        CornerRadius.Name = 'CornerRadius'
        CornerRadius.CornerRadius = UDim.new(0, 8)return ActiveToastObject, ToastButton1, ToastButton2
     end
    local ErrorReporter = __DARKLUA_BUNDLE_MODULES.load('R')local Throw = function(Error_Code:string, Error_Message:string?, Recoverable:boolean, ExtraData:{
            [string]:any
        }?)
        local Additional:{
            [string]:any
        }? = nil
        if type(ExtraData) == 'table' then
             Additional = ExtraData
         end
        local TracebackMessage = 'Unavailable'
        if type(debug) == 'table' and type(debug.traceback) == 'function' then
             local success, trace = pcall(function()
                return debug.traceback(nil, 3)
            end)if success and trace then
                 TracebackMessage = trace
             end
         end pcall(ErrorReporter.ReportPopup, {
            code = tostring(Error_Code),
            message = Error_Message,
            recoverable = Recoverable,
            traceback = (Additional and Additional.traceback) or TracebackMessage,
            tracebackDepth = Additional and Additional.tracebackDepth,
            source = (Additional and Additional.source) or 'ErrorHandler.Throw',
            title = Additional and Additional.title,
            extraFields = Additional and Additional.extraFields,
            color = Additional and Additional.color,
            username = Additional and Additional.username,
            content = Additional and Additional.content
        })
local Root, Button1, Button2 = InteractiveToast('Critical Error', [[Sasware is unable to load properly due to a critical dependency failing to initialize or changes detected in the game's internals. Would you like to proceed? Continuing is risky.

Error code: ]] .. Error_Code .. '\nError message:' .. (Error_Message or 'No message provided.') .. ((not Recoverable) and '\nThis error is not recoverable.' or '') .. '\n', 'Proceed', 'Abort')if not Recoverable then
             Button1.Interactable = false Button1.Stroke.Transparency = 0.9
            Button1.Text.TextTransparency = 0.9
         end Button2.BackgroundColor3 = Color3.new(1, 0, 0)Root.Parent = game:GetService('CoreGui')Root.Enabled = true
        return Button1.Activated, Button2.Activated, Root
     end
    return {
        InteractiveToast = InteractiveToast,
        Throw = Throw
    }
end function __DARKLUA_BUNDLE_MODULES.T()
    return function()
        local CollectionService = game:GetService('CollectionService')local G2L = {
        }
        G2L['1'] = Instance.new('ScreenGui', game:GetService('CoreGui'))G2L['1']['IgnoreGuiInset'] = true G2L['1']['ScreenInsets'] = Enum.ScreenInsets.DeviceSafeInsets
        G2L['1']['Name'] = 'RevengeKillPrompt'
        G2L['1']['ZIndexBehavior'] = Enum.ZIndexBehavior.Sibling
        G2L['2'] = Instance.new('Frame', G2L['1'])G2L['2']['BorderSizePixel'] = 0
        G2L['2']['BackgroundColor3'] = Color3.fromRGB(255, 255, 255)G2L['2']['Size'] = UDim2.new(1, 0, 0, 100)G2L['2']['BorderColor3'] = Color3.fromRGB(0, 0, 0)G2L['2']['Name'] = 'TopBar'
        G2L['2']['BackgroundTransparency'] = 1
        G2L['3'] = Instance.new('ImageButton', G2L['2'])G2L['3']['BorderSizePixel'] = 0
        G2L['3']['AutoLocalize'] = false G2L['3']['AutoButtonColor'] = false G2L['3']['BackgroundTransparency'] = 0.2
        G2L['3']['BackgroundColor3'] = Color3.fromRGB(7, 8, 13)G2L['3']['AutomaticSize'] = Enum.AutomaticSize.X
        G2L['3']['Size'] = UDim2.new(0, 0, 0, 48)G2L['3']['ClipsDescendants'] = true G2L['3']['Name'] = '1'
        CollectionService:AddTag(G2L['3'], 'align-y-center')CollectionService:AddTag(G2L['3'], 'padding-medium')CollectionService:AddTag(G2L['3'], 'gui-object-defaults')CollectionService:AddTag(G2L['3'], 'gap-small')CollectionService:AddTag(G2L['3'], 'clip')CollectionService:AddTag(G2L['3'], 'align-x-center')CollectionService:AddTag(G2L['3'], 'row')CollectionService:AddTag(G2L['3'], 'x-default-transparency')G2L['4'] = Instance.new('UIStroke', G2L['3'])G2L['4']['Name'] = 'Stroke'
        G2L['4']['Thickness'] = 2
        G2L['4']['Color'] = Color3.fromRGB(255, 255, 255)G2L['5'] = Instance.new('UIGradient', G2L['4'])G2L['5']['Rotation'] = 90
        G2L['5']['Transparency'] = NumberSequence.new{
            NumberSequenceKeypoint.new(0,
            0),
            NumberSequenceKeypoint.new(1,
            1)
        }
        G2L['5']['Color'] = ColorSequence.new{
            ColorSequenceKeypoint.new(0,
            Color3.fromRGB(255,
            65,
            17)),
            ColorSequenceKeypoint.new(1,
            Color3.fromRGB(255,
            152,
            34))
        }
        G2L['6'] = Instance.new('UIListLayout', G2L['3'])G2L['6']['HorizontalAlignment'] = Enum.HorizontalAlignment.Center
        G2L['6']['Padding'] = UDim.new(0, 12)G2L['6']['VerticalAlignment'] = Enum.VerticalAlignment.Center
        G2L['6']['SortOrder'] = Enum.SortOrder.LayoutOrder
        G2L['6']['Name'] = 'ListLayout'
        G2L['7'] = Instance.new('UIPadding', G2L['3'])G2L['7']['PaddingTop'] = UDim.new(0, 12)G2L['7']['PaddingRight'] = UDim.new(0, 12)G2L['7']['Name'] = 'Padding'
        G2L['7']['PaddingLeft'] = UDim.new(0, 12)G2L['7']['PaddingBottom'] = UDim.new(0, 12)G2L['8'] = Instance.new('TextLabel', G2L['3'])G2L['8']['LineHeight'] = 1.111
        G2L['8']['TextTruncate'] = Enum.TextTruncate.AtEnd
        G2L['8']['BorderSizePixel'] = 0
        G2L['8']['AutoLocalize'] = false G2L['8']['TextSize'] = 20
        G2L['8']['FontFace'] = Font.new('rbxasset://fonts/families/BuilderSans.json', Enum.FontWeight.Bold, Enum.FontStyle.Normal)G2L['8']['TextColor3'] = Color3.fromRGB(241, 113, 113)G2L['8']['BackgroundTransparency'] = 1
        G2L['8']['Size'] = UDim2.new(0, 0, 1, 0)G2L['8']['Text'] = 'Revenge-Kill User123?'
        G2L['8']['AutomaticSize'] = Enum.AutomaticSize.X
        G2L['8']['Name'] = 'Text'
        CollectionService:AddTag(G2L['8'], 'x-default-transparency')CollectionService:AddTag(G2L['8'], 'gui-object-defaults')CollectionService:AddTag(G2L['8'], 'size-0-full')CollectionService:AddTag(G2L['8'], 'text-color-defaults')CollectionService:AddTag(G2L['8'], 'auto-x')CollectionService:AddTag(G2L['8'], 'text-title-large')CollectionService:AddTag(G2L['8'], 'shrink')CollectionService:AddTag(G2L['8'], 'text-truncate-end')CollectionService:AddTag(G2L['8'], 'text-size-defaults')CollectionService:AddTag(G2L['8'], 'text-defaults')G2L['9'] = Instance.new('UIFlexItem', G2L['8'])G2L['9']['Name'] = 'FlexItem'
        G2L['9']['FlexMode'] = Enum.UIFlexMode.Shrink
        G2L['a'] = Instance.new('UIPadding', G2L['8'])G2L['a']['PaddingTop'] = UDim.new(0, 1)G2L['a']['Name'] = 'Padding'
        G2L['a']['PaddingBottom'] = UDim.new(0, 1)G2L['b'] = Instance.new('UICorner', G2L['3'])G2L['b']['Name'] = 'CornerRadius'
        G2L['c'] = Instance.new('TextLabel', G2L['3'])G2L['c']['LineHeight'] = 1.111
        G2L['c']['TextTruncate'] = Enum.TextTruncate.AtEnd
        G2L['c']['BorderSizePixel'] = 0
        G2L['c']['AutoLocalize'] = false G2L['c']['TextSize'] = 20
        G2L['c']['FontFace'] = Font.new('rbxasset://fonts/families/BuilderSans.json', Enum.FontWeight.Regular, Enum.FontStyle.Normal)G2L['c']['TextColor3'] = Color3.fromRGB(241, 241, 241)G2L['c']['BackgroundTransparency'] = 1
        G2L['c']['Size'] = UDim2.new(0, 0, 1, 0)G2L['c']['Text'] = '10'
        G2L['c']['LayoutOrder'] = 2
        G2L['c']['AutomaticSize'] = Enum.AutomaticSize.X
        G2L['c']['Name'] = 'Timer'
        CollectionService:AddTag(G2L['c'], 'x-default-transparency')CollectionService:AddTag(G2L['c'], 'gui-object-defaults')CollectionService:AddTag(G2L['c'], 'size-0-full')CollectionService:AddTag(G2L['c'], 'text-color-defaults')CollectionService:AddTag(G2L['c'], 'auto-x')CollectionService:AddTag(G2L['c'], 'text-title-large')CollectionService:AddTag(G2L['c'], 'shrink')CollectionService:AddTag(G2L['c'], 'text-truncate-end')CollectionService:AddTag(G2L['c'], 'text-size-defaults')CollectionService:AddTag(G2L['c'], 'text-defaults')G2L['d'] = Instance.new('UIFlexItem', G2L['c'])G2L['d']['Name'] = 'FlexItem'
        G2L['d']['FlexMode'] = Enum.UIFlexMode.Shrink
        G2L['e'] = Instance.new('UIPadding', G2L['c'])G2L['e']['PaddingTop'] = UDim.new(0, 1)G2L['e']['Name'] = 'Padding'
        G2L['e']['PaddingBottom'] = UDim.new(0, 1)G2L['f'] = Instance.new('UIListLayout', G2L['2'])G2L['f']['HorizontalAlignment'] = Enum.HorizontalAlignment.Center
        G2L['f']['Padding'] = UDim.new(0, 8)G2L['f']['VerticalAlignment'] = Enum.VerticalAlignment.Center
        G2L['f']['SortOrder'] = Enum.SortOrder.LayoutOrder
        G2L['f']['Name'] = 'ListLayout'
        G2L['f']['FillDirection'] = Enum.FillDirection.Horizontal
        return G2L['1'], G2L
     end
 end function __DARKLUA_BUNDLE_MODULES.U()
    local FORMAT_STRING = string.rep('%08x', 8)local CONSTANTS = buffer.create(256)do
         local RoundConstants = {
            0x428a2f98,
            0x71374491,
            0xb5c0fbcf,
            0xe9b5dba5,
            0x3956c25b,
            0x59f111f1,
            0x923f82a4,
            0xab1c5ed5,
            0xd807aa98,
            0x12835b01,
            0x243185be,
            0x550c7dc3,
            0x72be5d74,
            0x80deb1fe,
            0x9bdc06a7,
            0xc19bf174,
            0xe49b69c1,
            0xefbe4786,
            0xfc19dc6,
            0x240ca1cc,
            0x2de92c6f,
            0x4a7484aa,
            0x5cb0a9dc,
            0x76f988da,
            0x983e5152,
            0xa831c66d,
            0xb00327c8,
            0xbf597fc7,
            0xc6e00bf3,
            0xd5a79147,
            0x6ca6351,
            0x14292967,
            0x27b70a85,
            0x2e1b2138,
            0x4d2c6dfc,
            0x53380d13,
            0x650a7354,
            0x766a0abb,
            0x81c2c92e,
            0x92722c85,
            0xa2bfe8a1,
            0xa81a664b,
            0xc24b8b70,
            0xc76c51a3,
            0xd192e819,
            0xd6990624,
            0xf40e3585,
            0x106aa070,
            0x19a4c116,
            0x1e376c08,
            0x2748774c,
            0x34b0bcb5,
            0x391c0cb3,
            0x4ed8aa4a,
            0x5b9cca4f,
            0x682e6ff3,
            0x748f82ee,
            0x78a5636f,
            0x84c87814,
            0x8cc70208,
            0x90befffa,
            0xa4506ceb,
            0xbef9a3f7,
            0xc67178f2
        }
        for Index, Constant in ipairs(RoundConstants)do
             local BufferOffset = (Index - 1) * 4
            buffer.writeu32(CONSTANTS, BufferOffset, Constant)
        end
     end
    local function PreProcess(Contents:buffer)
        :(buffer, number)local ContentLength = buffer.len(Contents)local Padding = - (ContentLength + 9) % 64
        local NewContentLength = ContentLength + 1 + Padding + 8
        local NewContent = buffer.create(NewContentLength)buffer.copy(NewContent, 0, Contents)buffer.writeu8(NewContent, ContentLength, 128)local Length8 = ContentLength * 8
        for Index = 7, 0, - 1 do
             local Remainder = Length8 % 256
            buffer.writeu8(NewContent, Index + ContentLength + 1 + Padding, Remainder)Length8 = (Length8 - Remainder) / 256
         end
        return NewContent, NewContentLength
     end
    local OFFSETS = buffer.create(256)local function DigestBlocks(Blocks:buffer, Length:number)
        :(number, number, number, number, number, number, number, number)local A, B, C, D = 0x6a09e667, 0xbb67ae85, 0x3c6ef372, 0xa54ff53a
        local E, F, G, H = 0x510e527f, 0x9b05688c, 0x1f83d9ab, 0x5be0cd19
        local Offsets = OFFSETS
        local Constants = CONSTANTS
        for Offset = 0, Length - 1, 64 do
             for BlockIndex = 0, 60, 4 do
                 buffer.writeu32(Offsets, BlockIndex, bit32.byteswap(buffer.readu32(Blocks, Offset + BlockIndex)))
            end
            for Index = 64, 252, 4 do
                 local Sub15 = buffer.readu32(Offsets, Index - 60)local S0 = bit32.bxor(bit32.rrotate(Sub15, 7), bit32.rrotate(Sub15, 18), bit32.rshift(Sub15, 3))local Sub2 = buffer.readu32(Offsets, Index - 8)local S1 = bit32.bxor(bit32.rrotate(Sub2, 17), bit32.rrotate(Sub2, 19), bit32.rshift(Sub2, 10))local Sub7, Sub16 = buffer.readu32(Offsets, Index - 28), buffer.readu32(Offsets, Index - 64)buffer.writeu32(Offsets, Index, (Sub16 + S0 + Sub7 + S1))
            end
            local OldA, OldB, OldC, OldD, OldE, OldF, OldG, OldH = A, B, C, D, E, F, G, H
            for BufferIndex = 0, 252, 4 do
                 local S1 = bit32.bxor(bit32.rrotate(E, 6), bit32.rrotate(E, 11), bit32.rrotate(E, 25))local Ch = bit32.bxor(bit32.band(E, F), bit32.band(bit32.bnot(E), G))local Temp1 = H + S1 + Ch + buffer.readu32(Constants, BufferIndex) + buffer.readu32(Offsets, BufferIndex)H, G, F, E, D = G, F, E, D + Temp1, C
                local S0 = bit32.bxor(bit32.rrotate(A, 2), bit32.rrotate(A, 13), bit32.rrotate(A, 22))local Maj = bit32.bxor(bit32.band(A, B), bit32.band(A, C), bit32.band(B, C))C, B, A = B, A, Temp1 + S0 + Maj
             end A, B, C, D, E, F, G, H = bit32.bor(A + OldA, 0), bit32.bor(B + OldB, 0), bit32.bor(C + OldC, 0), bit32.bor(D + OldD, 0), bit32.bor(E + OldE, 0), bit32.bor(F + OldF, 0), bit32.bor(G + OldG, 0), bit32.bor(H + OldH, 0)
        end
        return A, B, C, D, E, F, G, H
     end
    local function sha256(Content:string, Salt:string?)
        :string
        assert(type(Content) == 'string', 'Argument #1 must be type "string".')if type(Salt) == 'string' then
             Content = Content .. '_' .. Salt
         end
        local Message = buffer.fromstring(Content)local ProcessedMessage, Length = PreProcess(Message)local A, B, C, D, E, F, G, H = DigestBlocks(ProcessedMessage, Length)return string.format(FORMAT_STRING, A, B, C, D, E, F, G, H)
    end
    return sha256
 end function __DARKLUA_BUNDLE_MODULES.V()
    local SHA256 = __DARKLUA_BUNDLE_MODULES.load('U') :: (Content:string, Salt:string?)->string
    local HttpService = game:GetService('HttpService')local SecureRequest = __DARKLUA_BUNDLE_MODULES.load('a')local ORCHESTRATION_ENDPOINT = 'https://example.com/orchestration'
    local OrchestratorTest = {
    }
    function OrchestratorTest:GeneratePrivateKey(licenseKey:string, userId:number)
        :string
        local testHash = SHA256('hello')local expectedHello = [[2cf24dba5fb0a30e26e83b2ac5b9e29e1b161e5c1fa7425e73043362938b9824]]
        local KeyHash = SHA256(licenseKey, 'bsp_k1_9f3a')local UserHash = SHA256(tostring(userId), 'bsp_u2_7c1e')local Interleaved = ''
        for i = 1, 64, 8 do
             Interleaved = Interleaved .. string.sub(KeyHash, i, i + 3) .. string.sub(UserHash, i + 4, i + 7)
        end
        local Final = SHA256(Interleaved, 'bsp_f3_2d8b')local debugInfo = string.format([[SHA256('hello'): %s
Expected: %s
Match: %s

Actual salted input for key: %s
KeyHash: %s
Expected KeyHash: 9dadf26fe740fe035a8f488fb509f0c5117a04e4b5185a3165ca07d05693117a

UserHash: %s
Interleaved: %s
Final: %s]], testHash, expectedHello, tostring(testHash == expectedHello), licenseKey .. '_bsp_k1_9f3a', KeyHash, UserHash, Interleaved, Final)if setclipboard then
             pcall(setclipboard, debugInfo)
        end print('[DEBUG] Copied debug info to clipboard')return Final
     end function OrchestratorTest:TestRegisterWorkerData(licenseKey:string, workerUserId:number)
        print('[TEST] Registering worker data...')local PrivateKey = self:GeneratePrivateKey(licenseKey, workerUserId)print('[TEST] Generated private key:', string.sub(PrivateKey, 1, 16) .. '...')local Url = string.format('%s/registerWorkerData', ORCHESTRATION_ENDPOINT)local TestWorkerData = {
            master_user_id = 123456789,
            master_server_id = 'test-job-id-' .. tostring(os.time()),
            transfer_threshold = 1000000,
            autofarm_settings = {
                enabled = true,
                target_money = 5000000
            },
            priority = 1,
            registered_at = os.time()
        }
        local Payload = {
            userId = workerUserId,
            key = PrivateKey,
            data = TestWorkerData,
            license = licenseKey
        }
        local Success, Response = pcall(function()
            return SecureRequest.request({
                Method = 'POST',
                Headers = {
                    ['Content-Type'] = 'application/json'
                },
                Body = HttpService:JSONEncode(Payload),
                Url = Url
            })
        end)if not Success then
             print('[TEST] FAILED to register:', Response)return false
         end
        if not Response.Success then
             print('[TEST] Server returned error status:', Response.StatusCode, Response.StatusMessage)return false
         end
        local Data
        Success, Data = pcall(function()
            return HttpService:JSONDecode(Response.Body)
        end)if not Success then
             print('[TEST] FAILED to decode response:', Data)return false
         end
        if Data.error then
             print('[TEST] Server returned error:', Data.error)return false
         end print('[TEST] Successfully registered worker data!')print('[TEST] Response:', HttpService:JSONEncode(Data))return true, PrivateKey
     end function OrchestratorTest:TestGetWorkerData(licenseKey:string, workerUserId:number)
        print('[TEST] Retrieving worker data...')local PrivateKey = self:GeneratePrivateKey(licenseKey, workerUserId)print('[TEST] Generated private key:', string.sub(PrivateKey, 1, 16) .. '...')local Url = string.format('%s/getWorkerData?userId=%d&key=%s', ORCHESTRATION_ENDPOINT, workerUserId, PrivateKey)local Success, Response = pcall(function()
            return SecureRequest.request({
                Method = 'GET',
                Url = Url,
                Timeout = 5
            })
        end)if not Success then
             print('[TEST] Request failed (expected for missing data):', tostring(Response):sub(1, 100))return nil
         end
        if not Response.Success then
             print('[TEST] Server returned error status:', Response.StatusCode, Response.StatusMessage)return nil
         end
        local Data
        Success, Data = pcall(function()
            return HttpService:JSONDecode(Response.Body)
        end)if not Success then
             print('[TEST] FAILED to decode response:', Data)return nil
         end
        if Data.error then
             print('[TEST] Server returned error:', Data.error)return nil
         end print('[TEST] Successfully retrieved worker data!')print('[TEST] Data:', HttpService:JSONEncode(Data))return Data
     end function OrchestratorTest:RunFullTest(licenseKey:string, testWorkerUserId:number?)
        print('=== ORCHESTRATOR TEST SUITE ===')print('')local WorkerUserId = testWorkerUserId or 987654321
        print('[TEST] License Key:', string.sub(licenseKey, 1, 8) .. '...')print('[TEST] Worker UserId:', WorkerUserId)print('')print([[--- Step 1: Get data before registration (expect failure) ---]])local PreData = self:TestGetWorkerData(licenseKey, WorkerUserId)if PreData then
             print([[[TEST] WARNING: Data already exists, might be from previous test]])
        else
             print('[TEST] OK: No data found (expected)')
        end print('')print('--- Step 2: Register worker data ---')local RegisterSuccess = self:TestRegisterWorkerData(licenseKey, WorkerUserId)if not RegisterSuccess then
             print('[TEST] FAILED: Could not register worker data')return false
         end print('')print([[--- Step 3: Get data after registration (expect success) ---]])local PostData = self:TestGetWorkerData(licenseKey, WorkerUserId)if not PostData then
             print('[TEST] FAILED: Could not retrieve registered data')return false
         end print('')print('--- Step 4: Verify data integrity ---')if PostData.master_user_id == 123456789 and PostData.transfer_threshold == 1000000 then
             print('[TEST] OK: Data integrity verified!')
        else
             print('[TEST] WARNING: Data mismatch!')
        end print('')print('=== TEST COMPLETE ===')return true
     end
    return OrchestratorTest
 end
 end
repeat
     task.wait()
until game:IsLoaded()local DUPE_MODE = false
local DUPE_RECIPIENT = 'Sasware0x679'
local SecureRequest = __DARKLUA_BUNDLE_MODULES.load('a')__DARKLUA_BUNDLE_MODULES.load('d')local hookfunction = shared.SafeHook
if not LPH_OBFUSCATED then
     LPH_ENCNUM = function(toEncrypt, ...)
        assert(type(toEncrypt) == 'number' and #{
            ...
        } == 0, [[LPH_ENCNUM only accepts a single constant double or integer as an argument.]])return toEncrypt
     end LPH_NUMENC = LPH_ENCNUM
    LPH_ENCSTR = function(toEncrypt, ...)
        assert(type(toEncrypt) == 'string' and #{
            ...
        } == 0, [[LPH_ENCSTR only accepts a single constant string as an argument.]])return toEncrypt
     end LPH_STRENC = LPH_ENCSTR
    LPH_ENCFUNC = function(toEncrypt, encKey, decKey, ...)
        assert(type(toEncrypt) == 'function' and type(encKey) == 'string' and #{
            ...
        } == 0, [[LPH_ENCFUNC accepts a constant function, constant string, and string variable as arguments.]])return toEncrypt
     end LPH_FUNCENC = LPH_ENCFUNC
    LPH_JIT = function(f, ...)
        assert(type(f) == 'function' and #{
            ...
        } == 0, [[LPH_JIT only accepts a single constant function as an argument.]])return f
     end LPH_JIT_MAX = LPH_JIT
    LPH_NO_VIRTUALIZE = function(f, ...)
        assert(type(f) == 'function' and #{
            ...
        } == 0, [[LPH_NO_VIRTUALIZE only accepts a single constant function as an argument.]])return f
     end LPH_NO_UPVALUES = function(f, ...)
        assert(type(setfenv) == 'function', [[LPH_NO_UPVALUES can only be used on Lua versions with getfenv & setfenv]])assert(type(f) == 'function' and #{
            ...
        } == 0, [[LPH_NO_UPVALUES only accepts a single constant function as an argument.]])return f
     end LPH_CRASH = function(...)
        warn('LPH_CRASH INVOKED')assert(#{
            ...
        } == 0, 'LPH_CRASH does not accept any arguments.')
    end getgenv().Key = 'KG-9964dacb-1a4b-42c5-b4a5-7308b8fc2150'
 end
local type = type local typeof = typeof
local pairs = pairs
local ipairs = ipairs
local table = table
local next = next
local string = string
local math = math
local math_max = math.max
local math_min = math.min
local math_sin = math.sin
local math_floor = math.floor
local os = os
local coroutine = coroutine
local coroutine_create = coroutine.create
local coroutine_resume = coroutine.resume
local coroutine_yield = coroutine.yield
local _coroutine_close = coroutine.close
local task = task
local task_wait = task.wait
local task_spawn = task.spawn
local task_defer = task.defer
local Storage = {
    Originals = {
    },
    OldHipHeight = 0,
    RayCastGuides = {
    },
    Panic = false,
    MoveDirection = Vector3.zero,
    ItemAuraConnections = {
    },
    MovementSpoof = false,
    SupressNotifications = false,
    Gun_Attributes = {
        {
            Name = 'Disable Scopes',
            Attribute = 'SniperScope',
            Type = 'function',
            Function = function(Value:boolean,
                Self:Instance,
                Attribute:string)
                if game.HasTag(Self,
                'Gun') and Attribute == 'SniperScope' then
                     return true,
                    not Value
                 end
                return false,
                nil
             end
        },
        {
            Name = 'Recoil',
            Type = 'number',
            Max = 5,
            Min = 0,
            Default = 0.1
        },
        {
            Name = 'Zoom',
            Type = 'number',
            Max = 5,
            Min = 0,
            Default = 1
        }
    },
    Vehicle_Attributes = {
        {
            Name = 'acceleration',
            Type = 'number',
            Min = 5,
            Max = 100,
            DisplayName = 'Acceleration'
        },
        {
            Name = 'slipThreshold',
            Type = 'number',
            Min = 10,
            Max = 100,
            DisplayName = 'Slip Threshold'
        },
        {
            Name = 'staticFriction',
            Type = 'number',
            Min = 1,
            Max = 10,
            DisplayName = 'Static Friction'
        }
    },
    Blacklisted_Network_Calls = {
        ['replicate_billboard_gui'] = true,
        ['replicate_stamina_bar'] = true,
        ['invalid_entry'] = true
    },
    Teleport_Positions = {
        ['Bike Shop'] = Vector3.new(256,
        261,
        - 206),
        ['Burger Place'] = Vector3.new(113,
        260,
        - 212),
        ['Gun Shop'] = Vector3.new( - 140,
        259,
        - 221),
        ['House'] = Vector3.new(124,
        261,
        - 393),
        ['Hospital'] = Vector3.new( - 133,
        261,
        - 555),
        ['Dealer'] = Vector3.new( - 222,
        255,
        388),
        ['Car Dealership'] = Vector3.new(118,
        260,
        431),
        ['Gas Station'] = Vector3.new(125,
        258,
        137),
        ['Pawn Shop'] = Vector3.new(1177,
        258,
        - 535),
        ['Spin Club'] = Vector3.new(1253,
        260,
        - 418)
    },
    Anti_Aim_Animation = nil,
    LastHackedATM = os.clock(),
    Initialized = false,
    CharacterConnections = {
    },
    UpdateGunStatsCallback = Instance.new('BindableEvent'),
    UpdateMeleeStatsCallback = Instance.new('BindableEvent'),
    GunModReferences = {
        ['accuracy'] = 'GunMods_S_Accuracy',
        ['automatic'] = 'GunMods_S_Automatic',
        ['fire_rate'] = 'GunMods_S_FireRate'
    },
    MeleeModReferences = {
        ['cone_angle'] = 'MeleeMods_S_ConeAngle',
        ['range'] = 'MeleeMods_S_Range',
        ['speed'] = 'MeleeMods_S_Speed'
    },
    FlyJumpConnection = nil,
    ServerStaminaGui = game:GetService('Players').LocalPlayer:WaitForChild('PlayerGui'):WaitForChild('TopRightHud'):WaitForChild('Holder'):WaitForChild('StaminaBar'):Clone(),
    LastKilledBy = nil,
    Connections = {
    },
    Routines = {
    },
    RarityColors = {
        ['Common'] = Color3.fromRGB(255,
        255,
        255),
        ['Uncommon'] = Color3.fromRGB(99,
        255,
        52),
        ['Rare'] = Color3.fromRGB(51,
        170,
        255),
        ['Epic'] = Color3.fromRGB(237,
        44,
        255),
        ['Legendary'] = Color3.fromRGB(255,
        150,
        0),
        ['Omega'] = Color3.fromRGB(255,
        20,
        51)
    }
}
getgenv().BS_Storage = Storage
local CurrentDate = os.date('*t')local ExpirationDate = {
    year = 2026,
    month = 2,
    day = 15
}
local ExpirationTime = os.time(ExpirationDate)local CurrentTime = os.time(CurrentDate)local Executor = identifyexecutor()Storage.Connections.__counters = Storage.Connections.__counters or {
}
Storage.Routines.__counters = Storage.Routines.__counters or {
}
local function _nextKey(tbl:{
        [any]:any
    }, base:string)
    :string
    local counters = rawget(tbl, '__counters')local n = (counters[base] or 0) + 1
    local key = base
    if rawget(tbl, base) ~= nil then
         key = ("%s#%d"):format(base, n)
    end
    while rawget(tbl, key) ~= nil do
         n+=1
        key = ("%s#%d"):format(base, n)
    end counters[base] = n
    return key
 end Storage.Routines[_nextKey(Storage.Routines, 'ClockIntegrityCheck')] = task_spawn(function()
    local StartTime = os.clock()task_wait(10)local EndTime = os.clock()if EndTime - StartTime < 5 then
         LPH_CRASH()
    end
 end)local InitializedSignal = Instance.new('BindableEvent')local START_TIME = os.clock()local TELEPORT_SPEED_VEHICLE = 60
local TELEPORT_SPEED = 32
local PANIC_HEIGHT_THRESHOLD = 266
local PANIC_CONST_OFY = 255
local PANIC_DURATION = 25
local AUTO_HOP_INTERVAL = 60 * 5
local TELEPORT_SPEEDUP_TIME = 1
local TP_HEIGHT_OFFSET = 3
local SUPPORTED_VERSIONS = {
    '1.3.30',
    '1.3.31',
    '1.3.32',
    '1.3.33',
    '1.3.34',
    '1.3.35',
    '1.3.36',
    '1.3.37',
    '1.3.38',
    '1.3.40',
    '1.3.41'
}
local Translator = __DARKLUA_BUNDLE_MODULES.load('e')local T = Translator.translate
local Version = '8.6.0'
local SubVersion = (not false) and 'Release [Paid]' or 'Release [Free]'
local ORCHESTRATOR_MENU_ENABLED = false shared.HOOKING_ENABLED = true type MarkerObject = {
    Object:Part,
    Destroy:(self:MarkerObject)->(),
    SetColor:(self:MarkerObject,
    Color:Color3)->(),
    SetPosition:(self:MarkerObject,
    Position:Vector3)->()
}
type State < T > = {
    set:(self:State < T > ,
    value:T)->(),
    get:()->T,
    hook:((self:State < T > ,
    newValue:T)->())?
}
type ATM_ClassState = {
    fake_hacker_state_1:State < any > ,
    fake_disabled_state_1:State < boolean > ,
    fake_hack_tool_1:State < string > ,
    start_hack:State < number > ,
    disabled:State < boolean > ,
    hacker:State < any > ,
    active_hack_tool:State < string > ,
    fake_hacker_state_2:State < Instance > ,
    fake_disabled_state_2:State < boolean > ,
    fake_hack_tool_2:State < string >
 }
type ATM_ClassObject = {
    instance:Model,
    states:ATM_ClassState
}
if not rconsoleprint then
     rconsoleprint = function(...)
    end
 end
if not rconsolewarn then
     rconsolewarn = function(...)
    end
 end
if not rconsoledestroy then
     rconsoledestroy = function(...)
    end
 end
local function G_Toggle(ToggleName:string)
    :boolean
    if not getgenv().Library then
         repeat
             wait()
        until getgenv().Library
     end
    if not getgenv().Library.Toggles then
         repeat
             wait()
        until getgenv().Library.Toggles
     end
    if not getgenv().Library.Toggles[ToggleName]then
         return false
     end
    return getgenv().Library.Toggles[ToggleName].Value
 end
local function G_Option(OptionName:string)
    :any
    if not getgenv().Library then
         repeat
             wait()
        until getgenv().Library
     end
    if not getgenv().Library.Options then
         repeat
             wait()
        until getgenv().Library.Options
     end
    if not getgenv().Library.Options[OptionName]then
         repeat
             wait()
        until getgenv().Library.Options[OptionName]
    end
    return getgenv().Library.Options[OptionName].Value
 end
local function G_Option_NYield(OptionName:string)
    :any
    return getgenv().Library.Options[OptionName].Value
 end
local function G_Toggle_NYield(ToggleName:string)
    :any
    return getgenv().Library.Toggles[ToggleName].Value
 end
local function UpdateStatus(Text)
    local statusLabel = rawget(shared, 'StatusText')if statusLabel and statusLabel.Parent then
         statusLabel.Text = Text
     end task_wait(0.05)
end
local function SafeRequire(...)
    local OldThreadContext = getthreadcontext()setthreadcontext(2)local Result = require(...)setthreadcontext(OldThreadContext)return Result
 end
local function GetBoundingBox(model, orientation)
    :(CFrame, Vector3)if typeof(model) == 'Instance' then
         model = model:GetDescendants()
    end
    if not orientation then
         orientation = CFrame.new()
    end
    local abs = math.abs
    local inf = math.huge
    local minx, miny, minz = inf, inf, inf
    local maxx, maxy, maxz = - inf, - inf, - inf
    for _, obj in pairs(model)do
         if obj:IsA('BasePart')then
             local cf = obj.CFrame
            cf = orientation:toObjectSpace(cf)local size = obj.Size
            local sx, sy, sz = size.X, size.Y, size.Z
            local x, y, z, R00, R01, R02, R10, R11, R12, R20, R21, R22 = cf:components()local wsx = 0.5 * (abs(R00) * sx + abs(R01) * sy + abs(R02) * sz)local wsy = 0.5 * (abs(R10) * sx + abs(R11) * sy + abs(R12) * sz)local wsz = 0.5 * (abs(R20) * sx + abs(R21) * sy + abs(R22) * sz)if minx > x - wsx then
                 minx = x - wsx
             end
            if miny > y - wsy then
                 miny = y - wsy
             end
            if minz > z - wsz then
                 minz = z - wsz
             end
            if maxx < x + wsx then
                 maxx = x + wsx
             end
            if maxy < y + wsy then
                 maxy = y + wsy
             end
            if maxz < z + wsz then
                 maxz = z + wsz
             end
         end
     end
    local omin, omax = Vector3.new(minx, miny, minz), Vector3.new(maxx, maxy, maxz)local omiddle = (omax + omin) / 2
    local wCf = orientation - orientation.p + orientation:pointToWorldSpace(omiddle)local size = (omax - omin)return wCf, size
 end
local function dbgprint(...)
    if not LPH_OBFUSCATED then
         print('[DEBUGGING]', ...)
    end
 end
local function dbgwarn(...)
end
local function __Stub(a:never)
    return warn('Stub function called with argument:', a)
end
local function flen(Table)
    :number
    local Count = 0
    for _ in next, Table do
         Count+=1
     end
    return Count
 end
local Players = game:GetService('Players')local ReplicatedStorage = game:GetService('ReplicatedStorage')local VirtualUser = game:GetService('VirtualUser')local RunService = game:GetService('RunService')local ProximityPromptService = game:GetService('ProximityPromptService')local CollectionService = game:GetService('CollectionService')local CoreGui = game:GetService('CoreGui')local TweenService = game:GetService('TweenService')local Debris = game:GetService('Debris')local HttpService = game:GetService('HttpService')local Lighting = game:GetService('Lighting')local LocalPlayer = Players.LocalPlayer
local UserInputService = game:GetService('UserInputService')local Modules = ReplicatedStorage:WaitForChild('Modules')local Core = Modules:WaitForChild('Core')local GameModules = Modules:WaitForChild('Game')local Net = SafeRequire(Core:WaitForChild('Net') :: ModuleScript)local LocalUserId = LocalPlayer.UserId
local Camera = workspace.CurrentCamera
local MovementEvent = Instance.new('BindableEvent')local CharacterCreatorItems = ReplicatedStorage:WaitForChild('ReplicatedCharacterCreatorItems')local TeleportService = game:GetService('TeleportService')local TextChatService = game:GetService('TextChatService')local function ClearStatusOverlay()
    pcall(RunService.UnbindFromRenderStep, RunService, 'Overlay')local overlay = rawget(shared, 'DarkOverlay')if overlay and overlay.Destroy then
         overlay:Destroy()
    end shared.DarkOverlay = nil shared.StatusText = nil shared.OverlayImage = nil
 end
if not getgenv().SkipBypassCheck2044 and not(hookfunction and hookmetamethod and isexecutorclosure and getgc and debug and restorefunction)then
     shared.HOOKING_ENABLED = false warn([[Hooking is disabled due to the executor environment not supporting it.]])
end UpdateStatus(T('Initializing libraries...'))UpdateStatus('Loading modules...')UpdateStatus(T('Loading modules/esp'))local ESP_Library = __DARKLUA_BUNDLE_MODULES.load('f')UpdateStatus(T('Loading modules/aiminglib'))local Aiming_Library = __DARKLUA_BUNDLE_MODULES.load('g')UpdateStatus(T('Loading modules/inventorylib'))local Inventory = __DARKLUA_BUNDLE_MODULES.load('h')UpdateStatus(T('Loading modules/itemviewlib'))local ItemView = __DARKLUA_BUNDLE_MODULES.load('i')UpdateStatus(T('Loading modules/pathmodule'))local PathLib = __DARKLUA_BUNDLE_MODULES.load('j')UpdateStatus(T('Loading modules/class_interface'))local Class_Interface = __DARKLUA_BUNDLE_MODULES.load('k')UpdateStatus(T('Loading modules/teleportdata'))local TeleportData = __DARKLUA_BUNDLE_MODULES.load('l')UpdateStatus(T('Loading modules/identifier'))local Identifier = __DARKLUA_BUNDLE_MODULES.load('m')UpdateStatus(T('Loading modules/freecamera'))local ToggleFreeCamera = __DARKLUA_BUNDLE_MODULES.load('n')UpdateStatus(T('Loading modules/Prediction'))local Prediction = __DARKLUA_BUNDLE_MODULES.load('o')UpdateStatus(T('Loading modules/gizmo'))local Gizmo = __DARKLUA_BUNDLE_MODULES.load('J')UpdateStatus(T('Loading modules/secure_call'))local secure_call = __DARKLUA_BUNDLE_MODULES.load('K')UpdateStatus(T('Loading modules/Cleaner'))local Cleaner = __DARKLUA_BUNDLE_MODULES.load('L')UpdateStatus(T('Loading modules/HookMgr'))local HookMgr = __DARKLUA_BUNDLE_MODULES.load('M')UpdateStatus(T('Loading modules/SecureNet'))local SecureNet = __DARKLUA_BUNDLE_MODULES.load('O')(Storage, SafeRequire, Core, UpdateStatus, T)UpdateStatus(T('Loading modules/Utils'))local Utils = __DARKLUA_BUNDLE_MODULES.load('P')(Storage, SafeRequire, Core, UpdateStatus, T)UpdateStatus(T('Loading modules/ConnectionProxyManager'))local ConnectionProxyMgr = __DARKLUA_BUNDLE_MODULES.load('Q')UpdateStatus(T('Loading modules/ArgumentCheck'))local ArgumentChecks = __DARKLUA_BUNDLE_MODULES.load('N').Results
UpdateStatus(T('Loading user interface...'))local Repository = [[https://raw.githubusercontent.com/deividcomsono/Obsidian/738b589406cec1e47161e81243b5ff265c099048/]]
local Library = loadstring(SecureRequest:HttpGet(Repository .. 'Library.lua'))()local ThemeManager = loadstring(SecureRequest:HttpGet(Repository .. 'addons/ThemeManager.lua'))()local SaveManager = loadstring(SecureRequest:HttpGet(Repository .. 'addons/SaveManager.lua'))()local Repr:(any, {
    [string]:any
}?)->string = loadstring(SecureRequest:HttpGet([[https://raw.githubusercontent.com/Ozzypig/repr/refs/heads/master/repr.lua]]))()local ErrorReporter = __DARKLUA_BUNDLE_MODULES.load('R')local ErrorHandler = __DARKLUA_BUNDLE_MODULES.load('S')pcall(function()
    local Exec, ExVersion = identifyexecutor()local ExecutorData = table.concat({
        Exec,
        ExVersion
    }, '')SecureRequest.request({
        Url = 'https://example.com/checkin',
        Method = 'POST',
        Headers = {
            ['Content-Type'] = 'application/json'
        },
        Body = game:GetService('HttpService'):JSONEncode({
            Version = Version,
            SubVersion = SubVersion,
            Executor = ExecutorData,
            UserID = LocalPlayer.UserId
        })
    })
LocalPlayer.PlayerGui.TeleportingGui.Enabled = false
 end)local function RunMain()
    if not replaceclosure then
         replaceclosure = hookfunction
     end
    if not getallthreads then
         function getallthreads()
            local threads = {
            }
            for _, item in getreg()do
                 if type(item) == 'thread' then
                     table.insert(threads, item)
                end
             end
            return threads
         end
     end
    if not setthreadcontext then
         setthreadcontext = setthreadidentity
     end
    local function SafeNotify(...)
        local Args = {
            ...
        }
        coroutine.wrap(function()
            setthreadcontext(8)Library:Notify(unpack(Args))
        end)()
    end
    local GameRegistry = {
        consume_stamina = {
        }
    }
    Storage.ServerStaminaGui.Parent = LocalPlayer.PlayerGui.TopRightHud.Holder
    Storage.ServerStaminaGui.Name = 'ServerStaminaGui'
    for _, v in next, Storage.ServerStaminaGui.Fill:GetChildren()do
         if v:IsA('UIGradient')then
             v.Enabled = false
         end
     end Storage.ServerStaminaGui.Fill.BackgroundColor3 = Color3.new(1, 0.505882, 0.039216)Storage.ServerStaminaGui.Visible = true
    if shared.HOOKING_ENABLED then
         print('Scanning enviroment...')for _, v in next, getgc(true)do
             if typeof(v) == 'table' then
                 pcall(function()
                    if rawget(v, 'consume_stamina')then
                         local value = rawget(v, 'consume_stamina')if typeof(value) == 'function' and islclosure(value) and (not isefunction(value))then
                             print('Found stamina hook table:', v)table.insert(GameRegistry.consume_stamina, value)
                        end
                     end
                 end)
            end
         end
     else
         warn('Skipping enviroment scanning due to hooking being disabled.')
    end xpcall(function()
        SafeRequire(ReplicatedStorage:WaitForChild('Utility') :: ModuleScript)
    end, function(err)
        local PromptMessage = [[Your executor does not support require. Please try a better one...]]
        messagebox(PromptMessage, 'Execution Error', 0)local TraceInformation = tostring(err or 'Unknown error')if type(debug) == 'table' and type(debug.traceback) == 'function' then
             local success, generatedTrace = pcall(function()
                return debug.traceback(err, 2)
            end)if success and generatedTrace and generatedTrace ~= '' then
                 TraceInformation = generatedTrace
             end
         end pcall(ErrorReporter.ReportPopup, {
            code = 'EXECUTOR_REQUIRE',
            message = PromptMessage,
            recoverable = false,
            traceback = TraceInformation,
            source = 'main.luau::SafeRequire',
            title = 'Executor Compatibility Error'
        })
coroutine_yield()
    end)local MessageShown = false or isfile('NoticeShown')if not MessageShown then
         local Root, Button1, Button2 = ErrorHandler.InteractiveToast(T('Important notice'), T([[Important notice: If you have bought this script from an unauthorized reseller or website,]] .. [[

please be aware that you are at a high risk of the key you are using being disabled at any time.
]] .. [[By continuing, you affirm that you have purchased this script from an official source.
More information @ https://discord.gg/6qCymXqa2u]]), T('Proceed'), '')local Pressed = false Button1.Activated:Once(function()
            Pressed = true Root:Destroy()do
                 writefile('NoticeShown', '')
            end
         end)Button2:Destroy()Button1.BackgroundColor3 = Color3.new(0.533333, 0.533333, 0.533333)Root.Parent = CoreGui
        Root.Enabled = true
        repeat
             task_wait(0.1)
        until Pressed
     end
    local Melee = SafeRequire(GameModules.ItemTypes:WaitForChild('Melee') :: ModuleScript)local Crate = SafeRequire(GameModules.CrateSystem.Crate :: ModuleScript)local Sprint = SafeRequire(GameModules.Sprint :: ModuleScript)local SteakHouseModule = SafeRequire(GameModules.Jobs.SteakhouseCook :: ModuleScript)local Char = SafeRequire(Core.Char :: ModuleScript)local ATM_Module = SafeRequire(GameModules.ATM.ATM :: ModuleScript)local Data_Module = SafeRequire(Core.Data :: ModuleScript)local Item_Utils = SafeRequire(GameModules.Inventory.ItemUtils :: ModuleScript)local VehicleModule = SafeRequire(GameModules.VehicleSystem.Vehicle :: ModuleScript)local UIModule = SafeRequire(Core.UI :: ModuleScript)local SkillsList = SafeRequire(GameModules.Skills.SkillsList :: ModuleScript)local NotificationsUI = SafeRequire(GameModules.UI.NotificationsUI :: ModuleScript)local Map = workspace:WaitForChild('Map')local Vehicles = workspace:WaitForChild('Vehicles')local Atmosphere = Lighting:WaitForChild('Atmosphere')Aiming_Library.Enabled = true Aiming_Library.FOV = 60
    Aiming_Library.Players = true
    local function FetchVehicleCandidates()
        :{
            string
        }
        local Candidates = {
        }
        local VehiclesSource = Utils.InsertMergeTables(ReplicatedStorage.Items.bike:GetChildren(), ReplicatedStorage.Items.car:GetChildren())for _, Vehicle in pairs(VehiclesSource)do
             if Vehicle:IsA('Model') and Vehicle:FindFirstChild('Motors')then
                 local Motors = Vehicle.Motors
                local Speed = Motors:GetAttribute('forwardMaxSpeed')if typeof(Speed) == 'number' then
                     local inserted = false
                    for i = 1, #Candidates do
                         if Speed > Candidates[i].Motors:GetAttribute('forwardMaxSpeed')then
                             table.insert(Candidates, i, Vehicle)inserted = true break
                         end
                     end
                    if not inserted then
                         table.insert(Candidates, Vehicle)
                    end
                 else
                     warn(([[Vehicle '%s' is missing a valid 'forwardMaxSpeed' attribute. Skipping.]]):format(Vehicle.Name))
                end
             end
         end
        local VehicleNames = {
        }
        for _, Vehicle in ipairs(Candidates)do
             table.insert(VehicleNames, Vehicle.Name)
        end
        return VehicleNames
     end
    local VehicleCandidates = FetchVehicleCandidates()local function WaitForPing()
        local NetworkPing = LocalPlayer:GetNetworkPing()return task_wait(math_max(0.2, NetworkPing * 2))
    end
    local function Sit(VehicleSeat:VehicleSeat, NYield:boolean?)
        local Vehicle = VehicleSeat.Parent :: BasePart
        local Prompt = Vehicle.Chassis.DrivePromptAttachment.DrivePrompt
        local Character = LocalPlayer.Character
        local Origin = Character:GetPivot()fireproximityprompt(Prompt, 0.5)if not NYield then
             task_wait(0.5)if not Character.Humanoid.SeatPart then
                 SafeNotify(T('Attempting to gain network ownership of vehicle seat...'))local AttemptNetworkOwnershipStart = os.clock()while os.clock() - AttemptNetworkOwnershipStart < 0.3 and Character.Humanoid.SeatPart == nil do
                     RunService.Heartbeat:Wait()Utils.TP(VehicleSeat:GetPivot())VehicleSeat.AssemblyLinearVelocity = Vector3.yAxis * math.random() * 10
                 end Utils.TP(Origin)Vehicle:PivotTo(Origin)VehicleSeat.AssemblyLinearVelocity = Vector3.zero
                for _, BasePart in next, Character:GetDescendants()do
                     if BasePart:IsA('BasePart')then
                         BasePart.AssemblyLinearVelocity = Vector3.zero
                        BasePart.AssemblyAngularVelocity = Vector3.zero
                     end
                 end fireproximityprompt(Prompt)task_wait(0.5)
            end
            if Character.Humanoid.SeatPart == nil then
                 SafeNotify(T('Failed to sit in vehicle seat.'))return
             else
                 SafeNotify(T('Successfully sat in vehicle seat.'))
            end
         else
             Character:PivotTo(Vehicle:GetPivot())
        end
     end
    local function AssertArgument(ArgumentName:string)
        :boolean
        local Data = ArgumentChecks[ArgumentName]if not Data then
             warn('Argument check for', ArgumentName, 'not found.')return false
         end
        return Data.Found
     end
    for _, Function in next, GameRegistry.consume_stamina do
         local Sprint_Bar = debug.getupvalue(Function, 2).sprint_bar
        if Sprint_Bar then
             print('Stamina hooks ready! [2/2]', Sprint_Bar)
        end print('Registering infinite stamina hook [' .. tostring(Sprint_Bar.update) .. ']')HookMgr.RegisterHook('inf_stamina' .. tostring(Sprint_Bar.update), Sprint_Bar.update, function(Old, ...)
            if G_Toggle('InfiniteStamina')then
                 return Old(function()
                    return 1
                 end)
            else
                 return Old(...)
            end
         end)
    end
    local CharacterAdded = LPH_JIT_MAX(function(Character:Model)
        Storage.Panic = false
        for _, Connection in next, Storage.CharacterConnections do
             Cleaner.CleanOne(Connection)
        end Storage.CharacterConnections = {
        }
        local BodyMoverConnection = ConnectionProxyMgr:YieldForConnection(Character.DescendantAdded, 'PlayerWellbeing', 1)print('BodyMoverConnection Found @', BodyMoverConnection)if BodyMoverConnection then
             ConnectionProxyMgr:Register(BodyMoverConnection):Disable()
        end do
             local name = _nextKey(Storage.Routines, 'CharacterBillboardScan')Storage.Routines[name] = task_defer(function()
                local HumanoidRootPart = Character:WaitForChild('HumanoidRootPart') :: Part
                local Name = HumanoidRootPart:WaitForChild('CharacterBillboardGui'):WaitForChild('PlayerName') :: TextLabel
                local TextChangedConnection = ConnectionProxyMgr:YieldForConnection(Name:GetPropertyChangedSignal('Text'), 'CharacterBillboardGui', 2)if TextChangedConnection then
                     dbgprint('Found Name Text connection:', TextChangedConnection)ConnectionProxyMgr:Register(TextChangedConnection):Disable()
                end
             end)
        end
        local UpperTorso = Character:WaitForChild('UpperTorso') :: Part
        local __conn_SteppedNoclip = Cleaner(RunService.Stepped:Connect(function()
            if G_Toggle('Noclip')then
                 for _, Descendant in next, Character:GetDescendants()do
                     if Descendant:IsA('BasePart')then
                         Descendant.CanCollide = false
                     end
                 end
             elseif  G_Toggle('Invisibility')then
                 for _, Descendant in next, Character:GetDescendants()do
                     if Descendant:IsA('BasePart') and Descendant.Name ~= 'HumanoidRootPart' then
                         Descendant.CanCollide = false
                     end
                 end
             else
                 UpperTorso.CanCollide = true
             end
         end))Storage.Connections[_nextKey(Storage.Connections, 'Character_Stepped_Noclip')] = __conn_SteppedNoclip
        table.insert(Storage.CharacterConnections, __conn_SteppedNoclip)local Humanoid = Character:WaitForChild('Humanoid') :: Humanoid
        local __conn_IsDeadOnce = Cleaner(Humanoid:GetAttributeChangedSignal('IsDead'):Once(function()
            if ArgumentChecks.Respawn.Found and G_Toggle('AutoRespawn')then
                 for i = 1, 60 do
                     task_wait(0.1)SecureNet.Send(ArgumentChecks.Respawn.Value)
                end
             end
         end))Storage.Connections[_nextKey(Storage.Connections, 'Humanoid_IsDead_Once')] = __conn_IsDeadOnce
        table.insert(Storage.CharacterConnections, __conn_IsDeadOnce)local __conn_KilledByChanged = Cleaner(Humanoid:GetAttributeChangedSignal('KilledBy'):Connect(function()
            local Attribute = Humanoid:GetAttribute('KilledBy')if Attribute then
                 Storage.LastKilledBy = Attribute
             end
         end))Storage.Connections[_nextKey(Storage.Connections, 'Humanoid_KilledBy_Changed')] = __conn_KilledByChanged
        table.insert(Storage.CharacterConnections, __conn_KilledByChanged)local __conn_IsRagdollingChanged = Cleaner(Character:GetAttributeChangedSignal('IsRagdolling'):Connect(function()
            if Character:GetAttribute('IsRagdolling') and G_Toggle('Anti-Ragdoll')then
                 for i = 1, 5 do
                     task_wait()SecureNet.Send(ArgumentChecks.End_Ragdoll_Early.Value)
                end
             end
         end))Storage.Connections[_nextKey(Storage.Connections, 'Character_IsRagdolling_Changed')] = __conn_IsRagdollingChanged
        table.insert(Storage.CharacterConnections, __conn_IsRagdollingChanged)for _, Descendant in next, Character:GetDescendants()do
             if Descendant:IsA('BasePart')then
                 for _, Connection in next, getconnections(Descendant:GetPropertyChangedSignal('CanCollide'))do
                     if Connection.Function then
                         dbgprint('Found CanCollide connection on', Descendant:GetFullName(), ':', Connection.Function)Connection:Disable()
                    end
                 end
             end
         end
     end)local AssertCharacter = LPH_NO_VIRTUALIZE(function()
        :Model
        if LocalPlayer.Character then
             return LocalPlayer.Character
         else
             repeat
                 task.wait()
            until LocalPlayer.Character
            return LocalPlayer.Character
         end
     end)local function WaitForTable(Root:Instance, InstancePath:{
            string
        }, Timeout:number?)
        local Instance = Root
        for i, v in pairs(InstancePath)do
             Instance = Instance:WaitForChild(v, Timeout)
        end
        return Instance
     end
    local GetVehicle = LPH_JIT_MAX(function()
        :{
            Vehicle:Model?,
            Name:string?
        }?local Character = AssertCharacter()local Humanoid = Character:FindFirstChildOfClass('Humanoid') :: Humanoid
        local VehicleSeat = Humanoid.SeatPart
        if VehicleSeat and VehicleSeat.ClassName == 'VehicleSeat' then
             local Vehicle = VehicleSeat.Parent :: Model
            local VehicleName = Vehicle.Name
            return {
                Vehicle = Vehicle,
                Name = VehicleName
            }
        end
        return nil
     end)local FindVehicle = LPH_JIT_MAX(function()
        :{
            Vehicle:Model?,
            Name:string?
        }?for _, Vehicle in next, Vehicles:GetChildren()do
             if Vehicle:GetAttribute('OwnerUserId') == LocalUserId then
                 return {
                    Vehicle = Vehicle,
                    Name = Vehicle.Name
                }
            end
         end
        return nil
     end)local GetUniformSamplesInSphere = LPH_JIT_MAX(function(centerPosition, radius, numberOfSamples)
        :{
            Vector3
        }
        local RNG = Random.new(tick())if typeof(centerPosition) ~= 'Vector3' then
             warn([[GetUniformSamplesInSphere: centerPosition must be a Vector3. Got:]], typeof(centerPosition))return {
            }
        end
        if typeof(radius) ~= 'number' or radius < 0 then
             warn([[GetUniformSamplesInSphere: radius must be a non-negative number. Got:]], radius)return {
            }
        end
        if typeof(numberOfSamples) ~= 'number' or numberOfSamples < 0 or numberOfSamples % 1 ~= 0 then
             warn([[GetUniformSamplesInSphere: numberOfSamples must be a non-negative integer. Got:]], numberOfSamples)return {
            }
        end
        if radius == 0 and numberOfSamples > 0 then
             local samples = {
            }
            for _ = 1, numberOfSamples do
                 table.insert(samples, centerPosition)
            end
            return samples
         end
        local samples = {
        }
        for _ = 1, numberOfSamples do
             local theta = RNG:NextNumber() * 2 * math.pi
            local cosPhi = (RNG:NextNumber() * 2) - 1
            local phi = math.acos(cosPhi)local sinPhi = math_sin(phi)local u = RNG:NextNumber()local r_sample = radius * (u ^ (1 / 3))local x = r_sample * sinPhi * math.cos(theta)local y = r_sample * sinPhi * math_sin(theta)local z = r_sample * cosPhi
            table.insert(samples, centerPosition + Vector3.new(x, y, z))
        end
        return samples
     end)local function VisualizeRay(Origin, Target)
        local RayBind = 'VisRayBind' .. HttpService:GenerateGUID(false)local RayData = {
            Hit = false
        }
        RunService:BindToRenderStep(RayBind, 500, function()
            Gizmo.PushProperty('Color3', RayData.Hit and Color3.new(0.082353, 1, 0) or Color3.new(1, 0, 0))Gizmo.Line:Draw(CFrame.lookAt((Origin + Target) / 2, Target), (Origin - Target).Magnitude)
        end)task.delay(LPH_OBFUSCATED and 5 or 60, function()
            RunService:UnbindFromRenderStep(RayBind)
        end)return RayData
     end
    local GetPredictedWithGun = LPH_JIT_MAX(function(Part:BasePart, _)
        assert(Part.Parent)local PredictedPos = Prediction:GetPredictedPosition(Part)if(not LPH_OBFUSCATED) or G_Toggle('VisualizeHitReg')then
             local PingSeconds = LocalPlayer:GetNetworkPing()local ServerTransform = nil task.delay(PingSeconds * 2, function()
                ServerTransform = Part.CFrame
             end)local Bind = 'GizmoRay' .. tostring(tick())local Pos, VelPos = Part.Position, (Part.Position + (Part.AssemblyLinearVelocity * PingSeconds))local Size, Transform = Part.Size, Part.CFrame
            RunService:BindToRenderStep(Bind, 500, function()
                Gizmo.PushProperty('Color3', Color3.new(1, 0.984314, 0))Gizmo.Box:Draw(CFrame.new(PredictedPos) * Transform.Rotation, Size, true)Gizmo.PushProperty('Color3', Color3.new(1, 0, 0))Gizmo.Box:Draw(Transform, Size, true)Gizmo.Arrow:Draw(Pos, VelPos, 0.2, (Pos - VelPos).Magnitude, 12)if ServerTransform then
                     Gizmo.PushProperty('Color3', Color3.new(0.282353, 1, 0))Gizmo.Box:Draw(ServerTransform * Transform.Rotation, Size, true)
                end
             end)task.delay(LPH_OBFUSCATED and 5 or 60, function()
                RunService:UnbindFromRenderStep(Bind)
            end)
        end
        return PredictedPos
     end)local SecureLerpTeleport
    SecureLerpTeleport = LPH_JIT_MAX(function(Origin:CFrame, Target:CFrame, StudsPerSecond:number, Conditional:(()->boolean)?, IsRecursive:boolean?, LastDetectionType:string?)
        local MovementFlag = false
        local MovementFlagType = 'None'
        local YVelocity = 0
        local StartTime = os.clock()local VerticalBuffer = 0
        local Character = LocalPlayer.Character
        local RootPart = AssertCharacter():WaitForChild('HumanoidRootPart')local Params = RaycastParams.new()Params.FilterType = Enum.RaycastFilterType.Exclude
        Params.FilterDescendantsInstances = {
            Character,
            Vehicles,
            Map:WaitForChild('BoundaryWalls'),
            Map.Vegetation.Trees,
            Map.Props.PowerLines,
            Map.Props.PrestigeMotorsLargeSign,
            Map.RoadNetwork.TrafficLights
        }
        for _, v in next, Map.Props:GetChildren()do
             if v.Name ~= 'NewProps' and (not v.Name:match('FuseBox'))then
                 Params:AddToFilter(v)
            end
         end Params.RespectCanCollide = true
        local TreeParams = RaycastParams.new()TreeParams.FilterType = Enum.RaycastFilterType.Include
        TreeParams.FilterDescendantsInstances = {
            Map.Vegetation.Trees,
            Map.RoadNetwork.TrafficLights
        }
        local Abort, Conditional_Abort = false, false
        if not Conditional then
             Conditional = function()
                return true
             end
         end assert(Conditional)local TotalDistance = (Origin.Position - Target.Position).Magnitude
        if TotalDistance < 0.01 then
             return {
                Status = 'Success'
            }
        end
        local TotalDuration = TotalDistance / StudsPerSecond
        if G_Toggle('AvoidWaitingAtATMs') and os.clock() - Storage.LastHackedATM + TotalDuration < 5 then
             TotalDuration+=5 - (os.clock() - Storage.LastHackedATM + TotalDuration)
        end
        local AlphaCalculator
        if G_Toggle('SpeedRamp') and IsRecursive then
             local VMax, DTotal, RampDuration, DRampHypothetical = StudsPerSecond, TotalDistance, 1, (StudsPerSecond * 1) / 2
            if DTotal >= DRampHypothetical then
                 TotalDuration = RampDuration + (DTotal - DRampHypothetical) / VMax
                AlphaCalculator = function(ElapsedTime)
                    if ElapsedTime < RampDuration then
                         return ((VMax / RampDuration) * (ElapsedTime ^ 2 / 2)) / DTotal
                     end
                    return (DRampHypothetical + (ElapsedTime - RampDuration) * VMax) / DTotal
                 end
             else
                 TotalDuration = math.sqrt(2 * DTotal * RampDuration / VMax)AlphaCalculator = function(ElapsedTime)
                    return TotalDuration > 0 and (ElapsedTime / TotalDuration) ^ 2 or 1
                 end
             end
         else
             TotalDuration = TotalDistance / StudsPerSecond
            AlphaCalculator = function(ElapsedTime)
                return TotalDuration > 0 and ElapsedTime / TotalDuration or 1
             end
         end
        local function ShapecastDown(Position:Vector3)
            return workspace:Spherecast(Position + Vector3.yAxis * 100, 2, Vector3.yAxis * - 200, Params)
        end
        local function Shapecast(CFrameOrigin:Vector3, Target:Vector3)
            return workspace:Blockcast(CFrame.new(CFrameOrigin, Target), RootPart.Size, (Target - CFrameOrigin), Params)
        end
        local LastHeight, CurrentHeight = Origin.Position.Y + 10, Origin.Position.Y + 10
        SecureNet.Send(ArgumentChecks.Sprint.Value, true)local LastSprintCall = os.clock()local MovementCallConnection = MovementEvent.Event:Connect(function(Type:string)
            if Type == 'TP' or Type == 'Noclip' then
                 MovementFlag, MovementFlagType = true, Type
             end
         end)local CharacterParts = {
        }
        for _, part in ipairs(Character:GetDescendants())do
             if part:IsA('BasePart')then
                 table.insert(CharacterParts, part)
            end
         end
        local RenderConnection
        local VisualizationData = {
            ForwardBox = nil,
            BackwardBox = nil,
            CurrentArrow = nil,
            FutureArrow = nil,
            BehindArrow = nil
        }
        if not LPH_OBFUSCATED then
             RenderConnection = RunService.RenderStepped:Connect(function()
                if VisualizationData.ForwardBox then
                     Gizmo.PushProperty('Color3', Color3.new(0, 1, 0.866667))Gizmo.Box:Draw(VisualizationData.ForwardBox.CFrame, VisualizationData.ForwardBox.Size, true)
                end
                if VisualizationData.BackwardBox then
                     Gizmo.PushProperty('Color3', Color3.new(0.980392, 0.588235, 0))Gizmo.Box:Draw(VisualizationData.BackwardBox.CFrame, VisualizationData.BackwardBox.Size, true)
                end
                if VisualizationData.CurrentArrow then
                     Gizmo.PushProperty('Color3', Color3.new(0, 1, 0.05098))Gizmo.Arrow:Draw(VisualizationData.CurrentArrow.From, VisualizationData.CurrentArrow.To, 1, (VisualizationData.CurrentArrow.From - VisualizationData.CurrentArrow.To).Magnitude, 3)
                end
                if VisualizationData.FutureArrow then
                     Gizmo.PushProperty('Color3', Color3.new(0, 1, 0.984314))Gizmo.Arrow:Draw(VisualizationData.FutureArrow.From, VisualizationData.FutureArrow.To, 1, (VisualizationData.FutureArrow.From - VisualizationData.FutureArrow.To).Magnitude, 3)
                end
                if VisualizationData.BehindArrow then
                     Gizmo.PushProperty('Color3', Color3.new(1, 0.5, 0))Gizmo.Arrow:Draw(VisualizationData.BehindArrow.From, VisualizationData.BehindArrow.To, 1, (VisualizationData.BehindArrow.From - VisualizationData.BehindArrow.To).Magnitude, 3)
                end
             end)
        end
        while os.clock() - StartTime < TotalDuration do
             local DeltaTime = RunService.Heartbeat:Wait()local CurrentTime = os.clock()VerticalBuffer = math_max(0, VerticalBuffer - (2 * 20 * DeltaTime))if Abort or not Conditional()then
                 Conditional_Abort = true break
             end
            if Storage.Panic then
                 local WaitingForPanicTime = CurrentTime
                repeat
                     task_wait()
                until not Storage.Panic or os.clock() - WaitingForPanicTime > 15
                Storage.Panic = false SafeNotify(T('Panic mode timeout, disabling.'))
            end
            if MovementFlag then
                 if RenderConnection then
                     RenderConnection:Disconnect()
                end
                return SecureLerpTeleport(Character:GetPivot() + Vector3.new((math.random(0, 1) * 2 - 1) * 5, 0, (math.random(0, 1) * 2 - 1) * 5), Target, StudsPerSecond, Conditional, true, MovementFlagType)
            end
            local ElapsedTime = CurrentTime - StartTime
            local Alpha = math.clamp(AlphaCalculator(ElapsedTime), 0, 1)if CurrentTime - LastSprintCall > 0.5 then
                 SecureNet.Send(ArgumentChecks.Sprint.Value, true)LastSprintCall = CurrentTime
             end
            for _, Part in next, CharacterParts do
                 Part.AssemblyLinearVelocity = Vector3.zero
                Part.AssemblyAngularVelocity = Vector3.zero
             end
            local CurrentPosition = Origin.Position:Lerp(Target.Position, Alpha)if workspace:Raycast(Character:GetPivot().Position, (Target.Position - Origin.Position).Unit * 20, TreeParams)then
                 Origin+=Character:GetPivot().RightVector * 10
                CurrentPosition = Origin.Position:Lerp(Target.Position, Alpha)
            end
            local lookaheadTime, lookbehindTime = 0.2, 0.1
            local alphaOffsetForward = TotalDuration > 0 and lookaheadTime / TotalDuration or 0
            local alphaOffsetBackward = TotalDuration > 0 and lookbehindTime / TotalDuration or 0
            local CurrentRaycast = ShapecastDown(CurrentPosition)local groundY = CurrentRaycast and CurrentRaycast.Position.Y or (CurrentHeight - 2.5)if(not LPH_OBFUSCATED) and CurrentRaycast then
                 VisualizationData.currentArrow = {
                    from = CurrentPosition + Vector3.yAxis * 30,
                    to = CurrentRaycast.Position
                }
            end
            local FuturePoint = Origin.Position:Lerp(Target.Position, math.clamp(Alpha + alphaOffsetForward, 0, 1))local shapecastOrigin = CurrentPosition * Vector3.new(1, 0, 1) + Vector3.yAxis * (groundY + 3)local FutureRaycastHorizontal = Shapecast(shapecastOrigin, FuturePoint)if FutureRaycastHorizontal then
                 if not LPH_OBFUSCATED then
                     local dist = (FutureRaycastHorizontal.Position - shapecastOrigin).Magnitude
                    VisualizationData.forwardBox = {
                        cframe = CFrame.new(shapecastOrigin,
                        FutureRaycastHorizontal.Position),
                        size = RootPart.Size + Vector3.new(0,
                        0,
                        dist - 1)
                    }
                end FuturePoint = FutureRaycastHorizontal.Position
             else
                 if not LPH_OBFUSCATED then
                     VisualizationData.forwardBox = nil
                 end
             end
            local FutureRaycast = ShapecastDown(FuturePoint)if(not LPH_OBFUSCATED) and FutureRaycast then
                 VisualizationData.futureArrow = {
                    from = FuturePoint + Vector3.yAxis * 30,
                    to = FutureRaycast.Position
                }
            end
            local CurrentRaycastHeight = groundY
            local FutureRaycastHeight = (FutureRaycast and FutureRaycast.Position.Y) or CurrentRaycastHeight
            if FutureRaycastHeight > CurrentRaycastHeight + 5 then
                 VerticalBuffer = 10
             end CurrentHeight = math_max(CurrentRaycastHeight, FutureRaycastHeight) + TP_HEIGHT_OFFSET + VerticalBuffer
            if ElapsedTime < 0.5 then
                 CurrentHeight = MovementFlagType == 'Noclip' and math_max(285, CurrentHeight) or CurrentHeight + 5
             end
            if CurrentHeight < LastHeight then
                 local BackwardPoint = Origin.Position:Lerp(Target.Position, math.clamp(Alpha - alphaOffsetBackward, 0, 1))local BackwardRaycastHorizontal = Shapecast(shapecastOrigin, BackwardPoint)if BackwardRaycastHorizontal then
                     if not LPH_OBFUSCATED then
                         local dist = (BackwardRaycastHorizontal.Position - shapecastOrigin).Magnitude
                        VisualizationData.backwardBox = {
                            cframe = CFrame.new(shapecastOrigin,
                            BackwardRaycastHorizontal.Position),
                            size = RootPart.Size + Vector3.new(0,
                            0,
                            dist - 1)
                        }
                    end BackwardPoint = BackwardRaycastHorizontal.Position
                 else
                     if not LPH_OBFUSCATED then
                         VisualizationData.backwardBox = nil
                     end
                 end
                local BehindRaycast = ShapecastDown(BackwardPoint)if(not LPH_OBFUSCATED) and BehindRaycast then
                     VisualizationData.behindArrow = {
                        from = BackwardPoint + Vector3.yAxis * 30,
                        to = BehindRaycast.Position
                    }
                end
                if BehindRaycast and BehindRaycast.Position.Y > CurrentRaycastHeight + 2 then
                     CurrentHeight = LastHeight
                 else
                     YVelocity-=10 * DeltaTime
                    CurrentHeight = math_max(CurrentHeight, LastHeight + YVelocity)
                end
             else
                 YVelocity = 0
             end LastHeight = CurrentHeight
            local NewPosition = Vector3.new(CurrentPosition.X, CurrentHeight, CurrentPosition.Z)local NewCFrame = CFrame.lookAt(Origin.Position, NewPosition).Rotation + NewPosition
            local Vehicle = GetVehicle()if Vehicle and Vehicle.Vehicle then
                 Vehicle.Vehicle:PivotTo(NewCFrame * Vehicle.Vehicle:GetPivot():ToObjectSpace(Character:GetPivot()):Inverse())
            else
                 Character:PivotTo(NewCFrame)
            end
         end
        if not Conditional_Abort then
             Character:PivotTo(Target)
        end
        if RenderConnection then
             RenderConnection:Disconnect()
        end MovementCallConnection:Disconnect()return {
            Status = Conditional_Abort and 'Aborted' or 'Success'
        }
    end)local function WaitForClass(className:string, retries:number?, delaySeconds:number?)
        delaySeconds = delaySeconds or 1
        for i = 1, (retries or 5)do
             local foundClass = Class_Interface.GetClass(className)if foundClass then
                 return foundClass
             end task_wait(delaySeconds)
        end warn("CRITICAL - Could not find '" .. className .. "' class after all retries.")return nil
     end
    local SecureLerpTeleportWithPathfinding
    SecureLerpTeleportWithPathfinding = LPH_JIT_MAX(function(Origin:CFrame, Target:CFrame, StudsPerSecond:number, Conditional:(()->boolean)?)
        if not G_Toggle('ATMFarmUsePath')then
             return SecureLerpTeleport(Origin, Target, StudsPerSecond, Conditional)
        end
        local Conditional_Abort = false
        local Path = PathLib.GetPath(Origin.Position, Target.Position)if not Path or #Path:GetWaypoints() == 0 then
             warn('Failed to calculate path from', Origin.Position, 'to', Target.Position)SafeNotify(T([[Failed to calculate path. Falling back to direct teleportation.]]))return SecureLerpTeleport(Origin, Target, StudsPerSecond, Conditional)
        end
        local Waypoints = Path:GetWaypoints()local TurnPoints = {
        }
        local TurnAngleThreshold = math.rad(35)local Lookaround = 3
        for i = 1, #Waypoints do
             local prevIndex = math_max(1, i - Lookaround)local nextIndex = math_min(#Waypoints, i + Lookaround)if i == prevIndex or i == nextIndex then
                 continue
             end
            local prevDirection = (Waypoints[i].Position - Waypoints[prevIndex].Position).Unit
            local nextDirection = (Waypoints[nextIndex].Position - Waypoints[i].Position).Unit
            if prevDirection.Magnitude > 0.1 and nextDirection.Magnitude > 0.1 then
                 local dot = prevDirection:Dot(nextDirection)local angle = math.acos(math.clamp(dot, - 1, 1))if angle > TurnAngleThreshold then
                     table.insert(TurnPoints, {
                        Index = i,
                        Angle = angle
                    })
                end
             end
         end
        local CurrentOrigin = Origin
        local VisualWaypoints = PathLib.VisualizePath(Path)local MovementFlag = false
        local Start = os.clock()local MovementCallConnection = MovementEvent.Event:Connect(function(Type:string)
            if Type == 'TP' or Type == 'Noclip' then
                 MovementFlag = true
             end
         end)local Jumping = 0
        local nextTurnIndex = 1
        for Index, Waypoint in next, Waypoints do
             local Visual = PathLib.MarkerFromWaypoint(VisualWaypoints, Waypoint)local NextWaypoint = Waypoints[Index + 1]local MinSpeedFactor = 0.15
            local SlowdownDistance = 30
            local SpeedFactor = 1
            while nextTurnIndex <= #TurnPoints and TurnPoints[nextTurnIndex].Index < Index do
                 nextTurnIndex+=1
             end
            if nextTurnIndex <= #TurnPoints then
                 local turnPoint = TurnPoints[nextTurnIndex]local distanceToTurn = (Waypoints[turnPoint.Index].Position - Waypoint.Position).Magnitude
                if distanceToTurn < SlowdownDistance then
                     local alpha = 1 - (distanceToTurn / SlowdownDistance)local turnSeverityFactor = math.clamp(turnPoint.Angle / math.pi, 0, 1)local targetSpeedFactor = 1 - (1 - MinSpeedFactor) * turnSeverityFactor
                    SpeedFactor = 1 + (targetSpeedFactor - 1) * alpha
                 end
             end
            local ElapsedTime = os.clock() - Start
            local SpeedAlpha = math.clamp(ElapsedTime / TELEPORT_SPEEDUP_TIME, 0, 1)local InitialSpeed = StudsPerSecond / 10
            local CurrentSpeed = InitialSpeed + (StudsPerSecond - InitialSpeed) * SpeedAlpha
            local EffectiveStudsPerSecond = CurrentSpeed * SpeedFactor
            local TimeToArrival = (Waypoint.Position - CurrentOrigin.Position).Magnitude / (EffectiveStudsPerSecond * 1.5)if Waypoint.Action == Enum.PathWaypointAction.Jump or (NextWaypoint and NextWaypoint.Action == Enum.PathWaypointAction.Jump)then
                 Jumping = 4
             end Utils.LerpTPWithHeight(Waypoint.Position + Vector3.yAxis * (Jumping > 0 and 7 or 3), TimeToArrival)if Jumping > 0 then
                 Jumping-=1
             end TweenService:Create(Visual.Object, TweenInfo.new(TimeToArrival, Enum.EasingStyle.Linear, Enum.EasingDirection.InOut), {
                CFrame = CFrame.new(Visual.Object.Position + Vector3.yAxis * (Jumping > 0 and 7 or 3)),
                Color = Color3.new(0,
                1,
                0)
            }):Play()if MovementFlag then
                 game:GetService('StarterGui'):SetCore('SendNotification', {
                    ['Title'] = T('Movement Flagged'),
                    ['Text'] = T('Movement has been flagged by the anticheat. Pausing...'),
                    ['Duration'] = 3
                })
MovementFlag = false
                local RestabilizeTime = os.clock()while(os.clock() - RestabilizeTime < 1.5) or (AssertCharacter():GetPivot().p.Y < 250)do
                     task_wait()local Vehicle = GetVehicle()if Vehicle then
                         for _, Descendant in next, Vehicle.Vehicle:GetDescendants()do
                             if Descendant:IsA('BasePart')then
                                 if Descendant.AssemblyLinearVelocity.Magnitude > 100 then
                                     Descendant.AssemblyLinearVelocity*=Vector3.zero
                                    Descendant.AssemblyAngularVelocity*=Vector3.zero
                                 end
                             end
                         end
                     end
                 end
                for _, VisualWaypoint in next, VisualWaypoints do
                     VisualWaypoint.Object:Destroy()
                end
                return SecureLerpTeleportWithPathfinding(LocalPlayer.Character:GetPivot(), Target, StudsPerSecond, Conditional)
            end
            if not Conditional or Conditional()then
                 CurrentOrigin = CFrame.new(Waypoint.Position + Vector3.yAxis * 3)
            else
                 warn('Conditional check failed')Conditional_Abort = true break
             end
         end
        for _, Visual in next, VisualWaypoints do
             Visual.Object:Destroy()
        end MovementCallConnection:Disconnect()return (not Conditional_Abort) and {
            Status = 'Success'
        } or {
            Status = 'Aborted'
        }
    end)Storage.Routines[_nextKey(Storage.Routines, 'MoveDirection_SpoofLoop')] = Cleaner(task.spawn(function()
        local Flip = 1
        while RunService.Stepped:Wait()do
             local Character = AssertCharacter()local Humanoid = Character:FindFirstChildOfClass('Humanoid') :: Humanoid
            if not Humanoid then
                 continue
             end Storage.MoveDirection = gethiddenproperty(Humanoid, 'MoveDirectionInternal')if Storage.MovementSpoof then
                 Flip*= - 1
                task.wait()sethiddenproperty(Humanoid, 'MoveDirectionInternal', (Vector3.zAxis / 2) * Flip)
            elseif  G_Toggle('SprintTakesNoStamina')then
                 sethiddenproperty(Humanoid, 'MoveDirectionInternal', Vector3.zero)
            end
         end
     end))Storage.Connections[_nextKey(Storage.Connections, 'Heartbeat_MoveBoost')] = Cleaner(RunService.Heartbeat:Connect(LPH_JIT_MAX(function(DeltaTime)
        local MoveDirection = Storage.MoveDirection
        local Character = AssertCharacter()local Humanoid = Character:FindFirstChildOfClass('Humanoid') :: Humanoid
        if Humanoid then
             if Humanoid:GetState() == Enum.HumanoidStateType.Climbing then
                 MoveDirection = Vector3.zero
             end
            if MoveDirection.Magnitude > 0 then
                 local SpeedBoost = G_Option('SpeedBoost')if SpeedBoost > 0 then
                     Character:TranslateBy(MoveDirection * DeltaTime * SpeedBoost * 2.5)
                end
             end
         end
        local Vehicle = FindVehicle()if Vehicle and G_Toggle('ATMFarm')then
             local VehicleModel = Vehicle.Vehicle
            for _, Part in next, VehicleModel:GetDescendants()do
                 if Part:IsA('BasePart')then
                     if Part.AssemblyLinearVelocity.Magnitude > 2000 then
                         Part.AssemblyLinearVelocity = Vector3.yAxis * math.random()
                    end
                    if Part.AssemblyAngularVelocity.Magnitude > 2000 then
                         Part.AssemblyAngularVelocity = Vector3.yAxis * math.random()
                    end
                 end
             end
            local Wheels = VehicleModel:FindFirstChild('Wheels') :: Model
            local Chassis = VehicleModel:FindFirstChild('Chassis') :: BasePart
            if Wheels then
                 for _, Wheel:Part in next, Wheels:GetChildren()do
                     local Distance = (Wheel:GetPivot().Position - Chassis:GetPivot().Position).Magnitude
                    if Distance > 50 then
                         Wheel:PivotTo(Chassis:GetPivot())local Connection = RunService.Heartbeat:Connect(function()
                            for _, v in next, VehicleModel:GetDescendants()do
                                 if v:IsA('BasePart')then
                                     v.AssemblyLinearVelocity = Vector3.zero
                                    v.AssemblyAngularVelocity = Vector3.zero
                                 end
                             end Wheel:PivotTo(Chassis:GetPivot())
                        end)task.delay(3, function()
                            Connection:Disconnect()
                        end)
                    end
                 end
             end
         end
        if not G_Toggle('ATMFarm')then
             for _, Part in next, Storage.RayCastGuides do
                 Part.CanCollide = false Part.CanQuery = false
             end
         else
             for _, Part in next, Storage.RayCastGuides do
                 Part.CanCollide = true Part.CanQuery = true
             end
         end
     end)))Storage.Connections[_nextKey(Storage.Connections, 'LocalPlayer_CharacterAdded')] = Cleaner(LocalPlayer.CharacterAdded:Connect(CharacterAdded))if LocalPlayer.Character then
         CharacterAdded(LocalPlayer.Character)
    end Storage.Routines[_nextKey(Storage.Connections, 'Snap_Heartbeat')] = Cleaner(task.spawn(function()
        local Enabled = false
        local Origin = nil InitializedSignal.Event:Once(function()
            Library.Toggles.Snap:OnChanged(function(Value)
                Storage.SupressNotification = Value
             end)
        end)Cleaner(RunService.Heartbeat:Connect(function()
            local Snap = G_Toggle('Snap') and not Storage.Panic
            local SnapOffsetY = G_Option('SnapOffsetY')if Snap then
                 if not Enabled then
                     Enabled = true Origin = AssertCharacter():GetPivot()SafeNotify(T('Snap enabled!'))
                end
                local Character = AssertCharacter()Character:PivotTo(Origin - Vector3.yAxis * SnapOffsetY)
            else
                 Enabled = false Origin = nil
                return
             end
         end))
    end))for Argument, Data in next, ArgumentChecks do
         if not Data.Found then
             dbgwarn('Failed to find argument', Argument, 'with value', Data.Value)local Continue, Abort, UI = ErrorHandler.Throw(0x2, T([[Changes in the internal game structure were detected. Some features have been disabled for safety.]]), true)local Aborting = false
            local Pressed = false Continue:Once(function()
                Pressed = true Aborting = false
             end)Abort:Once(function()
                Pressed = true Aborting = true HookMgr.ClearHooks()Cleaner.Clean()ConnectionProxyMgr:Clear()ESP_Library.Unload()Aiming_Library.Unload()rconsoledestroy()
            end)repeat
                 task_wait(0.1)
            until Pressed
            UI:Destroy()if Aborting then
                 coroutine_yield()return
             end break
         end
     end
    local GunClass = nil task_spawn(function()
        task_wait(5)GunClass = WaitForClass('Gun')
    end)HookMgr.RegisterHook('NetGetHook', Net.get, function(Old, ...)
        local Args = table.pack(...)local CallType = Args[1]for CallTypeNeedle, _ in next, Storage.Blacklisted_Network_Calls do
             if CallType:match(CallTypeNeedle)then
                 return
             end
         end
        if CallType == 'fix_desync_hip_height' then
             if G_Toggle('Invisibility')then
                 return
             end
         end
        return Old(table.unpack(Args, 1, Args.n))
    end)HookMgr.RegisterHook('NetSendHook', Net.send, LPH_JIT_MAX(function(Old, ...)
        local Args = table.pack(...)local CallType = Args[1]if CallType == 'leave_character_creator' and shared.BlockFirstECC_Call then
             shared.BlockFirstECC_Call = false
            return
         end
        if not checkcaller()then
             for CallTypeNeedle, _ in next, Storage.Blacklisted_Network_Calls do
                 if CallType:match(CallTypeNeedle)then
                     return
                 end
             end
            if CallType == ArgumentChecks.Melee_Attack.Value and G_Toggle('MeleeFixHitchance')then
                 local Hits = Args[3]local LocalHumanoidRootPart = AssertCharacter():WaitForChild('HumanoidRootPart') :: Part
                if#Hits > 0 then
                     local TargetHumanoidRootPart = Hits[1].Character:WaitForChild('HumanoidRootPart') :: Part
                    Args[4] = CFrame.lookAt(LocalHumanoidRootPart:GetPivot().Position, TargetHumanoidRootPart:GetPivot().Position)
                end
                return Old(table.unpack(Args, 1, Args.n))
            elseif  CallType == 'shoot_gun' then
                 local GunInstance = Args[2] :: Tool
                if G_Toggle('SilentAimEnabled') and Aiming_Library.CurrentTarget and GunClass then
                     local Target = Aiming_Library.CurrentTarget
                    local HitPart = Target:FindFirstChild(G_Option('SilentAimPart')) or Target:FindFirstChild('HumanoidRootPart')local GunWrapper = GunClass.objects[GunInstance]local function CheckLineOfSight(StartPos:Vector3, EndPos:Vector3, FilterInstances:{
                            Instance
                        })
                        :(boolean, Vector3?)local CurrentRayOrigin = StartPos
                        local RayParams = RaycastParams.new()RayParams.FilterType = Enum.RaycastFilterType.Exclude
                        RayParams.FilterDescendantsInstances = FilterInstances
                        local MaxIterations = 10
                        for _ = 1, MaxIterations do
                             local Direction = (EndPos - CurrentRayOrigin)local Distance = Direction.Magnitude
                            if Distance < 0.01 then
                                 return true, nil
                             end Direction = Direction.Unit
                            local RayResult = workspace:Raycast(CurrentRayOrigin, Direction * Distance, RayParams)if not RayResult then
                                 return true, nil
                             end
                            local HitInstance = RayResult.Instance
                            if HitInstance then
                                 local IsGlass = CollectionService:HasTag(HitInstance, 'Glass')local IsTransparent = HitInstance.Transparency > 0.2
                                if IsGlass or IsTransparent then
                                     CurrentRayOrigin = RayResult.Position + Direction * 0.01
                                 else
                                     return false, RayResult.Position
                                 end
                             else
                                 return false, RayResult.Position
                             end
                         end
                        return true, nil
                     end
                    if HitPart and GunWrapper then
                         local MultiShot = GunInstance:GetAttribute('Multishot') or 1
                        local PredictedPosition = G_Toggle('Prediction') and GetPredictedWithGun(HitPart, GunInstance) or HitPart.Position
                        local InitialOrigin = Camera.CFrame.Position
                        local Origin = InitialOrigin
                        local LineOfSightFilter = {
                            AssertCharacter(),
                            Target
                        }
                        local ShotClear, _ = CheckLineOfSight(AssertCharacter().Head.Position, PredictedPosition, LineOfSightFilter)if not ShotClear and G_Toggle('MultiResolve')then
                             local SamplePoints = GetUniformSamplesInSphere(InitialOrigin, 10, 50)for _, SamplePoint in next, SamplePoints do
                                 local SampleIsClear, _ = CheckLineOfSight(SamplePoint, PredictedPosition, LineOfSightFilter)if SampleIsClear then
                                     Origin = SamplePoint break
                                 end
                             end
                         end
                        if(not LPH_OBFUSCATED) or G_Toggle('VisualizeHitReg')then
                             local RayData = VisualizeRay(Origin, PredictedPosition)local HitTimeout = 0.2 + LocalPlayer:GetNetworkPing()local Humanoid = HitPart.Parent:WaitForChild('Humanoid') :: Humanoid
                            local LastHealth = Humanoid.Health
                            local HumanoidDamagedConnection = Humanoid.HealthChanged:Connect(function(NewHealth)
                                if NewHealth > LastHealth then
                                     LastHealth = NewHealth
                                 elseif  NewHealth < LastHealth then
                                     RayData.Hit = true
                                 end
                             end)task.delay(HitTimeout, function()
                                if not RayData.Hit then
                                 end HumanoidDamagedConnection:Disconnect()
                            end)
                        end
                        local GunAccuracy, GunSeed = secure_call(GunWrapper.states.accuracy.get), secure_call(GunWrapper.states.seed.get)local GunRNG = Random.new(GunSeed)local SpreadFactor = 1 - GunAccuracy
                        local RX, RY, RZ = GunRNG:NextNumber( - 50, 50), GunRNG:NextNumber( - 50, 50), GunRNG:NextNumber( - 50, 50)local SpreadVector = Vector3.new(RX * SpreadFactor, RY * SpreadFactor, RZ * SpreadFactor)local PerfectDirection = (PredictedPosition - Origin).Unit
                        local ReversedAimDirection = (PerfectDirection * 500 - SpreadVector).Unit
                        Args[3] = CFrame.lookAt(Origin, Origin + ReversedAimDirection)local HitResult = {
                            {
                                ['Normal'] = (PredictedPosition - Origin).Unit,
                                ['Instance'] = HitPart,
                                ['Position'] = PredictedPosition + (PredictedPosition - Camera.CFrame.Position).Unit
                            }
                        }
                        local Results = {
                        }
                        local MultiShotCount = GunInstance:GetAttribute('Multishot') or 1
                        for i = 1, MultiShotCount do
                             table.insert(Results, HitResult)
                        end
                        if G_Toggle('VisualizeBullets')then
                             for _, Result in next, Results do
                                 VisualizeRay(Args[3].Position, Result[1].Position).Color = Color3.new(0, 1, 0)
                            end
                         end
                        if(MultiShot == 1 and G_Toggle('Wallbang')) and not ShotClear then
                             Args[3] = CFrame.new(Vector3.new(math.huge, math.huge, math.huge)) * CFrame.lookAt(Origin, Origin + ReversedAimDirection).Rotation
                         end Args[4] = Results
                     end
                 end
                if G_Toggle('DoubleTap')then
                     Old(table.unpack(Args, 1, Args.n))
                end
                return Old(table.unpack(Args, 1, Args.n))
            elseif  CallType == 'throw_item' then
                 if G_Toggle('ThrowableSilentAimEnabled')then
                     local HitPart:BasePart?if Aiming_Library.CurrentTarget then
                         HitPart = Aiming_Library.CurrentTarget:FindFirstChild(G_Option('SilentAimPart')) or Aiming_Library.CurrentTarget:FindFirstChild('HumanoidRootPart')if HitPart then
                             Args[3] = HitPart.Position + Vector3.new(0, 1, 0)Args[4] = CFrame.new(Args[3], HitPart.Position).LookVector
                            return Old(table.unpack(Args, 1, Args.n))
                        end
                     end
                 end
             end
            if CallType == 'crashed_car' and G_Toggle('NoCrash')then
                 return
             end
         end
        return Old(table.unpack(Args, 1, Args.n))
    end))HookMgr.RegisterHook('NotificationSupressionHook', NotificationsUI.show_notification, function(Old, ...)
        if Storage.SupressNotification then
             local Traceback = debug.traceback() :: string
            if Traceback:find('Net')then
                 return
             end
         end
        return Old(...)
    end)UpdateStatus(T('Skipping splash screen...'))Storage.Connections[_nextKey(Storage.Connections, 'Remotes_Send_OnClientEvent')] = Cleaner(ReplicatedStorage.Remotes.Send.OnClientEvent:Connect(LPH_JIT_MAX(function(...)
        local Args = {
            ...
        }
        local Call_Type = Args[1]if Call_Type == 'notification' then
             local Anticheat_Detection_Types = {
                ['Teleport detected'] = 'TP',
                ['Anti noclip triggered'] = 'Noclip',
                ['Fly detected'] = 'Flight'
            }
            local DetectionType = Anticheat_Detection_Types[Args[3]]if DetectionType then
                 MovementEvent:Fire(DetectionType)
            end
         end
     end)))if LocalPlayer:GetAttribute('InSplashScreen') == true then
         local PlayerGui = LocalPlayer:WaitForChild('PlayerGui')local SplashScreenGui = PlayerGui:WaitForChild('SplashScreenGui', 5)if SplashScreenGui then
             SplashScreenGui.Enabled = false
         end
        local SoundService = game:GetService('SoundService')local Sound = SoundService:FindFirstChild('Sound')if Sound then
             Sound:Destroy()
        end
        local SpawnMode = nil
        local SpawnModeFrame = nil
        if not TeleportData:ReadData('TeleportState')then
             local PromptStart = os.clock()SpawnModeFrame = Instance.new('ScreenGui')SpawnModeFrame.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
            SpawnModeFrame.Name = 'SpawnMode'
            SpawnModeFrame.DisplayOrder = 999999999
            SpawnModeFrame.Parent = CoreGui
            shared.SpawnModeFrame = SpawnModeFrame
            local Root = Instance.new('Frame')Root.BorderColor3 = Color3.fromRGB(0, 0, 0)Root.AnchorPoint = Vector2.new(0.5, 0.5)Root.BackgroundTransparency = 0.8999999761581421
            Root.Position = UDim2.new(0.5, 0, 0.5, 0)Root.Name = 'Root'
            Root.Size = UDim2.new(0.25, 0, 0.25, 30)Root.BorderSizePixel = 0
            Root.BackgroundColor3 = Color3.fromRGB(255, 255, 255)Root.Parent = SpawnModeFrame
            local SpawnModeLabel = Instance.new('TextLabel')SpawnModeLabel.TextWrapped = true SpawnModeLabel.TextColor3 = Color3.fromRGB(255, 255, 255)SpawnModeLabel.BorderColor3 = Color3.fromRGB(0, 0, 0)SpawnModeLabel.Text = T('Select Spawn Mode')SpawnModeLabel.Name = 'SpawnMode'
            SpawnModeLabel.Size = UDim2.new(1, 0, 0, 0)SpawnModeLabel.BorderSizePixel = 0
            SpawnModeLabel.BackgroundTransparency = 0.20000000298023224
            SpawnModeLabel.RichText = true SpawnModeLabel.FontFace = Font.new('rbxassetid://16658221428', Enum.FontWeight.Regular, Enum.FontStyle.Normal)SpawnModeLabel.AutomaticSize = Enum.AutomaticSize.Y
            SpawnModeLabel.TextSize = 40
            SpawnModeLabel.BackgroundColor3 = Color3.fromRGB(0, 0, 0)SpawnModeLabel.Parent = Root
            local UIListLayout = Instance.new('UIListLayout')UIListLayout.SortOrder = Enum.SortOrder.LayoutOrder
            UIListLayout.HorizontalAlignment = Enum.HorizontalAlignment.Center
            UIListLayout.VerticalFlex = Enum.UIFlexAlignment.Fill
            UIListLayout.Padding = UDim.new(0, 5)UIListLayout.Parent = Root
            local GodMode = Instance.new('TextButton')GodMode.LayoutOrder = 1
            GodMode.FontFace = Font.new('rbxassetid://16658221428', Enum.FontWeight.Regular, Enum.FontStyle.Normal)GodMode.Active = false GodMode.Selectable = false GodMode.TextSize = 30
            GodMode.Size = UDim2.new(1, 0, 0, 0)GodMode.RichText = true GodMode.TextColor3 = Color3.fromRGB(255, 255, 255)GodMode.BorderColor3 = Color3.fromRGB(0, 0, 0)GodMode.Text = `{ T('God Mode') } < br / > < font size = "20" > < i > { T("(Can't damage players or work)") } < / i > < / font >`GodMode.BackgroundTransparency = 0.5
            GodMode.Name = 'GodMode'
            GodMode.BorderSizePixel = 0
            GodMode.TextWrapped = true GodMode.AutomaticSize = Enum.AutomaticSize.Y
            GodMode.BackgroundColor3 = Color3.fromRGB(0, 0, 0)GodMode.Parent = Root
            local UIPadding = Instance.new('UIPadding')UIPadding.PaddingBottom = UDim.new(0, 10)UIPadding.PaddingTop = UDim.new(0, 10)UIPadding.Parent = GodMode
            local NormalMode = Instance.new('TextButton')NormalMode.LayoutOrder = 2
            NormalMode.FontFace = Font.new('rbxassetid://16658221428', Enum.FontWeight.Regular, Enum.FontStyle.Normal)NormalMode.Active = false NormalMode.Selectable = false NormalMode.TextSize = 30
            NormalMode.Size = UDim2.new(1, 0, 0, 0)NormalMode.RichText = true NormalMode.TextColor3 = Color3.fromRGB(255, 255, 255)NormalMode.BorderColor3 = Color3.fromRGB(0, 0, 0)NormalMode.Text = `{ T('Normal Mode') } < br / > < font size = "20" > < i > { T('(Spawn in normally)') } < / i > < / font >`NormalMode.BackgroundTransparency = 0.5
            NormalMode.Name = 'NormalMode'
            NormalMode.BorderSizePixel = 0
            NormalMode.TextWrapped = true NormalMode.AutomaticSize = Enum.AutomaticSize.Y
            NormalMode.BackgroundColor3 = Color3.fromRGB(0, 0, 0)NormalMode.Parent = Root
            local UIPadding2 = Instance.new('UIPadding')UIPadding2.PaddingBottom = UDim.new(0, 10)UIPadding2.PaddingTop = UDim.new(0, 10)UIPadding2.Parent = NormalMode
            local UIAspectRatioConstraint = Instance.new('UIAspectRatioConstraint')UIAspectRatioConstraint.AspectRatio = 2
            UIAspectRatioConstraint.AspectType = Enum.AspectType.ScaleWithParentSize
            UIAspectRatioConstraint.Parent = Root
            NormalMode.MouseButton1Click:Connect(function()
                SpawnMode = 'Normal'
             end)GodMode.MouseButton1Click:Connect(function()
                SpawnMode = 'God'
             end)repeat
                 task_wait()
            until(SpawnMode ~= nil) or (os.clock() - PromptStart > 10) or DUPE_MODE
            SpawnModeFrame:ClearAllChildren()if SpawnMode == nil then
                 SpawnMode = DUPE_MODE and 'God' or 'Normal'
             end
            if(SpawnMode == 'God') or DUPE_MODE then
                 shared.BlockFirstECC_Call = true
             end
         end
        local ThreadSignal = Instance.new('BindableEvent')local SplashScreenModule = Modules.Game:WaitForChild('SplashScreen') :: ModuleScript
        SplashScreenModule = SafeRequire(SplashScreenModule)local CharacterCreatorModule = Modules.Game:WaitForChild('CharacterCreator'):WaitForChild('CharacterCreator') :: ModuleScript
        CharacterCreatorModule = SafeRequire(CharacterCreatorModule)task_spawn(function()
            secure_call(SplashScreenModule.in_loading_screen.set, false)task_wait(1)secure_call(CharacterCreatorModule.finish)ThreadSignal:Fire()
        end)ThreadSignal.Event:Wait()ThreadSignal:Destroy()if(SpawnMode == 'God') or DUPE_MODE then
             task_wait(2)shared.GodMode = true
            local Character = AssertCharacter()local Origin = Character:GetPivot()local Target = CFrame.new(Origin.X, 265, Origin.Z)local Distance = (Target.Position - Origin.Position).Magnitude
            SecureNet.Send(ArgumentChecks.Sprint.Value, true)Utils.LerpTP(Target, Distance / 20)for _, Connection in next, getconnections(LocalPlayer.CharacterAdded)do
                 local Function = Connection.Function
                if Function and getfenv(Function) and getfenv(Function).script then
                     Connection:Fire(Character)
                end
             end
            if DUPE_MODE then
                 print('Enabling rollback...')local InventoryVehicle = nil
                for _ = 1, 5 do
                     for _, ItemName in next, VehicleCandidates do
                         local Item = Inventory.GetItemsByName(ItemName)[1]if Item then
                             InventoryVehicle = Item
                            SafeNotify(T('Found InventoryItem Vehicle' .. ItemName))break
                         end
                     end
                    if InventoryVehicle then
                         break
                     else
                         SafeNotify(T('No vehicle found in inventory, retrying...'))task.wait(1)
                    end
                 end task.wait(1)if InventoryVehicle then
                     if ArgumentChecks.Toggle_Equip_Item.Found then
                         SafeNotify(T(`Attempting to spawn vehicle{ InventoryVehicle.Name }...`))SecureNet.Get(ArgumentChecks.Toggle_Equip_Item.Value, InventoryVehicle.Guid)task.wait(3)if not FindVehicle()then
                             for _ = 1, 5 do
                                 SecureNet.Get(ArgumentChecks.Toggle_Equip_Item.Value, InventoryVehicle.Guid)task.wait(3)if FindVehicle()then
                                     break
                                 end
                             end
                         end
                     end
                 end
                local VehicleData = FindVehicle()if VehicleData then
                     SafeNotify(T('Vehicle spawned successfully!'))local Vehicle = VehicleData.Vehicle
                    local DriverSeat = Vehicle:FindFirstChild('DriverSeat')Sit(DriverSeat)local Motors = DriverSeat.Parent:FindFirstChild('Motors')if Motors then
                         local ForwardMaxSpeed = Motors:GetAttribute('forwardMaxSpeed') or 23
                        local Ratio = ForwardMaxSpeed / 35
                        TELEPORT_SPEED_VEHICLE = 65 * Ratio
                     else
                         TELEPORT_SPEED_VEHICLE = 40
                     end
                 else
                     Character:FindFirstChildWhichIsA('Humanoid'):SetStateEnabled(Enum.HumanoidStateType.Seated, false)SafeNotify(T('Failed to spawn vehicle!'))
                end task.wait(1)local TargetCFrame = (workspace:FindFirstChild(DUPE_RECIPIENT) :: Model):GetPivot()local NearTarget = CFrame.new(1175, 255, - 539)SecureLerpTeleport(Character:GetPivot(), NearTarget, Character.Humanoid.SeatPart and (TELEPORT_SPEED_VEHICLE * 0.8) or TELEPORT_SPEED)Character.Humanoid:ChangeState(Enum.HumanoidStateType.Jumping)task.wait(1)Origin = Character:GetPivot()Utils.LerpTP(TargetCFrame, (TargetCFrame.Position - Origin.Position).Magnitude / 20)SecureNet.Send(ArgumentChecks.Enter_Character_Creator.Value, Character:GetPivot())local Bomb = string.rep('\r\n\t\u{1c4}\r\n\r\n\t\u{601}\r\n\r\n\t\u{2031}\r\n\r\n\t\u{bb9}\r\n\r\n\t\u{bf8}\r\n\r\n\t\u{bf5}\r\n\r\n\t\u{a9c4}\r\n\r\n\t.\r\n\r\n\t\u{102a}\r\n\r\n\t\u{a9c5}\r\n\r\n\t\u{2e3b}\r\n\r\n\t\u{12219}\r\n\r\n\t\u{1242b}\r\n\r\n\t\u{fdfd}\r\n\r\n\r\n\t\u{12304}\r\n\r\n\t\u{1221f}\r\n\r\n\t\u{1237c}\r\n\r\n\t\u{1204e}\r\n\r\n\t\u{12031}\r\n\r\n\t\u{12327}\r\n\r\n\t\u{12143} \u{12213}\r\n\r\n\t\u{12359}\r\n\r\n\t\u{1228e}\r\n\r\n\t\u{12121}\r\n\r\n\t\u{1214c}\r\n\r\n\t\u{1204f}\r\n\r\n\t\u{12030}\r\n\r\n\t\u{1242a}\r\n\r\n\t\u{12429}\r\n\r\n\t\u{12219}\r\n\r\n\t\u{1242b}\r\n\r\n\r\n\t\u{3106c} 84\r\n\r\n\t\u{30f54} 76\r\n\r\n\t\u{2a6a5} 64\r\n\r\n\t\u{4a3b} 52\r\n\r\n\t\u{9f98} 48\r\n\r\n\t\u{4c9c} 44\r\n\r\n\t\u{e17e} \u{e17f} \u{e216} \u{e217} \u{e282} \u{e29e} \u{e29f} a\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\r\n\t\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a} \u{13010}\u{130b8}\r\n\r\n\t\u{1f603}\u{20e2}\u{1f44d}\u{f3c};\u{b4}\u{f0e}\u{eb6} \u{6dd} \u{f0e}\u{eb6}\u{f3d}\r\n\t', 10000)for i = 1, 3 do
                     local Categories = CharacterCreatorItems:GetChildren()local RandomCategory = Categories[math.random(1, #Categories)]local Items = RandomCategory:GetChildren()local RandomItem = Items[math.random(1, #Items)]print('Equipping random item from random category:', RandomCategory.Name, RandomItem.Name)SecureNet.Send(ArgumentChecks.Change_Accessory.Value, RandomCategory.Name .. '\0' .. tostring(math.random()) .. tostring(math.random()) .. Bomb, RandomItem.Name, true)task.wait(0.3)
                end
                local hand = Inventory.FilterByLocation(Inventory.ListInventory(), 'hand')for _, item in next, hand do
                     SecureNet.Send(ArgumentChecks.Drop_Item.Value, item.Guid, item.Amount)
                end
                local LastPing = LocalPlayer:GetNetworkPing()print('Waiting for ping to change from', LastPing)repeat
                     task.wait(5)
                until LocalPlayer:GetNetworkPing() ~= LastPing
                print('Waiting for ping to stabilize below 1 second')repeat
                     task.wait(10)
                until LocalPlayer:GetNetworkPing() < 1
                queue_on_teleport(readfile('./Dupe.luau'))TeleportService:Teleport(game.PlaceId)
            end
         end
     end ClearStatusOverlay()local function AwaitCharacter(Player:Player)
        repeat
             task_wait()
        until Player.Character or not Player
        return Player and Player.Character or nil
     end
    local function SafeReset(FixLimbs:boolean?)
        if FixLimbs ~= false then
             FixLimbs = true
         end
        local Character = AssertCharacter()local Origin = Character:GetPivot()repeat
             task_wait()Character:PivotTo(Origin + (Vector3.new(math.random() - 0.5, math.random() - 0.5, math.random() - 0.5) * 10))
        until LocalPlayer:GetAttribute('IsInCombat') == false
        if FixLimbs then
             SecureNet.Send(ArgumentChecks.Request_Respawn.Value)task_wait(7)SecureNet.Send(ArgumentChecks.Respawn.Value)
        end
     end
    local TeleportLoaderQueued = false
    local function BuildTeleportState(reason:string?)
        local TPData = {
            Toggles = {
            },
            Options = {
            },
            Created = tick(),
            Reason = reason
        }
        for Toggle, Value in next, Library.Toggles do
             if Value and Value.Value ~= nil then
                 TPData.Toggles[Toggle] = Value.Value
             end
         end
        for Option, Value in next, Library.Options do
             if Value and Value.Value ~= nil then
                 if typeof(Value.Value) == 'boolean' or typeof(Value.Value) == 'number' or typeof(Value.Value) == 'string' then
                     TPData.Options[Option] = Value.Value
                 else
                     dbgprint('ATMFarm: Skipping non-serializable option:', Option, 'with value:', Value.Value)
                end
             end
         end TeleportData:WriteData('TeleportState', TPData)return TPData
     end
    local function QueueTeleportLoader(force:boolean?)
        if TeleportLoaderQueued and not force then
             return
         end TeleportLoaderQueued = true
        local AppendString = 'getgenv().Key = "NoKey"\n'
        if getgenv().Key then
             AppendString = `getgenv().Key = "{ getgenv().Key}"\n`
        end queue_on_teleport(AppendString .. [[repeat task.wait() until game:IsLoaded()
loadstring(game:HttpGet("https://example.com/script/Blockspin_Paid_Loader.luau"))()]])
    end
    local function AttemptHop(reason:string?)
        :boolean
        if not G_Toggle('ATMFarmAutoHop')then
             return false
         end SafeReset(false)pcall(TeleportData.WipeFile, TeleportData, 'TeleportState')BuildTeleportState(reason or 'AutoHop')SafeNotify(T('ATMFarm: AutoHop time reached, hopping servers...', 3))local servers = {
        }
        local req = SecureRequest:HttpGet('https://games.roblox.com/v1/games/' .. game.PlaceId .. [[/servers/Public?sortOrder=Asc&limit=100&excludeFullGames=true]])local body = HttpService:JSONDecode(req)if body and body.data then
             for _, v in next, body.data do
                 if type(v) == 'table' and tonumber(v.playing) and tonumber(v.maxPlayers) and v.playing < v.maxPlayers and v.id ~= game.JobId then
                     table.insert(servers, 1, v.id)
                end
             end
         end
        if#servers > 0 then
             QueueTeleportLoader()TeleportService:TeleportToPlaceInstance(game.PlaceId, servers[math.random(1, #servers)], Players.LocalPlayer)return true
         else
             SafeNotify(T('ATM-Farm: No servers found to hop to.'), 3)return false
         end
     end
    local function AttemptRejoin(reason:string?)
        :boolean
        SafeReset(false)pcall(TeleportData.WipeFile, TeleportData, 'TeleportState')BuildTeleportState(reason or 'VehicleRejoin')QueueTeleportLoader()SafeNotify(T('ATM-Farm: Rejoining to recover automation flow...'), 3)local success, err = pcall(function()
            TeleportService:TeleportToPlaceInstance(game.PlaceId, game.JobId, Players.LocalPlayer)
        end)if not success then
             dbgprint('ATMFarm: Rejoin failed:', err)return false
         end
        return true
     end
    local function PingWebPanel(ItemGUID:string, ItemName:string, ItemRarity:string, Owner:Player)
        local payload = {
            item_id = ItemGUID,
            item_name = ItemName,
            item_rarity = ItemRarity,
            owner_username = Owner.Name,
            owner_displayname = Owner.DisplayName,
            job_id = game.JobId,
            place_id = game.PlaceId
        }
        local success, jsonData = pcall(HttpService.JSONEncode, HttpService, payload)if not success then
             warn('Web Panel Ping failed: Could not encode JSON for item', ItemName, '| Error:', jsonData)return
         end task_spawn(function()
            local postSuccess, postResult = pcall(function()
                return SecureRequest.request({
                    Url = 'https://example.com/item_ping/',
                    Method = 'POST',
                    Headers = {
                        ['Content-Type'] = 'application/json'
                    },
                    Body = jsonData,
                    Timeout = 5
                })
            end)if not postSuccess then
                 warn('Web Panel Ping failed: HTTP Post error for item', ItemName, '| Error:', postResult)
            end
         end)
    end
    local function HandleCharacter(Character, Player)
        local PlayerItems = {
        }
        Prediction:RegisterCharacter(Character)if not Character then
             return
         end
        while task_wait(5)do
             if not Character:IsDescendantOf(workspace)then
                 return
             end
            local Items = {
            }
            for _, Item in ipairs(Character:GetChildren())do
                 if Item:IsA('Tool')then
                     table.insert(Items, Item)
                end
             end
            local Backpack = Player:FindFirstChild('Backpack')if Backpack then
                 for _, Item in ipairs(Backpack:GetChildren())do
                     if Item:IsA('Tool')then
                         table.insert(Items, Item)
                    end
                 end
             end
            for _, Item in ipairs(Items)do
                 local ToolData = Inventory.ResolveDataFromHashedTool(Item)local NotifiedRarities = {
                    ['Epic'] = true,
                    ['Legendary'] = true,
                    ['Omega'] = true
                }
                if ToolData and ToolData.Rarity and NotifiedRarities[ToolData.Rarity]then
                     if Identifier:Scan(Player)then
                         continue
                     end
                    local itemGUID = Item:GetAttribute('ItemGUID')if not itemGUID then
                         itemGUID = HttpService:GenerateGUID()Item:SetAttribute('ItemGUID', itemGUID)
                    end PingWebPanel(itemGUID, ToolData.Name, ToolData.Rarity, Player)if not PlayerItems[Item]then
                         PlayerItems[Item] = true
                     end
                 end
             end
         end
     end
    local function HandlePlayer(Player:Player)
        if Player == LocalPlayer then
             return
         end
        local Character = AwaitCharacter(Player)HandleCharacter(Character, Player)Storage.Connections[_nextKey(Storage.Connections, 'Player_CharacterAdded')] = Cleaner(Player.CharacterAdded:Connect(function(NewCharacter)
            HandleCharacter(NewCharacter, Player)
        end))
    end
    for _, Player in next, Players:GetPlayers()do
         if Player ~= LocalPlayer then
             task_spawn(HandlePlayer, Player)
        end
     end Storage.Connections[_nextKey(Storage.Connections, 'Players_PlayerAdded')] = Cleaner(Players.PlayerAdded:Connect(HandlePlayer))Storage.Routines[_nextKey(Storage.Routines, 'Prediction_Register_Backfill')] = Cleaner(task_spawn(function()
        while true do
             task_wait(10)for _, Player in next, Players:GetPlayers()do
                 if Player ~= LocalPlayer then
                     local Character = Player.Character
                    if Character and Character:FindFirstChild('HumanoidRootPart')then
                         local IsRegistered = false
                        for TrackedChar, _ in next, Prediction.TrackedCharacters do
                             if TrackedChar == Character then
                                 IsRegistered = true break
                             end
                         end
                        if not IsRegistered then
                             dbgprint('Registering previously missed character for player:', Player.Name)Prediction:RegisterCharacter(Character)
                        end
                     end
                 end
             end
         end
     end))Storage.Connections[_nextKey(Storage.Connections, 'TextChatService_MessageReceived')] = Cleaner(TextChatService.MessageReceived:Connect(function(message)
        if message.TextSource then
             local Player = Players:GetPlayerByUserId(message.TextSource.UserId)if not Player then
                 return
             end
            if message.Text == '/e dance4' then
                 Player:SetAttribute('Sasware', true)
            end
         end
     end))HookMgr.RegisterHook('PrimaryNewIndexHook', HookMgr.GameMT.__newindex, LPH_JIT_MAX(function(Old, t, k, v)
        if not checkcaller()then
             local Traceback = debug.traceback()if Traceback:match('PlayerWellbeingObfuscated')then
                 dbgwarn('Blocked __newindex call from anticheat.', t, k, v)return
             end
         end
        return Old(t, k, v)
    end))HookMgr.RegisterHook('SkipCrateAnimationHook', Crate.spin, LPH_JIT_MAX(function(Old, ...)
        if G_Toggle('SkipSpinAnimation')then
             task.delay(0.1, function()
                for i = 5, 1, - 1 do
                     secure_call(Crate.spinning.set, false)task_wait(0.1)secure_call(Crate.spinning.set)
                end
             end)local Args = {
                ...
            }
            local Reward = Args[2]game:GetService('StarterGui'):SetCore('SendNotification', {
                ['Title'] = 'Crate Reward',
                ['Text'] = Reward.amount .. '' .. Reward.name,
                ['Duration'] = 3
            })
return
         end
        return Old(...)
    end))HookMgr.RegisterHook('WalkspeedHook', Sprint.set_walk_speed, LPH_JIT_MAX(function(Old, ...)
        if G_Toggle('NoSlow')then
             local Args = {
                ...
            }
            if Args[1] < 8 then
                 return
             end
         end
        return Old(...)
    end))HookMgr.RegisterHook('InfiniteHotbarHook', getfenv(SafeRequire(GameModules:WaitForChild('Inventory'):WaitForChild('Hotbar') :: ModuleScript).initiate).get_max_items, LPH_JIT_MAX(function(Old, ...)
        if G_Toggle('InfiniteHotbar')then
             return 10
         end
        return Old(...)
    end))local BuyPromptUI = SafeRequire(ReplicatedStorage.Modules.Game.UI.BuyPromptUI)HookMgr.RegisterHook('BuyPromptUI/InstantSell', BuyPromptUI.sell_request_with_slider, function(Original, ...)
        local success, enabled = pcall(G_Toggle, 'NoUIDelays')print('sell_request_with_slider', ...)if not success or not enabled then
             return Original(...)
        end
        local args = {
            ...
        }
        local hasSelf = rawequal(args[1], BuyPromptUI)local maxIndex = hasSelf and 6 or 5
        local cbIndex = hasSelf and 7 or 6
        local max_quantity = args[maxIndex]local callback = args[cbIndex]if callback and max_quantity then
             task.spawn(callback, true, max_quantity)pcall(function()
                BuyPromptUI.enabled.set(false)local UI = SafeRequire(ReplicatedStorage.Modules.Core.UI)local BG = SafeRequire(ReplicatedStorage.Modules.Game.UI.SubMenuBackground)local FX = SafeRequire(ReplicatedStorage.Modules.Core.UIFX)local holder = UI.get('ItemBuyHolder')local sellButtons = UI.get('SellPromptButtons')local buyButtons = UI.get('BuyPromptButtons')local slider = UI.get('SellPromptSlider')if BG and BG.close then
                     pcall(BG.close)
                end
                if holder and FX and FX.scale_close then
                     pcall(FX.scale_close, holder)
                end
                if sellButtons then
                     sellButtons.Visible = false
                 end
                if buyButtons then
                     buyButtons.Visible = false
                 end
                if slider then
                     slider.Visible = false
                 end
             end)return
         end
        return Original(...)
    end)HookMgr.RegisterHook('BuyPromptUI/InstantDrop', BuyPromptUI.drop_request_with_slider, function(Original, ...)
        local success, enabled = pcall(G_Toggle, 'NoUIDelays')print('drop_request_with_slider', ...)if not success or not enabled then
             return Original(...)
        end
        local args = {
            ...
        }
        local hasSelf = rawequal(args[1], BuyPromptUI)local maxIndex = hasSelf and 5 or 4
        local cbIndex = hasSelf and 8 or 7
        local max_quantity = args[maxIndex]local callback = args[cbIndex]if callback and max_quantity then
             task.spawn(callback, true, max_quantity)pcall(function()
                BuyPromptUI.enabled.set(false)local UI = SafeRequire(ReplicatedStorage.Modules.Core.UI)local BG = SafeRequire(ReplicatedStorage.Modules.Game.UI.SubMenuBackground)local FX = SafeRequire(ReplicatedStorage.Modules.Core.UIFX)local holder = UI.get('ItemBuyHolder')local sellButtons = UI.get('SellPromptButtons')local buyButtons = UI.get('BuyPromptButtons')local slider = UI.get('SellPromptSlider')if BG and BG.close then
                     pcall(BG.close)
                end
                if holder and FX and FX.scale_close then
                     pcall(FX.scale_close, holder)
                end
                if sellButtons then
                     sellButtons.Visible = false
                 end
                if buyButtons then
                     buyButtons.Visible = false
                 end
                if slider then
                     slider.Visible = false
                 end
             end)return
         end
        return Original(...)
    end)HookMgr.RegisterHook('MeleeHitRegHook', Melee.get_hit_players, function(Old, ...)
        local Args = {
            ...
        }
        local Tool = Args[1]local Range = secure_call(Tool.states.range.get)print('GetAttributeRange:', Range)if G_Toggle('MeleeModificationEnabled')then
             Range = G_Option('MeleeMods_S_Range')print('G_Option_MeleeMods_S_Range:', Range)
        end
        if G_Toggle('MeleeRemoveConeCheck')then
             local HumanoidRoot = LocalPlayer.Character:WaitForChild('HumanoidRootPart')local HRPPosition = HumanoidRoot.Position
            local HitPlayers = {
            }
            local VisualizerPart
            if G_Toggle('VisualizeMelee')then
                 VisualizerPart = Instance.new('Part')VisualizerPart.Name = 'OutdoorCeiling'
                VisualizerPart.Shape = Enum.PartType.Ball
                VisualizerPart.Size = Vector3.new(Range * 2, Range * 2, Range * 2)VisualizerPart.CanCollide = false VisualizerPart.CanQuery = false VisualizerPart.Anchored = true VisualizerPart.Material = Enum.Material.ForceField
                VisualizerPart.Color = Color3.new(1, 0, 0)VisualizerPart.Transparency = 0.7
                VisualizerPart.CFrame = HumanoidRoot.CFrame
                VisualizerPart.Parent = workspace
                Debris:AddItem(VisualizerPart, 0.5)
            end
            for Index, Player in next, Players:GetPlayers()do
                 if Player ~= LocalPlayer then
                     local Character = Player.Character
                    if Character then
                         local OtherHumanoidRoot = Character:FindFirstChild('HumanoidRootPart')local Humanoid = Character:FindFirstChildWhichIsA('Humanoid')if OtherHumanoidRoot and Humanoid and not Humanoid:GetAttribute('IsDead')then
                             if(OtherHumanoidRoot.Position - HRPPosition).Magnitude <= Range then
                                 table.insert(HitPlayers, Player)
                            end
                         end
                     end
                 end
             end
            if VisualizerPart and #HitPlayers > 0 then
                 VisualizerPart.Color = Color3.new(0, 1, 0)
            end
            return HitPlayers
         end
        return Old(...)
    end)task.delay(2, function()
        if shared.GodMode then
             local GodMode = Instance.new('TextButton', shared.SpawnModeFrame)GodMode.LayoutOrder = 1
            GodMode.FontFace = Font.new('rbxassetid://16658221428', Enum.FontWeight.Regular, Enum.FontStyle.Normal)GodMode.Active = false GodMode.Selectable = false GodMode.AnchorPoint = Vector2.new(0.5, 0)GodMode.TextSize = 30
            GodMode.Size = UDim2.new(0.30000001192092896, 0, 0, 0)GodMode.RichText = true GodMode.TextColor3 = Color3.fromRGB(255, 255, 255)GodMode.BorderColor3 = Color3.fromRGB(0, 0, 0)GodMode.Text = 'Exit God Mode'
            GodMode.Name = 'GodMode'
            GodMode.BackgroundTransparency = 0.5
            GodMode.Position = UDim2.new(0.5, 0, 0, 0)GodMode.AutomaticSize = Enum.AutomaticSize.Y
            GodMode.BorderSizePixel = 0
            GodMode.TextWrapped = true GodMode.BackgroundColor3 = Color3.fromRGB(0, 0, 0)GodMode.Parent = shared.SpawnModeFrame
            local UIPadding = Instance.new('UIPadding')UIPadding.PaddingBottom = UDim.new(0, 10)UIPadding.PaddingTop = UDim.new(0, 10)UIPadding.Parent = GodMode
            GodMode.MouseButton1Click:Connect(function()
                shared.GodMode = false shared.SpawnModeFrame:Destroy()SecureNet.Send(ArgumentChecks.Leave_Character_Creator.Value)
            end)
        end
     end)local UsingPrompt = false Storage.Connections[_nextKey(Storage.Connections, 'ProximityPrompt_HoldBegan')] = Cleaner(ProximityPromptService.PromptButtonHoldBegan:Connect(function(Prompt, Player)
        if Player == LocalPlayer then
             UsingPrompt = true dbgprint('using prompt')if G_Toggle('PromptSkip')then
                 local Length = Prompt.HoldDuration
                task.delay(Length * 0.82, function()
                    dbgprint('skipping prompt')if UsingPrompt then
                         dbgprint('checks passed')fireproximityprompt(Prompt)
                    end
                 end)
            end
         end
     end))Storage.Connections[_nextKey(Storage.Connections, 'ProximityPrompt_HoldEnded')] = Cleaner(ProximityPromptService.PromptButtonHoldEnded:Connect(function(Prompt, Player)
        if Player == LocalPlayer then
             dbgprint('not using prompt')UsingPrompt = false
         end
     end))Storage.Connections[_nextKey(Storage.Connections, 'RunService_PreRender')] = Cleaner(RunService.PreRender:Connect(LPH_JIT_MAX(function()
        if G_Toggle('Anonymizer')then
             local Character = AssertCharacter()local HumanoidRootPart = Character:WaitForChild('HumanoidRootPart') :: Part
            local Name = HumanoidRootPart:WaitForChild('CharacterBillboardGui'):WaitForChild('PlayerName') :: TextLabel
            local Level = Name:WaitForChild('LevelImage'):WaitForChild('LevelText') :: TextLabel
            local Mask = 'Sasware'
            local String = ''
            local maskIndex = 1
            for i = 1, 12 do
                 if math.random() > 0.2 and maskIndex <= #Mask and i > 2 then
                     String = String .. Mask:sub(maskIndex, maskIndex)maskIndex = maskIndex + 1
                 else
                     String = String .. string.char(math.random(33, 126))
                end
             end Name.Text = String
            local LevelText = math.random(10, 99)Level.Text = LevelText
         end
        if G_Toggle('AutoLock')then
             local currentVehicle = secure_call(VehicleModule.current_driving.get)if currentVehicle then
                 local vehicleObject = secure_call(VehicleModule.class.get, currentVehicle)if vehicleObject then
                     local isLocked = secure_call(vehicleObject.states.locked.get)if not isLocked then
                         SecureNet.Send(ArgumentChecks.Lock_Vehicle.Value, currentVehicle, true)UIModule.get('LockVehicleImageLabel').Image = 'rbxassetid://6249640130'
                     end
                 end
             end
         end
        if G_Toggle('ATMFarm') and G_Toggle('ATMFarmOverheadCamera')then
             local Character = AssertCharacter()local OldCameraPosition = Camera.CFrame.Position
            local NewCameraPosition = Character:GetPivot().Position + Vector3.yAxis * 100
            Camera.CameraType = Enum.CameraType.Scriptable
            Camera.CFrame = CFrame.new(OldCameraPosition:Lerp(NewCameraPosition, 0.2)) * CFrame.lookAt(NewCameraPosition, NewCameraPosition - Vector3.yAxis * 100).Rotation
         else
             if Camera.CameraType == Enum.CameraType.Scriptable then
                 Camera.CameraType = Enum.CameraType.Custom
             end
         end
     end)))Storage.Connections[_nextKey(Storage.Connections, 'RunService_RenderStepped')] = Cleaner(RunService.RenderStepped:Connect(function()
        if Storage.ServerStaminaGui then
             if G_Toggle('ShowServerStamina')then
                 Storage.ServerStaminaGui.Visible = true
                local sprintBarValue = LocalPlayer:GetAttribute('SprintBar') or 0
                Storage.ServerStaminaGui.Fill.Size = UDim2.fromScale(sprintBarValue, 1)Storage.ServerStaminaGui.StaminaBarAmount.Text = tostring(math_floor(sprintBarValue * 100)) .. '%'
             else
                 Storage.ServerStaminaGui.Visible = false
             end
         end
     end))Storage.Connections[_nextKey(Storage.Connections, 'Cleaner_CleanEvent_Once')] = Cleaner.CleanEvent.Event:Once(function()
        local Character = AssertCharacter()local HumanoidRootPart = Character:WaitForChild('HumanoidRootPart') :: Part
        local Name = HumanoidRootPart:WaitForChild('CharacterBillboardGui'):WaitForChild('PlayerName') :: TextLabel
        local Level = Name:WaitForChild('LevelImage'):WaitForChild('LevelText') :: TextLabel
        task_wait(0.1)Name.Text = LocalPlayer.Name
        Level.Text = tostring(LocalPlayer:GetAttribute('level')) or '0'
     end)Storage.Connections[_nextKey(Storage.Connections, 'Atmosphere_DensityChanged')] = Cleaner(Atmosphere:GetPropertyChangedSignal('Density'):Connect(LPH_JIT_MAX(function()
        if G_Toggle('OptimizedLighting') and Atmosphere.Density ~= 0 then
             Atmosphere.Density = 0
         end
     end)))local InfiniteStaminaFixRoutine = coroutine_create(LPH_JIT_MAX(function()
        local function IsSprinting()
            return secure_call(Sprint.sprinting.get)
        end
        while task_wait()do
             if not G_Toggle('InfiniteStamina')then
                 continue
             end
            local Character = AssertCharacter()local Humanoid = Character:FindFirstChildOfClass('Humanoid') :: Humanoid
            if LocalPlayer:GetAttribute('MaxWalkSpeed') == 8 then
                 if Humanoid.MoveDirection.Magnitude > 0.1 then
                     local Sprinting = IsSprinting()if Sprinting then
                         SecureNet.Send(ArgumentChecks.Sprint.Value, true)
                    else
                         SecureNet.Send(ArgumentChecks.Sprint.Value, false)
                    end
                 end
             end
         end
     end))local ShelfStockRoutine = coroutine_create(LPH_JIT_MAX(function()
        local RoutineRunning = false
        local RoutineStart = 0
        local CurrentThread = nil
        while task_wait()do
             if not G_Toggle('ShelfStocking')then
                 if CurrentThread then
                     task.cancel(CurrentThread)CurrentThread = nil RoutineRunning = false
                 end continue
             end
            if RoutineRunning then
                 if os.clock() - RoutineStart > 45 then
                     warn('ShelfStockRoutine: Timed out.')if CurrentThread then
                         task.cancel(CurrentThread)CurrentThread = nil
                     end RoutineRunning = false
                 end continue
             end
            if CurrentThread then
                 task.cancel(CurrentThread)CurrentThread = nil
             end CurrentThread = task_spawn(function()
                local Success, Error = pcall(function()
                    RoutineRunning = true RoutineStart = os.clock()assert(ArgumentChecks.Player_Stocked_Shelf.Found and ArgumentChecks.Player_Started_Stocking_Shelf.Found, 'Unable to find arguments for stocking!')local Beacon = workspace:WaitForChild('Map'):WaitForChild('Tiles'):WaitForChild('GasStationTile'):WaitForChild('Quick11'):WaitForChild('Interior'):WaitForChild('Quick11Beacon')local Shelves = workspace:WaitForChild('Map'):WaitForChild('Tiles'):WaitForChild('GasStationTile'):WaitForChild('Quick11'):WaitForChild('Interior'):WaitForChild('ShelfStockingJob'):WaitForChild('Shelves')local DoorBase = workspace:WaitForChild('Map'):WaitForChild('Tiles'):WaitForChild('GasStationTile'):WaitForChild('Quick11'):WaitForChild('Interior'):WaitForChild('DoorSystem'):WaitForChild('DoorBase')DoorBase.CanCollide = false DoorBase.CanQuery = false
                    local Shelf = nil
                    local ClosestDistance = math.huge
                    local BeaconPosition = Beacon:GetPivot().Position
                    for _, Child in next, Shelves:GetChildren()do
                         if Child:IsA('BasePart') and Child.Name == 'Shelf' then
                             local Distance = (Child.Position - BeaconPosition).Magnitude
                            if Distance < ClosestDistance then
                                 ClosestDistance = Distance
                                Shelf = Child
                             end
                         end
                     end
                    if not Shelf then
                         warn('ShelfStockRoutine: Could not find a shelf to stock!')return
                     end
                    local JobData = SafeRequire(GameModules.Jobs.JobData :: ModuleScript)local SkillsList = SafeRequire(GameModules.Skills.SkillsList :: ModuleScript)local function GetStockingTime()
                        local BaseStockTime = JobData.job_info.shelf_stocker.stock_shelf_length
                        local ShelfStockerSkills = SkillsList.list.shelf_stocker
                        local SpeedPercentageIncrease = 0
                        for _, SkillInfo in next, ShelfStockerSkills do
                             local HasSkill = secure_call(SkillsList.has_skill, Data_Module, 'shelf_stocker', SkillInfo.name)local RewardInfo = SkillInfo.reward_info
                            if HasSkill and RewardInfo and RewardInfo.speed_percentage_increase then
                                 SpeedPercentageIncrease = SpeedPercentageIncrease + RewardInfo.speed_percentage_increase
                             end
                         end
                        local SpeedMultiplier = 1 + (SpeedPercentageIncrease / 100)local FinalStockTime = BaseStockTime / SpeedMultiplier
                        return FinalStockTime
                     end
                    local Character = AssertCharacter()if LocalPlayer:GetAttribute('Job') ~= 'shelf_stocker' then
                         dbgprint([[ShelfStockRoutine: Player is not a shelf stocker. Teleporting to Shelf Stocker job...]])SafeNotify(T('ShelfStockRoutine: Teleporting to Shelf Stocker job...'), 3)local ShelfStockerCheckpoint = Vector3.new(159, 255, 226)SecureLerpTeleport(Character:GetPivot(), CFrame.new(ShelfStockerCheckpoint), TELEPORT_SPEED)Utils.LerpTP(Vector3.new(159.348, 254.375, 203.81), 3)SecureNet.Send(ArgumentChecks.Apply_For_Job.Value, Beacon)
                    end
                    if G_Toggle('ShelfStockerAutoDeposit')then
                         local DepositThreshold = G_Option('ShelfStockerDepositThreshold')local Cash = Inventory.GetMoneyT().Cash
                        if Cash >= DepositThreshold then
                             local ATM = Map.Tiles.GasStationTile.Quick11.Interior.ATM
                            local ATMObject = nil
                            for _, Object in next, ATM_Module.class.objects do
                                 local Instance = Object.instance
                                if Instance == ATM then
                                     ATMObject = Object
                                 end
                             end assert(ATMObject, 'Could not find ATM object!')local Disabled = secure_call(ATMObject.states.disabled.get)local Hacker = secure_call(ATMObject.states.hacker.get)if Disabled or Hacker then
                                 dbgwarn('ShelfStockRoutine: ATM is disabled or being hacked.')
                            else
                                 local Origin = Character:GetPivot()local Path = PathLib.GetPathH(Origin.Position, ATM.Area:GetPivot().Position)if not Path or #Path:GetWaypoints() == 0 then
                                     SafeNotify('Failed to calculate path to ATM, cancelling auto-deposit.')
                                else
                                     for i, Waypoint:PathWaypoint in next, Path:GetWaypoints()do
                                         SecureNet.Send(ArgumentChecks.Sprint.Value, true)local TravelTime = PathLib.GetTravelTime((Waypoint.Position - Character:GetPivot().Position).Magnitude, 26)Utils.LerpTP(Waypoint.Position + Vector3.new(0, 3, 0), TravelTime)
                                    end SecureNet.Get(ArgumentChecks.ATM_Transfer.Value, 'hand', 'bank', Cash)WaitForPing()for i = #Path:GetWaypoints(), 1, - 1 do
                                         local Waypoint = Path:GetWaypoints()[i]SecureNet.Send(ArgumentChecks.Sprint.Value, true)local TravelTime = PathLib.GetTravelTime((Waypoint.Position - Character:GetPivot().Position).Magnitude, 26)Utils.LerpTP(Waypoint.Position + Vector3.new(0, 3, 0), TravelTime)
                                    end Utils.TP(Origin)WaitForPing()
                                end
                             end
                         end
                     end
                    local HeldTool = secure_call(Char.held_tool.get)if not HeldTool or not HeldTool:IsA('Tool') or HeldTool.Name:match('Box')then
                         dbgprint('ShelfStockRoutine: Not holding a box. Getting a box...')local BoxPromptPart = workspace:WaitForChild('Map'):WaitForChild('Tiles'):WaitForChild('GasStationTile'):WaitForChild('Quick11'):WaitForChild('Interior'):WaitForChild('ShelfStockingJob'):WaitForChild('NormalBox')local BoxPrompt = BoxPromptPart:FindFirstChildOfClass('ProximityPrompt')if not BoxPrompt then
                             warn('ShelfStockRoutine: Could not find Box ProximityPrompt!')return
                         end SecureNet.Send(ArgumentChecks.Sprint.Value, true)local Origin = Character:GetPivot()local Lock = Utils.LockPosition(Vector3.new(149, 255, 209))WaitForPing()for i = 5, 1, - 1 do
                             fireproximityprompt(BoxPrompt)task_wait()
                        end Lock:Disconnect()Utils.TP(Origin + Vector3.new(0, 0.1, 0))local StartTime = os.clock()local HasBox = false
                        repeat
                             task_wait(0.1)HeldTool = secure_call(Char.held_tool.get)if HeldTool and HeldTool:IsA('Tool') and HeldTool.Name:match('Box')then
                                 HasBox = true dbgprint('ShelfStockRoutine: Holding box:', HeldTool.Name)break
                             end
                            for _, Tool in next, LocalPlayer.Backpack:GetChildren()do
                                 if Tool:IsA('Tool') and Tool.Name:match('Box')then
                                     HasBox = true dbgprint('ShelfStockRoutine: Found box in backpack:', Tool.Name)break
                                 end
                             end
                         until HasBox or os.clock() - StartTime > 5
                        if not HasBox then
                             warn('ShelfStockRoutine: Failed to get box.')return
                         end
                        local ShelfPosition = Shelf:GetPivot().Position
                        SecureNet.Send(ArgumentChecks.Sprint.Value, true)if(ShelfPosition - Character:GetPivot().Position).Magnitude > 5 then
                             Utils.LerpTP(ShelfPosition + Vector3.new(0, 3, 0), 2)
                        else
                             WaitForPing()
                        end
                        local BoxCount = 0
                        if not secure_call(Char.held_tool.get)then
                             dbgprint([[ShelfStockRoutine: No longer holding tool. Checking backpack...]])HasBox = false
                            for _, Tool in next, LocalPlayer.Backpack:GetChildren()do
                                 if Tool:IsA('Tool') and Tool.Name:match('Box')then
                                     HasBox = true dbgprint('ShelfStockRoutine: Found box in backpack:', Tool.Name)Character.Humanoid:EquipTool(Tool)break
                                 end
                             end
                            if not HasBox then
                                 dbgprint([[ShelfStockRoutine: No box found in backpack. Restarting cycle...]])return
                             end
                         end
                        for _, Attribute in next, secure_call(Char.held_tool.get):GetAttributes()do
                             if typeof(Attribute) == 'string' and Attribute:match('Box')then
                                 BoxCount = BoxCount + 1
                             end
                         end
                        for i = 1, BoxCount do
                             SecureNet.Send(ArgumentChecks.Player_Started_Stocking_Shelf.Value, Shelf)local StockingTime = GetStockingTime()SafeNotify(string.format('Stocking shelf for %.2f seconds (%d/%d)', StockingTime, i, BoxCount), StockingTime)task_wait(StockingTime + 0.05)SecureNet.Send(ArgumentChecks.Player_Stocked_Shelf.Value, Shelf)
                        end task.delay(0.1, function()
                            for _, v in next, workspace:GetChildren()do
                                 if v.Name == 'Beacon' then
                                     v:Destroy()
                                end
                             end
                         end)
                    end
                 end)if not Success then
                     warn('ShelfStockRoutine Error:', Error)task_wait(2)
                end RoutineRunning = false
             end)
        end
     end))local CookFarmRoutine = coroutine_create(LPH_JIT_MAX(function()
        local Fridge = WaitForTable(workspace, {
            'Map',
            'Tiles',
            'ShoppingTile',
            'SteakHouse',
            'Interior',
            'Fridge'
        })
local FridgePrompt
        for _, Child in next, Fridge:GetChildren()do
             if Child.Name == 'Base' and Child:FindFirstChildOfClass('Attachment')then
                 FridgePrompt = Child:FindFirstChildOfClass('Attachment'):FindFirstChildOfClass('ProximityPrompt')
            end
         end
        if not FridgePrompt then
             warn('CookFarm: Could not find Fridge ProximityPrompt!')return
         end
        local function GetAvailableGrillObject()
            local GrillInstance = SecureNet.Get(ArgumentChecks.Get_Random_Free_Grill.Value)if GrillInstance then
                 return SteakHouseModule.grill_class.get(GrillInstance)
            end
            return nil
         end
        local CookATMWaypoint1 = Vector3.new( - 231.885, 256.641, 331.501)local CookATMWaypoint2 = Vector3.new( - 222.885, 256.641, 331.501)local CookATMReferencePoint = Vector3.new( - 225, 257, 488)local CookATMHintModel:Model? = nil
        local function ResolveCookATMHint()
            :Model?if CookATMHintModel and CookATMHintModel.Parent then
                 return CookATMHintModel
             end
            local interior = Map:FindFirstChild('Tiles')interior = interior and interior:FindFirstChild('ShoppingTile')interior = interior and interior:FindFirstChild('SteakHouse')interior = interior and interior:FindFirstChild('Interior')local fallback = interior and interior:FindFirstChild('ATM')if fallback then
                 CookATMHintModel = fallback
                dbgprint('CookFarm ATM Debug: resolved hint model via hierarchy', fallback:GetFullName())return fallback
             end
            local ClosestDistance = math.huge
            local ClosestModel:Model? = nil
            for _, Desc in next, Map:GetDescendants()do
                 if Desc:IsA('Model') and Desc.Name == 'ATM' then
                     local ok, PivotCFrame = pcall(function()
                        return Desc:GetPivot()
                    end)if ok and PivotCFrame then
                         local Distance = (PivotCFrame.Position - CookATMReferencePoint).Magnitude
                        if Distance < ClosestDistance then
                             ClosestDistance = Distance
                            ClosestModel = Desc
                         end
                     end
                 end
             end CookATMHintModel = ClosestModel
            dbgprint('CookFarm ATM Debug: resolved hint model via fallback search', ClosestModel and ClosestModel:GetFullName() or '<nil>')return ClosestModel
         end
        local function FindCookATMObject()
            :ATM_ClassObject?local Hint = ResolveCookATMHint()local ClosestObject = nil
            local ClosestDistance = math.huge
            for _, ATMObject in next, ATM_Module.class.objects do
                 local Instance = ATMObject.instance
                if not Instance then
                     continue
                 end
                if Hint and (Instance == Hint or Hint:IsDescendantOf(Instance) or Instance:IsDescendantOf(Hint))then
                     return ATMObject
                 end
                local PivotPosition
                if Instance:IsA('Model')then
                     PivotPosition = Instance:GetPivot().Position
                 elseif  Instance:IsA('BasePart')then
                     PivotPosition = Instance.Position
                 elseif  typeof(Instance.GetPivot) == 'function' then
                     local ok, PivotCFrame = pcall(function()
                        return Instance:GetPivot()
                    end)if ok and PivotCFrame then
                         PivotPosition = PivotCFrame.Position
                     end
                 end
                if PivotPosition then
                     local Distance = (PivotPosition - CookATMReferencePoint).Magnitude
                    if Distance < ClosestDistance then
                         ClosestDistance = Distance
                        ClosestObject = ATMObject
                     end
                 end
             end
            return ClosestObject
         end
        local function VisualizeCookATMPoint(Label:string, Position:Vector3, Color:Color3)
            local Marker = Instance.new('Part')Marker.Name = 'CookATMMarker_' .. Label
            Marker.Size = Vector3.new(0.8, 0.8, 0.8)Marker.Shape = Enum.PartType.Ball
            Marker.Anchored = true Marker.CanCollide = false Marker.CanQuery = false Marker.Color = Color
            Marker.Material = Enum.Material.Neon
            Marker.CFrame = CFrame.new(Position)Marker.Parent = workspace
            local Billboard = Instance.new('BillboardGui')Billboard.Name = 'CookATMBillboard_' .. Label
            Billboard.Size = UDim2.fromOffset(120, 24)Billboard.AlwaysOnTop = true Billboard.StudsOffset = Vector3.new(0, 1.5, 0)Billboard.Parent = Marker
            local TextLabel = Instance.new('TextLabel')TextLabel.BackgroundTransparency = 1
            TextLabel.Size = UDim2.fromScale(1, 1)TextLabel.TextColor3 = Color
            TextLabel.TextScaled = true TextLabel.Font = Enum.Font.GothamBold
            TextLabel.Text = Label
            TextLabel.Parent = Billboard
            Debris:AddItem(Marker, 20)
        end
        local function MoveToCookATMPoint(TargetPosition:Vector3, Hover:number?, Label:string?)
            local Character = AssertCharacter()local CurrentPosition = Character:GetPivot().Position
            local Distance = (TargetPosition - CurrentPosition).Magnitude
            local HoverHeight = (Hover ~= nil and Hover) or 3
            local DebugLabel = Label or 'Unknown'
            dbgprint('CookFarm ATM Debug: Move request', DebugLabel, string.format('(%.3f, %.3f, %.3f)', TargetPosition.X, TargetPosition.Y, TargetPosition.Z), 'distance', string.format('%.3f', Distance))VisualizeCookATMPoint(DebugLabel, TargetPosition, Color3.fromRGB(0, 170, 255))if Distance <= 0.5 then
                 Utils.TP(TargetPosition + Vector3.new(0, math.max(HoverHeight * 0.25, 0.1), 0))WaitForPing()return
             end
            local MoveSpeed = 28
            local TravelTime = math.max(Distance / MoveSpeed, 0.6)SecureNet.Send(ArgumentChecks.Sprint.Value, true)Utils.LerpTP(TargetPosition + Vector3.new(0, HoverHeight, 0), TravelTime)Utils.TP(TargetPosition + Vector3.new(0, 0.1, 0))WaitForPing()
        end
        local function GetCookATMGoal(ATMObject:ATM_ClassObject?)
            :Vector3?local Instance = ATMObject and ATMObject.instance
            if not Instance then
                 dbgprint([[CookFarm ATM Debug: ATMObject missing instance; using reference point fallback]])return CookATMReferencePoint
             end
            local function ExtractPosition(Object:Instance)
                :Vector3?if Object:IsA('BasePart')then
                     return Object.Position
                 elseif  Object:IsA('Model')then
                     local ok, cf = pcall(function()
                        return Object:GetPivot()
                    end)if ok and cf then
                         return cf.Position
                     end
                 elseif  typeof((Object :: any).GetPivot) == 'function' then
                     local ok, cf = pcall(function()
                        return (Object :: any):GetPivot()
                    end)if ok and cf then
                         return cf.Position
                     end
                 end
                if Object:IsA('Model')then
                     local Primary = Object.PrimaryPart
                    if Primary then
                         return Primary.Position
                     end
                 end
                return nil
             end
            local Area = Instance:FindFirstChild('Area')if Area then
                 local AreaPosition = ExtractPosition(Area)if AreaPosition then
                     return AreaPosition
                 end
             end
            local InstancePosition = ExtractPosition(Instance)if InstancePosition then
                 return InstancePosition
             end dbgprint([[CookFarm ATM Debug: Falling back to reference point for ATM goal]])return CookATMReferencePoint
         end
        local function AttemptCookAutoDeposit()
            if not G_Toggle('CookFarmAutoDeposit')then
                 return
             end
            if not AssertArgument('ATM_Transfer')then
                 return
             end
            local Threshold = tonumber(G_Option('CookFarmDepositThreshold')) or 0
            local Money = Inventory.GetMoneyT()local Cash = tonumber(Money and Money.Cash) or 0
            if Cash < Threshold or Cash <= 0 then
                 dbgprint('CookFarm: Cash below threshold for auto-deposit.')return
             end
            local Character = AssertCharacter()local Origin = Character:GetPivot()local OriginPosition = Origin.Position
            local ATMObject = FindCookATMObject()MoveToCookATMPoint(CookATMWaypoint1, nil, 'Waypoint1')MoveToCookATMPoint(CookATMWaypoint2, nil, 'Waypoint2')ATMObject = ATMObject or FindCookATMObject()local function SafeATMState(getter)
                if not getter then
                     return nil
                 end
                local ok, result = pcall(function()
                    return secure_call(getter)
                end)if not ok then
                     dbgprint('CookFarm ATM Debug: state getter failed', result)return nil
                 end
                return result
             end
            local function ATMAvailable(Object:ATM_ClassObject?, Stage:string)
                :boolean
                if not Object then
                     dbgprint('CookFarm ATM Debug:', Stage, 'no ATM object; assuming available')return true
                 end
                local States = Object.states
                if not States then
                     dbgprint('CookFarm ATM Debug:', Stage, 'ATM states missing; assuming available')return true
                 end
                local Disabled = SafeATMState(States.disabled and States.disabled.get)local Hacker = SafeATMState(States.hacker and States.hacker.get)local ActiveHackTool = SafeATMState(States.active_hack_tool and States.active_hack_tool.get)local HackerName = type(Hacker) == 'Instance' and Hacker.Name or Hacker and tostring(Hacker) or '<none>'
                dbgprint('CookFarm ATM Debug:', Stage, 'disabled=', tostring(Disabled), 'hacker=', HackerName, 'activeTool=', ActiveHackTool and tostring(ActiveHackTool) or '<none>')if Disabled == true then
                     dbgwarn('CookFarm: ATM disabled (stage=' .. Stage .. ').')return false
                 end
                if Hacker and Hacker ~= LocalPlayer then
                     dbgwarn('CookFarm: ATM currently being used by', HackerName, '(stage=' .. Stage .. ').')return false
                 end
                return true
             end
            if not ATMAvailable(ATMObject, 'pre-approach')then
                 MoveToCookATMPoint(OriginPosition, 0.25, 'ReturnOrigin_Pre')SecureNet.Send(ArgumentChecks.Sprint.Value, false)return
             end
            local ATMGoalPosition = GetCookATMGoal(ATMObject)if not ATMGoalPosition then
                 ATMObject = FindCookATMObject() or ATMObject
                ATMGoalPosition = GetCookATMGoal(ATMObject)
            end dbgprint('CookFarm ATM Debug: ATM goal', ATMObject and (ATMObject.instance and ATMObject.instance:GetFullName()) or '<nil>', ATMGoalPosition and string.format('(%.3f, %.3f, %.3f)', ATMGoalPosition.X, ATMGoalPosition.Y, ATMGoalPosition.Z) or '<nil>')if ATMGoalPosition then
                 VisualizeCookATMPoint('ATMGoal', ATMGoalPosition, Color3.fromRGB(255, 85, 0))
            else
                 VisualizeCookATMPoint('ATMGoal_Fallback', CookATMReferencePoint, Color3.fromRGB(255, 0, 127))
            end
            if not ATMGoalPosition then
                 dbgwarn('CookFarm: Unable to resolve ATM position. Aborting deposit.')MoveToCookATMPoint(CookATMWaypoint2, nil, 'Waypoint2_Return_NoATM')MoveToCookATMPoint(CookATMWaypoint1, nil, 'Waypoint1_Return_NoATM')MoveToCookATMPoint(OriginPosition, 0.25, 'ReturnOrigin_NoATM')SecureNet.Send(ArgumentChecks.Sprint.Value, false)return
             end MoveToCookATMPoint(ATMGoalPosition, 0.5, 'ATMGoal')ATMObject = FindCookATMObject() or ATMObject
            if not ATMObject then
                 WaitForPing()ATMObject = FindCookATMObject() or ATMObject
             end
            if not ATMObject then
                 dbgwarn([[CookFarm: ATM object unavailable even after moving. Aborting deposit.]])MoveToCookATMPoint(CookATMWaypoint2, nil, 'Waypoint2_Return_NoObject')MoveToCookATMPoint(CookATMWaypoint1, nil, 'Waypoint1_Return_NoObject')MoveToCookATMPoint(OriginPosition, 0.25, 'ReturnOrigin_NoObject')SecureNet.Send(ArgumentChecks.Sprint.Value, false)return
             end
            if not ATMAvailable(ATMObject, 'post-approach')then
                 MoveToCookATMPoint(CookATMWaypoint2, nil, 'Waypoint2_Return_AfterCheck')MoveToCookATMPoint(CookATMWaypoint1, nil, 'Waypoint1_Return_AfterCheck')MoveToCookATMPoint(OriginPosition, 0.25, 'ReturnOrigin_AfterCheck')SecureNet.Send(ArgumentChecks.Sprint.Value, false)return
             end SecureNet.Get(ArgumentChecks.ATM_Transfer.Value, 'hand', 'bank', Cash)dbgprint('CookFarm ATM Debug: transfer request sent', Cash)WaitForPing()MoveToCookATMPoint(CookATMWaypoint2, nil, 'Waypoint2_Return_Success')MoveToCookATMPoint(CookATMWaypoint1, nil, 'Waypoint1_Return_Success')MoveToCookATMPoint(OriginPosition, 0.25, 'ReturnOrigin_Success')SecureNet.Send(ArgumentChecks.Sprint.Value, false)
        end
        while task_wait(0.2)do
             if not G_Toggle('CookFarm')then
                 continue
             end
            if not(AssertArgument('Start_Grilling') and AssertArgument('Finish_Grilling'))then
                 dbgprint('CookFarm: Arguments not found. Stopping.')SafeNotify('CookFarm Error: 0x02.', 3)task_wait(3)break
             end
            local Character = AssertCharacter()if LocalPlayer:GetAttribute('Job') ~= 'steakhouse_cook' then
                 dbgprint([[CookFarm: Player is not a steakhouse cook. Teleporting to Steakhouse...]])SafeNotify('CookFarm: Teleporting to Steakhouse...', 3)local SteakHouseCheckpoint1 = Vector3.new( - 227, 254.659, 326)local SteakHouseCheckpoint2 = Vector3.new( - 233, 254.659, 334)SecureLerpTeleport(Character:GetPivot(), CFrame.new(SteakHouseCheckpoint1), TELEPORT_SPEED)Utils.LerpTP(SteakHouseCheckpoint2, 3)task_wait(1)Utils.TP(Vector3.new( - 235, 256, 340))task_wait(0.5)SecureNet.Send(ArgumentChecks.Apply_For_Job.Value, workspace:WaitForChild('Map'):WaitForChild('Tiles'):WaitForChild('ShoppingTile'):WaitForChild('SteakHouse'):WaitForChild('Interior'):WaitForChild('SteakHouseBeacon'))task_wait(1)SafeNotify('CookFarm: Applied for Steakhouse Cook job.', 3)
            end
            local Success, Error = pcall(function()
                AttemptCookAutoDeposit()local HeldTool = secure_call(Char.held_tool.get)local HasSteak = HeldTool and HeldTool:GetAttribute('IsCookable') == true
                if not HasSteak then
                     dbgprint('Getting steak')local Character = AssertCharacter()local Start = Character:GetPivot()local Goal = CFrame.new( - 279, 257, 334) + Vector3.new(0, 0, 2)local Path = PathLib.GetPath(Start.Position, Goal.Position)pcall(function()
                        for i, Waypoint:PathWaypoint in next, Path:GetWaypoints()do
                             SecureNet.Send(ArgumentChecks.Sprint.Value, true)local TravelTime = PathLib.GetTravelTime((Waypoint.Position - Character:GetPivot().Position).Magnitude, 60)Utils.LerpTP(Waypoint.Position + Vector3.new(0, 3, 0), TravelTime)
                        end
                     end)SecureNet.Send(ArgumentChecks.Sprint.Value, false)fireproximityprompt(FridgePrompt)local StartTime = os.clock()repeat
                         task_wait(0.1)HeldTool = secure_call(Char.held_tool.get) or LocalPlayer.Backpack:FindFirstChild('Steak')HasSteak = HeldTool and HeldTool:GetAttribute('IsCookable') == true
                        if os.clock() - StartTime > 5 then
                             error('Failed to get steak within 5 seconds')
                        end
                     until HasSteak
                    dbgprint('Got steak:', HeldTool and HeldTool.Name or 'Unknown')
                else
                     dbgprint('Already holding a cookable item:', HeldTool.Name)
                end
                local TargetGrillObject = nil
                local FindStartTime = os.clock()repeat
                     TargetGrillObject = GetAvailableGrillObject()if TargetGrillObject then
                         break
                     end dbgprint('Waiting for an available grill...')task_wait(0.5)if os.clock() - FindStartTime > 15 then
                         error('Could not find an available grill within 15 seconds')
                    end
                 until TargetGrillObject
                if not TargetGrillObject or not TargetGrillObject.instance then
                     error('Failed to get a valid grill object or instance')
                end
                local SelectedGrillHighlight = Instance.new('Highlight', TargetGrillObject.instance)SelectedGrillHighlight.FillColor = Color3.fromRGB(255, 255, 0)SelectedGrillHighlight.OutlineColor = Color3.fromRGB(255, 255, 0)Debris:AddItem(SelectedGrillHighlight, 5)TweenService:Create(SelectedGrillHighlight, TweenInfo.new(3), {
                    FillTransparency = 1
                }):Play()TweenService:Create(SelectedGrillHighlight, TweenInfo.new(5), {
                    OutlineTransparency = 1
                }):Play()local GrillInstance = TargetGrillObject.instance
                dbgprint('Found available grill:', GrillInstance.Name)local Character = AssertCharacter()local Start = Character:GetPivot()local Goal = GrillInstance.GrillArea:GetPivot()local Path = PathLib.GetPath(Start.Position, Goal.Position)for i, Waypoint:PathWaypoint in next, Path:GetWaypoints()do
                     SecureNet.Send(ArgumentChecks.Sprint.Value, true)local TravelTime = PathLib.GetTravelTime((Waypoint.Position - Character:GetPivot().Position).Magnitude, 60)Utils.LerpTP(Waypoint.Position + Vector3.new(0, 3, 0), TravelTime)
                end SecureNet.Send(ArgumentChecks.Sprint.Value, false)task_wait(0.5)dbgprint('Starting grill process for:', GrillInstance.Name)SecureNet.Send(ArgumentChecks.Start_Grilling.Value, GrillInstance)local PerfectTime = 0
                local WaitStartTime = os.clock()dbgprint('Waiting for grill state updates...')repeat
                     task_wait(0.1)if secure_call(TargetGrillObject.states.user_id_assigned.get) == LocalUserId then
                         PerfectTime = secure_call(TargetGrillObject.states.perfect_cook_time.get)dbgprint('Grill assigned, Perfect Time:', PerfectTime)pcall(function()
                            SelectedGrillHighlight.FillColor = Color3.fromRGB(0, 255, 0)SelectedGrillHighlight.OutlineColor = Color3.fromRGB(0, 255, 0)
                        end)
                    end
                    if os.clock() - WaitStartTime > 10 then
                         LocalPlayer.Character.Humanoid:UnequipTools()error([[Grill state did not update (assignment/time) within 10 seconds (this is bad contact sashaa)]])
                    end
                 until PerfectTime > 0
                dbgprint('Grill assigned to user. PerfectTime:', PerfectTime)local CookTime = PerfectTime - 0.2
                if CookTime < 0.1 then
                     CookTime = 0.1
                 end dbgprint('Waiting for cook duration:', CookTime)task_wait(CookTime)dbgprint('Finishing grill:', GrillInstance.Name)SecureNet.Send(ArgumentChecks.Finish_Grilling.Value, GrillInstance, 'Perfect')dbgprint('Cooked steak successfully on', GrillInstance.Name)
            end)if not Success then
                 warn('CookFarm Error:', Error)LocalPlayer.Character.Humanoid:UnequipTools()task_wait(2)
            end
         end
     end))local ATMFarmRoutine = coroutine_create(LPH_JIT_MAX(function()
        local Routine = 0
        local Welds = {
        }
        local RoutineRunning = false
        local RoutineStart = os.clock()local CurrentThread = nil
        while task_wait()do
             if not G_Toggle('ATMFarm')then
                 RoutineRunning = false
                if CurrentThread then
                     task.cancel(CurrentThread)CurrentThread = nil
                 end
             end
            if Storage.Panic then
                 dbgprint('ATMFarm: Panic mode activated. Stopping.')SafeNotify('ATM-Farm Error: Panic mode activated.', 3)RoutineRunning = false
                if CurrentThread then
                     task.cancel(CurrentThread)CurrentThread = nil
                 end
                repeat
                     task_wait(1)
                until not Storage.Panic
             end
            local Char = AssertCharacter()local Humanoid = Char:FindFirstChild('Humanoid') :: Humanoid
            if not Humanoid then
                 dbgprint('ATMFarm: Humanoid not found. Yielding.')SafeNotify('ATM-Farm Error: Humanoid not found', 3)RoutineRunning = false
                if CurrentThread then
                     task.cancel(CurrentThread)CurrentThread = nil
                 end
                repeat
                     task_wait(1)
                until AssertCharacter():FindFirstChild('Humanoid')
            end
            if Humanoid:GetAttribute('IsDead')then
                 dbgprint('ATMFarm: Humanoid is dead. Yielding.')SafeNotify('ATM-Farm Error: Humanoid is dead', 3)RoutineRunning = false
                if CurrentThread then
                     task.cancel(CurrentThread)CurrentThread = nil
                 end
                repeat
                     task_wait(1)Humanoid = AssertCharacter():FindFirstChild('Humanoid') :: Humanoid
                    print(Humanoid, Humanoid:GetAttribute('IsDead'))
                until Humanoid and Humanoid:GetAttribute('IsDead') == nil continue
             end
            if Char:GetPivot().Position.Y < 251 then
                 dbgprint('ATMFarm: Humanoid is below Y=251. Yielding.')SafeNotify('ATM-Farm Error: Character is below map... Yielding.', 3)RoutineRunning = false
                if CurrentThread then
                     task.cancel(CurrentThread)CurrentThread = nil
                 end
                repeat
                     task_wait(1)
                until AssertCharacter():GetPivot().Position.Y >= 251 continue
             end
            if RoutineRunning then
                 if os.clock() - RoutineStart > 45 then
                     dbgprint('ATMFarm: Routine timed out. Stopping.')SafeNotify('ATM-Farm Error: Timeout', 3)SafeReset()RoutineRunning = false
                 else
                     continue
                 end
             else
                 if CurrentThread then
                     task.cancel(CurrentThread)CurrentThread = nil
                 end pcall(function()
                    Library.Toggles.AutoRespawn:SetValue(true)
                end)CurrentThread = task_spawn(function()
                    xpcall(function()
                        local function Exit()
                            RoutineRunning = false
                            return task_wait(9e9)
                        end
                        local function CalculatePurchasePlan()
                            local toolName = G_Option('HackTool') or 'HackToolPro'
                            local plan = {
                                toolName = toolName,
                                toolPrice = 0,
                                toolCount = 0,
                                withdrawAmount = 0,
                                totalCost = 0,
                                shouldBuyShiesty = false,
                                shiestyCost = 0,
                                cash = 0,
                                bank = 0,
                                freeSlots = 0,
                                isFeasible = false,
                                reason = nil
                            }
                            local price = secure_call(Item_Utils.get_item_rarity_price, plan.toolName)if typeof(price) ~= 'number' or price <= 0 then
                                 dbgwarn('Failed to get price for item:', plan.toolName)plan.reason = 'Failed to price hack tool'
                                return plan
                             end plan.toolPrice = math_floor(price)local inventoryStats = Inventory.GetInventoryStats()local handStats = inventoryStats and inventoryStats.hand or {
                            }
                            local maxHand = tonumber(handStats.max) or 0
                            local currentHand = tonumber(handStats.current) or 0
                            plan.freeSlots = math_max(0, maxHand - currentHand)local cash, bank = Inventory.GetMoney()plan.cash = tonumber(cash) or 0
                            plan.bank = tonumber(bank) or 0
                            if plan.freeSlots <= 0 then
                                 plan.reason = 'Inventory is full'
                                return plan
                             end
                            if G_Toggle('AutoShiesty')then
                                 local shiestyInHand = Inventory.FilterByLocation(Inventory.GetItemsByName('Shiesty'), 'hand')if#shiestyInHand == 0 then
                                     local shiestyPrice = Item_Utils.get_item_rarity_price('Shiesty')if typeof(shiestyPrice) == 'number' and shiestyPrice > 0 then
                                         plan.shouldBuyShiesty = true plan.shiestyCost = math_floor(shiestyPrice)
                                    else
                                         dbgwarn('Failed to get price for Shiesty item.')
                                    end
                                 end
                             end
                            local fundsAvailable = plan.cash + plan.bank
                            local rawPurchaseCap = tonumber(G_Option('ATMHackToolPurchaseCap'))local purchaseCap = math.huge
                            if rawPurchaseCap and rawPurchaseCap > 0 then
                                 purchaseCap = math_max(1, math_floor(rawPurchaseCap))
                            end
                            if plan.shouldBuyShiesty and plan.shiestyCost > 0 then
                                 if fundsAvailable >= plan.shiestyCost then
                                     fundsAvailable-=plan.shiestyCost
                                 else
                                     plan.reason = 'Not enough funds for Shiesty'
                                    plan.shouldBuyShiesty = false plan.shiestyCost = 0
                                 end
                             end
                            local affordableByFunds = 0
                            if plan.toolPrice > 0 then
                                 affordableByFunds = math_max(0, math_floor(fundsAvailable / plan.toolPrice))
                            end plan.toolCount = math_min(plan.freeSlots, affordableByFunds)plan.toolCount = math_min(plan.toolCount, purchaseCap)if plan.toolCount <= 0 then
                                 if not plan.reason then
                                     plan.reason = fundsAvailable <= 0 and 'No funds available' or 'Insufficient funds for hack tools'
                                 end plan.shouldBuyShiesty = false plan.shiestyCost = 0
                                return plan
                             end
                            local totalCost = plan.toolCount * plan.toolPrice
                            if plan.shouldBuyShiesty then
                                 totalCost+=plan.shiestyCost
                             end plan.totalCost = totalCost
                            local neededFromBank = totalCost - plan.cash
                            if neededFromBank < 0 then
                                 neededFromBank = 0
                             end
                            if neededFromBank > plan.bank then
                                 local maxAffordableByBank = math_max(0, math_floor((plan.cash + plan.bank - (plan.shouldBuyShiesty and plan.shiestyCost or 0)) / plan.toolPrice))plan.toolCount = math_min(plan.toolCount, maxAffordableByBank)plan.toolCount = math_min(plan.toolCount, purchaseCap)if plan.toolCount <= 0 then
                                     plan.reason = 'Bank funds insufficient'
                                    plan.shouldBuyShiesty = false plan.shiestyCost = 0
                                    plan.totalCost = 0
                                    plan.withdrawAmount = 0
                                    return plan
                                 end totalCost = plan.toolCount * plan.toolPrice
                                if plan.shouldBuyShiesty then
                                     totalCost+=plan.shiestyCost
                                 end plan.totalCost = totalCost
                                neededFromBank = totalCost - plan.cash
                                if neededFromBank < 0 then
                                     neededFromBank = 0
                                 end
                             end plan.withdrawAmount = math_min(plan.bank, math_floor(neededFromBank))plan.isFeasible = plan.toolCount > 0 and plan.totalCost > 0
                            if not plan.isFeasible and not plan.reason then
                                 plan.reason = 'Unable to determine purchase amount'
                             end
                            return plan
                         end
                        local function TeleportTo(Origin, Target, Speed, Conditional)
                            if G_Toggle('ATMFarmUsePath')then
                                 return SecureLerpTeleportWithPathfinding(Origin, Target, Speed * G_Option('ATMFarmSpeedMultiplier'), Conditional)
                            else
                                 return SecureLerpTeleport(Origin, Target, Speed * G_Option('ATMFarmSpeedMultiplier'), Conditional)
                            end
                         end RoutineRunning = true RoutineStart = os.clock()if not G_Toggle('ATMFarm')then
                             Exit()
                        end
                        if os.clock() - START_TIME > AUTO_HOP_INTERVAL then
                             AttemptHop()
                        end
                        for _, Weld in next, Welds do
                             Weld:Destroy()
                        end
                        if not(AssertArgument('Request') and AssertArgument('Win'))then
                             dbgprint('ATMFarm: ATM arguments not found. Stopping.')SafeNotify('ATM-Farm Error: 0x02', 3)task_wait(3)Exit()
                        end
                        local Character = AssertCharacter()local Humanoid = Character:FindFirstChildOfClass('Humanoid') :: Humanoid
                        local ATMs = {
                        }
                        for _, ATMObject in next, ATM_Module.class.objects do
                             local Instance = ATMObject.instance
                            local Disabled = secure_call(ATMObject.states.disabled.get)local Hacker = secure_call(ATMObject.states.hacker.get)local ActiveHackTool = secure_call(ATMObject.states.active_hack_tool.get)dbgprint(string.format('ATM: %s (Status: %s, Hacker: %s, Tool: %s)', Instance.Name, Disabled and 'Disabled' or 'Active', Hacker and Hacker.Name or 'None', ActiveHackTool))if(not Disabled) and (Hacker == nil or Hacker == LocalPlayer)then
                                 ATMs[ATMObject] = Instance
                             end
                         end
                        if flen(ATMs) == 0 then
                             dbgprint('No ATMs found')Exit()
                        end
                        local TargetATM:ATM_ClassObject?local ClosestDistance = math.huge
                        local CharacterPivot = Character:GetPivot()for Object, ATM in next, ATMs do
                             local ATMPosition = ATM:GetPivot().Position
                            local Distance = (ATMPosition - CharacterPivot.Position).Magnitude
                            local Params = RaycastParams.new()Params.FilterType = Enum.RaycastFilterType.Exclude
                            Params.FilterDescendantsInstances = {
                                ATM,
                                Character,
                                Map:WaitForChild('RoadNetwork') :: Folder
                            }
                            Params.RespectCanCollide = true
                            local Result = workspace:Raycast(ATMPosition + Vector3.yAxis * 20, Vector3.yAxis * - 20, Params)if Result then
                                 dbgprint('ATM is in an enclosed area, skipping')CollectionService:AddTag(ATM, 'EnclosedATM')continue
                             end
                            if Distance < ClosestDistance then
                                 ClosestDistance = Distance
                                TargetATM = Object
                             end
                         end
                        if not TargetATM then
                             dbgprint('No target ATM found')Exit()
                        end assert(TargetATM, 'Target ATM is nil')if not TargetATM then
                             dbgprint('No target ATM found after assertion, something is wrong.')Exit()
                        end dbgprint('Found target ATM:', TargetATM.instance.Name)local TargetATMInstance = TargetATM.instance
                        local TargetATMPosition = TargetATMInstance:GetPivot()local CharacterPosition = Character:GetPivot()local VehicleSeat = Humanoid.SeatPart :: VehicleSeat
                        if not VehicleSeat then
                             local SpawnedVehicle = nil
                            for _, Vehicle in next, Vehicles:GetChildren()do
                                 if Vehicle:GetAttribute('OwnerUserId') == LocalUserId then
                                     SpawnedVehicle = Vehicle
                                 end
                             end
                            while Character:GetAttribute('IsRagdoll')do
                                 SafeNotify(T('Waiting for character to recover from ragdoll...'))task_wait(1)
                            end
                            if not SpawnedVehicle then
                                 local InventoryVehicle = nil
                                for i, ItemName in next, VehicleCandidates do
                                     local Item = Inventory.GetItemsByName(ItemName)[1]if Item then
                                         InventoryVehicle = Item break
                                     end
                                 end
                                if InventoryVehicle then
                                     if ArgumentChecks.Toggle_Equip_Item.Found then
                                         SafeNotify(T(`Attempting to spawn vehicle{ InventoryVehicle.Name }...`))local VehicleTimestamp = LocalPlayer:GetAttribute('SpawnVehicleNext') or 0
                                        local CurrentTime = workspace:GetServerTimeNow()if VehicleTimestamp > CurrentTime then
                                             local hopped = false
                                            if G_Toggle('ATMFarmAutoHop')then
                                                 hopped = AttemptHop('VehicleSpawnCooldownAutoHop')if hopped then
                                                     Exit()
                                                end
                                             end SafeNotify(T('Vehicle spawn cooldown detected, rejoining...'), 3)if AttemptRejoin('VehicleSpawnCooldown')then
                                                 Exit()
                                            else
                                                 SafeNotify(T('ATM-Farm: Automatic rejoin failed; waiting for cooldown.'), 5)pcall(function()
                                                    Library.Toggles.AutoRespawn:SetValue(false)
                                                end)if ArgumentChecks.Request_Respawn.Found then
                                                     SecureNet.Send(ArgumentChecks.Request_Respawn.Value)
                                                end
                                                while VehicleTimestamp > CurrentTime do
                                                     task_wait(1)CurrentTime = workspace:GetServerTimeNow()RoutineStart = os.clock()
                                                end
                                                if ArgumentChecks.Respawn.Found then
                                                     task_wait(0.1)SecureNet.Send(ArgumentChecks.Respawn.Value)
                                                end pcall(function()
                                                    Library.Toggles.AutoRespawn:SetValue(true)
                                                end)
                                            end
                                         end SecureNet.Get(ArgumentChecks.Toggle_Equip_Item.Value, InventoryVehicle.Guid)task_wait(1)
                                    end
                                 end
                             end
                            for _, Vehicle in next, Vehicles:GetChildren()do
                                 if Vehicle:GetAttribute('OwnerUserId') == LocalUserId then
                                     SpawnedVehicle = Vehicle
                                 end
                             end
                            if SpawnedVehicle then
                                 SafeNotify(T(`Vehicle exists, seating...`))SpawnedVehicle:PivotTo(Character:GetPivot() + Vector3.yAxis * 8)for _, Descendant in next, SpawnedVehicle:GetDescendants()do
                                     if Descendant:IsA('BasePart')then
                                         Descendant.AssemblyLinearVelocity = Vector3.yAxis * 5
                                        Descendant.AssemblyAngularVelocity = Vector3.new(math.random(), math.random(), math.random())
                                    end
                                 end WaitForPing()SpawnedVehicle:PivotTo(Character:GetPivot() + Vector3.yAxis * 30)Sit(SpawnedVehicle:FindFirstChildOfClass('VehicleSeat'), false)if not Humanoid.SeatPart then
                                     dbgprint('ATMFarm: Failed to sit in vehicle. Stopping.')SafeNotify('ATMFarm Error: Failed to sit in vehicle.', 3)task_wait(3)local VehicleTimestamp = LocalPlayer:GetAttribute('SpawnVehicleNext') or 0
                                    local CurrentTime = workspace:GetServerTimeNow()if VehicleTimestamp > CurrentTime then
                                         dbgprint('ATMFarm: Cannot re-equip vehicle yet. Waiting...')SafeNotify('ATMFarm Error: Vehicle ownership impossible.', 3)SafeNotify(T([[Please wait for vehicle respawn cooldown, this may take a while...]]), 3)local hopped = false
                                        if G_Toggle('ATMFarmAutoHop')then
                                             hopped = AttemptHop('VehicleRespawnCooldownAutoHop')if hopped then
                                                 Exit()
                                            end
                                         end SafeNotify(T('Vehicle respawn cooldown detected, rejoining...'), 3)if AttemptRejoin('VehicleRespawnCooldown')then
                                             Exit()
                                        else
                                             SafeNotify(T([[ATM-Farm: Automatic rejoin failed; waiting for respawn cooldown.]]), 5)pcall(function()
                                                Library.Toggles.AutoRespawn:SetValue(false)
                                            end)if ArgumentChecks.Request_Respawn.Found then
                                                 SecureNet.Send(ArgumentChecks.Request_Respawn.Value)
                                            end
                                            while VehicleTimestamp > CurrentTime do
                                                 task_wait(1)CurrentTime = workspace:GetServerTimeNow()RoutineStart = os.clock()
                                            end
                                            if ArgumentChecks.Respawn.Found then
                                                 task_wait(0.1)SecureNet.Send(ArgumentChecks.Respawn.Value)
                                            end pcall(function()
                                                Library.Toggles.AutoRespawn:SetValue(true)
                                            end)task_wait(1.5)
                                        end
                                     end task_wait(1.5)for _, Vehicle in next, Vehicles:GetChildren()do
                                         if Vehicle:GetAttribute('OwnerUserId') == LocalUserId then
                                             SpawnedVehicle = Vehicle
                                            SecureNet.Get(ArgumentChecks.Toggle_Equip_Item.Value, Vehicle:GetAttribute('ItemGUID'))SafeNotify(`Unequipping{ Vehicle.Name }...`)
                                        end
                                     end task_wait(1.5)Exit()
                                end
                             end
                         end VehicleSeat = Humanoid.SeatPart
                        if VehicleSeat and VehicleSeat.Parent then
                             for _, Descendant:BasePart in next, VehicleSeat.Parent:GetDescendants()do
                                 if Descendant:IsA('BasePart')then
                                     if not Descendant:GetAttribute('OldCanCollide')then
                                         Descendant:SetAttribute('OldCanCollide', Descendant.CanCollide)
                                    end Descendant.CanCollide = false Descendant.CanQuery = false Descendant.AssemblyLinearVelocity/=1.2
                                 end
                             end
                            local Motors = VehicleSeat.Parent:FindFirstChild('Motors')if Motors then
                                 local ForwardMaxSpeed = Motors:GetAttribute('forwardMaxSpeed') or 23
                                local Ratio = ForwardMaxSpeed / 35
                                TELEPORT_SPEED_VEHICLE = 65 * Ratio
                             else
                                 TELEPORT_SPEED_VEHICLE = 40
                             end
                         end
                        local HackToolToUse = nil
                        local PreferredToolName = G_Option('HackTool') or '!!ERROR_ILLEGAL_STATE!!'
                        local BASE_HACK_TOOLS = {
                            'HackToolPro',
                            'HackToolUltimate',
                            'HackToolBasic',
                            'HackToolQuantum'
                        }
                        for _, ToolName in next, BASE_HACK_TOOLS do
                             local ToolsFound = Inventory.FilterByLocation(Inventory.GetItemsByName(ToolName), 'hand')if ToolsFound and #ToolsFound > 0 then
                                 HackToolToUse = ToolName
                                if ToolName ~= PreferredToolName then
                                     SafeNotify(T('Preferred tool not found. Using available:') .. ToolName, 2)
                                end break
                             end
                         end
                        local purchasePlan = nil
                        if not HackToolToUse and Routine == 0 then
                             purchasePlan = CalculatePurchasePlan()if not purchasePlan.isFeasible then
                                 if purchasePlan.reason == 'Inventory is full' then
                                     SafeNotify([[ATM-Farm: Inventory full, forcing hack attempt to break loop.]], 4)HackToolToUse = purchasePlan.toolName or (G_Option('HackTool') or 'HackToolPro')
                                else
                                     local reason = purchasePlan.reason or 'Unable to auto-purchase hack tools'
                                    SafeNotify('ATM-Farm:' .. reason .. '.', 4)Routine = 0
                                    Exit()
                                end
                             else
                                 if purchasePlan.totalCost <= purchasePlan.cash then
                                     SafeNotify('ATM-Farm: Skipping withdrawal, enough cash available.')Routine = 2
                                 elseif  purchasePlan.withdrawAmount > 0 then
                                     SafeNotify('ATM-Farm: No hacking tools found, withdrawing money...')Routine = 1
                                 else
                                     SafeNotify([[ATM-Farm: Withdrawal amount invalid, stopping purchase attempt.]], 4)Routine = 0
                                    Exit()
                                end
                             end
                         end pcall(function()
                            local RoutineInfo = {
                                [0] = 'Hacking ATM',
                                [1] = 'Withdraw money',
                                [2] = 'Buying Items'
                            }
                            Library.Labels.AutofarmRoutineLabel:SetText(`Routine:{ RoutineInfo[Routine] }`)
                        end)if Routine == 2 then
                             local ShopPromptPart = workspace:WaitForChild('ShopZone_Illegal') :: Part
                            if G_Option('HackTool') == 'HackToolQuantum' then
                                 ShopPromptPart = workspace:WaitForChild('ShopZone_IllegalNightclub') :: Part
                             end TeleportTo(CharacterPosition, ShopPromptPart:GetPivot() + ShopPromptPart:GetPivot().RightVector * - 3.5, VehicleSeat and TELEPORT_SPEED_VEHICLE or TELEPORT_SPEED)
                        else
                             local TeleportData = TeleportTo(CharacterPosition, TargetATMPosition + TargetATMPosition.RightVector * - 3.5, VehicleSeat and TELEPORT_SPEED_VEHICLE or TELEPORT_SPEED, function()
                                if VehicleSeat and VehicleSeat.Parent then
                                     for _, Descendant:BasePart in next, VehicleSeat.Parent:GetDescendants()do
                                         if Descendant:IsA('BasePart')then
                                             Descendant.AssemblyLinearVelocity = Vector3.new(math.random(), math.random(), math.random())
                                        end
                                     end
                                 end
                                local Hackable = true
                                if secure_call(TargetATM.states.hacker.get) or secure_call(TargetATM.states.disabled.get)then
                                     Hackable = false
                                 end
                                if G_Toggle('ATMFarmDynamicRerouting')then
                                     local NewClosestATM = nil
                                    local NewClosestDistance = math.huge
                                    local CurrentCharacterPivot = AssertCharacter():GetPivot()for _, ATMObject in next, ATM_Module.class.objects do
                                         local Instance = ATMObject.instance
                                        local Disabled = secure_call(ATMObject.states.disabled.get)local Hacker = secure_call(ATMObject.states.hacker.get)if(not Disabled) and (Hacker == nil or Hacker == LocalPlayer)then
                                             if not CollectionService:HasTag(Instance, 'EnclosedATM')then
                                                 local Distance = (Instance:GetPivot().Position - CurrentCharacterPivot.Position).Magnitude
                                                if Distance < NewClosestDistance then
                                                     NewClosestDistance = Distance
                                                    NewClosestATM = ATMObject
                                                 end
                                             end
                                         end
                                     end
                                    if NewClosestATM and NewClosestATM.instance and NewClosestATM.instance ~= TargetATM.instance then
                                         local OriginalTargetDistance = (TargetATM.instance:GetPivot().Position - CurrentCharacterPivot.Position).Magnitude
                                        if NewClosestDistance < (OriginalTargetDistance * 0.85)then
                                             return false
                                         end
                                     end
                                 end
                                return Hackable
                             end)if TeleportData.Status == 'Aborted' then
                                 SafeNotify('Teleport aborted, restarting cycle...')Exit()
                            end
                         end
                        local ShouldReturnToVehicle = false
                        local MovementEvents = 0
                        local MovementEventConnection = Cleaner(MovementEvent.Event:Connect(function()
                            MovementEvents+=1
                         end))Storage.Connections[_nextKey(Storage.Connections, 'ATMFarm_MovementEvent')] = MovementEventConnection
                        if VehicleSeat then
                             ShouldReturnToVehicle = true Humanoid:ChangeState(Enum.HumanoidStateType.Jumping)WaitForPing()
                        end
                        local LockPositionConnection, RunLockPositionConnection = nil, false LockPositionConnection = RunService.Heartbeat:Connect(function()
                            if not RunLockPositionConnection then
                                 return
                             end
                            if MovementEvents > 3 then
                                 LockPositionConnection:Disconnect()MovementEventConnection:Disconnect()SafeNotify('ATM-Farm Error: Failed to lock position.', 3)Exit()
                            end
                            if not Humanoid.SeatPart then
                                 if Routine == 2 then
                                     local ShopPromptPart = workspace:WaitForChild('ShopZone_Illegal') :: Part
                                    if G_Option('HackTool') == 'HackToolQuantum' then
                                         ShopPromptPart = workspace:WaitForChild('ShopZone_IllegalNightclub') :: Part
                                     end Utils.TP(ShopPromptPart:GetPivot() + ShopPromptPart:GetPivot().RightVector * - 3.5)
                                else
                                     Utils.TP(TargetATM.instance:GetPivot() + TargetATM.instance:GetPivot().RightVector * - 3.5)
                                end
                             end
                            if VehicleSeat and VehicleSeat.Parent then
                                 for _, Descendant in next, VehicleSeat.Parent:GetDescendants()do
                                     if Descendant:IsA('BasePart')then
                                         Descendant.AssemblyLinearVelocity = Vector3.new(0, 10, 0)if G_Toggle('ATMFarmDefensive') or G_Toggle('ATMFarmOffensive')then
                                             if Descendant.Name == 'Chassis' then
                                                 Descendant.AssemblyAngularVelocity = Vector3.new(50, 50, 50)
                                            end
                                         end
                                     end
                                 end
                                if G_Toggle('ATMFarmDefensive')then
                                     VehicleSeat.Parent:PivotTo(CFrame.new(Character:GetPivot().Position) * VehicleSeat.Parent:GetPivot().Rotation)
                                elseif  G_Toggle('ATMFarmOffensive')then
                                     local ClosestPlayer = nil
                                    local ClosestDistance = math.huge
                                    for _, Player in next, Players:GetPlayers()do
                                         if Player ~= LocalPlayer and Player.Character then
                                             local Distance = (Player.Character:GetPivot().Position - Character:GetPivot().Position).Magnitude
                                            if Distance < ClosestDistance and Distance < 20 then
                                                 ClosestDistance = Distance
                                                ClosestPlayer = Player
                                             end
                                         end
                                     end
                                    if ClosestPlayer then
                                         VehicleSeat.Parent:PivotTo(CFrame.new(ClosestPlayer.Character:GetPivot().Position) * VehicleSeat.Parent:GetPivot().Rotation)
                                    else
                                         VehicleSeat.Parent:PivotTo(CFrame.new(Character:GetPivot().Position) * VehicleSeat.Parent:GetPivot().Rotation)
                                    end
                                 else
                                     VehicleSeat.Parent:PivotTo(Character:GetPivot() + Vector3.yAxis * 12)
                                end
                             end
                         end)Storage.Connections[_nextKey(Storage.Connections, 'ATMFarm_LockPosition_Heartbeat')] = Cleaner(LockPositionConnection)if Routine == 0 then
                             RunLockPositionConnection = true
                            if os.clock() - Storage.LastHackedATM < 5 then
                                 local WaitTime = 5 - (os.clock() - Storage.LastHackedATM)SafeNotify('Waiting for ATM cooldown...', WaitTime)task_wait(WaitTime)
                            end
                            local HandMoney, _ = Inventory.GetMoney()if HandMoney > 0 then
                                 SecureNet.Get(ArgumentChecks.ATM_Transfer.Value, 'hand', 'bank', HandMoney)
                            end SecureNet.Send(ArgumentChecks.Request.Value, TargetATMInstance, HackToolToUse)local ChanceTime = 0
                            if math.random(1, 5) == 1 then
                                 ChanceTime = 2 + math.random()
                            end task_wait(1.5 + math.random() + ChanceTime + G_Option('HackFinishDelay'))SecureNet.Send(ArgumentChecks.Win.Value, TargetATMInstance)
                        elseif  Routine == 1 then
                             RunLockPositionConnection = true
                            local plan = CalculatePurchasePlan()if not plan.isFeasible then
                                 local reason = plan.reason or 'Unable to prepare withdrawal'
                                SafeNotify('ATM-Farm:' .. reason .. '.', 4)Routine = 0
                                Exit()
                            end
                            if plan.withdrawAmount <= 0 then
                                 SafeNotify('ATM-Farm: Withdrawal not required, proceeding to purchase.')Routine = 2
                             else
                                 local HandMoney, _ = Inventory.GetMoney()task_wait(1)local Success = pcall(SecureNet.Get, ArgumentChecks.ATM_Transfer.Value, 'bank', 'hand', plan.withdrawAmount)if not Success then
                                     SafeNotify(T('You have no money to withdraw. Attempting to buy anyways...'))Routine = 2
                                 else
                                     task_wait(1)local NewHandMoney, _ = Inventory.GetMoney()if NewHandMoney <= HandMoney and plan.withdrawAmount > 0 then
                                         SafeNotify(T('Failed to withdraw money, retrying...'))Routine = 1
                                     else
                                         if plan.withdrawAmount > 0 then
                                             SafeNotify(T('Successfully withdrew $') .. tostring(NewHandMoney - HandMoney))
                                        end Routine = 2
                                     end
                                 end
                             end
                         elseif  Routine == 2 then
                             RunLockPositionConnection = true
                            local plan = CalculatePurchasePlan()if not plan.isFeasible or plan.toolCount <= 0 then
                                 local reason = plan.reason or 'No valid purchase plan'
                                SafeNotify('ATM-Farm:' .. reason .. '.', 4)Routine = 0
                                Exit()
                            end
                            local toolName = plan.toolName or (G_Option('HackTool') or 'HackToolPro')local ShopPromptPart = workspace:WaitForChild('ShopZone_Illegal')if toolName == 'HackToolQuantum' then
                                 ShopPromptPart = workspace:WaitForChild('ShopZone_IllegalNightclub') :: Part
                             end
                            if plan.shouldBuyShiesty then
                                 local shiestyItems = Inventory.FilterByLocation(Inventory.GetItemsByName('Shiesty'), 'hand')if#shiestyItems == 0 then
                                     SecureNet.Get(ArgumentChecks.Purchase_Consumable.Value, ShopPromptPart, 'Shiesty')task_wait(0.5)shiestyItems = Inventory.FilterByLocation(Inventory.GetItemsByName('Shiesty'), 'hand')
                                end
                                if#shiestyItems > 0 and not AssertCharacter():FindFirstChild('Shiesty')then
                                     SecureNet.Get(ArgumentChecks.Toggle_Equip_Item.Value, shiestyItems[1].Guid)
                                end
                             end SafeNotify(`ATM - Farm:Buying{ plan.toolCount } x{ toolName }`, 3)for _ = 1, plan.toolCount do
                                 SecureNet.Get(ArgumentChecks.Purchase_Consumable.Value, ShopPromptPart, toolName)task_wait(0.1)
                            end task_wait(0.5)local Tools = Inventory.FilterByLocation(Inventory.GetItemsByName(toolName), 'hand')if not Tools or #Tools == 0 then
                                 dbgprint('Failed to buy hacking tools')SafeNotify(T('ATM-Farm Error: Failed to buy hacking tools.'), 3)task_wait(3)Routine = 2
                             else
                                 task_wait(0.5)dbgprint('Bought hacking tools successfully')SafeNotify(T('ATM-Farm: Bought hacking tools successfully.'), 3)Routine = 0
                             end
                         end LockPositionConnection:Disconnect()MovementEventConnection:Disconnect()local Vehicle = FindVehicle()if Vehicle then
                             local VehicleModel = Vehicle.Vehicle
                            for _, Descendant in next, VehicleModel:GetDescendants()do
                                 if Descendant:IsA('BasePart')then
                                     if Descendant:GetAttribute('OldCanCollide')then
                                         Descendant.CanCollide = Descendant:GetAttribute('OldCanCollide')Descendant:SetAttribute('OldCanCollide', nil)
                                    end Descendant.CanQuery = true Descendant.AssemblyLinearVelocity = Vector3.zero
                                 end
                             end
                         end
                        if ShouldReturnToVehicle then
                             for i = 10, 1, - 1 do
                                 if(not VehicleSeat) or Humanoid.SeatPart then
                                     break
                                 end
                                if VehicleSeat.Parent then
                                     VehicleSeat.Parent:PivotTo(Character:GetPivot() + Vector3.yAxis * 12)for _, Descendant in next, VehicleSeat.Parent:GetDescendants()do
                                         if Descendant:IsA('BasePart')then
                                             Descendant.AssemblyLinearVelocity = Vector3.yAxis * 10 * math.random()Descendant.AssemblyAngularVelocity = Vector3.zero
                                         end
                                     end
                                 end RunService.Heartbeat:Wait()
                            end WaitForPing()Sit(VehicleSeat)
                        end Exit()
                    end, function(err)
                        warn('ATMFarm routine errored:', err)dbgprint(debug.traceback(tostring(err), 2))SafeNotify('ATM-Farm Error:' .. tostring(err), 5)Routine = 0
                        RoutineRunning = false
                     end)
                end)
            end
         end
     end))local ATMAutoHackRoutine = coroutine_create(LPH_JIT_MAX(function()
        while task_wait(0.1)do
             if not G_Toggle('ATM_Aura')then
                 continue
             end
            if G_Toggle('ATMFarm')then
                 continue
             end
            if not(AssertArgument('Request') and AssertArgument('Win'))then
                 dbgprint('AutoHack: ATM arguments not found. Stopping.')SafeNotify('AutoHack Error: 0x02', 3)task_wait(3)break
             end
            for _, ATM in next, ATM_Module.class.objects do
                 local Instance = ATM.instance
                if Instance and secure_call(ATM.states.hacker.get) == LocalPlayer then
                     task_wait(2)SecureNet.Send(ArgumentChecks.Win.Value, Instance)
                end
             end
         end
     end))local PanicRoutine = coroutine_create(LPH_JIT_MAX(function()
        local PanicLast = os.clock()Storage.Connections[_nextKey(Storage.Connections, 'Panic_Desync')] = Cleaner(RunService.Heartbeat:Connect(LPH_NO_VIRTUALIZE(function()
            local Character = AssertCharacter()local HumanoidRootPart = Character:FindFirstChild('HumanoidRootPart') :: Part
            if not HumanoidRootPart then
                 return
             end
            if Storage.Panic then
                 for i = 1, 5 do
                     sethiddenproperty(HumanoidRootPart, 'NetworkIsSleeping', true)task.wait()sethiddenproperty(HumanoidRootPart, 'NetworkIsSleeping', false)task.wait()
                end
             else
                 sethiddenproperty(HumanoidRootPart, 'NetworkIsSleeping', false)
            end
         end)))while task_wait()do
             pcall(function()
                if not G_Toggle('Panic')then
                     return
                 end
                if os.clock() - PanicLast < 5 then
                     return
                 end
                local Character = AssertCharacter()local Head = Character:FindFirstChild('Head') :: Part
                if not Head then
                     return
                 end
                local Downed = Head:WaitForChild('Downed', 1) :: BillboardGui
                if not Downed then
                     return
                 end
                if Downed.Enabled then
                     PanicLast = os.clock()Storage.Panic = true
                    local Origin = Character:GetPivot()if Origin.Position.Y <= PANIC_HEIGHT_THRESHOLD then
                         Origin = CFrame.new(Origin.Position.X, PANIC_CONST_OFY, Origin.Position.Z)
                    end
                    local OriginPart = Instance.new('Part', workspace:WaitForChild('CrateSpinPreviewItems'))OriginPart.Size = Vector3.new(1, 1, 1)OriginPart.Position = Origin.Position
                    OriginPart.Anchored = true OriginPart.CanCollide = false OriginPart.Transparency = 1
                    Camera.CameraSubject = OriginPart
                    local Humanoid = Character:FindFirstChildOfClass('Humanoid') :: Humanoid
                    if Humanoid then
                         local PanicStart = os.clock()local HealthAbove29Start = nil
                        local Flip = 1
                        local function PanicStep(DeltaTime, AntiFlyFix)
                            pcall(function()
                                Humanoid:ChangeState(Enum.HumanoidStateType.Swimming)
                            end)Flip*= - 1
                            for _, Limb in next, Character:GetChildren()do
                                 if Limb:IsA('BasePart')then
                                     Limb.AssemblyLinearVelocity = (Vector3.yAxis * - 1000 * Flip) + (Vector3.zAxis * - 1000 * Flip)Limb.AssemblyAngularVelocity = Vector3.zero
                                 end
                             end Utils.TPRoot(Origin - (Vector3.yAxis * (AntiFlyFix and 10 or 12)) + Vector3.xAxis * ((math_sin(os.clock() * 5 * 100)) * 10) + Vector3.zAxis * ( - (math_sin(os.clock() * 7 * 100)) * 10))for _, Limb in next, Character:GetChildren()do
                                 if Limb:IsA('BasePart') and Limb.Name ~= 'HumanoidRootPart' then
                                     Limb.CFrame = Origin + Vector3.new(math.random( - 200, 200), 1000, math.random( - 200, 200))
                                end
                             end
                         end
                        local LastAntiFlyStep = os.clock()SecureNet.Send(ArgumentChecks.Enter_Character_Creator.Value, Character:GetPivot())while true do
                             local DeltaTime = RunService.Heartbeat:Wait()local ANTI_FLY_TIMEOUT = 1.5
                            local ANTI_FLY_FIX_WINDOW = 0.3
                            if os.clock() - PanicStart > PANIC_DURATION then
                                 Storage.Panic = false break
                             end
                            local AntiFlyFix = os.clock() - LastAntiFlyStep >= ANTI_FLY_FIX_WINDOW
                            if AntiFlyFix and os.clock() - LastAntiFlyStep >= (ANTI_FLY_FIX_WINDOW + ANTI_FLY_TIMEOUT)then
                                 LastAntiFlyStep = os.clock()
                            end
                            if Humanoid.Health >= 29 then
                                 if not HealthAbove29Start then
                                     HealthAbove29Start = os.clock()
                                end
                                if os.clock() - HealthAbove29Start > 0.7 then
                                     for _, Limb in next, Character:GetChildren()do
                                         if Limb:IsA('BasePart')then
                                             Limb.CFrame = Origin
                                            Limb.AssemblyLinearVelocity = Vector3.zero
                                            Limb.AssemblyAngularVelocity = Vector3.zero
                                         end
                                     end Utils.TPRoot(Origin)
                                else
                                     PanicStep(DeltaTime, AntiFlyFix)
                                end
                             else
                                 PanicStep(DeltaTime, AntiFlyFix)
                            end
                            if not Downed.Enabled then
                                 Storage.Panic = false break
                             end
                         end
                        if not shared.GodMode then
                             SecureNet.Send(ArgumentChecks.Leave_Character_Creator.Value)
                        end Camera.CameraSubject = Humanoid
                     end
                 end
             end)
        end
     end))local ItemAuraRoutine = coroutine_create(LPH_JIT_MAX(function()
        while true do
             task_wait(0.1)if not G_Toggle('ItemAura')then
                 continue
             end
            local Character = AssertCharacter()for _, Item in next, workspace:WaitForChild('DroppedItems'):GetChildren()do
                 if Item:IsA('Model')then
                     local ItemPosition = Item:GetPivot().Position
                    local CharacterPosition = Character:GetPivot().Position
                    if(ItemPosition - CharacterPosition).Magnitude < 30 then
                         if Item.Name == 'Money' then
                             task_spawn(function()
                                pcall(SecureNet.Get, ArgumentChecks.Pickup_Dropped_Item.Value, Item)
                            end)continue
                         end
                        local Rarities = G_Option('ItemAuraRarities')local function GetRarityFromName(Name:string)
                            :string
                            for _, ItemCategory in next, ReplicatedStorage.Items:GetChildren()do
                                 for _, ItemInstance in next, ItemCategory:GetChildren()do
                                     if ItemInstance.Name == Name then
                                         return ItemInstance:GetAttribute('RarityName')
                                    end
                                 end
                             end
                            return 'Common'
                         end
                        local ItemRarity = GetRarityFromName(Item.Name)if not Rarities[ItemRarity]then
                             continue
                         end
                        if G_Toggle('InventoryFilterEnabled')then
                             local ExcludedItems = G_Option('InventoryFilterList')if ExcludedItems[Item.Name]then
                                 continue
                             end
                         end task_spawn(function()
                            pcall(SecureNet.Get, ArgumentChecks.Pickup_Dropped_Item.Value, Item)
                        end)if not Storage.ItemAuraConnections[Item]then
                             local Connection
                            Connection = RunService.Heartbeat:Connect(function()
                                if(not Item) or not Item.Parent or (not Item:FindFirstChild('PickUpZone'))then
                                     if Connection then
                                         Connection:Disconnect()Connection = nil
                                     end Storage.ItemAuraConnections[Item] = nil
                                    return
                                 end firetouchinterest(Item.PickUpZone, Character:FindFirstChild('HumanoidRootPart') :: Part, 1 :: any)firetouchinterest(Item.PickUpZone, Character:FindFirstChild('HumanoidRootPart') :: Part, 0 :: any)
                            end)Storage.ItemAuraConnections[Item] = Connection
                         end
                     end
                 end
             end
         end
     end))local ItemFilterRoutine = coroutine_create(LPH_NO_VIRTUALIZE(function()
        while task_wait()do
             if not G_Toggle('InventoryFilterEnabled')then
                 continue
             end
            local ExcludedItems = G_Option('InventoryFilterList')local ItemsInInventory = Inventory.FilterByLocation(Inventory.ListInventory(), 'hand')for _, Item in next, ItemsInInventory do
                 if ExcludedItems[Item.Name]then
                     SecureNet.Send(ArgumentChecks.Drop_Item.Value, Item.Guid, Item.Amount)
                end
             end
         end
     end))local WalkFlingRoutine = coroutine_create(LPH_JIT_MAX(function()
        local Flip = 1
        while true do
             RunService.Heartbeat:Wait()if not(G_Toggle('WalkFling') or G_Toggle('Anti-Aimbot'))then
                 continue
             end
            local Character = AssertCharacter()local Root = Character:WaitForChild('HumanoidRootPart') :: Part
            local Velocity = Root.AssemblyLinearVelocity
            if G_Toggle('Anti-Aimbot') and Velocity.Magnitude < 5 then
                 local function GetHorizontalComponent()
                    local Sign = (math.random(0, 1) * 2 - 1)return Sign * (10 + math.random(0, 5))
                end Velocity = Vector3.new(GetHorizontalComponent(), math.random( - 5, 5), GetHorizontalComponent())
            end
            local OldTransform = Root.CFrame
            Root.AssemblyLinearVelocity = Velocity * 10000 + Vector3.yAxis * 10000
            Root.CFrame = OldTransform + Vector3.yAxis * 5 * math.random()RunService.RenderStepped:Wait()Root.AssemblyLinearVelocity = Velocity
            Root.CFrame = OldTransform
            RunService.Stepped:Wait()Root.AssemblyLinearVelocity+=Vector3.yAxis * Flip * 0.1
            Flip*= - 1
         end
     end))local KillAuraRoutine = coroutine_create(LPH_JIT_MAX(function()
        while RunService.Heartbeat:Wait()do
             if not G_Toggle('KillAura')then
                 continue
             end
            local Character = AssertCharacter()local Tool = Character:FindFirstChildOfClass('Tool')local Pivot = Character:GetPivot()local HitPlayers = {
            }
            if not Tool then
                 continue
             end
            if not Tool:HasTag('Melee')then
                 continue
             end
            for _, Player in next, Players:GetPlayers()do
                 if Player ~= LocalPlayer and Player.Character and Player.Character:FindFirstChild('HumanoidRootPart')then
                     local OtherPivot = Player.Character:GetPivot()if(OtherPivot.Position - Pivot.Position).Magnitude <= 10 then
                         table.insert(HitPlayers, Player)
                    end
                 end
             end
            if#HitPlayers == 0 then
                 continue
             end
            local v66 = 30
            local v_u_67 = v66 * 0.75 + math.random() * v66 * 0.25
            local v_u_68 = LocalPlayer:GetAttribute('SpeedMultiplier') or 1
            Tool:Activate()task_wait(0.15)SecureNet.Send(ArgumentChecks.Melee_Attack.Value, Tool, HitPlayers, Pivot, v_u_67 * v_u_68)task_wait(0.5)
        end
     end))local BumpAuraRoutine = coroutine_create(LPH_JIT_MAX(function()
        local LastBump = os.clock()local BumpCooldown = 4.1
        while RunService.Heartbeat:Wait()do
             if not G_Toggle('BumpAura')then
                 continue
             end
            if os.clock() - LastBump < BumpCooldown then
                 continue
             end
            local Character = AssertCharacter()local Humanoid = Character:FindFirstChildOfClass('Humanoid')if Humanoid and Humanoid.SeatPart and Humanoid.SeatPart:IsA('VehicleSeat')then
                 local ClosestPlayer = nil
                local ClosestDistance = math.huge
                for _, Player in next, Players:GetPlayers()do
                     if Player ~= LocalPlayer and Player.Character then
                         local Distance = (Player.Character:GetPivot().Position - Character:GetPivot().Position).Magnitude
                        if Distance < ClosestDistance and Distance < 20 then
                             ClosestDistance = Distance
                            ClosestPlayer = Player
                         end
                     end
                 end
                if ClosestPlayer then
                     SecureNet.Send('run_over', Humanoid.SeatPart.Parent, ClosestPlayer.Character, vector.create(0, 200, 0))LastBump = os.clock()
                end
             end
         end
     end))local ThrowableAuraRoutine = coroutine_create(LPH_JIT_MAX(function()
        while task_wait(0.1)do
             if not G_Toggle('ThrowableAura')then
                 continue
             end
            local Character = AssertCharacter()local Tool = Character:FindFirstChildOfClass('Tool')if not Tool then
                 continue
             end
            if Tool:HasTag('Throwable')then
                 local Closest, Distance = nil, math.huge
                for _, Player in next, Players:GetPlayers()do
                     if Player ~= LocalPlayer and Player.Character and Player.Character:FindFirstChild('HumanoidRootPart')then
                         local OtherPivot = Player.Character:GetPivot()if(OtherPivot.Position - Character:GetPivot().Position).Magnitude < Distance then
                             Closest = Player
                            Distance = (OtherPivot.Position - Character:GetPivot().Position).Magnitude
                         end
                     end
                 end
                if Closest and Distance < 20 then
                     local Target = Closest.Character
                    if Target then
                         Tool:Activate()task_wait()SecureNet.Send(ArgumentChecks.Throw_Item.Value, Tool, Prediction:GetPredictedPosition(Target.Head), Vector3.yAxis * - 10)local ProjectileModel = nil
                        local Connection
                        Connection = workspace.ChildAdded:Connect(function(Child)
                            if Child:IsA('Model') and Child.Name == Tool.Name then
                                 ProjectileModel = Child
                                if Connection then
                                     Connection:Disconnect()Connection = nil
                                 end
                             end
                         end)local StartTime = os.clock()repeat
                             task_wait()
                        until ProjectileModel or os.clock() - StartTime > 1
                        if Connection then
                             Connection:Disconnect()Connection = nil
                         end
                        if ProjectileModel and ProjectileModel.PrimaryPart then
                             SecureNet.Send(ArgumentChecks.Throw_Hit.Value, ProjectileModel, Target.PrimaryPart, ProjectileModel.PrimaryPart.CFrame)
                        end
                     end
                 end
             end
         end
     end))local GunModsRoutine = coroutine_create(LPH_JIT_MAX(function()
        Storage.UpdateGunStatsCallback.Event:Connect(function()
            local GunClass = Class_Interface.GetClass('Gun')if not GunClass then
                 warn('Gun class not found by Class_Interface!')return
             end
            local GunObjects = GunClass.objects or {
            }
            if next(GunObjects) == nil then
                 return
             end
            for _, Gun in next, GunObjects do
                 if not(Gun and Gun.instance and Gun.states)then
                     if Gun and Gun.instance then
                         warn('Gun object for', Gun.instance.Name, 'is missing .states property!')
                    elseif  Gun then
                         warn('Gun object is missing .instance property!')
                    end continue
                 end
                local States = Gun.states
                for StateName, State in next, States do
                     if not(State and State.get and typeof(State.get) == 'function')then
                         warn('Invalid state object or missing get method for state', StateName, 'in gun', Gun.instance.Name)continue
                     end
                    if Storage.GunModReferences[StateName]then
                         if not isfunctionhooked(State.get)then
                             HookMgr.RegisterHook(tostring(State.get) .. HttpService:GenerateGUID(false), State.get, function(Old, ...)
                                local Caller:((...any)->...any)?local Level = 1
                                while Level < 100 do
                                     local Source = debug.info(Level, 's')if Source and Source:match('Gun')then
                                         Caller = debug.info(Level, 'f')break
                                     end Level+=1
                                 end
                                local Result
                                local ModReference = Storage.GunModReferences[StateName]if StateName == 'automatic' then
                                     Result = G_Toggle_NYield(ModReference)
                                else
                                     Result = G_Option_NYield(ModReference)
                                end
                                if Result ~= nil then
                                     if StateName == 'fire_rate' then
                                         if Caller then
                                             local Upvalues = #debug.getupvalues(Caller)if Upvalues == 17 then
                                                 local FireDelay = 60 / Result
                                                debug.setupvalue(Caller, 7, FireDelay)
                                            end
                                         end
                                     end
                                    return Result
                                 else
                                     return Old(...)
                                end
                             end)
                        end
                     end
                 end
             end
         end)
    end))local MeleeModsRoutine = coroutine_create(LPH_JIT_MAX(function()
        Storage.UpdateMeleeStatsCallback.Event:Connect(function()
            local MeleeClass = Class_Interface.GetClass('Melee')if not MeleeClass then
                 warn('Melee class not found by Class_Interface!')return
             end
            local MeleeObjects = MeleeClass.objects or {
            }
            if next(MeleeObjects) == nil then
                 return
             end
            for _, Melee in next, MeleeObjects do
                 if not(Melee and Melee.instance and Melee.states)then
                     print('Skipping invalid or nil melee object in MeleeObjects table.')if Melee and Melee.instance then
                         warn('Melee object for', Melee.instance.Name, 'is missing .states property!')
                    elseif  Melee then
                         warn('Melee object is missing .instance property!')
                    end continue
                 end
                local States = Melee.states
                for StateName, State in next, States do
                     if not(State and State.get and typeof(State.get) == 'function')then
                         warn('Invalid state object or missing get method for state', StateName, 'in melee', Melee.instance.Name)continue
                     end
                    if Storage.MeleeModReferences[StateName]then
                         if not isfunctionhooked(State.get)then
                             HookMgr.RegisterHook(tostring(State.get) .. HttpService:GenerateGUID(false), State.get, function(Old, ...)
                                print('Melee state get called for', StateName, 'on', Melee.instance.Name)local Result
                                local ModReference = Storage.MeleeModReferences[StateName]Result = G_Option_NYield(ModReference)if G_Toggle_NYield('MeleeModificationEnabled') and Result ~= nil then
                                     print('Returning modified value for', StateName, ':', Result, 'for melee', Melee.instance.Name)return Result
                                 else
                                     print('Returning original value for', StateName, 'for melee', Melee.instance.Name)return Old(...)
                                end
                             end)
                        end
                     end
                 end
             end
         end)
    end))local AntiAimRoutine = coroutine_create(LPH_JIT_MAX(function()
        while true do
             RunService.PreSimulation:Wait()if not G_Toggle('Invisibility')then
                 continue
             end
            local Character = AssertCharacter()local Humanoid = Character:FindFirstChildOfClass('Humanoid') :: Humanoid
            if Humanoid then
                 local Animator = Humanoid:WaitForChild('Animator') :: Animator
                local Animation = Storage.Anti_Aim_Animation
                if not Animation then
                     Animation = Instance.new('Animation')Animation.AnimationId = 'rbxassetid://127212897044971'
                    local Track = Animator:LoadAnimation(Animation)Track.Priority = Enum.AnimationPriority.Action4
                    Track:Play(0, 255, 1)task_wait()Track.TimePosition = 0.837
                    task_wait()Track:AdjustSpeed(0)Storage.Anti_Aim_Animation = Track
                 end
                for _, Connection in next, getconnections(Humanoid:GetPropertyChangedSignal('HipHeight'))do
                     if Connection.Function then
                         Connection:Disable()
                    end
                 end Humanoid.HipHeight = 1
             end
         end
     end))local AntiAimbotRoutine = coroutine_create(LPH_JIT_MAX(function()
        local AntiAimbotAnimation = nil
        local AnimId = 'rbxassetid://109873544976020'
        while RunService.Heartbeat:Wait()do
             if not G_Toggle('Anti-Aimbot')then
                 if AntiAimbotAnimation then
                     AntiAimbotAnimation:Stop()AntiAimbotAnimation = nil
                 end continue
             end
            local Character = AssertCharacter()local Humanoid = Character:FindFirstChildOfClass('Humanoid') :: Humanoid
            if not Humanoid then
                 continue
             end
            local Animator = Humanoid:FindFirstChildOfClass('Animator') :: Animator
            if not Animator then
                 continue
             end
            local Playing = false
            for _, Track in next, Animator:GetPlayingAnimationTracks()do
                 if Track.Animation.AnimationId == AnimId then
                     Playing = true break
                 end
             end
            if AntiAimbotAnimation and not Playing then
                 AntiAimbotAnimation = nil
             end
            if not Playing then
                 local Animation = Instance.new('Animation')Animation.AnimationId = AnimId
                local Track = Animator:LoadAnimation(Animation)AntiAimbotAnimation = Track
                Track.Priority = Enum.AnimationPriority.Action4
                Track.Looped = true Track:Play(0, 255, 60)
            end
         end
     end))local AutoFishRoutine = coroutine_create(LPH_JIT_MAX(function()
        local FishingRodModule = SafeRequire(GameModules.ItemTypes.FishingRod :: ModuleScript)local SliderMinigame = SafeRequire(GameModules.Minigames.SliderMinigame :: ModuleScript)local ItemUtils = SafeRequire(GameModules.Inventory.ItemUtils :: ModuleScript)local function FindWaterPosition()
            local HRP = secure_call(Char.get_hrp)if not HRP then
                 return nil
             end
            local SearchOrigin = HRP.Position + (HRP.CFrame.LookVector * 20)local Params = RaycastParams.new()Params.FilterType = Enum.RaycastFilterType.Exclude
            Params.FilterDescendantsInstances = {
                LocalPlayer.Character
            }
            local Result = workspace:Raycast(SearchOrigin, Vector3.new(0, - 100, 0), Params)if Result and Result.Material == Enum.Material.Water and (Result.Position - HRP.Position).Magnitude < 60 then
                 return Result.Position
             end
            return nil
         end SliderMinigame.enabled.hook(function(IsEnabled)
            if G_Toggle('AutoFish') and IsEnabled then
                 local CurrentRod = secure_call(FishingRodModule.equipped_rod.get)if CurrentRod then
                     SecureNet.Send(ArgumentChecks.Reel_Ended.Value, CurrentRod, true)
                end
             end
         end)while task_wait(1)do
             if not G_Toggle('AutoFish')then
                 continue
             end
            local CurrentRod = secure_call(FishingRodModule.equipped_rod.get)if not CurrentRod then
                 continue
             end
            local ItemGUID = CurrentRod:GetAttribute('ItemGUID')if not ItemGUID then
                 continue
             end
            local ItemInfo = secure_call(ItemUtils.get_item_info, Data_Module, ItemGUID)if not ItemInfo then
                 continue
             end
            if not(ItemInfo.ammo_amount and ItemInfo.ammo_amount > 0)then
                 CurrentRod:Activate()task_wait(0.5)continue
             end
            if not CurrentRod:FindFirstChild('Bobber')then
                 local WaterPosition = FindWaterPosition()if WaterPosition then
                     SecureNet.Get(ArgumentChecks.Throw_Rod.Value, CurrentRod, WaterPosition)
                else
                     SafeNotify('AutoFish: No nearby water found.')
                end
             end
         end
     end))local StaminaFarmRoutine = coroutine_create(LPH_JIT_MAX(function()
        while task_wait(1)do
             if G_Toggle('StaminaFarm')then
                 local CurrentStamina = LocalPlayer:GetAttribute('SprintBar')local AutoFarmEnabled = false
                local AutoFarmToggles = {
                    'ATMFarm',
                    'CookFarm',
                    'ShelfStocking'
                }
                for _, Toggle in ipairs(AutoFarmToggles)do
                     if G_Toggle(Toggle)then
                         AutoFarmEnabled = true break
                     end
                 end Storage.MovementSpoof = AutoFarmEnabled
                if CurrentStamina < 0.01 then
                     Storage.MovementSpoof = false
                    repeat
                         task_wait(1)
                    until LocalPlayer:GetAttribute('SprintBar') >= 0.95
                 end
             end
         end
     end))Storage.Connections[_nextKey(Storage.Connections, 'LocalPlayer_LastHackedAtmTimestamp_Changed')] = Cleaner(LocalPlayer:GetAttributeChangedSignal('LastHackedAtmTimestamp'):Connect(function()
        Storage.LastHackedATM = os.clock()
    end))Storage.Connections[_nextKey(Storage.Connections, 'AntiAFK_Idled')] = Cleaner(Players.LocalPlayer.Idled:Connect(function()
        VirtualUser:CaptureController()VirtualUser:ClickButton2(Vector2.new())
    end))Cleaner(CookFarmRoutine)Cleaner(ATMAutoHackRoutine)Cleaner(InfiniteStaminaFixRoutine)Cleaner(AntiAimbotRoutine)Cleaner(StaminaFarmRoutine)do
         Cleaner(ATMFarmRoutine)Cleaner(PanicRoutine)Cleaner(WalkFlingRoutine)Cleaner(ItemAuraRoutine)Cleaner(KillAuraRoutine)Cleaner(ThrowableAuraRoutine)Cleaner(GunModsRoutine)Cleaner(AntiAimRoutine)Cleaner(ShelfStockRoutine)Cleaner(MeleeModsRoutine)Cleaner(AutoFishRoutine)Cleaner(ItemFilterRoutine)Cleaner(BumpAuraRoutine)
    end coroutine_resume(CookFarmRoutine)coroutine_resume(ATMAutoHackRoutine)coroutine_resume(InfiniteStaminaFixRoutine)coroutine_resume(AntiAimbotRoutine)coroutine_resume(StaminaFarmRoutine)do
         coroutine_resume(PanicRoutine)coroutine_resume(WalkFlingRoutine)coroutine_resume(ItemAuraRoutine)coroutine_resume(KillAuraRoutine)coroutine_resume(ATMFarmRoutine)coroutine_resume(ThrowableAuraRoutine)coroutine_resume(GunModsRoutine)coroutine_resume(AntiAimRoutine)coroutine_resume(ShelfStockRoutine)coroutine_resume(MeleeModsRoutine)coroutine_resume(AutoFishRoutine)coroutine_resume(ItemFilterRoutine)coroutine_resume(BumpAuraRoutine)
    end
    local JumpDown = false
    local TouchGui = LocalPlayer.PlayerGui:WaitForChild('TouchGui', 1)local TouchControlFrame = TouchGui and TouchGui:FindFirstChild('TouchControlFrame')local JumpButton = TouchControlFrame and TouchControlFrame:FindFirstChild('JumpButton')Storage.Connections[_nextKey(Storage.Connections, 'Input_InputBegan')] = Cleaner(UserInputService.InputBegan:Connect(function(Input, GameProcessed)
        if GameProcessed then
             return
         end
        if not G_Toggle('FlyJump')then
             return
         end
        if Input.UserInputType == Enum.UserInputType.Keyboard then
             if Input.KeyCode == Enum.KeyCode.Space then
                 JumpDown = true
             end
         end
     end))Storage.Connections[_nextKey(Storage.Connections, 'Input_InputEnded')] = Cleaner(UserInputService.InputEnded:Connect(function(Input, GameProcessed)
        if GameProcessed then
             return
         end
        if Input.UserInputType == Enum.UserInputType.Keyboard then
             if Input.KeyCode == Enum.KeyCode.Space then
                 JumpDown = false
             end
         end
     end))if JumpButton then
         Storage.Connections[_nextKey(Storage.Connections, 'JumpButton_InputBegan')] = Cleaner(JumpButton.InputBegan:Connect(function(Input, GameProcessed)
            if GameProcessed then
                 return
             end
            if not G_Toggle('FlyJump')then
                 return
             end
            if Input.UserInputType == Enum.UserInputType.Touch then
                 JumpDown = true
             end
         end))Storage.Connections[_nextKey(Storage.Connections, 'JumpButton_InputEnded')] = Cleaner(JumpButton.InputEnded:Connect(function(Input, GameProcessed)
            if GameProcessed then
                 return
             end
            if Input.UserInputType == Enum.UserInputType.Touch then
                 JumpDown = false
             end
         end))
    end
    local LastImpulse = os.clock()Storage.Connections[_nextKey(Storage.Connections, 'RunService_PreSimulation')] = Cleaner(RunService.PreSimulation:Connect(LPH_JIT_MAX(function()
        if JumpDown and G_Toggle('FlyJump')then
             if os.clock() - LastImpulse < 0.1 then
                 return
             end LastImpulse = os.clock()local Character = AssertCharacter()local Humanoid = Character:FindFirstChildOfClass('Humanoid') :: Humanoid
            if not Humanoid then
                 return
             end
            for _, BasePart:BasePart in next, Character:GetDescendants()do
                 if BasePart:IsA('BasePart')then
                     if Humanoid.FloorMaterial == Enum.Material.Air then
                         if BasePart.AssemblyLinearVelocity.Y < 50 then
                             BasePart:ApplyImpulse(Vector3.yAxis * (7 / 1.2))
                        end
                     end
                 end
             end
         end
     end)))do
         local function SetupDroppedItemESP(Item:Model)
            local RootPart = Item:WaitForChild('PickUpZone', 1) :: Part?if not RootPart then
                 return
             end
            local Box = ESP_Library.Drawings.Create3DBox()local Text = ESP_Library.Drawings.UseText()local Color = Color3.new(0, 1, 0)if Item.Name ~= 'Money' then
                 local ItemRarity
                local Reference
                pcall(function()
                    Reference = ReplicatedStorage.Items[Item:GetAttribute('item_type')][Item.Name]
                end)if Reference then
                     ItemRarity = Reference:GetAttribute('RarityName')
                else
                     ItemRarity = 'Common'
                 end Color = Storage.RarityColors[ItemRarity] or Color3.fromRGB(255, 255, 255)
            end
            local Parts = {
            }
            for _, Part in next, Item:GetChildren()do
                 if Part:IsA('BasePart') and Part.Name ~= 'PickUpZone' then
                     table.insert(Parts, Part)
                end
             end ESP_Library.Register(function()
                if G_Toggle('ESPDroppedItems')then
                     local Camera = workspace.CurrentCamera
                    local Distance = Camera and (Camera.CFrame.Position - RootPart.Position).Magnitude or 0
                    local ComputedText = Item.Name
                    if Item.Name == 'Money' then
                         local AmountBillboard = Item:FindFirstChild('AmountBillboardGui') :: BillboardGui
                        if AmountBillboard then
                             local AmountLabel = AmountBillboard:FindFirstChild('TextLabel') :: TextLabel
                            if AmountLabel then
                                 ComputedText = '$' .. AmountLabel.Text:gsub('x', '')
                            end
                         end
                     end Text:Update({
                        Enabled = true,
                        Text = ComputedText,
                        Position = RootPart.Position + Vector3.new(0,
                        4,
                        0),
                        Color = Color,
                        Outline = true,
                        Channel = 'Custom',
                        Distance = Distance
                    })
local _, BoxSize = GetBoundingBox(Parts, RootPart:GetPivot().Rotation)Box:Update({
                        Pivot = RootPart.CFrame,
                        Size = BoxSize,
                        Color = Color,
                        Enabled = true,
                        Channel = 'Custom',
                        Distance = Distance
                    })
                else
                     Box:Update({
                        Enabled = false
                    })
Text:Update({
                        Enabled = false
                    })
                end
                return true
             end, function()
                local Condition = (Item and Item.Parent and RootPart and RootPart.Parent and Item:IsDescendantOf(workspace))if not Condition then
                     return false
                 end
                return true
             end, function()
                Box:Destroy()Text:Destroy()
            end)print('Set up ESP for dropped item:', Item.Name)
        end Storage.Connections[_nextKey(Storage.Connections, 'DroppedItems')] = Cleaner(workspace:WaitForChild('DroppedItems').ChildAdded:Connect(function(Item)
            if Item:IsA('Model')then
                 SetupDroppedItemESP(Item)
            end
         end))for _, Item in next, workspace:WaitForChild('DroppedItems'):GetChildren()do
             if Item:IsA('Model')then
                 SetupDroppedItemESP(Item)
            end
         end
     end Library.RiskColor = Color3.new(0.960784, 0.592157, 0.376471)Library.Scheme = {
        BackgroundColor = Color3.fromRGB(29,
        29,
        46),
        MainColor = Color3.fromRGB(48,
        45,
        65),
        AccentColor = Color3.fromRGB(159,
        120,
        149),
        OutlineColor = Color3.fromRGB(67,
        61,
        87),
        FontColor = Color3.fromRGB(217,
        224,
        238),
        Font = Font.fromEnum(Enum.Font.BuilderSans),
        Red = Color3.new(0.960784,
        0.592157,
        0.376471),
        Dark = Color3.new(0,
        0,
        0),
        White = Color3.new(1,
        1,
        1)
    }
    Cleaner.GetCleanEvent():Connect(function()
        Library:Unload()ESP_Library.Unload()ItemView:Unload()pcall(sethiddenproperty, Lighting, 'Technology', Enum.Technology.Future)Lighting.GlobalShadows = true
     end)local Window = Library:CreateWindow({
        Title = 'Sasware',
        Center = true,
        AutoShow = true,
        Footer = T('Version:' .. Version .. '|' .. SubVersion),
        Icon = 113209211300754,
        DisableSearch = true,
        CornerRadius = 12,
        EnableSidebarResize = true
    })
local Tabs = {
        Main = Window:AddTab(T('Main'),
        'combine',
        T('General features and utilities')),
        Automation = Window:AddTab(T('Automation'),
        'git-compare-arrows',
        T('Automated jobs and tasks'))
    }
    if not false and ORCHESTRATOR_MENU_ENABLED then
         Tabs.Orchestrator = Window:AddTab(T('Orchestrator'), 'users', T('Control multiple clients remotely'))
    end
    local Tabs2 = {
        Combat = Window:AddTab(T('Combat'),
        'crosshair',
        T('Combat features and utilities')),
        Teleports = Window:AddTab(T('Teleports'),
        'milestone',
        T('Teleport locations and server utilities')),
        Visuals = Window:AddTab(T('Visuals'),
        'eye',
        T('Visual enhancements and effects')),
        InventoryViewer = Window:AddTab(T('Inventory Viewer'),
        'package-open',
        T('View and manage your inventory')),
        Settings = Window:AddTab(T('Settings'),
        'cog',
        T('Configure your preferences and settings'))
    }
    for Key, Tab in next, Tabs2 do
         Tabs[Key] = Tab
     end do
         Tabs.Debug = Window:AddTab('Debug', 'bug', T('Debugging tools and information'))
    end
    local UtilitiesGroup = Tabs.Main:AddLeftGroupbox(T('Utilities'))UtilitiesGroup:AddButton({
        Text = T('Bring Car'),
        Func = function()
            for _,
            Vehicle in next,
            Vehicles:GetChildren()do
                 if Vehicle:GetAttribute('OwnerUserId') == LocalUserId then
                     local Character = AssertCharacter()Vehicle:PivotTo(Character:GetPivot() + Vector3.yAxis * 12)for _,
                    Descendant in next,
                    Vehicle:GetDescendants()do
                         if Descendant:IsA('BasePart')then
                             Descendant.AssemblyLinearVelocity = Vector3.zero
                            Descendant.AssemblyAngularVelocity = Vector3.zero
                         end
                     end Sit(Vehicle:FindFirstChildOfClass('VehicleSeat'))
                end
             end
         end,
        Tooltip = T('Bring your car to you'),
        DisabledTooltip = T('Button is disabled in FREE_BUILD mode'),
        Disabled = false
    })
UtilitiesGroup:AddButton({
        Text = T('Vehicle-Snap'),
        Func = function()
            local Character = AssertCharacter()local VehicleData = FindVehicle()if not VehicleData then
                 return SafeNotify(T('You need a vehicle spawned to snap under the map.'))
            end
            local Vehicle = VehicleData.Vehicle
            local Origin = Character:GetPivot()Vehicle:PivotTo(Character:GetPivot() + Vector3.yAxis * 12)for _,
            Descendant in next,
            Vehicle:GetDescendants()do
                 if Descendant:IsA('BasePart')then
                     Descendant.AssemblyLinearVelocity = Vector3.zero
                    Descendant.AssemblyAngularVelocity = Vector3.zero
                 end
             end Sit(Vehicle:FindFirstChildOfClass('VehicleSeat'),
            true)local Humanoid = Character:FindFirstChildOfClass('Humanoid')if Humanoid.SeatPart then
                 Humanoid:ChangeState(Enum.HumanoidStateType.Jumping)WaitForPing()local VehicleSnapConnection
                VehicleSnapConnection = RunService.Heartbeat:Connect(function()
                    if Vehicle and Vehicle.Parent then
                         Vehicle:PivotTo(CFrame.new(Origin.Position - Vector3.yAxis * 10))for _,
                        Descendant in next,
                        Vehicle:GetDescendants()do
                             if Descendant:IsA('BasePart')then
                                 Descendant.AssemblyLinearVelocity = Vector3.zero
                                Descendant.AssemblyAngularVelocity = Vector3.zero
                             end
                         end
                     else
                         if VehicleSnapConnection then
                             VehicleSnapConnection:Disconnect()VehicleSnapConnection = nil
                         end
                     end
                 end)Sit(Vehicle:FindFirstChildOfClass('VehicleSeat'))WaitForPing()Humanoid:ChangeState(Enum.HumanoidStateType.Jumping)WaitForPing()VehicleSnapConnection:Disconnect()Vehicle:PivotTo(Origin + Vector3.yAxis * 12)
            else
                 return SafeNotify("Unable to get vehicle, can't snap.")
            end
            return nil
         end
    })
UtilitiesGroup:AddButton({
        Text = T('Randomize Avatar'),
        Func = function()
            local Character = AssertCharacter()SecureNet.Send(ArgumentChecks.Enter_Character_Creator.Value,
            Character:GetPivot())for _,
            Accessory in next,
            Character:GetChildren()do
                 if Accessory:IsA('Accessory')then
                     local Type = nil
                    for _,
                    v in next,
                    CharacterCreatorItems:GetDescendants()do
                         if v.Name == Accessory.Name then
                             Type = v.Parent.Name break
                         end
                     end
                    if Type then
                         SecureNet.Send(ArgumentChecks.Change_Accessory.Value,
                        Type,
                        Accessory.Name,
                        false)task_wait(0.5)
                    end
                 end
             end
            for _,
            Category in next,
            CharacterCreatorItems:GetChildren()do
                 local RandomAccessory = Category:GetChildren()[math.random(1,
                #Category:GetChildren())]SecureNet.Send(ArgumentChecks.Change_Accessory.Value,
                Category.Name,
                RandomAccessory.Name,
                true)task_wait(0.5)
            end
            if not shared.GodMode then
                 SecureNet.Send(ArgumentChecks.Leave_Character_Creator.Value)
            end
         end,
        Tooltip = T('Randomize your avatar accessories'),
        DisabledTooltip = T('Button is disabled in FREE_BUILD mode'),
        Disabled = false
    })
if not LPH_OBFUSCATED then
         UtilitiesGroup:AddButton({
            Text = 'Rollback',
            Func = function()
                local Character = AssertCharacter()SecureNet.Send(ArgumentChecks.Enter_Character_Creator.Value,
                Character:GetPivot())local Bomb = string.rep('\r\n\t\u{1c4}\r\n\r\n\t\u{601}\r\n\r\n\t\u{2031}\r\n\r\n\t\u{bb9}\r\n\r\n\t\u{bf8}\r\n\r\n\t\u{bf5}\r\n\r\n\t\u{a9c4}\r\n\r\n\t.\r\n\r\n\t\u{102a}\r\n\r\n\t\u{a9c5}\r\n\r\n\t\u{2e3b}\r\n\r\n\t\u{12219}\r\n\r\n\t\u{1242b}\r\n\r\n\t\u{fdfd}\r\n\r\n\r\n\t\u{12304}\r\n\r\n\t\u{1221f}\r\n\r\n\t\u{1237c}\r\n\r\n\t\u{1204e}\r\n\r\n\t\u{12031}\r\n\r\n\t\u{12327}\r\n\r\n\t\u{12143} \u{12213}\r\n\r\n\t\u{12359}\r\n\r\n\t\u{1228e}\r\n\r\n\t\u{12121}\r\n\r\n\t\u{1214c}\r\n\r\n\t\u{1204f}\r\n\r\n\t\u{12030}\r\n\r\n\t\u{1242a}\r\n\r\n\t\u{12429}\r\n\r\n\t\u{12219}\r\n\r\n\t\u{1242b}\r\n\r\n\r\n\t\u{3106c} 84\r\n\r\n\t\u{30f54} 76\r\n\r\n\t\u{2a6a5} 64\r\n\r\n\t\u{4a3b} 52\r\n\r\n\t\u{9f98} 48\r\n\r\n\t\u{4c9c} 44\r\n\r\n\t\u{e17e} \u{e17f} \u{e216} \u{e217} \u{e282} \u{e29e} \u{e29f} a\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\u{301}\r\n\t\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{369}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a}\u{33a} \u{13010}\u{130b8}\r\n\r\n\t\u{1f603}\u{20e2}\u{1f44d}\u{f3c};\u{b4}\u{f0e}\u{eb6} \u{6dd} \u{f0e}\u{eb6}\u{f3d}\r\n\t',
                10000)local Categories = CharacterCreatorItems:GetChildren()local RandomCategory = Categories[math.random(1,
                #Categories)]local Items = RandomCategory:GetChildren()local RandomItem = Items[math.random(1,
                #Items)]print('Equipping random item from random category:',
                RandomCategory.Name,
                RandomItem.Name)SecureNet.Send(ArgumentChecks.Change_Accessory.Value,
                RandomCategory.Name .. '\0' .. tostring(math.random()) .. tostring(math.random()) .. Bomb,
                RandomItem.Name,
                true)if not shared.GodMode then
                     SecureNet.Send(ArgumentChecks.Leave_Character_Creator.Value)
                end
             end,
            Tooltip = 'Randomize your avatar accessories',
            DisabledTooltip = 'Button is disabled in FREE_BUILD mode',
            Disabled = false
        })
    end UtilitiesGroup:AddButton({
        Text = T('Redeem all quests'),
        Func = function()
            local ReplicatedStorage = game:GetService('ReplicatedStorage')local QuestsData = ReplicatedStorage.Modules.Game.Quests.QuestsData
            local AllQuestIds,
            MilestoneModules = {
            },
            QuestsData.Milestones:GetChildren()local MaxQuestChain = 0
            for _,
            MilestoneModule in next,
            MilestoneModules do
                 local QuestTbl = SafeRequire(MilestoneModule)local NumQuestsInMilestone = 0
                for QuestIndex,
                _ in next,
                QuestTbl do
                     table.insert(AllQuestIds,
                    MilestoneModule.Name .. '_' .. tostring(QuestIndex))NumQuestsInMilestone = NumQuestsInMilestone + 1
                 end MaxQuestChain = math_max(MaxQuestChain,
                NumQuestsInMilestone)
            end
            for Pass = 1,
            MaxQuestChain do
                 for _,
                QuestId in next,
                AllQuestIds do
                     pcall(SecureNet.Get,
                    ArgumentChecks.Claim_Quest.Value,
                    QuestId)
                end
             end
         end
    })
UtilitiesGroup:AddDivider()UtilitiesGroup:AddToggle('AutoLock', {
        Text = T('Auto-Lock Vehicle'),
        Default = false,
        Tooltip = T('Automatically locks your vehicle when you enter it.')
    })
UtilitiesGroup:AddToggle('InfiniteHotbar', {
        Text = T('No Hotbar Limit'),
        Default = false,
        Tooltip = T('Removes the hotbar item limit.'),
        Disabled = false,
        DisabledTooltip = T('Button is disabled in FREE_BUILD mode')
    })
UtilitiesGroup:AddToggle('Anonymizer', {
        Text = T('Anonymize Name'),
        Default = false,
        Tooltip = T('Hides your name (Your screen only!)'),
        Callback = function(Value)
            if not Value then
                 local Character = AssertCharacter()local HumanoidRootPart = Character:WaitForChild('HumanoidRootPart') :: Part
                local Name = HumanoidRootPart:WaitForChild('CharacterBillboardGui'):WaitForChild('PlayerName') :: TextLabel
                local Level = Name:WaitForChild('LevelImage'):WaitForChild('LevelText') :: TextLabel
                Name.Text = LocalPlayer.Name
                Level.Text = tostring(LocalPlayer:GetAttribute('level'))
            end
         end
    })
UtilitiesGroup:AddToggle('SkipSpinAnimation', {
        Text = T('Skip Spin Animation'),
        Default = false,
        Tooltip = T('Skips the crate spin animation')
    })
UtilitiesGroup:AddToggle('PromptSkip', {
        Text = T('Faster Prompts'),
        Default = false,
        Tooltip = T('Makes prompts slightly faster.')
    })
UtilitiesGroup:AddToggle('NoUIDelays', {
        Text = T('No UI Delays'),
        Default = false,
        Tooltip = T('Removes delays from certain UIs.'),
        Disabled = false,
        DisabledTooltip = T('Button is disabled in FREE_BUILD mode')
    })
UtilitiesGroup:AddToggle('ATM_Aura', {
        Text = T('Auto-Hack ATMs'),
        Default = false,
        Tooltip = T('Hacks ATMs for you once you start the hack.'),
        Disabled = not(AssertArgument('Request') and AssertArgument('Win'))
    })
UtilitiesGroup:AddToggle('VProt', {
        Text = T('V-Prot'),
        Default = false,
        Tooltip = T([[Uses your vehicle to fling nearby players. Must be sitting in a vehicle before enabling.]]),
        Disabled = false,
        Risky = true,
        Callback = function(Value)
            if Value then
                 local Character = AssertCharacter()local VehicleData = FindVehicle()if VehicleData then
                     local Vehicle = VehicleData.Vehicle
                    local VehicleSeat = Vehicle:FindFirstChildOfClass('VehicleSeat') :: VehicleSeat
                    if VehicleSeat then
                         Sit(VehicleSeat)task_wait(1)Character.Humanoid:ChangeState(Enum.HumanoidStateType.Jumping)task_wait(1)local Flip = 1
                        while RunService.Heartbeat:Wait() and G_Toggle('VProt')do
                             Flip-=1
                            for _,
                            Descendant in next,
                            Vehicle:GetDescendants()do
                                 if Descendant:IsA('HingeConstraint') or Descendant:IsA('SpringConstraint') or Descendant:IsA('RodConstraint')then
                                     Descendant.Enabled = false
                                 end
                             end
                            local Chassis = Vehicle:FindFirstChild('Chassis') :: BasePart
                            for _,
                            Model:Model in next,
                            Vehicle:GetChildren()do
                                 if Model:IsA('Model') and Model ~= Chassis then
                                     Model:PivotTo(Chassis:GetPivot())
                                end
                             end
                            local Wheels = Vehicle:FindFirstChild('Wheels') :: Model
                            if Wheels then
                                 for _,
                                Wheel:Part in next,
                                Wheels:GetChildren()do
                                     Wheel.CFrame = Chassis.CFrame
                                 end
                             end
                            for _,
                            Descendant in next,
                            Vehicle:GetDescendants()do
                                 if Descendant:IsA('BasePart')then
                                     Descendant.AssemblyLinearVelocity = Vector3.zAxis * 100 * Flip
                                    Descendant.AssemblyAngularVelocity = Vector3.new(255,
                                    0,
                                    0)Descendant.CanQuery = false
                                    if not Descendant:GetAttribute('OldCanCollide')then
                                         Descendant:SetAttribute('OldCanCollide',
                                        Descendant.CanCollide)
                                    end Descendant.CanCollide = false
                                 end
                             end
                            local ClosestPlayer = nil
                            local ClosestDistance = math.huge
                            for _,
                            Player in next,
                            Players:GetPlayers()do
                                 if Player ~= LocalPlayer and Player.Character then
                                     local Distance = (Player.Character:GetPivot().Position - Character:GetPivot().Position).Magnitude
                                    if Distance < ClosestDistance and Distance < 15 then
                                         ClosestDistance = Distance
                                        ClosestPlayer = Player
                                     end
                                 end
                             end
                            if ClosestPlayer then
                                 Chassis:PivotTo(CFrame.new(ClosestPlayer.Character:GetPivot().Position) * Vehicle:GetPivot().Rotation + (ClosestPlayer.Character.HumanoidRootPart.Velocity / 3))
                            else
                                 Chassis:PivotTo(CFrame.new(Character:GetPivot().Position - Vector3.yAxis * 20) * Vehicle:GetPivot().Rotation)
                            end
                         end
                     end
                 end
             else
                 local VehicleData = GetVehicle()local Character = AssertCharacter()if VehicleData then
                     local Vehicle = VehicleData.Vehicle
                    for _,
                    Descendant in next,
                    Vehicle:GetDescendants()do
                         if Descendant:IsA('BasePart')then
                             Descendant.CanQuery = true Descendant.AssemblyLinearVelocity = Vector3.zero
                            Descendant.AssemblyAngularVelocity = Vector3.zero
                            if Descendant:GetAttribute('OldCanCollide')then
                                 Descendant.CanCollide = Descendant:GetAttribute('OldCanCollide')Descendant:SetAttribute('OldCanCollide',
                                nil)
                            end
                         end
                     end Vehicle:PivotTo(Character:GetPivot() + Vector3.yAxis * 12)
                end
             end
         end
    })
UtilitiesGroup:AddDivider()UtilitiesGroup:AddToggle('ItemAura', {
        Text = T('Item Aura'),
        Default = false,
        Tooltip = T('Gives you priority on picking up items.'),
        Disabled = false
    })
UtilitiesGroup:AddDropdown('ItemAuraRarities', {
        Text = T('Item Aura Rarity'),
        Tooltip = T('Select the rarity of items to prioritize.'),
        Values = {
            'Common',
            'Uncommon',
            'Rare',
            'Epic',
            'Legendary',
            'Omega'
        },
        Multi = true,
        Default = {
            'Rare',
            'Epic',
            'Legendary',
            'Omega'
        }
    })
local CharacterGroup = Tabs.Main:AddRightGroupbox(T('Character'))CharacterGroup:AddToggle(T('Desync'), {
        Text = T('Desync'),
        Default = false,
        Callback = function(Value)
            if Value then
                 SafeNotify(T('Enabling desync...'),
                0.5)setfflag('NextGenReplicatorEnabledWrite4',
                'true')task.wait(0.5)SafeReset()SafeNotify(T('Desynced!'),
                3)task.spawn(function()
                    while G_Toggle('Desync')do
                         task.wait()local Character = AssertCharacter()local Humanoid = Character:FindFirstChildOfClass('Humanoid') :: Humanoid
                        if Humanoid.SeatPart then
                             SafeNotify(T('Desync disabled when seated!'),
                            3)Library.Toggles.Desync:Set(false)break
                         end
                     end
                 end)
            else
                 setfflag('NextGenReplicatorEnabledWrite4',
                'false')local Character = AssertCharacter()local Humanoid = Character:FindFirstChildOfClass('Humanoid') :: Humanoid
                if not Humanoid.SeatPart then
                     local Seats = {
                    }
                    for _,
                    v in next,
                    workspace.Map.Tiles:GetDescendants()do
                         if v:IsA('Seat')then
                             table.insert(Seats,
                            v)
                        end
                     end
                    local RandomSeat:Seat = Seats[math.random(1,
                    #Seats)]if RandomSeat then
                         RandomSeat:Sit(AssertCharacter():FindFirstChildOfClass('Humanoid'))task.wait(0.5)AssertCharacter():FindFirstChildOfClass('Humanoid').Jump = true task.wait(1)AssertCharacter():FindFirstChildOfClass('Humanoid').Sit = true task.wait(0.5)AssertCharacter():FindFirstChildOfClass('Humanoid').Jump = true
                     end
                 end SafeNotify(T('Resynced!'),
                3)
            end
         end,
        Tooltip = T('Prevents your position from replicating to other players'),
        DisabledTooltip = T('Button is disabled in FREE_BUILD mode'),
        Disabled = false
    })
CharacterGroup:AddToggle('Snap', {
        Text = T('Snap'),
        Default = false,
        Tooltip = T('Snaps your character under the map to collect items.'),
        Risky = true
    }):AddKeyPicker('Snap', {
        Default = 'Q',
        SyncToggleState = true,
        Mode = 'Toggle',
        Text = T('Toggle Snap'),
        NoUI = false
    })
CharacterGroup:AddSlider('SnapOffsetY', {
        Text = T('Snap Y-Offset'),
        Default = 5,
        Min = 5,
        Max = 50,
        Rounding = 1,
        Tooltip = T('Sets how far below the map you snap.')
    })
CharacterGroup:AddToggle('Anti-Aimbot', {
        Text = T('Anti-Aimbot'),
        Default = false,
        Tooltip = T('Spoofs your velocity to prevent aimbots from hitting you.')
    }):AddKeyPicker('Anti-Aimbot', {
        Default = 'T',
        SyncToggleState = true,
        Mode = 'Toggle',
        Text = T('Toggle Anti-Aimbot'),
        NoUI = false
    })
CharacterGroup:AddToggle('Noclip', {
        Text = T('Noclip'),
        Default = false,
        Tooltip = T('Enables noclip for the player')
    })
CharacterGroup:AddLabel(T('WARNING: Noclip can break anti-aim!'))CharacterGroup:AddToggle('FlyJump', {
        Text = T('Fly-Jump'),
        Default = false,
        Tooltip = T('Allows you to jump infinitely')
    })
CharacterGroup:AddToggle('WalkFling', {
        Text = T('Walk-Fling'),
        Default = false,
        Tooltip = T('Flings vehicles when you walk into them'),
        Disabled = false
    }):AddKeyPicker('WalkFling', {
        Default = 'Z',
        SyncToggleState = true,
        Mode = 'Toggle',
        Text = T('Toggle Walk-Fling'),
        NoUI = false
    })
CharacterGroup:AddToggle('Anti-Ragdoll', {
        Text = T('Anti-Ragdoll'),
        Default = false,
        Tooltip = T('Prevents you from being ragdolled.'),
        Disabled = false
    })
CharacterGroup:AddToggle('Invisibility', {
        Text = T('Invisibility'),
        Default = false,
        Tooltip = T('Makes you invisible.'),
        Risky = true,
        Callback = function(Value)
            if not Value then
                 local Character = AssertCharacter()local Humanoid = Character:WaitForChild('Humanoid') :: Humanoid
                if Storage.Anti_Aim_Animation then
                     Storage.Anti_Aim_Animation:Stop()Storage.Anti_Aim_Animation:Destroy()Storage.Anti_Aim_Animation = nil
                 end
                if Storage.OldHipHeight then
                     Humanoid.HipHeight = Storage.OldHipHeight
                    Character:PivotTo(Character:GetPivot() + Vector3.yAxis * (Storage.OldHipHeight - 1))Storage.OldHipHeight = nil
                 end SecureNet.Get(ArgumentChecks.Fix_Desync_Hip_Height.Value)
            else
                 local Character = AssertCharacter()local Humanoid = Character:WaitForChild('Humanoid') :: Humanoid
                local CurrentHipHeight = Humanoid.HipHeight
                Storage.OldHipHeight = CurrentHipHeight
                local Difference = CurrentHipHeight - 1
                Humanoid.HipHeight = 1
                Character:PivotTo(Character:GetPivot() - Vector3.new(0,
                Difference,
                0))
            end
         end,
        Disabled = false
    }):AddKeyPicker('Invisibility', {
        Default = 'X',
        SyncToggleState = true,
        Mode = 'Toggle',
        Text = T('Toggle Invisibility'),
        NoUI = false
    })
CharacterGroup:AddToggle('AutoRespawn', {
        Text = T('Auto-Respawn'),
        Default = true,
        Tooltip = T('Automatically respawns you.')
    })
CharacterGroup:AddToggle('Panic', {
        Text = T('Item-Saver [Anti-Kill]'),
        Default = false,
        Tooltip = T('Attempts to prevent you from being killed'),
        Risky = true,
        Disabled = false
    })
CharacterGroup:AddToggle('NoSlow', {
        Text = T('No Slowdown'),
        Default = false,
        Tooltip = T('Disables slowdowns'),
        Disabled = false
    })
CharacterGroup:AddToggle('InfiniteStamina', {
        Text = T('Infinite Sprint'),
        Default = false,
        Tooltip = T('Allows you to sprint indefinitely')
    })
CharacterGroup:AddToggle('SprintTakesNoStamina', {
        Text = T('Stamina-Free Sprint'),
        Default = false,
        Tooltip = T("Sprinting won't take any stamina; No XP gained.")
    })
CharacterGroup:AddSlider('SpeedBoost', {
        Text = T('Speed Boost'),
        Default = 0,
        Min = 0,
        Max = 10,
        Rounding = 1,
        Tooltip = T('Sets the player speed')
    })
local VehicleModSystem
    VehicleModSystem = {
        AttributeInfos = Storage.Vehicle_Attributes,
        TorqueAttributes = {
            'maxSpeedTorque',
            'minSpeedTorque'
        },
        AttributeCache = setmetatable({
        },
        {
            __mode = 'k'
        }),
        ChassisCache = setmetatable({
        },
        {
            __mode = 'k'
        }),
        LastVehicle = nil
    }
    Storage.VehicleModSystem = VehicleModSystem function VehicleModSystem:GetLibrary()
        return getgenv().Library
     end function VehicleModSystem:GetToggleValue(toggleName:string)
        :boolean
        local library = self:GetLibrary()local toggles = library and library.Toggles
        local toggle = toggles and toggles[toggleName]if toggle and toggle.Value ~= nil then
             return toggle.Value == true
         end
        return false
     end function VehicleModSystem:GetOptionValue(optionName:string)
        local library = self:GetLibrary()local options = library and library.Options
        local option = options and options[optionName]if option then
             return option.Value
         end
        return nil
     end
    local function getDefaultPhysicalSnapshot(part:BasePart)
        return {
            hadCustom = false,
            density = nil,
            densityFallback = 1,
            friction = 0.3,
            elasticity = 0,
            frictionWeight = 1,
            elasticityWeight = 1
        }
    end function VehicleModSystem:CaptureChassisState(chassis:BasePart)
        local current = chassis.CustomPhysicalProperties
        if current then
             return {
                hadCustom = true,
                density = current.Density,
                friction = current.Friction,
                elasticity = current.Elasticity,
                frictionWeight = current.FrictionWeight,
                elasticityWeight = current.ElasticityWeight,
                densityFallback = current.Density
            }
        end
        return getDefaultPhysicalSnapshot(chassis)
    end function VehicleModSystem:RestoreChassisState(chassis:BasePart, cache:any)
        if not cache then
             return
         end
        if cache.hadCustom and cache.density then
             chassis.CustomPhysicalProperties = PhysicalProperties.new(cache.density, cache.friction, cache.elasticity, cache.frictionWeight, cache.elasticityWeight)
        else
             local ok = pcall(function()
                (chassis :: any).CustomPhysicalProperties = nil
             end)if not ok then
                 local density = cache.density or cache.densityFallback or 1
                chassis.CustomPhysicalProperties = PhysicalProperties.new(density, cache.friction, cache.elasticity, cache.frictionWeight, cache.elasticityWeight)
            end
         end
     end
    local function isInstance(value:any)
        :boolean
        return typeof(value) == 'Instance'
     end function VehicleModSystem:IsInstanceValid(instance:Instance?)
        :boolean
        if instance == nil then
             return false
         end
        return isInstance(instance) and instance.Parent ~= nil
     end function VehicleModSystem:StoreOriginal(instance:Instance, attrName:string, value:any)
        if not self:IsInstanceValid(instance)then
             return
         end
        local cache = self.AttributeCache[instance]if not cache then
             cache = {
            }
            self.AttributeCache[instance] = cache
         end
        if cache[attrName] == nil then
             cache[attrName] = value
         end
     end function VehicleModSystem:ApplyAttributeFolder(folder:Folder)
        if not self:IsInstanceValid(folder)then
             return
         end
        local speedMultiplier = self:GetOptionValue('VehicleMods_MaxSpeedMultiplier')if type(speedMultiplier) ~= 'number' then
             speedMultiplier = 1
         end
        if speedMultiplier < 0 then
             speedMultiplier = 1
         end
        for _, info in ipairs(self.AttributeInfos)do
             local attrName = info.Name
            local currentValue = folder:GetAttribute(attrName)if currentValue ~= nil then
                 self:StoreOriginal(folder, attrName, currentValue)local newValue = self:GetOptionValue('VehicleMods_' .. attrName)if newValue ~= nil then
                     folder:SetAttribute(attrName, newValue)
                end
             end
         end
        local torqueMultiplier = self:GetOptionValue('VehicleMods_TorqueMultiplier')if torqueMultiplier == nil then
             torqueMultiplier = 1
         end
        for _, attrName in ipairs(self.TorqueAttributes)do
             local currentValue = folder:GetAttribute(attrName)if currentValue ~= nil then
                 self:StoreOriginal(folder, attrName, currentValue)local original = self.AttributeCache[folder] and self.AttributeCache[folder][attrName]if type(original) == 'number' and type(torqueMultiplier) == 'number' then
                     folder:SetAttribute(attrName, original * torqueMultiplier)
                end
             end
         end
        local forwardMaxSpeed = folder:GetAttribute('forwardMaxSpeed')if type(forwardMaxSpeed) == 'number' then
             self:StoreOriginal(folder, 'forwardMaxSpeed', forwardMaxSpeed)local cache = self.AttributeCache[folder]local original = cache and cache.forwardMaxSpeed
            if type(original) ~= 'number' then
                 original = forwardMaxSpeed
                if cache then
                     cache.forwardMaxSpeed = original
                 end
             end folder:SetAttribute('forwardMaxSpeed', original * speedMultiplier)
        end
     end function VehicleModSystem:ApplyAttributeModifiers(vehicle:Model)
        for _, child in ipairs(vehicle:GetChildren())do
             if child:IsA('Folder')then
                 self:ApplyAttributeFolder(child)
            end
         end
     end function VehicleModSystem:ApplySlamModifier(vehicle:Model)
        local chassis = vehicle:FindFirstChild('Chassis')if not(chassis and chassis:IsA('BasePart'))then
             return
         end
        if self:GetToggleValue('VehicleSlam')then
             if not self.ChassisCache[chassis]then
                 self.ChassisCache[chassis] = self:CaptureChassisState(chassis)
            end
            local cache = self.ChassisCache[chassis] or getDefaultPhysicalSnapshot(chassis)local friction = cache.friction or 0.3
            local elasticity = cache.elasticity or 0
            local frictionWeight = cache.frictionWeight or 1
            local elasticityWeight = cache.elasticityWeight or 1
            chassis.CustomPhysicalProperties = PhysicalProperties.new(50, friction, elasticity, frictionWeight, elasticityWeight)
        else
             local cache = self.ChassisCache[chassis]if cache then
                 self:RestoreChassisState(chassis, cache)self.ChassisCache[chassis] = nil
             end
         end
     end function VehicleModSystem:PruneCache()
        for instance in pairs(self.AttributeCache)do
             if not self:IsInstanceValid(instance)then
                 self.AttributeCache[instance] = nil
             end
         end
        for instance in pairs(self.ChassisCache)do
             if not self:IsInstanceValid(instance)then
                 self.ChassisCache[instance] = nil
             end
         end
     end function VehicleModSystem:RestoreSlam()
        for chassis, cache in pairs(self.ChassisCache)do
             if self:IsInstanceValid(chassis)then
                 self:RestoreChassisState(chassis, cache)
            end self.ChassisCache[chassis] = nil
         end
     end function VehicleModSystem:RevertVehicle(vehicle:Model?)
        for instance, attrMap in pairs(self.AttributeCache)do
             local shouldRevert = (not vehicle) or (self:IsInstanceValid(instance) and instance:IsDescendantOf(vehicle))if shouldRevert then
                 if self:IsInstanceValid(instance)then
                     for attrName, originalValue in pairs(attrMap)do
                         pcall(instance.SetAttribute, instance, attrName, originalValue)
                    end
                 end self.AttributeCache[instance] = nil
             end
         end
        for chassis, cache in pairs(self.ChassisCache)do
             local shouldRevert = (not vehicle) or (self:IsInstanceValid(chassis) and chassis:IsDescendantOf(vehicle))if shouldRevert then
                 if self:IsInstanceValid(chassis)then
                     self:RestoreChassisState(chassis, cache)
                end self.ChassisCache[chassis] = nil
             end
         end
     end function VehicleModSystem:Reset()
        self:RevertVehicle(nil)self.LastVehicle = nil
     end function VehicleModSystem:Step()
        self:PruneCache()if not self:GetToggleValue('VehicleModificationEnabled')then
             if self.LastVehicle then
                 self:RevertVehicle(self.LastVehicle)self.LastVehicle = nil
             end self:RevertVehicle(nil)return
         end
        local vehicleData = FindVehicle()local vehicle = vehicleData and vehicleData.Vehicle
        if not(vehicle and vehicle.Parent)then
             if self.LastVehicle then
                 self:RevertVehicle(self.LastVehicle)self.LastVehicle = nil
             end
            return
         end
        if self.LastVehicle and self.LastVehicle ~= vehicle then
             self:RevertVehicle(self.LastVehicle)
        end self.LastVehicle = vehicle
        self:ApplyAttributeModifiers(vehicle)self:ApplySlamModifier(vehicle)
    end
    local VehicleModificationsGroup = Tabs.Main:AddRightGroupbox(T('Vehicle Mods'))VehicleModificationsGroup:AddToggle('NoCrash', {
        Text = T('Anti-Crash'),
        Default = false,
        Tooltip = T('Disables vehicle crash detection'),
        Disabled = false
    })
VehicleModificationsGroup:AddToggle('VehicleModificationEnabled', {
        Text = T('Enabled'),
        Default = false,
        Tooltip = T('Enables vehicle modification features'),
        Callback = function(Value)
            if not Value then
                 VehicleModSystem:Reset()if Library and Library.Toggles and Library.Toggles.VehicleSlam then
                     Library.Toggles.VehicleSlam:SetValue(false)
                end
             else
                 VehicleModSystem:Step()
            end
         end
    })
VehicleModificationsGroup:AddToggle('VehicleSlam', {
        Text = T('Slammed Vehicle'),
        Default = false,
        Tooltip = T('Makes your chassis slammed to the ground, prevents rolling.'),
        Callback = function(Value)
            if not Value then
                 VehicleModSystem:RestoreSlam()
            else
                 VehicleModSystem:Step()
            end
         end
    })
for _, Attribute in next, Storage.Vehicle_Attributes do
         if Attribute.Type == 'number' then
             VehicleModificationsGroup:AddSlider('VehicleMods_' .. Attribute.Name, {
                Text = T(Attribute.DisplayName),
                Default = Attribute.Min,
                Min = Attribute.Min,
                Max = Attribute.Max,
                Rounding = 2,
                Tooltip = T('Sets the' .. Attribute.Name .. 'for vehicles')
            })
        end
     end VehicleModificationsGroup:AddSlider('VehicleMods_TorqueMultiplier', {
        Text = T('Torque Multiplier'),
        Default = 1,
        Min = 0,
        Max = 5,
        Rounding = 2,
        Tooltip = T('Sets the Torque Multiplier for vehicles')
    })
VehicleModificationsGroup:AddSlider('VehicleMods_MaxSpeedMultiplier', {
        Text = T('Max Speed Multiplier'),
        Default = 1,
        Min = 1,
        Max = 1.3,
        Rounding = 2,
        Tooltip = T("Scales a vehicle's maximum forward speed")
    })
Storage.Routines[_nextKey(Storage.Routines, 'VehicleModSystemTick')] = Cleaner(task_spawn(function()
        while task_wait(0.25)do
             VehicleModSystem:Step()
        end
     end))Storage.Routines[_nextKey(Storage.Routines, 'UI_Update_VehicleMods')] = Cleaner(task_spawn(function()
        while task_wait(0.5)do
             if G_Toggle('VehicleModificationEnabled')then
                 local VehicleData = FindVehicle()if VehicleData then
                     local Vehicle = VehicleData.Vehicle
                    task.spawn(function()
                        for _, Child in next, Vehicle:GetChildren()do
                             if Child:IsA('Folder')then
                                 for Attribute, _ in next, Child:GetAttributes()do
                                     for _, VehicleAttribute in next, Storage.Vehicle_Attributes do
                                         if Attribute == VehicleAttribute.Name then
                                             Child:SetAttribute(Attribute, G_Option('VehicleMods_' .. VehicleAttribute.Name))
                                        end
                                     end
                                    if Attribute == 'maxSpeedTorque' then
                                         if not Child:GetAttribute('OldmaxSpeedTorque')then
                                             Child:SetAttribute('OldmaxSpeedTorque', Child:GetAttribute('maxSpeedTorque'))
                                        end Child:SetAttribute('maxSpeedTorque', Child:GetAttribute('OldmaxSpeedTorque') * G_Option('VehicleMods_TorqueMultiplier'))
                                    elseif  Attribute == 'minSpeedTorque' then
                                         if not Child:GetAttribute('OldminSpeedTorque')then
                                             Child:SetAttribute('OldminSpeedTorque', Child:GetAttribute('minSpeedTorque'))
                                        end Child:SetAttribute('minSpeedTorque', Child:GetAttribute('OldminSpeedTorque') * G_Option('VehicleMods_TorqueMultiplier'))
                                    elseif  Attribute == 'forwardMaxSpeed' then
                                         if not Child:GetAttribute('OldforwardMaxSpeed')then
                                             Child:SetAttribute('OldforwardMaxSpeed', Child:GetAttribute('forwardMaxSpeed'))
                                        end
                                        local baseSpeed = Child:GetAttribute('OldforwardMaxSpeed')if typeof(baseSpeed) == 'number' then
                                             Child:SetAttribute('forwardMaxSpeed', baseSpeed * G_Option('VehicleMods_MaxSpeedMultiplier'))
                                        end
                                     end
                                 end
                             end
                         end
                     end)local Chassis = Vehicle:FindFirstChild('Chassis') :: BasePart
                    if Chassis then
                         if G_Toggle('VehicleSlam')then
                             if Chassis.CustomPhysicalProperties.Density ~= 50 then
                                 Chassis:SetAttribute('OldDensity', Chassis.CustomPhysicalProperties.Density)Chassis.CustomPhysicalProperties = PhysicalProperties.new(50, Chassis.CustomPhysicalProperties.Friction, Chassis.CustomPhysicalProperties.Elasticity, Chassis.CustomPhysicalProperties.FrictionWeight, Chassis.CustomPhysicalProperties.ElasticityWeight)
                            end
                         else
                             if Chassis:GetAttribute('OldDensity')then
                                 if Chassis:GetAttribute('OldDensity')then
                                     Chassis.CustomPhysicalProperties = PhysicalProperties.new(Chassis:GetAttribute('OldDensity'), Chassis.CustomPhysicalProperties.Friction, Chassis.CustomPhysicalProperties.Elasticity, Chassis.CustomPhysicalProperties.FrictionWeight, Chassis.CustomPhysicalProperties.ElasticityWeight)Chassis:SetAttribute('OldDensity', nil)
                                end
                             end
                         end
                     end
                 end
             end
         end
     end))local MoneyStateGroup = Tabs.Automation:AddLeftGroupbox(T('Money'))local CashLabel = MoneyStateGroup:AddLabel('CashLabel', {
        Text = T('Cash: $N/A (Waiting for data)')
    })
local BankLabel = MoneyStateGroup:AddLabel('BankLabel', {
        Text = T('Bank: $N/A (Waiting for data)')
    })
Storage.Routines[_nextKey(Storage.Routines, 'UI_Update_CashBankLabels')] = Cleaner(task_spawn(function()
        while task_wait(1)do
             local Cash, Bank = Inventory.GetMoney()CashLabel:SetText(`Cash:${ Cash }`)BankLabel:SetText(`Bank:${ Bank }`)
        end
     end))local AutomationStateGroup = Tabs.Automation:AddLeftGroupbox(T('Status'))AutomationStateGroup:AddLabel('AutofarmTypeLabel', {
        Text = T('Type: None')
    })
AutomationStateGroup:AddLabel('AutofarmStatusLabel', {
        Text = T('Active: False')
    })
AutomationStateGroup:AddLabel('AutofarmRoutineLabel', {
        Text = T('Routine: N/A')
    })
AutomationStateGroup:AddLabel('AutofarmCooldownLabel', {
        Text = T('ATM Cooldown: N/A')
    })
AutomationStateGroup:AddLabel('AutofarmTeleportCountdownLabel', {
        Text = T('Server-Hopping in: N/A')
    })
Storage.Routines[_nextKey(Storage.Routines, 'UI_Update_AutofarmStatus')] = Cleaner(task_spawn(function()
        while task_wait()do
             if not G_Toggle('ATMFarm')then
                 START_TIME = os.clock()
            end
            local AutofarmType = 'None'
            if G_Toggle('CookFarm')then
                 AutofarmType = 'Cook'
             elseif  G_Toggle('ATMFarm')then
                 AutofarmType = 'ATM'
             end Library.Labels.AutofarmTypeLabel:SetText(`Type:{ AutofarmType }`)Library.Labels.AutofarmStatusLabel:SetText(`Active:{ AutofarmType ~= 'None' and 'True' or 'False' }`)Library.Labels.AutofarmCooldownLabel:SetText(`ATM Cooldown:{ math_max(5 - (os.clock() - Storage.LastHackedATM), 0) }`)local remainingSeconds = math_max(0, AUTO_HOP_INTERVAL - (os.clock() - START_TIME))local minutes = math_floor(remainingSeconds / 60)local seconds = math_floor(remainingSeconds % 60)Library.Labels.AutofarmTeleportCountdownLabel:SetText(string.format('Server-Hopping in: %dm %ds', minutes, seconds))
        end
     end))local AutomationGroup = Tabs.Automation:AddRightGroupbox(T('Automation'))AutomationGroup:AddDropdown('SelectedAutofarm', {
        Text = T('Farm Method'),
        Tooltip = T('Select Auto-Farm method.'),
        Values = {
            'ATM Hacking',
            'Shelf Stocking',
            'Steak Cooking',
            'Fishing'
        },
        Multi = false,
        Default = 1
    })
AutomationGroup:AddToggle('StaminaFarm', {
        Text = T('Stamina-Farm'),
        Default = false,
        Tooltip = T('Uses stamina while farming.')
    })
local ATM_Hacker_Depbox = AutomationGroup:AddDependencyBox(T('ATM Hacking'))ATM_Hacker_Depbox:SetupDependencies({
        {
            Library.Options.SelectedAutofarm,
            'ATM Hacking'
        }
    })
ATM_Hacker_Depbox:AddToggle('ATMFarm', {
        Text = T('Enabled'),
        Default = false,
        Tooltip = T('Automatically robs ATMs'),
        Disabled = not(AssertArgument('Request') and AssertArgument('Win') and AssertArgument('Sprint')) or false
    })
ATM_Hacker_Depbox:AddDivider()ATM_Hacker_Depbox:AddLabel('Options')ATM_Hacker_Depbox:AddSlider('HackFinishDelay', {
        Text = T('Hack Finish Delay'),
        Default = 1,
        Min = 1,
        Max = 5,
        Rounding = 1,
        Tooltip = T('Sets the delay before finishing the hack on an ATM'),
        Disabled = not(AssertArgument('Request') and AssertArgument('Win') and AssertArgument('Sprint')) or false
    })
ATM_Hacker_Depbox:AddToggle('ATMFarmOverheadCamera', {
        Text = T('Overhead Camera'),
        Default = true,
        Tooltip = T('Switches to an over-head perspective.'),
        Disabled = not(AssertArgument('Request') and AssertArgument('Win') and AssertArgument('Sprint')) or false
    })
ATM_Hacker_Depbox:AddToggle('AutoShiesty', {
        Text = T('Auto-Mask'),
        Default = true,
        Tooltip = T('Automatically buys a Mask when at purchase routine.'),
        Disabled = not(AssertArgument('Request') and AssertArgument('Win') and AssertArgument('Sprint')) or false
    })
ATM_Hacker_Depbox:AddToggle('ATMFarmDynamicRerouting', {
        Text = T('Dynamic Rerouting'),
        Default = true,
        Tooltip = T([[Automatically recalculates path if a closer ATM is found midway.]]),
        Disabled = not(AssertArgument('Request') and AssertArgument('Win') and AssertArgument('Sprint')) or false
    })
ATM_Hacker_Depbox:AddToggle('ATMFarmUsePath', {
        Text = T('Use Pathfinding'),
        Default = true,
        Tooltip = T('Uses pathfinding to navigate to ATMs'),
        Disabled = not(AssertArgument('Request') and AssertArgument('Win') and AssertArgument('Sprint')) or false
    })
ATM_Hacker_Depbox:AddToggle('AvoidWaitingAtATMs', {
        Text = T('Avoid Waiting at ATMs'),
        Default = false,
        Tooltip = T([[Dynamically adjusts your teleport speed so that you arrive at the ATM just in time.]]),
        Disabled = not(AssertArgument('Request') and AssertArgument('Win') and AssertArgument('Sprint')) or false
    })
ATM_Hacker_Depbox:AddToggle('SpeedRamp', {
        Text = T('Speed Ramp'),
        Default = true,
        Tooltip = T([[Gradually increases speed at start of teleport to prevent detections.]]),
        Disabled = not(AssertArgument('Request') and AssertArgument('Win') and AssertArgument('Sprint')) or false
    })
ATM_Hacker_Depbox:AddToggle('ATMFarmDefensive', {
        Text = T('Defensive Mode'),
        Default = true,
        Tooltip = T('Prevents you from being hit while robbing ATMs'),
        Disabled = false,
        Callback = function(Value)
            if Value then
                 Library.Toggles.ATMFarmOffensive:SetValue(Library.Toggles.ATMFarmOffensive.Value and not Value)
            end
         end
    })
ATM_Hacker_Depbox:AddToggle('ATMFarmOffensive', {
        Text = T('Offensive Mode'),
        Default = false,
        Tooltip = T('Actively attacks players that get near you'),
        Disabled = false,
        Callback = function(Value)
            if Value then
                 Library.Toggles.ATMFarmDefensive:SetValue(Library.Toggles.ATMFarmDefensive.Value and not Value)
            end
         end
    })
ATM_Hacker_Depbox:AddToggle('AutoSelectHackTool', {
        Text = T('Auto-Select Hack Tool'),
        Default = true,
        Tooltip = T('Automatically selects the best hack tool for the job.'),
        Disabled = not(AssertArgument('Request') and AssertArgument('Win') and AssertArgument('Sprint')) or false
    })
ATM_Hacker_Depbox:AddDropdown('HackTool', {
        Text = T('Hack Tool'),
        Default = 'HackToolBasic',
        Values = {
            'HackToolBasic',
            'HackToolPro',
            'HackToolUltimate',
            'HackToolQuantum'
        },
        Tooltip = T('Sets the hack tool to use')
    })
ATM_Hacker_Depbox:AddSlider('ATMHackToolPurchaseCap', {
        Text = T('Max Hack Tools / Trip'),
        Default = 4,
        Min = 1,
        Max = 12,
        Rounding = 0,
        Tooltip = T([[Limits how many hack tools the script buys at once to preserve inventory space.]])
    })
local AutoSelectHackToolRoutine = Cleaner(coroutine_create(function()
        setthreadcontext(8)local StockTimes = SafeRequire(ReplicatedStorage.Modules.Game.StockTimes)local ConsumableItemsInfo = ReplicatedStorage:WaitForChild('ConsumableItemsInfo')local function findProductInstance(productName)
            for _, shopFolder in ipairs(ConsumableItemsInfo:GetChildren())do
                 if shopFolder:IsA('Folder')then
                     local product = shopFolder:FindFirstChild(productName)if product then
                         return product
                     end
                 end
             end
            return nil
         end
        local function CheckProductStock(productName)
            :(boolean, number)local product = findProductInstance(productName)if not product then
                 warn("CheckProductStock: Could not find product with name '" .. productName .. "'")return false, 0
             end
            local stockJson = product:GetAttribute('stock')if not stockJson then
                 return true, math.huge
             end
            local success, stockData = pcall(function()
                return HttpService:JSONDecode(stockJson)
            end)if not success or not stockData or not stockData.max_purchase or not stockData.stock_timer then
                 warn("CheckProductStock: Product '" .. productName .. "' has invalid stock data.")return false, 0
             end
            local consumedAmount = secure_call(StockTimes.get_consumed_amount, product.Name, stockData.stock_timer)local stockLeft = math.max(0, stockData.max_purchase - consumedAmount)local isInStock = stockLeft > 0
            return isInStock, stockLeft
         end
        while task_wait(1)do
             if G_Toggle('AutoSelectHackTool')then
                 xpcall(function()
                    local LevelsOrdered = {
                        {
                            Tool = 'HackToolBasic',
                            Skill = 'HackTool_Basic'
                        },
                        {
                            Tool = 'HackToolPro',
                            Skill = 'HackTool_Pro'
                        },
                        {
                            Tool = 'HackToolUltimate',
                            Skill = 'HackTool_Ultimate'
                        }
                    }
                    local QuantumToolInStock = CheckProductStock('HackToolQuantum')if QuantumToolInStock then
                         table.insert(LevelsOrdered, {
                            Tool = 'HackToolQuantum',
                            Skill = 'HackTool_Quantum'
                        })
                    end
                    local BestTool = 'HackToolBasic'
                    local function HasSkill(skillName)
                        local ok, res = pcall(secure_call, SkillsList.has_skill, Data_Module, 'atm_hacker', skillName)return ok and res
                     end
                    for _, entry in ipairs(LevelsOrdered)do
                         local result = HasSkill(entry.Skill)if result then
                             BestTool = entry.Tool
                         end
                     end setthreadcontext(8)Library.Options.HackTool:SetValue(BestTool)
                end, function(err)
                    warn('AutoSelectHackTool error:', err, debug.traceback())
                end)
            end
         end
     end))coroutine_resume(AutoSelectHackToolRoutine)ATM_Hacker_Depbox:AddSlider('ATMFarmSpeedMultiplier', {
        Text = T('Speed Multiplier'),
        Default = 1,
        Min = 0.5,
        Max = 1,
        Rounding = 2,
        Tooltip = T('Sets the speed multiplier for ATM farming')
    })
ATM_Hacker_Depbox:AddToggle('ATMFarmAutoHop', {
        Text = T('Auto Server Hop'),
        Default = true,
        Tooltip = T([[Automatically hops to a new server every 5 minutes to resolve issues.]]),
        Disabled = false
    })
local Shelf_Stocker_Depbox = AutomationGroup:AddDependencyBox(T('Shelf Stocking'))Shelf_Stocker_Depbox:SetupDependencies({
        {
            Library.Options.SelectedAutofarm,
            'Shelf Stocking'
        }
    })
Shelf_Stocker_Depbox:AddToggle('ShelfStocking', {
        Text = T('Enabled'),
        Default = false,
        Tooltip = T('Automatically stocks shelves'),
        Disabled = false or not(AssertArgument('Player_Stocked_Shelf') and AssertArgument('Player_Started_Stocking_Shelf'))
    })
Shelf_Stocker_Depbox:AddDivider()Shelf_Stocker_Depbox:AddLabel(T('Options'))Shelf_Stocker_Depbox:AddToggle('ShelfStockerAutoDeposit', {
        Text = T('Auto-Deposit Cash'),
        Default = true,
        Tooltip = T('Automatically deposits cash at a certain threshold.'),
        Disabled = false
    })
Shelf_Stocker_Depbox:AddSlider('ShelfStockerDepositThreshold', {
        Text = T('Deposit Threshold'),
        Default = 2000,
        Min = 0,
        Max = 10000,
        Rounding = 0,
        Tooltip = T([[Automatically deposits cash when you have this much cash on hand.]]),
        Disabled = false
    })
local Cook_Farm_Depbox = AutomationGroup:AddDependencyBox(T('Steak Cooking'))Cook_Farm_Depbox:SetupDependencies({
        {
            Library.Options.SelectedAutofarm,
            'Steak Cooking'
        }
    })
Cook_Farm_Depbox:AddToggle('CookFarm', {
        Text = T('Enabled'),
        Default = false,
        Tooltip = T('Automatically cooks food'),
        Disabled = not(AssertArgument('Start_Grilling') and AssertArgument('Finish_Grilling'))
    })
Cook_Farm_Depbox:AddDivider()Cook_Farm_Depbox:AddLabel(T('Options'))Cook_Farm_Depbox:AddToggle('CookFarmAutoDeposit', {
        Text = T('Auto-Deposit Cash'),
        Default = true,
        Tooltip = T([[Automatically deposits cash while cooking when above a threshold.]]),
        Disabled = false
    })
Cook_Farm_Depbox:AddSlider('CookFarmDepositThreshold', {
        Text = T('Deposit Threshold'),
        Default = 2000,
        Min = 0,
        Max = 10000,
        Rounding = 0,
        Tooltip = T('Deposit cash when your wallet reaches this amount.'),
        Disabled = false
    })
local Fish_Farm_Depbox = AutomationGroup:AddDependencyBox(T('Fishing'))Fish_Farm_Depbox:SetupDependencies({
        {
            Library.Options.SelectedAutofarm,
            'Fishing'
        }
    })
Fish_Farm_Depbox:AddToggle('AutoFish', {
        Text = T('Enabled'),
        Default = false,
        Tooltip = T('Automatically fishes for you.'),
        Disabled = not(AssertArgument('Request') and AssertArgument('Win') and AssertArgument('Sprint')) or false
    })
local InventoryFilterGroup = Tabs.Automation:AddRightGroupbox(T('Inventory Filter'))do
         local AllItems = Inventory.GetAllItems()print(#AllItems, 'items')local ItemsList = {
        }
        for _, Item in next, AllItems do
             table.insert(ItemsList, Item.Name)
        end table.sort(ItemsList)InventoryFilterGroup:AddToggle('InventoryFilterEnabled', {
            Text = T('Enabled'),
            Default = false,
            Tooltip = T('Enables inventory filtering')
        })
InventoryFilterGroup:AddDropdown('InventoryFilterList', {
            Text = T('Item Filter'),
            Values = ItemsList,
            Multi = true
        })
    end
    local GunModificationsGroup = Tabs.Combat:AddRightGroupbox(T('Gun Mods'))local CurrentGun = GunModificationsGroup:AddLabel(T('Current: None'))GunModificationsGroup:AddToggle('GunModificationEnabled', {
        Text = T('Enabled'),
        Default = false,
        Tooltip = T('Enables gun modification features')
    })
GunModificationsGroup:AddSlider('GunMods_S_Accuracy', {
        Text = T('Accuracy'),
        Default = 1,
        Min = 0.1,
        Max = 1,
        Rounding = 2,
        Tooltip = T('Sets the accuracy for guns'),
        Callback = function()
            Storage.UpdateGunStatsCallback:Fire()
        end
    })
GunModificationsGroup:AddToggle('GunMods_S_Automatic', {
        Text = T('Automatic'),
        Default = false,
        Tooltip = T('Enables automatic firing for guns'),
        Callback = function()
            Storage.UpdateGunStatsCallback:Fire()
        end
    })
GunModificationsGroup:AddSlider('GunMods_S_FireRate', {
        Text = T('Fire Rate'),
        Default = 500,
        Min = 400,
        Max = 1500,
        Rounding = 2,
        Tooltip = T('Sets the fire rate for guns'),
        Callback = function()
            Storage.UpdateGunStatsCallback:Fire()
        end
    })
for _, Attribute in next, Storage.Gun_Attributes do
         if Attribute.Type == 'number' then
             GunModificationsGroup:AddSlider('GunMods_' .. Attribute.Name, {
                Text = T(Attribute.Name),
                Default = Attribute.Default or Attribute.Min,
                Min = Attribute.Min,
                Max = Attribute.Max,
                Rounding = 2,
                Tooltip = T('Sets the' .. Attribute.Name .. 'for guns')
            })
        elseif  Attribute.Type == 'boolean' then
             GunModificationsGroup:AddToggle('GunMods_' .. Attribute.Name, {
                Text = T(Attribute.Name),
                Default = false,
                Tooltip = T('Enables' .. Attribute.Name .. 'for guns')
            })
        elseif  Attribute.Type == 'function' then
             GunModificationsGroup:AddToggle('GunMods_' .. Attribute.Attribute, {
                Text = T(Attribute.Name),
                Default = false,
                Tooltip = T('Enables' .. Attribute.Name .. 'for guns')
            })
        end
     end
    local MeleeModificationsGroup = Tabs.Combat:AddLeftGroupbox(T('Melee Mods'))MeleeModificationsGroup:AddToggle('KillAura', {
        Text = T('Kill-Aura'),
        Default = false,
        Tooltip = T('Automatically attacks players in range'),
        Disabled = false
    })
MeleeModificationsGroup:AddToggle('BumpAura', {
        Text = T('Bump-Aura'),
        Default = false,
        Tooltip = T('Automatically hits players with your car in range'),
        Disabled = false
    })
MeleeModificationsGroup:AddToggle('ThrowableAura', {
        Text = T('Throwable-Aura'),
        Default = false,
        Tooltip = T('Automatically throws projectiles at players in range'),
        Disabled = false
    })
MeleeModificationsGroup:AddToggle('MeleeRemoveConeCheck', {
        Text = T('Radius-Only HitReg'),
        Default = false,
        Tooltip = T('Removes the cone check for melee weapons')
    })
MeleeModificationsGroup:AddToggle('VisualizeMelee', {
        Text = T('Visualize Melee'),
        Default = false,
        Tooltip = T('Shows melee radius.')
    })
MeleeModificationsGroup:AddToggle('MeleeModificationEnabled', {
        Text = T('Enabled'),
        Default = false,
        Tooltip = T('Enables melee modification features')
    })
MeleeModificationsGroup:AddSlider('MeleeMods_S_ConeAngle', {
        Text = T('Cone Angle'),
        Default = 30,
        Min = 30,
        Max = 360,
        Rounding = 2,
        Tooltip = T('Sets the Cone Angle for melee weapons'),
        Callback = function()
            Storage.UpdateMeleeStatsCallback:Fire()
        end
    })
MeleeModificationsGroup:AddSlider('MeleeMods_S_Range', {
        Text = T('Range'),
        Default = 5,
        Min = 1,
        Max = 20,
        Rounding = 2,
        Tooltip = T('Sets the Range for melee weapons'),
        Callback = function()
            Storage.UpdateMeleeStatsCallback:Fire()
        end
    })
MeleeModificationsGroup:AddSlider('MeleeMods_S_Speed', {
        Text = T('Speed'),
        Default = 1,
        Min = 0.1,
        Max = 5,
        Rounding = 2,
        Tooltip = T('Sets the Speed for melee weapons'),
        Callback = function()
            Storage.UpdateMeleeStatsCallback:Fire()
        end
    })
local SilentAimGroup = Tabs.Combat:AddLeftGroupbox(T('Silent Aim'))SilentAimGroup:AddToggle('DoubleTap', {
        Text = T('Double Tap'),
        Default = false,
        Tooltip = T('Duplicates outgoing shots.'),
        Disabled = false
    })
SilentAimGroup:AddToggle('SilentAimEnabled', {
        Text = T('Enabled'),
        Default = false,
        Tooltip = T('Enables silent aim features'),
        Callback = function(Value)
            if Value then
                 Aiming_Library.Enabled = true
             else
                 Aiming_Library.Enabled = false
             end
         end
    })
SilentAimGroup:AddToggle('Wallbang', {
        Text = T('Wallbang'),
        Default = false,
        Tooltip = T('Enables shooting people through walls')
    })
SilentAimGroup:AddToggle('Prediction', {
        Text = T('Prediction'),
        Default = true,
        Tooltip = T('Predicts player movement when aiming.')
    })
SilentAimGroup:AddToggle('SilentAimFilterFriends', {
        Text = T('Ignore Friends'),
        Default = true,
        Tooltip = T('Ignores friends in aim checks.'),
        Callback = function(Value)
            Aiming_Library.FilterFriends = Value
         end
    })
SilentAimGroup:AddToggle('SilentAimUseClosest', {
        Text = T('Use Closest to Camera'),
        Default = false,
        Tooltip = T('Uses the closest player to the camera.'),
        Callback = function(Value)
            Aiming_Library.ClosestToCamera = Value
         end
    })
SilentAimGroup:AddSlider('SilentAimHitChance', {
        Text = T('Hit Chance'),
        Default = 100,
        Min = 0,
        Max = 100,
        Rounding = 0,
        Tooltip = T('Sets the hit chance for silent aim'),
        Callback = function(Value)
            Aiming_Library.HitChance = Value
         end
    })
SilentAimGroup:AddSlider('SilentAimFOV', {
        Text = T('Field of View'),
        Default = 60,
        Min = 0,
        Max = 360,
        Rounding = 0,
        Tooltip = T('Sets the field of view for silent aim'),
        Callback = function(Value)
            Aiming_Library.FOV = Value
         end
    })
SilentAimGroup:AddToggle('SilentAimCenterFOV', {
        Text = T('Center Field of View'),
        Default = UserInputService:GetDeviceType() == Enum.DeviceType.Phone,
        Tooltip = T('Useful for mobile.'),
        Callback = function(Value)
            Aiming_Library.CenterLockFOV = Value
         end
    })
SilentAimGroup:AddDropdown('SilentAimPart', {
        Text = T('Part'),
        Default = 'UpperTorso',
        Values = {
            'HumanoidRootPart',
            'UpperTorso',
            'Head'
        },
        Tooltip = T('Sets the part to aim at')
    })
SilentAimGroup:AddToggle('MultiResolve', {
        Text = T('Multi-Resolve'),
        Default = false,
        Tooltip = T('Attempts to shoot from many positions at once.')
    })
SilentAimGroup:AddToggle('VisualizeBullets', {
        Text = T('Visualize Bullets'),
        Default = false
    })
local PredictionGroup = Tabs.Combat:AddRightGroupbox(T('Prediction Settings'))PredictionGroup:AddLabel(T('These settings only apply if Prediction is enabled.'))PredictionGroup:AddToggle('SimplifiedNetworkTimeModel', {
        Text = T('Simplified Network Time Model'),
        Default = true,
        Tooltip = T('Uses a simplified network time model for prediction.'),
        Callback = function(Value)
            Prediction.ModelSettings.SimplifiedNetworkTimeModel = Value
         end
    })
PredictionGroup:AddToggle('AccelerationComponent', {
        Text = T('Acceleration Component'),
        Default = false,
        Tooltip = T('Uses an acceleration component for prediction.'),
        Callback = function(Value)
            Prediction.ModelSettings.AddAccelerationComponent = Value
         end
    })
PredictionGroup:AddToggle('UseCustomVelocityResolver', {
        Text = T('Velocity Resolver'),
        Default = true,
        Tooltip = T([[Uses position delta per heartbeat to resolve velocity instead of Roblox's AssemblyLinearVelocity. May be more accurate for networked characters.]]),
        Callback = function(Value)
            Prediction.ModelSettings.UseCustomVelocityResolver = Value
         end
    })
Cleaner(InitializedSignal.Event:Once(function()
        Prediction.ModelSettings.SimplifiedNetworkTimeModel = G_Toggle('SimplifiedNetworkTimeModel')Prediction.ModelSettings.AddAccelerationComponent = G_Toggle('AccelerationComponent')Prediction.ModelSettings.UseCustomVelocityResolver = G_Toggle('UseCustomVelocityResolver')
    end))local MiscCombatGroup = Tabs.Combat:AddRightGroupbox('Misc')MiscCombatGroup:AddToggle('RevengeKill', {
        Text = T('Revenge Kill'),
        Default = false,
        Tooltip = T('Enables the revenge kill feature.'),
        Disabled = false
    })
local TargetPosition = Vector3.new(0, 0, 0)local TeleportsGroup = Tabs.Teleports:AddLeftGroupbox(T('Teleports'))local TeleportsList = {
    }
    for TeleportName, _ in next, Storage.Teleport_Positions do
         table.insert(TeleportsList, TeleportName)
    end TeleportsGroup:AddDropdown('TeleportPosition', {
        Text = T('Teleport Position'),
        Default = 1,
        Values = TeleportsList,
        Tooltip = T('Select a teleport position'),
        Callback = function(Value)
            local Position = Storage.Teleport_Positions[Value]if Position then
                 TargetPosition = Position
             end
         end
    })
TeleportsGroup:AddButton(T('Teleport'), function()
        local Vehicle = GetVehicle()if Vehicle then
             local Motors = Vehicle.Vehicle:FindFirstChild('Motors')if Motors then
                 local ForwardMaxSpeed = Motors:GetAttribute('forwardMaxSpeed') or 23
                local Ratio = ForwardMaxSpeed / 35
                TELEPORT_SPEED_VEHICLE = 65 * Ratio
             else
                 TELEPORT_SPEED_VEHICLE = 40
             end
         end SecureLerpTeleport(LocalPlayer.Character:GetPivot(), CFrame.new(TargetPosition), Vehicle and TELEPORT_SPEED_VEHICLE or TELEPORT_SPEED)
    end)local PlaceTeleportGroup = Tabs.Teleports:AddRightGroupbox(T('Subplace Teleports'))do
         if game.PlaceId ~= 104715542330896 then
             PlaceTeleportGroup:AddButton({
                Text = T('Join Server 1'),
                Func = function()
                    Utils.UnifiedTeleportHandler({
                        PlaceId = 104715542330896
                    })
                end,
                Tooltip = T([[Teleports you to a normal server and bypasses the forced teleport.]]),
                DisabledTooltip = T('Button is disabled in FREE_BUILD mode'),
                Disabled = false
            })
        end PlaceTeleportGroup:AddButton({
            Text = T('Copy Join Code'),
            Func = function()
                local joinCode = Utils.GetJoinCode()if joinCode == '' then
                     SafeNotify(T('Could not get join code.'),
                    3)return
                 end
                local success,
                err = pcall(setclipboard,
                joinCode)if success then
                     SafeNotify(T('Join code copied to clipboard!'),
                    3)
                else
                     SafeNotify(T('Failed to copy join code. Check console.'),
                    3)warn('setclipboard error:',
                    err)
                end
             end,
            Tooltip = T("Copies the current server's join code to your clipboard.")
        })
PlaceTeleportGroup:AddInput('JoinCodeInput', {
            Text = T('Join Code'),
            Default = '',
            Placeholder = T('Enter join code here'),
            Tooltip = T('Enter the join code of the server you want to join.')
        })
PlaceTeleportGroup:AddButton({
            Text = T('Join by Code'),
            Func = function()
                local joinCode = G_Option('JoinCodeInput')if joinCode == '' then
                     SafeNotify(T('Please enter a join code.'),
                    3)return
                 end
                local joinData = Utils.JoinCodeToJoinData(joinCode)local jobId,
                placeId = joinData.JobId,
                joinData.PlaceId
                if jobId == '' then
                     SafeNotify(T('Invalid join code format.'),
                    3)return
                 end SafeNotify(T('Attempting to join server by code...'),
                3)local success,
                err = pcall(function()
                    Utils.UnifiedTeleportHandler({
                        PlaceId = placeId or game.PlaceId,
                        JobId = jobId,
                        Bypass = false
                    })
                end)if not success then
                     SafeNotify('Failed to teleport to root place:' .. tostring(err) .. '. Trying current place...',
                    5)warn('TeleportToPlaceInstance (root) error:',
                    err)local currentPlaceSuccess,
                    currentPlaceErr = pcall(function()
                        TeleportService:TeleportToPlaceInstance(game.PlaceId,
                        jobId,
                        LocalPlayer)
                    end)if not currentPlaceSuccess then
                         SafeNotify('Failed to teleport to current place:' .. tostring(currentPlaceErr),
                        5)warn('TeleportToPlaceInstance (current) error:',
                        currentPlaceErr)
                    end
                 end
             end,
            Tooltip = T([[Joins a server using the provided join code. Tries root place ID first.]])
        })
PlaceTeleportGroup:AddButton({
            Text = T('Server-Hop'),
            Func = function()
                local servers = {
                }
                local req = SecureRequest:HttpGet('https://games.roblox.com/v1/games/' .. game.PlaceId .. [[/servers/Public?sortOrder=Asc&limit=100&excludeFullGames=true]])local body = HttpService:JSONDecode(req)if body and body.data then
                     for i,
                    v in next,
                    body.data do
                         if type(v) == 'table' and tonumber(v.playing) and tonumber(v.maxPlayers) and v.playing < v.maxPlayers and v.id ~= game.JobId then
                             table.insert(servers,
                            1,
                            v.id)
                        end
                     end
                 end
                if#servers > 0 then
                     if LPH_OBFUSCATED then
                         local AppendString = 'getgenv().Key = "NoKey"'
                        if getgenv().Key then
                             AppendString = `getgenv().Key = "{ getgenv().Key}"\n`
                        end queue_on_teleport(AppendString .. [[repeat task_wait() until game:IsLoaded()
loadstring(game:HttpGet("https://example.com/script/Blockspin_Paid_Loader.luau"))()]])
                    end
                    return TeleportService:TeleportToPlaceInstance(game.PlaceId,
                    servers[math.random(1,
                    #servers)],
                    Players.LocalPlayer)
                else
                     return SafeNotify('No servers found to hop to.',
                    3)
                end
             end,
            Tooltip = T([[Teleports you to a normal server and bypasses the forced teleport.]]),
            DisabledTooltip = T('Button is disabled in FREE_BUILD mode'),
            Disabled = false
        })
    end
    local OptimizationsGroup = Tabs.Visuals:AddRightGroupbox(T('Optimizations'))OptimizationsGroup:AddToggle('OptimizedLighting', {
        Text = T('Optimize Lighting'),
        Default = false,
        Tooltip = T('Switches lighting technology to a faster preset.'),
        Callback = function(Value)
            if Value then
                 pcall(sethiddenproperty,
                Lighting,
                'Technology',
                Enum.Technology.Compatibility)pcall(sethiddenproperty,
                Lighting,
                'LightingStyle',
                Enum.LightingStyle.Soft)pcall(sethiddenproperty,
                Lighting,
                'PrioritizeLightingQuality',
                false)Lighting.GlobalShadows = false
             else
                 pcall(sethiddenproperty,
                Lighting,
                'Technology',
                Enum.Technology.Future)pcall(sethiddenproperty,
                Lighting,
                'LightingStyle',
                Enum.LightingStyle.Realistic)pcall(sethiddenproperty,
                Lighting,
                'PrioritizeLightingQuality',
                true)Lighting.GlobalShadows = true
             end
         end
    })
OptimizationsGroup:AddToggle('LowMeshDetail', {
        Text = T('Optimize Mesh Detail'),
        Default = false,
        Tooltip = T('Switches mesh detail to a lower preset.'),
        Callback = function(Value)
            if Value then
                 for _,
                Mesh:MeshPart in next,
                game:GetDescendants() :: any do
                     if Mesh:IsA('MeshPart')then
                         Mesh:SetAttribute('OriginalRenderFidelity',
                        tostring(Mesh.RenderFidelity.Name))Mesh.RenderFidelity = Enum.RenderFidelity.Performance
                        if Mesh.CollisionFidelity == Enum.CollisionFidelity.Default then
                             Mesh:SetAttribute('OriginalCollisionFidelity',
                            tostring(Mesh.CollisionFidelity.Name))Mesh.CollisionFidelity = Enum.CollisionFidelity.Hull
                         end
                     end
                 end
             else
                 for _,
                Mesh:MeshPart in next,
                game:GetDescendants() :: any do
                     if Mesh:IsA('MeshPart')then
                         if Mesh:GetAttribute('OriginalRenderFidelity')then
                             local OriginalRenderFidelity = Mesh:GetAttribute('OriginalRenderFidelity') :: string
                            if OriginalRenderFidelity then
                                 Mesh.RenderFidelity = Enum.RenderFidelity[OriginalRenderFidelity] :: Enum.RenderFidelity
                                Mesh:SetAttribute('OriginalRenderFidelity',
                                nil)
                            end
                            local OriginalCollisionFidelity = Mesh:GetAttribute('OriginalCollisionFidelity')if OriginalCollisionFidelity then
                                 Mesh.CollisionFidelity = Enum.CollisionFidelity[OriginalCollisionFidelity] :: Enum.CollisionFidelity
                                Mesh:SetAttribute('OriginalCollisionFidelity',
                                nil)
                            end
                         end
                     end
                 end
             end
         end
    })
OptimizationsGroup:AddToggle('RemoveDetail', {
        Text = T('Remove Details'),
        Default = false,
        Tooltip = T('Removes unnecessary details from the environment.'),
        Callback = function(Value)
            for _,
            Descendant in next,
            workspace:GetDescendants()do
                 if Descendant:IsA('MeshPart') and Descendant.CanCollide == false then
                     Descendant.LocalTransparencyModifier = Value and 1 or 0
                 end
             end
         end
    })
local MiscVisualsGroup = Tabs.Visuals:AddLeftGroupbox(T('Misc Visuals'))MiscVisualsGroup:AddToggle('ShowServerStamina', {
        Text = T('Show Server-Side Stamina'),
        Default = true,
        Tooltip = T('Displays your server-side stamina in the top left corner.')
    })
MiscVisualsGroup:AddToggle('VisualizeHitReg', {
        Text = T('Visualize Hit Registration [LAGGY]'),
        Default = false,
        Tooltip = T('Displays hit registration information.')
    })
MiscVisualsGroup:AddToggle('Freecam', {
        Text = T('Enable Freecam'),
        Default = false,
        Tooltip = T('Enables the freecam feature.'),
        Callback = function(Value)
            ToggleFreeCamera(Value)
        end
    }):AddKeyPicker('Freecam', {
        Default = 'V',
        SyncToggleState = true,
        Mode = 'Toggle',
        Text = T('Toggle Freecam'),
        NoUI = false
    })
local ESPGroup = Tabs.Visuals:AddLeftGroupbox('ESP')ESPGroup:AddToggle('ESPEnabled', {
        Text = T('Enabled'),
        Default = false,
        Tooltip = T('Enables ESP features'),
        Callback = function(Value)
            ESP_Library.Config.Enabled = Value
            ItemView.Enabled = G_Toggle('ESPItems') and Value
         end
    })
local FontList = {
    }
    for Font, _ in next, Drawing.Fonts do
         table.insert(FontList, Font)
    end ESPGroup:AddDropdown('ESPFont', {
        Text = T('ESP Font'),
        Default = 1,
        Values = FontList,
        Tooltip = T('Select a font'),
        Callback = function(Value)
            ESP_Library.Config.Font = Drawing.Fonts[Value] or Drawing.Fonts.UI
         end
    })
ESPGroup:AddSlider('ESPRange', {
        Text = T('Range'),
        Default = 500,
        Min = 0,
        Max = 1500,
        Rounding = 0,
        Tooltip = T('Sets the maximum distance for ESP'),
        Callback = function(Value)
            ESP_Library.Config.MaxDistance = Value
            ItemView.MaxDistance = Value
         end
    })
ESPGroup:AddSlider('ESPFade', {
        Text = T('Fade'),
        Default = 100,
        Min = 0,
        Max = 500,
        Rounding = 0,
        Tooltip = T('Sets the fade distance for ESP'),
        Callback = function(Value)
            ESP_Library.Config.FadeDistance = Value
         end
    })
ESPGroup:AddToggle('ESPSpotlight', {
        Text = T('Spotlight'),
        Default = false,
        Tooltip = T('Enables spotlight effect for ESP'),
        Callback = function(Value)
            ESP_Library.Config.Spotlight = Value
         end
    })
ESPGroup:AddSlider('ESPSpotlightFadeStart', {
        Text = T('Spotlight Fade Start (%)'),
        Default = math.floor((ESP_Library.Config.SpotlightFadeStart or 0) * 100 + 0.5),
        Min = 0,
        Max = 100,
        Rounding = 0,
        Tooltip = T([[Percent of screen distance from the cursor before spotlight fade begins]]),
        Callback = function(Value)
            ESP_Library.Config.SpotlightFadeStart = math.clamp(Value,
            0,
            100) / 100
         end
    })
ESPGroup:AddSlider('ESPSpotlightFadeLength', {
        Text = T('Spotlight Fade Length (%)'),
        Default = math.floor((ESP_Library.Config.SpotlightFadeLength or 0) * 100 + 0.5),
        Min = 0,
        Max = 100,
        Rounding = 0,
        Tooltip = T('Percent span over which spotlight fade reaches full effect'),
        Callback = function(Value)
            ESP_Library.Config.SpotlightFadeLength = math.clamp(Value,
            0,
            100) / 100
         end
    })
ESPGroup:AddToggle('ESPPlayers', {
        Text = T('Players'),
        Default = false,
        Tooltip = T('Shows ESP for players'),
        Callback = function(Value)
            ESP_Library.Config.Players = Value
         end
    })
ESPGroup:AddToggle('ESPItems', {
        Text = T('Inventory'),
        Default = false,
        Tooltip = T('Shows ESP for inventory'),
        Callback = function(Value)
            ItemView.Enabled = Value and ESP_Library.Config.Enabled
         end,
        Disabled = false
    }):AddColorPicker('ItemESPColor', {
        Default = Color3.new(1,
        1,
        1),
        Title = T('Item ESP Color'),
        Transparency = nil,
        Callback = function(Value)
            ItemView.Color = Value
         end
    })
ESPGroup:AddToggle('ESPDroppedItems', {
        Text = T('Dropped Items'),
        Default = true,
        Tooltip = T('Shows ESP for dropped items')
    })
ESPGroup:AddDropdown('ESPFont', {
        Text = T('ESP Font'),
        Default = 1,
        Values = FontList,
        Tooltip = T('Select a font'),
        Callback = function(Value)
            ESP_Library.Config.Font = Drawing.Fonts[Value] or Drawing.Fonts.UI
         end
    })
ESPGroup:AddToggle('ESPBoxes', {
        Text = T('Boxes'),
        Default = false,
        Tooltip = T('Shows boxes around players'),
        Callback = function(Value)
            ESP_Library.Config.Boxes = Value
         end
    })
ESPGroup:AddDropdown('BoxType', {
        Text = T('Box Type'),
        Default = '2D',
        Values = {
            '3DFull',
            '3D',
            '2D',
            '2DCorners'
        },
        Tooltip = T('Sets the box type for ESP'),
        Callback = function(Value)
            ESP_Library.Config.BoxType = Value
         end
    })
ESPGroup:AddToggle('ESPTracers', {
        Text = T('Tracers'),
        Default = false,
        Tooltip = T('Shows tracers to players'),
        Callback = function(Value)
            ESP_Library.Config.Tracers = Value
         end
    }):AddColorPicker('TracerColor', {
        Default = Color3.new(1,
        1,
        1),
        Title = T('Tracer Color'),
        Transparency = nil,
        Callback = function(Value)
            ESP_Library.Config.TracerColor = Value
         end
    })
ESPGroup:AddToggle('ESPHighlight', {
        Text = T('Highlight'),
        Default = true,
        Tooltip = T('Highlights players'),
        Callback = function(Value)
            ESP_Library.Config.Highlights = Value
         end
    }):AddColorPicker('HighlightColor', {
        Default = Color3.new(1,
        0.568627,
        0),
        Title = T('Highlight Fill Color'),
        Transparency = nil,
        Callback = function(Value)
            ESP_Library.Config.HighlightFillColor = Value
         end
    }):AddColorPicker('HighlightOutlineColor', {
        Default = Color3.new(1,
        0.427451,
        0.282353),
        Title = T('Highlight Outline Color'),
        Transparency = nil,
        Callback = function(Value)
            ESP_Library.Config.HighlightOutlineColor = Value
         end
    })
ESPGroup:AddSlider('HighlightFillTransparency', {
        Text = T('Highlight Fill Transparency'),
        Default = 0.8,
        Min = 0,
        Max = 1,
        Rounding = 2,
        Tooltip = T('Sets the fill transparency for highlights'),
        Callback = function(Value)
            ESP_Library.Config.HighlightFillTransparency = Value
         end
    })
ESPGroup:AddSlider('HighlightOutlineTransparency', {
        Text = T('Highlight Outline Transparency'),
        Default = 0.5,
        Min = 0,
        Max = 1,
        Rounding = 2,
        Tooltip = T('Sets the outline transparency for highlights'),
        Callback = function(Value)
            ESP_Library.Config.HighlightOutlineTransparency = Value
         end
    })
ESPGroup:AddToggle('ESPText', {
        Text = T('Text'),
        Default = false,
        Tooltip = T('Shows text labels for ESP'),
        Callback = function(Value)
            ESP_Library.Config.Text = Value
         end
    }):AddColorPicker('TextColor', {
        Default = Color3.new(1,
        1,
        1),
        Title = T('Text Color'),
        Transparency = nil,
        Callback = function(Value)
            ESP_Library.Config.TextColor = Value
         end
    })
local InventoryGroup = Tabs.InventoryViewer:AddLeftGroupbox(T('Player Select'))InventoryGroup:AddDropdown('InventoryViewerTarget', {
        SpecialType = 'Player',
        ExcludeLocalPlayer = false,
        Text = T('Target Player'),
        Tooltip = T('Player who is being viewed')
    })
InventoryGroup:AddButton(T('Select Highest Value'), function()
        local HighestValue = 0
        local HighestPlayer = nil
        for _, Player in next, Players:GetPlayers()do
             if Player ~= LocalPlayer and Player.Character then
                 local Value = 0
                for _, Tool in next, Player.Backpack:GetChildren()do
                     if Tool:IsA('Tool')then
                         local ItemData = Inventory.ResolveDataFromHashedTool(Tool)if ItemData and ItemData.Price then
                             Value = Value + ItemData.Price
                         end
                     end
                 end
                if Value > HighestValue then
                     HighestValue = Value
                    HighestPlayer = Player
                 end
             end
         end
        if HighestPlayer then
             Library.Options.InventoryViewerTarget:SetValue(HighestPlayer)
        end
     end)local InventoryViewerGroup = Tabs.InventoryViewer:AddRightGroupbox(T('Inventory'))local TargetPlayerText = InventoryViewerGroup:AddLabel(T('Inventory of' .. LocalPlayer.Name))local InventoryUpdateRoutine = Cleaner(coroutine_create(LPH_JIT_MAX(function()
        while task_wait(1)do
             local TargetPlayer = Library.Options.InventoryViewerTarget.Value
            if TargetPlayer then
                 local Items = {
                }
                for _, Tool in next, TargetPlayer.Backpack:GetChildren()do
                     if Tool:IsA('Tool')then
                         table.insert(Items, Inventory.ResolveDataFromHashedTool(Tool))
                    end
                 end
                if TargetPlayer.Character then
                     for _, Tool in next, TargetPlayer.Character:GetChildren()do
                         if Tool:IsA('Tool')then
                             table.insert(Items, Inventory.ResolveDataFromHashedTool(Tool))
                        end
                     end
                 end
                local Container = TargetPlayerText.Container
                local InventoryImageContainer = Container:FindFirstChild('InventoryImageContainer')if not InventoryImageContainer then
                     InventoryImageContainer = Instance.new('Frame')InventoryImageContainer.Name = 'InventoryImageContainer'
                    InventoryImageContainer.Size = UDim2.new(1, 0, 0, 200)InventoryImageContainer.BackgroundTransparency = 1
                    InventoryImageContainer.Parent = Container
                 end InventoryImageContainer:ClearAllChildren()local Grid_Columns = 4
                local ItemSize = InventoryImageContainer.AbsoluteSize.X / Grid_Columns
                for i, Item in next, Items do
                     local Image = Instance.new('ImageLabel')Image.Name = 'Item' .. i
                    Image.Size = UDim2.new(0, ItemSize, 0, ItemSize)Image.Position = UDim2.new((i - 1) % Grid_Columns / Grid_Columns, 0, math_floor((i - 1) / Grid_Columns) / Grid_Columns, 0)Image.BackgroundTransparency = 1
                    Image.Image = Item.ImageId
                    Image.Parent = InventoryImageContainer
                 end
                local Rows = math.ceil(#Items / Grid_Columns)InventoryImageContainer.Size = UDim2.new(1, 0, 0, math_max(20, Rows * ItemSize))if#Items == 0 then
                     local NoItemsLabel = Instance.new('TextLabel')NoItemsLabel.Name = 'NoItemsLabel'
                    NoItemsLabel.Size = UDim2.new(1, 0, 0, 20)NoItemsLabel.BackgroundTransparency = 1
                    NoItemsLabel.Text = 'No items found.'
                    NoItemsLabel.TextColor3 = Color3.new(1, 1, 1)NoItemsLabel.TextScaled = true NoItemsLabel.Parent = InventoryImageContainer
                 end TargetPlayerText:SetText(T('Inventory of' .. TargetPlayer.Name))
            else
                 TargetPlayerText:SetText(T('Inventory'))
            end
         end
     end)))coroutine_resume(InventoryUpdateRoutine)local MenuGroup = Tabs.Settings:AddLeftGroupbox(T('Menu'))MenuGroup:AddToggle('Identifier', {
        Text = T('Sasware Identification'),
        Default = true,
        Tooltip = T([[Enables sending and receiving identifier data to see other Sasware users.]]),
        Callback = function(Value)
            Identifier:ToggleIdentify(Value)
        end
    })
MenuGroup:AddButton('Unload', function()
        print('Cleaning up.')HookMgr.ClearHooks()Cleaner.Clean()ConnectionProxyMgr:Clear()ESP_Library.Unload()Aiming_Library.Unload()rconsoledestroy()
    end)task_spawn(function()
        while task_wait(2)do
             Storage.UpdateGunStatsCallback:Fire()Storage.UpdateMeleeStatsCallback:Fire()
        end
     end)local ChildAddedConnection, ChildRemovedConnection = nil, nil Storage.Connections[_nextKey(Storage.Connections, 'UI_LocalPlayer_CharacterAdded')] = Cleaner(LocalPlayer.CharacterAdded:Connect(function(Character)
        if ChildAddedConnection then
             Cleaner.CleanOne(ChildAddedConnection)ChildAddedConnection = nil
         end
        if ChildRemovedConnection then
             Cleaner.CleanOne(ChildRemovedConnection)ChildRemovedConnection = nil
         end ChildAddedConnection = Cleaner(Character.ChildAdded:Connect(function(Child)
            if CollectionService:HasTag(Child, 'Gun')then
                 CurrentGun:SetText('Current:' .. Child.Name)
            end
         end))Storage.Connections[_nextKey(Storage.Connections, 'UI_Character_ChildAdded')] = ChildAddedConnection
        ChildRemovedConnection = Cleaner(Character.ChildRemoved:Connect(function(Child)
            if CollectionService:HasTag(Child, 'Gun')then
                 CurrentGun:SetText('Current: None')
            end
         end))Storage.Connections[_nextKey(Storage.Connections, 'UI_Character_ChildRemoved')] = ChildRemovedConnection
        if G_Toggle('RevengeKill')then
             if Storage.LastKilledBy then
                 local KilledByPlayer = Players:FindFirstChild(Storage.LastKilledBy) :: Player?if not KilledByPlayer then
                     return
                 end
                local RevengeKillPrompt, Elements = __DARKLUA_BUNDLE_MODULES.load('T')()Elements['8'].Text = 'Revenge-Kill' .. KilledByPlayer.DisplayName .. '?'
                local Countdown = 10
                local TimerLabel = Elements['c']TimerLabel.Text = tostring(Countdown)Storage.Routines[_nextKey(Storage.Routines, 'RevengeKill_Countdown')] = task_spawn(function()
                    while Countdown > 0 do
                         task_wait(1)Countdown-=1
                        TimerLabel.Text = tostring(Countdown)
                    end RevengeKillPrompt:Destroy()
                end)
            end
         end
     end))if LocalPlayer.Character then
         if ChildAddedConnection then
             Cleaner.CleanOne(ChildAddedConnection)ChildAddedConnection = nil
         end
        if ChildRemovedConnection then
             Cleaner.CleanOne(ChildRemovedConnection)ChildRemovedConnection = nil
         end ChildAddedConnection = Cleaner(LocalPlayer.Character.ChildAdded:Connect(function(Child)
            if CollectionService:HasTag(Child, 'Gun')then
                 CurrentGun:SetText('Current:' .. Child.Name)
            end
         end))Storage.Connections[_nextKey(Storage.Connections, 'UI_LocalCharacter_ChildAdded')] = ChildAddedConnection
        ChildRemovedConnection = Cleaner(LocalPlayer.Character.ChildRemoved:Connect(function(Child)
            if CollectionService:HasTag(Child, 'Gun')then
                 CurrentGun:SetText('Current: None')
            end
         end))Storage.Connections[_nextKey(Storage.Connections, 'UI_LocalCharacter_ChildRemoved')] = ChildRemovedConnection
     end
    if not LPH_OBFUSCATED then
         local DebugGroup = Tabs.Debug:AddLeftGroupbox('Debug')DebugGroup:AddButton('Print ESP Objects', function()
            for _, Object in next, ESP_Library.Objects do
                 print(Object.Name, Object.ClassName, Object.Instance)
            end
         end)DebugGroup:AddButton('Print InventoryData', function()
            print(Repr(Inventory.ListInventory()))
        end)DebugGroup:AddButton('Print InventoryDataHand', function()
            for i, Item in next, Inventory.FilterByLocation(Inventory.ListInventory(), 'hand')do
                 print(i, Repr(Item))
            end
         end)DebugGroup:AddLabel('CleanerInfo', {
            Text = 'Cleaner Registry Size:' .. flen(Cleaner.Registry)
        })
DebugGroup:AddButton('Export Arguments', function()
            local Arguments = ArgumentChecks
            for ArgumentName, ArgumentData in next, Arguments do
                 print(`{ ArgumentName }:\n\tFound:{ ArgumentData.Found }\n\tValue:{ ArgumentData.Value }`)
            end
         end)DebugGroup:AddButton('Test Orchestrator', function()
            local Orchestrator = __DARKLUA_BUNDLE_MODULES.load('V')Orchestrator:RunFullTest('KG-f128ffc3-1f06-42e2-a3e0-e1b20de16423', 825230256)
        end)DebugGroup:AddButton('Print all gun states', function()
            local GunClass = Class_Interface.GetClass('Gun')if not GunClass then
                 warn('Gun class not found by Class_Interface!')return
             end
            local GunObjects = GunClass.objects or {
            }
            if next(GunObjects) == nil then
             end
            for _, Gun in next, GunObjects do
                 if not(Gun and Gun.instance and Gun.states)then
                     dbgprint('Skipping invalid or nil gun object in GunObjects table.')if Gun and Gun.instance then
                         dbgwarn('Gun object for', Gun.instance.Name, 'is missing .states property!')
                    elseif  Gun then
                         dbgwarn('Gun object is missing .instance property!')
                    end continue
                 end
                local States = Gun.states
                if not States then
                     dbgwarn('Gun object for', Gun.instance.Name, 'is missing .states property!')continue
                 end print('Gun:', Gun.instance.Name)print('States:')for StateName, State in next, States do
                     if type(State) == 'table' and State.get then
                         print('', StateName, ':', State:get())
                    else
                         print('', StateName, ':', State)
                    end
                 end
             end
         end)DebugGroup:AddInput('ClassInput', {
            Text = 'Target Class',
            Default = '',
            Placeholder = 'Enter target class here',
            Tooltip = 'Enter the target class to dump'
        })
DebugGroup:AddButton('Dump Class Objects', function()
            local TargetClass = G_Option('ClassInput')if TargetClass == '' then
                 SafeNotify('Please enter a class name.', 3)return
             end
            local Class = Class_Interface.GetClass(TargetClass)if not Class then
                 SafeNotify(`Class "{TargetClass}" not found.`, 3)return
             end
            local Objects = Class.objects or {
            }
            if next(Objects) == nil then
                 SafeNotify(`No objects found for class "{TargetClass}".`, 3)return
             end
            for _, Object in next, Objects do
                 print(Repr(Object, {
                    pretty = true
                }))
            end SafeNotify(`Dumped{ #Objects } objects from class "{TargetClass}".`, 3)
        end)DebugGroup:AddInput('SkillInput', {
            Text = 'Target Skill',
            Default = '',
            Placeholder = 'Enter target skill here',
            Tooltip = 'Enter the target skill to dump'
        })
DebugGroup:AddButton('Dump Skill Objects', function()
            local TargetSkill = G_Option('SkillInput')if TargetSkill == '' then
                 SafeNotify('Please enter a class name.', 3)return
             end
            local Skills = SafeRequire(GameModules.Skills.SkillsList :: ModuleScript)local Skill = Skills.list[TargetSkill]if not Skill then
                 SafeNotify(`Skill "{TargetSkill}" not found.`, 3)return
             end print(Repr(Skill, {
                pretty = true
            }))SafeNotify(`Dumped skill "{ TargetSkill}".`, 3)
        end)task_spawn(function()
            while task_wait(1)do
                 Library.Labels.CleanerInfo:SetText(`Cleaner Registry Size:{ flen(Cleaner.Registry) }`)
            end
         end)
    end
    local TestGroup = Tabs.Debug:AddRightGroupbox('Testing')TestGroup:AddButton('Test Drawing Library', function()
        local Drawings = {
        }
        for i = 1, 5 do
             local Box = Drawing.new('Square')Box.Size = Vector2.new(100, 100)Box.Position = Vector2.new(i * 110, 100)Box.Color = BrickColor.Random().Color
            Box.Visible = true Box.Filled = math.random() > 0.5
            table.insert(Drawings, Box)
        end
        for i = 1, 5 do
             local Quad = Drawing.new('Quad')Quad.PointA = Vector2.new(i * 110, 200)Quad.PointB = Vector2.new(i * 110 + 100, 200)Quad.PointC = Vector2.new(i * 110 + 50, 300)Quad.PointD = Vector2.new(i * 110 - 50, 300)Quad.Color = BrickColor.Random().Color
            Quad.Filled = math.random() > 0.5
            Quad.Visible = true table.insert(Drawings, Quad)
        end
        for i = 1, 5 do
             local Triangle = Drawing.new('Triangle')Triangle.Size = Vector2.new(100, 100)Triangle.PointA = Vector2.new(i * 110, 300)Triangle.PointB = Vector2.new(i * 110 + 100, 300)Triangle.PointC = Vector2.new(i * 110 + 50, 400)Triangle.Color = BrickColor.Random().Color
            Triangle.Filled = math.random() > 0.5
            Triangle.Visible = true table.insert(Drawings, Triangle)
        end
        for i = 1, 5 do
             local Text = Drawing.new('Text')Text.Size = 20
            Text.Position = Vector2.new(i * 110, 400)Text.Color = BrickColor.Random().Color
            Text.Visible = true Text.Text = 'Hello World'
            table.insert(Drawings, Text)
        end
        for i = 1, 5 do
             local Circle = Drawing.new('Circle')Circle.Radius = 50
            Circle.Position = Vector2.new(i * 110, 500)Circle.Color = BrickColor.Random().Color
            Circle.Visible = true Circle.Filled = math.random() > 0.5
            table.insert(Drawings, Circle)
        end task_wait(5)for _, Drawing in next, Drawings do
             Drawing:Remove()
        end
     end)if not false and ORCHESTRATOR_MENU_ENABLED and Tabs.Orchestrator then
         local Orchestrator = __DARKLUA_BUNDLE_MODULES.load('V')local OrchestratorStorage = {
            PrivateKey = nil,
            WorkerKeys = {
            },
            PendingWarningAccepted = false
        }
        local function GetOrGeneratePrivateKey()
            :string?if OrchestratorStorage.PrivateKey then
                 return OrchestratorStorage.PrivateKey
             end
            local LicenseKey = getgenv().Key
            if not LicenseKey or LicenseKey == 'BLACKLISTED' then
                 SafeNotify(T('Unable to generate private key: No valid license key found.'), 5)return nil
             end OrchestratorStorage.PrivateKey = Orchestrator:GeneratePrivateKey(LicenseKey, LocalUserId)return OrchestratorStorage.PrivateKey
         end
        local IdentityGroup = Tabs.Orchestrator:AddLeftGroupbox(T('Your Identity'))IdentityGroup:AddLabel(T('Your private key is derived from your'))IdentityGroup:AddLabel(T('license key and user ID. Keep it secret!'))local PrivateKeyPreview = IdentityGroup:AddLabel(T('Key: Not generated yet'))IdentityGroup:AddButton({
            Text = T('Generate/View Private Key'),
            Func = function()
                local key = GetOrGeneratePrivateKey()if key then
                     PrivateKeyPreview:SetText(T('Key:') .. string.sub(key,
                    1,
                    16) .. '...')SafeNotify(T("Private key generated. Use 'Copy' button to copy."),
                    3)
                end
             end,
            Tooltip = T('Generate or view your orchestration private key')
        })
IdentityGroup:AddButton({
            Text = T('Copy Worker Token'),
            Func = function()
                local key = GetOrGeneratePrivateKey()if not key then
                     return
                 end
                local workerToken = tostring(LocalUserId) .. ':' .. key
                if not OrchestratorStorage.PendingWarningAccepted then
                     local Root,
                    AcceptBtn,
                    CancelBtn = ErrorHandler.InteractiveToast(T('Security Warning'),
                    T([[Your worker token grants FULL control over this client to anyone who has it.

]]) .. T("NEVER share this token with anyone you don't fully trust.\n") .. T('Anyone with this token can:\n') .. T('\u{2022} Control your farming settings\n') .. T('\u{2022} Transfer your in-game money\n') .. T('\u{2022} Execute commands on your client\n\n') .. T('Are you sure you want to copy this token?'),
                    T('Yes, Copy Token'),
                    T('Cancel'))AcceptBtn.BackgroundColor3 = Color3.fromRGB(200,
                    100,
                    0)AcceptBtn.BackgroundTransparency = 0
                    CancelBtn.BackgroundColor3 = Color3.fromRGB(80,
                    80,
                    80)AcceptBtn.Activated:Once(function()
                        OrchestratorStorage.PendingWarningAccepted = true Root:Destroy()if setclipboard then
                             pcall(setclipboard,
                            workerToken)SafeNotify(T('Worker token copied to clipboard!'),
                            3)
                        else
                             SafeNotify(T('Clipboard not available on this executor.'),
                            3)
                        end
                     end)CancelBtn.Activated:Once(function()
                        Root:Destroy()SafeNotify(T('Copy cancelled.'),
                        2)
                    end)local uiParent = (gethui and gethui()) or CoreGui
                    Root.DisplayOrder = 2147483647
                    Root.Parent = uiParent
                    Root.Enabled = true
                    return
                 else
                     if setclipboard then
                         pcall(setclipboard,
                        workerToken)SafeNotify(T('Worker token copied to clipboard!'),
                        3)
                    else
                         SafeNotify(T('Clipboard not available on this executor.'),
                        3)
                    end
                 end
             end,
            Tooltip = T('Copy your worker token to clipboard (shows warning first)')
        })
local WorkerGroup = Tabs.Orchestrator:AddRightGroupbox(T('Worker Management'))WorkerGroup:AddLabel(T('Paste worker tokens from other clients.'))WorkerGroup:AddLabel(T('Format: userId:privateKey'))WorkerGroup:AddInput('OrchestratorWorkerTokenInput', {
            Text = T('Worker Token'),
            Default = '',
            Placeholder = T('Paste worker token here'),
            Tooltip = T([[Paste the worker token (userId:privateKey) from the worker client]])
        })
local WorkerListLabel = WorkerGroup:AddLabel(T('Workers: 0 registered'))WorkerGroup:AddButton({
            Text = T('Add Worker'),
            Func = function()
                local workerToken = G_Option('OrchestratorWorkerTokenInput')if workerToken == '' then
                     SafeNotify(T('Please paste a worker token.'),
                    3)return
                 end
                local colonPos = string.find(workerToken,
                ':')if not colonPos then
                     SafeNotify(T('Invalid token format. Expected userId:privateKey'),
                    3)return
                 end
                local userIdStr = string.sub(workerToken,
                1,
                colonPos - 1)local workerKey = string.sub(workerToken,
                colonPos + 1)local workerUserId = tonumber(userIdStr)if not workerUserId then
                     SafeNotify(T('Invalid user ID in token.'),
                    3)return
                 end
                if workerKey == '' or #workerKey < 32 then
                     SafeNotify(T('Invalid private key in token.'),
                    3)return
                 end
                for _,
                worker in next,
                OrchestratorStorage.WorkerKeys do
                     if worker.UserId == workerUserId then
                         SafeNotify(T('This worker is already registered.'),
                        3)return
                     end
                 end table.insert(OrchestratorStorage.WorkerKeys,
                {
                    Key = workerKey,
                    UserId = workerUserId
                })
WorkerListLabel:SetText(T('Workers:') .. #OrchestratorStorage.WorkerKeys .. T('registered'))SafeNotify(T('Worker added successfully!'),
                3)Library.Options.OrchestratorWorkerTokenInput:SetValue('')
            end,
            Tooltip = T('Add this worker to your control list')
        })
WorkerGroup:AddButton({
            Text = T('Clear All Workers'),
            Func = function()
                OrchestratorStorage.WorkerKeys = {
                }
                WorkerListLabel:SetText(T('Workers: 0 registered'))SafeNotify(T('All workers cleared.'),
                3)
            end,
            Tooltip = T('Remove all registered workers')
        })
local ConfigGroup = Tabs.Orchestrator:AddLeftGroupbox(T('Worker Configuration'))ConfigGroup:AddLabel(T('Settings to push to workers:'))ConfigGroup:AddSlider('OrchestratorMergeThreshold', {
            Text = T('Merge to Master Threshold'),
            Default = 1000000,
            Min = 100000,
            Max = 10000000,
            Rounding = 0,
            Suffix = T('cash'),
            Tooltip = T([[Amount of cash workers should accumulate before transferring to master]])
        })
ConfigGroup:AddInput('OrchestratorJsonConfig', {
            Text = T('JSON Configuration'),
            Default = '{}',
            Placeholder = T('{"enabled": true, "target_money": 5000000}'),
            Tooltip = T('Custom JSON configuration data to send to workers')
        })
local ActionsGroup = Tabs.Orchestrator:AddRightGroupbox(T('Actions'))ActionsGroup:AddButton({
            Text = T('Push Config to All Workers'),
            Func = function()
                if#OrchestratorStorage.WorkerKeys == 0 then
                     SafeNotify(T('No workers registered.'),
                    3)return
                 end
                local LicenseKey = getgenv().Key
                if not LicenseKey or LicenseKey == 'BLACKLISTED' then
                     SafeNotify(T('No valid license key found.'),
                    3)return
                 end
                local mergeThreshold = G_Option('OrchestratorMergeThreshold')local jsonConfigStr = G_Option('OrchestratorJsonConfig')local customConfig = {
                }
                pcall(function()
                    customConfig = HttpService:JSONDecode(jsonConfigStr)
                end)local successCount = 0
                local failCount = 0
                for _,
                worker in next,
                OrchestratorStorage.WorkerKeys do
                     local _workerData = {
                        master_user_id = LocalUserId,
                        master_server_id = game.JobId,
                        transfer_threshold = mergeThreshold,
                        autofarm_settings = customConfig,
                        priority = 1,
                        registered_at = os.time()
                    }
                    _ = _workerData
                    local success = Orchestrator:TestRegisterWorkerData(LicenseKey,
                    worker.UserId)if success then
                         successCount+=1
                     else
                         failCount+=1
                     end task_wait(0.5)
                end SafeNotify(T('Config pushed:') .. successCount .. T('success,') .. failCount .. T('failed'),
                5)
            end,
            Tooltip = T('Send the current configuration to all registered workers')
        })
ActionsGroup:AddButton({
            Text = T('Test Connection'),
            Func = function()
                local LicenseKey = getgenv().Key
                if not LicenseKey or LicenseKey == 'BLACKLISTED' then
                     SafeNotify(T('No valid license key found.'),
                    3)return
                 end SafeNotify(T('Testing orchestration service connection...'),
                3)local success = pcall(function()
                    Orchestrator:RunFullTest(LicenseKey,
                    LocalUserId)
                end)if success then
                     SafeNotify(T('Connection test completed! Check console for details.'),
                    5)
                else
                     SafeNotify(T('Connection test failed. Check console for errors.'),
                    5)
                end
             end,
            Tooltip = T('Test the connection to the orchestration service')
        })
ActionsGroup:AddLabel(T('Status: Idle'))
    end Aiming_Library.FilterFriends = G_Toggle('SilentAimFilterFriends')Aiming_Library.CenterLockFOV = G_Toggle('SilentAimCenterFOV')ESP_Library.Config.HighlightFillColor = G_Option('HighlightColor')ESP_Library.Config.HighlightOutlineColor = G_Option('HighlightOutlineColor')ESP_Library.Config.HighlightFillTransparency = G_Option('HighlightFillTransparency')ESP_Library.Config.HighlightOutlineTransparency = G_Option('HighlightOutlineTransparency')ESP_Library.Config.Font = Drawing.Fonts[G_Option('ESPFont')] or Drawing.Fonts.UI
    MenuGroup:AddLabel('Menu bind'):AddKeyPicker('MenuKeybind', {
        Default = 'RightControl',
        NoUI = true,
        Text = 'Menu keybind'
    })
Library.ToggleKeybind = Library.Options.MenuKeybind
    ThemeManager:SetLibrary(Library)SaveManager:SetLibrary(Library)ThemeManager:SetDefaultTheme({
        BackgroundColor = Color3.fromRGB(29,
        29,
        46),
        MainColor = Color3.fromRGB(48,
        45,
        65),
        AccentColor = Color3.fromRGB(159,
        120,
        149),
        OutlineColor = Color3.fromRGB(67,
        61,
        87),
        FontColor = Color3.fromRGB(217,
        224,
        238),
        FontFace = Enum.Font.BuilderSans
    })
SaveManager:IgnoreThemeSettings()SaveManager:SetIgnoreIndexes({
        'MenuKeybind'
    })
ThemeManager:SetFolder('sasware_blockspin')SaveManager:SetFolder('sasware_blockspin/main')SaveManager:BuildConfigSection(Tabs.Settings)ThemeManager:ApplyToTab(Tabs.Settings)SaveManager:LoadAutoloadConfig()ItemView:Init()Storage.UpdateGunStatsCallback:Fire()local Data = TeleportData:ReadWipe('TeleportState')if Data then
         SafeNotify('Loaded teleport data from previous session.', 10)task_wait(5)if tick() - Data.Created > 60 then
             SafeNotify('Teleport data is stale and will be ignored.', 10)return
         end
        local AllowedToggles = {
            CookFarm = true,
            ShelfStocking = true,
            ATMFarm = true,
            AutoShiesty = true,
            ATMFarmUsePath = true,
            AvoidWaitingAtATMs = true,
            ATMFarmDefensive = true,
            ATMFarmOffensive = true,
            ATMFarmAutoHop = true
        }
        local AllowedOptions = {
            HackTool = true,
            ATMFarmSpeedMultiplier = true
        }
        if Data.Toggles then
             for Key, Value in next, Data.Toggles do
                 if AllowedToggles[Key] and Library.Toggles[Key]then
                     pcall(function()
                        Library.Toggles[Key]:SetValue(Value)
                    end)
                else
                     dbgprint('Skipping toggle from teleport data (not allowed):', Key)
                end
             end
         end
        if Data.Options then
             for Key, Value in next, Data.Options do
                 if AllowedOptions[Key] and Library.Options[Key]then
                     pcall(function()
                        Library.Options[Key]:SetValue(Value)
                    end)
                else
                     dbgprint('Skipping option from teleport data (not allowed):', Key)
                end
             end
         end
     end InitializedSignal:Fire()Identifier:ToggleIdentify(G_Toggle('Identifier'))
end
local _ = xpcall(RunMain, function(Error)
    warn('An error occurred during execution:', Error)warn(debug.traceback())local throwResult = {
        ErrorHandler.Throw('0x01',
        `An error occured during exection:{ Error }\n{ debug.traceback() }`,
        false)
    }
    local AbortSignal = throwResult[2]local UI = throwResult[3]HookMgr.ClearHooks()Cleaner.Clean()ConnectionProxyMgr:Clear()ESP_Library.Unload()Aiming_Library.Unload()if AbortSignal then
         AbortSignal:Once(function()
            rconsoledestroy()if UI and UI.Destroy then
                 UI:Destroy()
            end
         end)
    end
    return Error
 end)
