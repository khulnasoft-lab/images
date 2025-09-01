# Use a Windows Server Core image with .NET Framework
FROM mcr.microsoft.com/dotnet/framework/sdk:4.8.1

# Install Visual Studio Build Tools with required workloads
RUN curl -SL --output %TEMP%\vs_buildtools.exe https://aka.ms/vs/17/release/vs_buildtools.exe

RUN %TEMP%\vs_buildtools.exe --quiet --wait --norestart --nocache --noUpdateInstaller \
    --add Microsoft.VisualStudio.Workload.VisualStudioExtensionBuildTools

RUN del /F /Q %TEMP%\vs_buildtools.exe
