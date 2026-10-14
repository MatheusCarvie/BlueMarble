# BlueMarble

Engine gráfica em C++20 com OpenGL.

## Dependências

| Lib | Uso |
|-----|-----|
| GLFW | Janela e input |
| GLAD | Loader de funções OpenGL |
| GLM | Matemática (vetores, matrizes) |
| OpenGL | Renderização |

## Build

### Windows (MSVC)

1. Instale o [Visual Studio](https://visualstudio.microsoft.com/) com o workload "Desktop development with C++"
2. Instale o [CMake](https://cmake.org/download/) (ou use o que vem com o VS)
3. As libs pré-compiladas já estão em `deps/glfw/`
4. Build (x64 Native Tools Command Prompt):

```bash
cmake -B build
cmake --build build
```

Ou abra a pasta no VS Code e use o task de build.

### Ubuntu / Debian

```bash
sudo apt install build-essential cmake libglfw3-dev
```

```bash
cmake -B build
cmake --build build
```

### Fedora

```bash
sudo dnf install gcc-c++ cmake glfw-devel
```

```bash
cmake -B build
cmake --build build
```

### Arch

```bash
sudo pacman -S base-devel cmake glfw-x11
# ou para Wayland:
# sudo pacman -S base-devel cmake glfw-wayland
```

```bash
cmake -B build
cmake --build build
```
