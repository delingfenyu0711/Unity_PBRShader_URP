# Unity PBR (Physically Based Rendering) Implementation
This repository contains a custom Physically Based Rendering (PBR) implementation for Unity. By simulating the interaction between light and matter in the real world, it achieves realistic material rendering effects. The included shaders and auxiliary files follow industry-standard PBR principles, ensuring consistent and physically plausible visual effects under different lighting conditions.
Physically Based Rendering (PBR) is a rendering method based on physical properties. Unlike traditional rendering, its core focuses include:
- Energy Conservation: The intensity of reflected light will not exceed that of incident light
- Realistic Material Properties: Accurately restore physical parameters such as metallicity, roughness, and albedo
- Lighting Consistency: The response of different materials under the same light conforms to physical laws
- Direct/Indirect Light Processing: Accurately calculate the contribution of direct and indirect lighting

## 1. Shader Files
File Path
Function Description
`Scripts/Shader/Lit_BPR.shader`
Core PBR shader, handling core calculations such as specular reflection, diffuse reflection, and environmental reflection
`Scripts/Shader/LitForwardPass_dlfy.hlsl`
Forward rendering pass logic, containing code for light interaction calculations in the forward rendering pipeline
`Scripts/Shader/Lighting_dlfy.hlsl`
Lighting utility function library, including auxiliary calculations such as light attenuation, shadow processing, and BRDF implementation

## 2. Folder Structure
Scripts/
├── Shader/                # All PBR-related shaders and HLSL files
│   ├── Lit_BPR.shader
│   ├── LitForwardPass_dlfy.hlsl
│   ├── Lighting_dlfy.hlsl
│   └── [Related .meta files]
└── Player/                # Optional: Player-related scripts interacting with PBR materials/lighting
    └── [Related files and .meta files]
- ✅ Physically accurate material response
- ✅ Supports Metallic/Roughness workflow
- ✅ Energy-conserving Bidirectional Reflectance Distribution Function (BRDF)
- ✅ Correct handling of direct and indirect illumination
- ✅ Fully compatible with Unity's lighting system
