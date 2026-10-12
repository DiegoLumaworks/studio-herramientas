# Studio · herramientas

Programas ya compilados que **Studio** descarga dentro de la carpeta del alumno, para que no tenga que instalar Homebrew, cmake ni compilar nada.

## whisper-1.7.6

`whisper-cli` de [whisper.cpp](https://github.com/ggml-org/whisper.cpp) v1.7.6 (licencia MIT, incluida en cada zip), compilado sin cambios desde el código oficial:

```
cmake -DCMAKE_BUILD_TYPE=Release -DBUILD_SHARED_LIBS=OFF -DGGML_NATIVE=OFF \
  -DGGML_METAL=ON -DGGML_METAL_EMBED_LIBRARY=ON -DCMAKE_OSX_DEPLOYMENT_TARGET=12.0 \
  -DCMAKE_OSX_ARCHITECTURES=<arm64|x86_64>
```

Estático: solo usa librerías del sistema (Accelerate, Metal, Foundation). Studio verifica cada zip con su huella SHA-256 antes de usarlo.

| Archivo | SHA-256 |
|---|---|
| whisper-cli-1.7.6-macos-arm64.zip | `3aad1deaad8a6c970fb0183633ace4087381724529fa739e50f738c71e79a1db` |
| whisper-cli-1.7.6-macos-x64.zip | `f521d5db75f12bc8d5a458cdbe16f7c961d6c7768f7b3060e39ad24c3be8ac52` |
