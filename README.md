# gmsh_meshing

## Installation Guide (Windows)

This guide will help you set up the required tools using **Chocolatey**.

### Step 1: Install Chocolatey
1. Open **PowerShell as Administrator**.
2. Run:
   ```powershell
   Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
   ```
3. Restart **PowerShell** and verify installation:
   ```sh
   choco --version
   ```

### Step 2: Install Required Software
Run the following commands in **PowerShell (Admin)**:

#### 1. Install Git
```powershell
choco install git -y
```
Verify:
```sh
git --version
```

#### 2. Install MinGW (GCC Compiler)
```powershell
choco install mingw  -y
```
Verify:
```sh
g++ --version
```

#### 3. Install CMake
```powershell
choco install cmake --installargs 'ADD_CMAKE_TO_PATH=System' -y
```
Verify:
```sh
cmake --version
```

#### 4. Install Gmsh SDK (Includes Viewer)
```powershell
choco install gmsh -y
```
Verify:
```sh
gmsh -version
```
Run Gmsh GUI:
```sh
gmsh
```

### Step 3: Ensure Environment Variables
If paths are missing, add manually:
- **MinGW**: `C:\ProgramData\chocolatey\lib\mingw\tools\install\mingw64\bin`
- **CMake**: `C:\Program Files\CMake\bin`
- **Gmsh**: `C:\ProgramData\chocolatey\lib\gmsh\tools\gmsh\bin`

### Step 4: Final Verification
Run the following commands:
```sh
git --version
g++ --version
cmake --version
gmsh -version
```
If all return versions, setup is complete! 🚀
