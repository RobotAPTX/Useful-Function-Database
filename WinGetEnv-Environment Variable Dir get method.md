        #include <windows.h>

        const char* DownloadManager::WinGetEnv(const char* name)
        {
            const DWORD buffSize = 65535;
            static char buffer[buffSize];
            if (GetEnvironmentVariableA(name, buffer, buffSize)) {
                return buffer;
            } else {
                return 0;
            }
        }
