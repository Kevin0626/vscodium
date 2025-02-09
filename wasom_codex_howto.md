

## 环境配置

### VPN设置：clash

### Missing spectre mitigated libraries on Windows
https://github.com/microsoft/vscode/wiki/How-to-Contribute#missing-spectre-mitigated-libraries-on-windows 
If you are using npm >= 10.2.3 or node-gyp >= 10.0.0, then you might see error when building native modules of this project
Spectre-mitigated libraries are required for this project.
To fix this error open Visual Studio Installer, add the following components corresponding to the architecture you are building for (x64/ARM/ARM64) and restart your build session
●MSVC Spectre-mitigated libs (latest)
●C++ ATL for latest build tools with Spectre Mitigations
●C++ MFC for latest build tools with Spectre Mitigations


https://github.com/microsoft/vscode/wiki/How-to-Contribute 
●Windows 10/11（x64 或 ARM64）https://visualstudio.microsoft.com/thank-you-downloading-visual-studio/?sku=BuildTools 或https://visualstudio.microsoft.com/thank-you-downloading-visual-studio/?sku=Community 来安装 Visual C++ 构建环境。安装的最小工作量为Desktop Development with C++。但“单个组件”中还有其他组件：MSVC v143 - VS 2022 C++ x64/x86 Spectre-mitigated libs (Latest)（用于ARM64ARM 上的 Windows，但可能仍然需要 x64/x86）
■C++ ATL for latest build tools with Spectre Mitigations
■C++ MFC for latest build tools with Spectre Mitigations
■注意：对于 ARM 上的 Windows，您可能需要将版本指定为 v14.41-17.11，而不是 (最新)，以及MSVC v143 - VS 2022 C++ build tools。
○打开命令提示符并运行npm config edit并添加或修改msvs_version与您的 vs 版本相同的设置。（例如msvs_version=2022对于 visual studio 2022）
○警告：确保您的配置文件路径仅包含 ASCII 字母，例如John，否则可能会导致https://github.com/nodejs/node-gyp/issues/297 
○注意：目前不支持通过 Windows 的 Linux 子系统 (WSL) 进行构建和调试。



### npm

华为npm源：  
npm config set registry https://mirrors.huaweicloud.com/repository/npm/

淘宝npm源：  
npm config set registry https://registry.npmmirror.com/

npm config get registry
https://mirrors.huaweicloud.com/repository/npm/



1. 在

git config --global http.proxy http://127.0.0.1:7890
git config --global https.proxy https://proxy.example.com:8080




git config http.proxy http://127.0.0.1:7890
git config https.proxy https://127.0.0.1:7890

## 更换图片

src/insider/src/vs/workbench/browser/media/code-icon.svg

src/stable/src/vs/workbench/browser/media/code-icon.svg

src/stable/src/vs/workbench/browser/parts/editor/media/
- letterpress-dark.svg
- letterpress-hcDark.svg
- letterpress-hcLight.svg
- letterpress-light.svg