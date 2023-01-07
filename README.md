# walasim

a small library to simulate a physical [walabot](https://walabot.com/collections/all) radar device.

## Notes

get all walabot api methods and properties, then extract the functions only

```python
import WalabotAPI
print(dir(WalabotAPI))
```

<details>
<summary>output</summary>
'ARRAY', 'AntennaPair', 'AppProfile', 'AppStatus', 'ArgumentError', 'Array', 'BigEndianStructure', 'CDLL', 'CFUNCTYPE', 'CancelCalibration', 'Clean', 'Connect', 'ConnectAny', 'DEFAULT_MODE', 'Disconnect', 'DllCanUnloadNow', 'DllGetClassObject', 'FILTER_TYPE_DERIVATIVE', 'FILTER_TYPE_MTI', 'FILTER_TYPE_NONE', 'FilterType', 'FormatError', 'GetAdvancedParameter', 'GetAntennaPairs', 'GetArenaPhi', 'GetArenaR', 'GetArenaTheta', 'GetArenaX', 'GetArenaY', 'GetArenaZ', 'GetDynamicImageFilter', 'GetErrorString', 'GetExtendedError', 'GetImageEnergy', 'GetImagingTargets', 'GetInstrumentsList', 'GetLastError', 'GetRawImage', 'GetRawImageSlice', 'GetSensorTargets', 'GetSignal', 'GetStatus', 'GetThreshold', 'GetTrackerTargets', 'GetVersion', 'HRESULT', 'ImagingTarget', 'Init', 'Initialize', 'IsInitialized', 'LibraryLoader', 'LittleEndianStructure', 'OleDLL', 'PARAM_CONFIDENCE_FACTOR', 'PARAM_DIELECTRIC_CONSTANT', 'POINTER', 'PROF_SENSOR', 'PROF_SENSOR_NARROW', 'PROF_SHORT_RANGE_IMAGING', 'PROF_TRACKER', 'PROF_WIDE', 'PYFUNCTYPE', 'PyDLL', 'RTLD_GLOBAL', 'RTLD_LOCAL', 'STATUS_CALIBRATING', 'STATUS_CALIBRATING_NO_MOVEMENT', 'STATUS_CLEAN', 'STATUS_CONFIGURED', 'STATUS_CONNECTED', 'STATUS_INITIALIZED', 'STATUS_SCANNING', 'SensorTarget', 'SetAdvancedParameter', 'SetArenaPhi', 'SetArenaR', 'SetArenaTheta', 'SetArenaX', 'SetArenaY', 'SetArenaZ', 'SetDynamicImageFilter', 'SetPointerType', 'SetProfile', 'SetSettingsFolder', 'SetThreshold', 'SetTrackerAquisitionThreshold', 'Start', 'StartCalibration', 'Stop', 'Structure', 'TARGET_TYPE_OTHER', 'TARGET_TYPE_PIPE', 'TARGET_TYPE_STUD', 'TARGET_TYPE_STUD90', 'TARGET_TYPE_STUD_METAL', 'TARGET_TYPE_UNKNOWN', 'TrackerTarget', 'Trigger', 'Union', 'WALABOT_ERROR', 'WALABOT_SUCCESS', 'WINFUNCTYPE', 'WalabotError', 'WalabotResult', 'WalabotVersion', 'WinDLL', 'WinError', '_Ctypes_AntennaPairs', '_Ctypes_ImagingTarget', '_Ctypes_SensorTarget', '_Ctypes_TrackerTarget', '_Ctypes_WalabotVersion', '_GetArenaHelper', '_GetDefaultPaths', '_RaiseIfErr', '_SetArenaHelper', '_WalabotResultDict', '__builtins__', '__cacet', 'SetAdvancedParameter', 'SetArenaPhi', 'SetArenaR', 'SetArenaTheta', 'SetArenaX', 'SetArenaY', 'SetArenaZ', 'SetDynamicImageFilter', 'SetPointerType', 'SetProfile', 'SetSettingsFolder', 'SetThreshold', 'SetTrackerAquisitionThreshold', 'Start', 'StartCalibration', 'Stop', 'Structure', 'TARGET_TYPE_OTHER', 'TARGET_TYPE_PIPE', 'TARGET_TYPE_STUD', 'TARGET_TYPE_STUD90', 'TARGET_TYPE_STUD_METAL', 'TARGET_TYPE_UNKNOWN', 'TrackerTarget', 'Trigger', 'Union', 'WALABOT_ERROR', 'WALABOT_SUCCESS', 'WINFUNCTYPE', 'WalabotError', 'WalabotResult', 'WalabotVersion', 'WinDLL', 'et', 'SetAdvancedParameter', 'SetArenaPhi', 'SetArenaR', 'SetArenaTheta', 'SetArenaX', 'SetArenaY', 'SetArenaZ', 'SetDynamicImageFilter', 'SetPointerType', 'SetProfile', 'SetSettingsFolder', 'SetThreshold', 'SetTrackerAquisitionThFolder', 'SetThreshold', 'SetTrackerAquisitionThreshold', 'Start', 'StartCalibration', 'Stop', 'Structure', 'TARGET_TYPE_OTHER', 'TARGET_TYPE_PIPE', 'TARGET_TYPE_STUD', 'TARGET_TYPE_STUD90', 'TARGET_TYPE_STUD_METAL', 'TARGET_TYPE_UNKNOWN', 'TrackerTarget', 'Trigger', 'Union', 'WALABOT_ERROR', 'WALABOT_SUCCESS', 'WINFUNCTYPE', 'WalabotError', 'WalabotResult', 'WalabotVersion', 'WinDLL', 'WinError', '_Ctypes_AntennaPairs', '_Ctypes_ImagingTarget', '_Ctypes_SensorTarget', '_Ctypes_TrackerTarget', '_Ctypes_WalabotVersion', '_GetArenaHelper', '_GetDefaultPaths', '_RaiseIfErr', '_SetArenaHelper', '_WalabotResultDict', '__builtins__', '__cached__', '__doc__', '__file__', '__loader__', '__name__', '__package__', '__spec__', '_defaultConfigFilePath', '_defaultLibPath', '_defaultSettingsFolderPath', '_depLibPaths', 'addressof', 'alignment', 'byref', 'c_bool', 'c_buffer', 'c_byte', 'c_char', 'c_char_p', 'c_double', 'c_float', 'c_int', 'c_int16', 'c_int32', 'c_int64', 'c_int8', 'c_long', 'c_longdouble', 'c_longlong', 'c_short', 'c_size_t', 'c_ssize_t', 'c_ubyte', 'c_uint', 'c_uint16', 'c_uint32', 'c_uint64', 'c_uint8', 'c_ulong', 'c_ulonglong', 'c_ushort', 'c_void_p', 'c_voidp', 'c_wchar', 'c_wchar_p', 'calcsize', 'cast', 'cdll', 'create_string_buffer', 'create_unicode_buffer', 'exists', 'get_errno', 'get_last_error', 'join', 'maxsize', 'memmove', 'memset', 'namedtuple', 'oledll', 'platform', 'pointer', 'py_object', 'pydll', 'pythonapi', 'resize', 'set_errno', 'set_last_error', 'sizeof', 'string_at', 'unicode_literals', 'windll', 'wstring_at'
</details>
<br>

to get the functions run

```python
import WalabotAPI
help(WalabotAPI)
```

<details>
<summary>functions</summary>

    CancelCalibration()
        Stops calibration.
        To check on calibration progress, use GetStatus().

    Clean()
        Cleans walabot library and release memory.

    Connect(uid)
        Establishes communication with a specified Walabot device.

        Connection is required before WalabotAPI.Start().
        If only a single Walabot device is present, it is simpler to use WalabotAPI.ConnectAny(), so the uid is not required.

            Parameters:
                uid             Walabot device ID string, obtained from
                                GetInstrumentsList()

    ConnectAny()
        Establishes communication with Walabot.
        Connection is required before Start(). If multiple Walabots are
        present a single available Walabot is selected. To specify one, use
        Connect().

    Disconnect()
        Stops communication with Walabot.

    GetAntennaPairs()
        Obtains a list of Walabot antenna pairs.
        For use before GetSignal(). To identify the antennas on your Walabot
        device, see the specifications for your model.
        Returns:
            antennaPairs:   List of antenna pairs (of AntennaPair namedtuple)

    GetArenaPhi()
        Obtains azimuth range and resolution of arena.
        Can be changed with SetArenaPhi(). Spherical coordinates are relevant
        only to get image data from a triggered scan that used one of the
        Sensor profiles. Otherwise the SetArena functions for cartesian
        coordinates apply.
        Returns:
            minInDegrees:   Beginning of azimuth angular range (degrees)
            maxInDegrees:   End of azimuth angular range (degrees)
            resInDegrees:   Angle between pixels across polar angle (degrees)

    GetArenaR()
        Obtains radial range and resolution of arena.
        Can be changed with SetArenaR(). Spherical coordinates are relevant
        only to get image data from a triggered scan that used one of the
        Sensor profiles. Otherwise the SetArena functions for cartesian
        coordinates apply.
        Returns:
            startInCm:      Beginning of radial distance range (cm)
            endInCm:        End of radial distance range (cm)
            resInCm:        Image resolution along radius (cm)

    GetArenaTheta()
        Obtains polar range and resolution of arena.
        Can be changed with SetArenaTheta(). Spherical coordinates are
        relevant only to get image data from a triggered scan that used one of
        the Sensor profiles. Otherwise the SetArena functions for cartesian
        coordinates apply.
        Returns:
            minInDegrees:   Beginning of polar angular range (degrees)
            maxInDegrees:   End of polar angular range (degrees)
            resInDegrees:   Angle between pixels across polar angle (degrees)

    GetArenaX()
        Obtains current X-axis range and resolution of arena.
        Can be changed with SetArenaX(). Cartesian coordinates are relevant
        only to get image data from a triggered scan that used the short-range
        profile. Otherwise the SetArena functions for spherical coordinates
        apply.
        Returns:
            minInCm:        Beginning of range on axis (cm)
            maxInCm:        End of range on axis (cm)
            resInCm:        Distance between pixels along axis (cm)

    GetArenaY()
        Obtains current Y-axis range and resolution of arena.
        Can be changed with SetArenaY(). Cartesian coordinates are relevant
        only to get image data from a triggered scan that used the short-range
        profile. Otherwise the SetArena functions for spherical coordinates
        apply.
        Returns:
            minInCm:        Beginning of range on axis (cm)
            maxInCm:        End of range on axis (cm)
            resInCm:        Distance between pixels along axis (cm)

    GetArenaZ()
        Obtains current Z-axis range and resolution of arena.
        Can be changed with SetArenaZ(). Cartesian coordinates are relevant
        only to get image data from a triggered scan that used the short-range
        profile. Otherwise the SetArena functions for spherical coordinates
        apply.
        Returns:
            startInCm:      Beginning of range on axis (cm)
            endInCm:        End of range on axis (cm)
            resInCm:        Distance between pixels along axis (cm)

    GetDynamicImageFilter()
        Obtains current Walabot Dynamic-imaging filter setting.
        Can be called at any time, default value is FILTER_TYPE_NONE
        Returns:
            filterType      Dynamic-imaging filter current setting.

    GetErrorString()
        Obtains the detailed string of the last error.

    GetExtendedError()
        Obtains additional error information, for Vayyar support.

    GetImageEnergy()
        Provides the sum of all the raw images pixels signal power.
        Requires previous Trigger(); provides data based on last completed
        triggered image. Provided image data is dependent on current
        configured arena.
        Returns:
            energy:         Number representing the sum of all the raw images
                            pixels signal power

    GetImagingTargets()
        Provides a list of identified targets.
        Available only if the short-range scan profile was used. Requires
        previous Trigger(); provides data based on last completed triggered
        image. Provided image data is dependent on current configured arena
        and on current configuration from SetDynamicImageFilter() and
        SetThreshold(). Note: In the current API version, provides only the
        single target with the strongest signal, in format appropriate for pipe
        Returns:
            targets:        List of targets (in current API version, a single
                            target) (of ImagingTarget namedtuple)

    GetInstrumentsList()
        Obtains a string listing connected Walabots.

        For use before WalabotAPI.Connect(). A Walabot ID obtained here is used to identify the device to connect to.

    GetRawImage()
        Provides tridimensional (3-D) image data.
        Image data is a 3-dimensional matrix in which each element represents
        the reflected power at (x,y,z) spatial location corresponding to this
        element indexing in the matrix. The coordinates are according to the
        profile used. For sensor profile, the coordinates are Theta-Phi-R
        (polar coordinates), while for short-range sensor, the coordinates are
        to X-Y-Z plane (carthesian coordinates). The matrix is transferred
        using a vector which is the concatenated matrix rows. Meaning: assuming
        3D matrix with indexes i, j & k. the vector is represented as followed:
        The matrix is represented as follows, for 3D index coordinates {i,j,k}:
            sizeX:  represnts the i dimension length
            sizeY:  represnts the j dimension length
            sizeZ:  represnts the k dimension length
            img3d:  represtes the walabot 3D scanned image (internal data)
        normalized_abs_val = abs( img3d[i][j][k] ), normalized between 0 to 1
        rasterImage[i][j][k] = (int)(normalized_abs_val * 255)
        Each index represent the location along its axis according to the arena
        defined. For Carthesian coordinates Arena (using WalabotAPI.SetArenaX(),
        WalabotAPI.SetArenaY(), WalabotAPI.SetArenaZ()):
            dx = (xMax-xMin) / (sizeX-1)
            dy = (yMax-yMin) / (sizeY-1)
            dz = (zMax-zMin) / (sizeZ-1)
        Then:
            M[i][j][k] = strength at position (xMin + i*dx, yMin + j*dy, zMin + k*dz)

            dTheta = (thetaMax-thetaMin) / (sizeX-1)
            dPhi = (phiMax-phiMin) / (sizeY-1)
            dR = (RMax-RMin) / (sizeZ-1)
        Then:
            M[i][j][k] = strength at position (thetaMin + i*dTheta, phiMin + j*dPhi, RMin + k*dR)
        Requires previous WalabotAPI.Trigger(). Provides data based on last completed
        triggered image. Output is details of array variable populated by
        provided image data. Provided image data is dependent on current
        configured arena and on current configuration from
        WalabotAPI.SetDynamicImageFilter() and WalabotAPI.SetThreshold().
        Returns:
            rasterImage:    Name of array variable populated by output image data
            sizeX:          Dimension of array variable populated by output
                            image data.
            sizeY:          Dimension of array variable populated by output
                            image data.
            sizeZ:          Dimension of array variable populated by output
                            image data.
            power:          Peak measured power in arena (value of strongest
                            pixel).

    GetRawImageSlice()
        Provides bidimensional (2-D) image data of the 3D image projected to a plane.


        while for short-range sensor, the projection is to X-Y plane (carthesian coordinates).
        One can always use the original 3D raw data to create other planes of interests.
        The value of the element indicates the reflected power measured in its location.

        The matrix is represented as follows, for 2D index coordinates {i,j}:
            sizeX:  represnts the i dimension length
            sizeY:  represnts the j dimension length
            img3d: represents the walabot 2D scanned image (internal data)
            normalized_abs_val = abs( img3d[i][j] )  ## normalized between 0 to 1
            rasterImage[i][j] = (int)(normalized_abs_val * 255)

        Each index represents the location along its axis according to the arena defined:

            For Carthesian coordinates Arena (using WalabotAPI.SetArenaX(), WalabotAPI.SetArenaY()):
                dx = (xMax-xMin) / (sizeX-1)
                dy = (yMax-yMin) / (sizeY-1)

            Then:
                M[i][j] = strength at position (xMin + i*dx, yMin + j*dy)

            For Polar coordinates Arena ( using WalabotAPI.SetArenaR(), WalabotAPI.SetArenaPhi()):
                dPhi = (phiMax-phiMin) / (sizeX-1)
                dR = (RMax-RMin) / (sizeY-1)
            Then:
                M[i][j] = strength at position (phiMin + i*dPhi, RMin + j*dR)
            Requires previous WalabotAPI.Trigger(). Provides data based on last completed
            triggered image. Output is details of array variable populated by
            provided image data. Provided image data is dependent on current
            configured arena and on current configuration from
            WalabotAPI.SetDynamicImageFilter() and WalabotAPI.SetThreshold().
            Returns:
                rasterImage:    Name of list variable populated by output image data.
                sizeX:          Dimension of list variable populated by output
                                image data.
                sizeY:          Dimension of list variable populated by output
                                image data
                sliceDepth:     Third dimension coordinate of maximum target power.
                power:          Peak measured power in arena (value of strongest
                                pixel).

    GetSensorTargets()
        Provides a list of and the number of identified targets.
        Available only if one of the Sensor scan profiles was used. Requires
        previous Trigger(); provides data based on last completed triggered
        image. Provided image data is dependent on current configured arena
        and on current configuration from SetDynamicImageFilter() and
        SetThreshold().
        Returns:
            targets:        List of targets (of SensorTarget namedtuple)

    GetSignal(antennaPair)
        Obtains raw image data from specified antennas.
        Args:
            antennaPair:    Transmitting antenna ID and receiving antenna ID
                            as obtained from GetAntennaPairs()
        Returns:
            signal:         List of amplitude values representing received
                            signal amplitude in time domain
            timeAxis:       List of time axis ticks values

    GetStatus()
        Obtains Walabot status.
        Returns:
            appStatus       Walabot's status
            param           Percentage of calibration completed, if status
                            is STATUS_CALIBRATING

    GetThreshold()
        Obtains the current sensitivity threshold.
        To set the threshold, use SetThreshold().
        Returns:
            threshold:      The current threshold value

    GetTrackerTargets()
        Provides a list of and the number of identified targets.
        Available only if one of the Sensor scan profiles was used. Requires
        previous Trigger(); provides data based on last completed triggered
        image. Provided image data is dependent on current configured arena
        and on current configuration from SetDynamicImageFilter() and
        SetThreshold().
        Returns:
            targets:        List of targets (of TrackerTarget namedtuple)

    GetVersion()
        Obtains current Walabot version.
        The version is build from according to the following parameters:
        1) HW version - Walabot device revision.
        2) SW version - Walabot SW revision.
        3) Regulation information (where applicable).
        The function can be called only after connecting to the device.
        Returns:
            version:        Walabot version

        Must be called before using WalabotAPI functions.
        Args:
            libPath:        Full path to Walabot shared library. If not set, will use default path.
            depLibPaths:    List of full paths to shared libraries that Walabot depends on.
                            This parameter is only necessary if shared libraries are not installed on your path,
                            and/or you want to use them from some other location.

    Initialize(configFileName='C:/Program Files\\Walabot\\WalabotSDK\\bin\\.config')
        Obtains Sets location of Walabot internal database, if moved from
        default.
        Args:
            path           (Optional) Database location. Uses default location
                            if no path is given.

    IsInitialized()

    SetAdvancedParameter(paramName, value)
        Set advanced Walabot parameter.
        Parameters:
            paramName:      Advance parameter name, can be one of the following:
                            PARAM_CONFIDENCE_FACTOR, PARAM_DIELECTRIC_CONSTANT.
            value:          Value to set (floating-point value).

    SetArenaPhi(minInDegrees, maxInDegrees, resInDegrees)
        Sets polar range and resolution of arena.
        To check the current value, use GetArenaTheta(). Spherical coordinates
        should be used only to get image data from a triggered scan that used
        one of the Sensor profiles. Otherwise use the SetArena functions for
        cartesian coordinates.
        Args:
            minInDegrees    Beginning of polar angular range (degrees)
            maxInDegrees    End of polar angular range (degrees)
            resInDegrees    Angle between pixels across polar angle (degrees)

    SetArenaR(startInCm, endInCm, resInCm)
        Sets radial range and resolution of arena.
        To check the current value, use GetArenaR(). Note: Cartesian (X-Y-Z)
        coordinates should be used only to get image data from a triggered scan
        that used the short-range profile. Otherwise use the SetArena functions
        for spherical coordinates.
        Args:
            startInCm       Beginning of range on axis (cm)
            endInCm         End of range on axis (cm)
            resInCm         Distance between pixels along axis (cm)

    SetArenaTheta(minInDegrees, maxInDegrees, resInDegrees)
        Sets polar range and resolution of arena.
        To check the current value, use GetArenaTheta(). Spherical coordinates
        should be used only to get image data from a triggered scan that used
        one of the Sensor profiles. Otherwise use the SetArena functions for
        cartesian coordinates.
        Args:
            minInDegrees    Beginning of polar angular range (degrees)
            maxInDegrees    End of polar angular range (degrees)
            resInDegrees    Angle between pixels across polar angle (degrees)

    SetArenaX(minInCm, maxInCm, resInCm)
        Sets X-axis range and resolution of arena.
        To check the current value, use GetArenaX(). Note: Cartesian (X-Y-Z)
        coordinates should be used only to get image data from a triggered scan
        that used the short-range profile. Otherwise use the SetArena functions
        for spherical coordinates.
        Args:
            minInCm         Beginning of range on axis (cm)
            maxInCm         End of range on axis (cm)
            resInCm         Distance between pixels along axis (cm)

    SetArenaY(minInCm, maxInCm, resInCm)
        Sets Y-axis range and resolution of arena.
        To check the current value, use GetArenaY(). Note: Cartesian (X-Y-Z)
        coordinates should be used only to get image data from a triggered scan
        that used the short-range profile. Otherwise use the SetArena functions
        for spherical coordinates.
        Args:
            minInCm         Beginning of range on axis (cm)
            maxInCm         End of range on axis (cm)
            resInCm         Distance between pixels along axis (cm)

    SetArenaZ(startInCm, endInCm, resInCm)
        Sets Z-axis range and resolution of arena.
        To check the current value, use GetArenaZ(). Note: Cartesian (X-Y-Z)
        coordinates should be used only to get image data from a triggered scan
        that used the short-range profile. Otherwise use the SetArena functions
        for spherical coordinates.
        Args:
            startInCm       Beginning of range on axis (cm)
            endInCm         End of range on axis (cm)
            resInCm         Distance between pixels along axis (cm)

    SetDynamicImageFilter(filterType)
        Dynamic-imaging filter removes static signals, leaving only changing
        signals. Specify filter algorithm to use. Filter is not applied to
        GetImageEnergy(). To check the current value, use
        GetDynamicImageFilter().
        Args:
            filterTyp       Filter algorithm to use

    SetProfile(appProfile)
        Sets scan profile.
        Args:
            appProfile:     The scan profile to use

    SetSettingsFolder(path='C:/ProgramData\\Walabot\\WalabotSDK')
        Obtains Sets location of Walabot internal database, if moved from
        default.
        Args:
            path           (Optional) Database location. Uses default location
                            if no path is given.

    SetThreshold(threshold)
        Changes the sensitivity threshold.
        For raw images (3-D and Slice), Walabot removes very weak signals,
        below this threshold. If the threshold is not set, a default value is
        used. To check the current value, use GetThreshold().
        Args:
            threshold       The threshold to set

    SetTrackerAquisitionThreshold(threshold)

    Start()
        Starts Walabot in preparation for scanning.
        Requires previous Connect (ConnectAny() or Connect()) and SetProfile().
        Required before Trigger() and GET actions.

    StartCalibration()
        Initiates calibration.
        Ignores or reduces the signals of fixed reflectors such as walls
        according to environment. Must be performed initially (to avoid delays
        preferably before Start()), upon any profile change, and is recommended
        upon possible changes to environment. Calibration is done via recording
        and processing. So after calling StartCalibration, a continues trigger
        & GetImage/GetTargets function calls is required. To check on
        calibration progress, use GetStatus().

    Stop()
        Stops Walabot when finished scanning.

    Trigger()
        Initiates a scan and records signals.
        Initiates a scan according to profile and records signals to be
        available for processing and retrieval. Should be performed before
        every GET action.
</details>
<br>

## TODO

* implement the above mentioned functions to fully (including delayed timing) simulate a walabot radar.
* write a good documentation.