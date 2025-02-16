# Performance Comparison Tables

- [Table 1: Comparison of localization methods on Replica](#table-1-comparison-of-localization-methods-on-replica)
- [Table 2: Comparison of mapping methods on Replica](#table-2-comparison-of-mapping-methods-on-replica)
- [Table 3: Comparison of reconstruction methods on D-NeRF](#table-3-comparison-of-reconstruction-methods-on-d-nerf)
- [Table 4: Comparison of reconstruction methods on ZJU-MoCap](#table-4-comparison-of-reconstruction-methods-on-zju-mocap)
- [Table 5: Comparison of reconstruction methods on EndoNeRF](#table-5-comparison-of-reconstruction-methods-on-endonerf)

---

## Table 1: Comparison of localization methods on Replica

Comparison of localization methods on Replica (static scenes), in terms of absolute trajectory error (ATE, cm).

| Method                                                       | GS   | Room0                           | Room1                           | Room2                           | Office0                         | Office1                         | Office2                         | Office3                         | Office4                         | Average                         |
| ------------------------------------------------------------ | ---- | ------------------------------- | ------------------------------- | ------------------------------- | ------------------------------- | ------------------------------- | ------------------------------- | ------------------------------- | ------------------------------- | ------------------------------- |
| [Vox-Fusion](https://github.com/zju3dv/Vox-Fusion)           |      | 1.37                            | 4.70                            | 1.47                            | 8.48                            | 2.04                            | 2.58                            | 1.11                            | 2.94                            | 3.09                            |
| [NICE-SLAM](https://github.com/cvg/nice-slam)                |      | 0.97                            | 1.31                            | 1.07                            | 0.88                            | 1.00                            | 1.06                            | 1.10                            | 1.13                            | 1.06                            |
| [ESLAM](https://github.com/idiap/ESLAM)                      |      | 0.71                            | 0.70                            | 0.52                            | 0.57                            | 0.55                            | 0.58                            | 0.72                            | 0.63 | 0.63                            |
| [Point-SLAM](https://github.com/eriksandstroem/Point-SLAM)   |      | 0.61                            | 0.41 | 0.37                            | 0.38  | 0.48                            | 0.54                            | 0.69                            | 0.72                            | 0.52                            |
| [Co-SLAM](https://github.com/HengyiWang/Co-SLAM)             |      | 0.70                            | 0.95                            | 1.35                            | 0.59                            | 0.55                            | 2.03                            | 1.56                            | 0.72                            | 1.00                            |
| [Gaussian-SLAM](https://github.com/VladimirYugay/Gaussian-SLAM) | ✓    | 3.35                            | 8.74                            | 3.13                            | 1.11                            | 0.81                            | 0.78                            | 1.08                            | 7.21                            | 3.27                            |
| [GSSLAM](https://github.com/muskie82/MonoGS)                 | ✓    | 0.47 | 0.43                            | 0.31 | 0.70                            | 0.57                            | 0.31 | 0.31  | 0.31                            | 0.79                            |
| [GS-SLAM](https://github.com/yanchi-3dv/diff-gaussian-rasterization-for-gsslam) | ✓    | 0.48                            | 0.53                            | 0.33                            | 0.52                            | 0.41 | 0.59                            | 0.46                            | 0.70                            | 0.50 |
| [SplaTAM](https://github.com/spla-tam/SplaTAM)               | ✓    | 0.31  | 0.40  | 0.29  | 0.47 | 0.27  | 0.29  | 0.32 | 0.55  | 0.36  |

---

## Table 2: Comparison of mapping methods on Replica

Comparison of mapping methods on Replica (static scenes), in terms of PSNR, SSIM, and LPIPS.

| Method                                                       | GS   | Metric | Room0                            | Room1                               | Room2                            | Office0                          | Office1                          | Office2                             | Office3                              | Office4                          | Average                          | FPS  |
| ------------------------------------------------------------ | ---- | ------ | -------------------------------- | ----------------------------------- | -------------------------------- | -------------------------------- | -------------------------------- | ----------------------------------- | ------------------------------------ | -------------------------------- | -------------------------------- | ---- |
| [NICE-SLAM](https://github.com/cvg/nice-slam)                |      | PSNR↑  | 22.12                            | 22.47                               | 24.52                            | 29.07                            | 30.34                            | 19.66                               | 22.23                                | 24.94                            | 24.42                            | 0.81 |
|                                                              |      | SSIM↑  | 0.69                             | 0.76                                | 0.81                             | 0.87                             | 0.89                             | 0.80                                | 0.80                                 | 0.86                             | 0.81                             |      |
|                                                              |      | LPIPS↓ | 0.33                             | 0.27                                | 0.21                             | 0.23                             | 0.18                             | 0.23                                | 0.21                                 | 0.20                             | 0.23                             |      |
| [Vox-Fusion](https://github.com/zju3dv/Vox-Fusion)           |      | PSNR↑  | 22.39                            | 22.36                               | 23.92                            | 27.79                            | 29.83                            | 20.33                               | 23.47                                | 25.21                            | 24.41                            | 2.17 |
|                                                              |      | SSIM↑  | 0.68                             | 0.75                                | 0.80                             | 0.86                             | 0.88                             | 0.79                                | 0.80                                 | 0.85                             | 0.80                             |      |
|                                                              |      | LPIPS↓ | 0.30                             | 0.27                                | 0.23                             | 0.24                             | 0.18                             | 0.24                                | 0.21                                 | 0.20                             | 0.24                             |      |
| [Point-SLAM](https://github.com/eriksandstroem/Point-SLAM)   |      | PSNR↑  | 32.40                            | 34.08                               | 35.50                            | 38.26                            | 39.16                            | 33.99    | 33.48      | 33.49                            | 35.17                            | 1.33 |
|                                                              |      | SSIM↑  | 0.97                             | 0.98                                | 0.98                             | 0.98                             | 0.98                             | 0.96                                | 0.96                                 | 0.98                             | 0.97                             |      |
|                                                              |      | LPIPS↓ | 0.11                             | 0.12                                | 0.11                             | 0.10                             | 0.12                             | 0.16                                | 0.13                                 | 0.14                             | 0.12                             |      |
| [SplaTAM](https://github.com/spla-tam/SplaTAM)               | ✓    | PSNR↑  | 32.86                            | 33.89                               | 35.25                            | 38.26                            | 39.17                            | 31.97                               | 29.70                                | 31.81                            | 34.11                            | -    |
|                                                              |      | SSIM↑  | 0.98   | 0.98      | 0.98   | 0.98                             | 0.98                             | 0.95                                | 0.95                                 | 0.97                             |                                  |      |
|                                                              |      | LPIPS↓ | 0.07  | 0.10                                | 0.08                             | 0.09                             | 0.09                             | 0.10                                | 0.12                                 | 0.15                             | 0.10                             |      |
| [GSSLAM](https://github.com/yanchi-3dv/diff-gaussian-rasterization-for-gsslam) | ✓    | PSNR↑  | 31.56                            | 32.86                               | 32.59                            | 38.70                            | 41.17  | 32.36                               | 32.03                                | 32.92                            | 34.27                            | -    |
|                                                              |      | SSIM↑  | 0.97                             | 0.97                                | 0.97                             | 0.99  | 0.99  | 0.98     | 0.98      | 0.97  | 0.97  |      |
|                                                              |      | LPIPS↓ | 0.07  | 0.07     | 0.07  | 0.05   | 0.03   | 0.09                                | 0.11                                 | 0.11                             | 0.08                             |      |
|                                                              |      | SSIM↑  | 0.98   | 0.98      | 0.99   | 0.99   | 0.99   | 0.97      | 0.97       | 0.98   | 0.98   |      |
|                                                              |      | LPIPS↓ | 0.05                             | 0.05                                | 0.04                             | 0.03                             | 0.03                             | 0.07     | 0.08      | 0.08                             | 0.05                             |      |
| [GSSLAM](https://github.com/muskie82/MonoGS)                 | ✓    | PSNR↑  | 34.83 | 	36.43 | 37.49  | 39.95  | 42.09   | 	36.24 | 	36.70 | 36.07 | 37.50  | 769  |
|                                                              |      | SSIM↑  | 0.98  | 0.98     | 0.96                             | 0.97                             | 0.98   | 0.98      | 0.98       | 0.96                             | 0.98   |      |
|                                                              |      | LPIPS↓ | 0.07  | 0.08                                | 0.07  | 0.07  | 0.06  | 0.08                                | 0.07      | 0.10                             | 0.07  |      |
| [Gaussian-SLAM](https://github.com/VladimirYugay/gaussian-slam)   | ✓    | PSNR↑  | 34.31  | 37.28    | 38.18   | 43.97   | 43.56 | 37.39      | 36.48       | 40.19   | 38.90   | -    |
|                                                              |      | SSIM↑  | 0.99    | 0.99       | 0.99    | 1.00    | 0.99    | 0.99       | 0.99        | 1.00    | 0.99    | -    |
|                                                              |      | LPIPS  | 0.08                             | 0.07      | 0.07   | 0.04    | 0.04    | 0.07      | 0.07       | 0.07   | 0.07   | -    |

---

## Table 3: Comparison of reconstruction methods on D-NeRF

Comparison of reconstruction methods on D-NeRF (dynamic scenes), in terms of PSNR, SSIM, and LPIPS.

| Method                                                       | GS   | PSNR↑                            | SSIM↑                         | LPIPS↓                          |
| ------------------------------------------------------------ | ---- | -------------------------------- | ----------------------------- | ------------------------------- |
| [D-NeRF](https://github.com/albertpumarola/D-NeRF)           |      | 30.50                            | 0.95                          | 0.07                            |
| [TiNeuVox-B](https://github.com/hustvl/TiNeuVox)             |      | 32.67                            | 0.97                          | 0.04                            |
| [KPlanes](https://github.com/sarafridov/K-Planes)            |      | 31.61                            | 0.97                          | -                               |
| [HexPlane-Slim](https://github.com/Caoang327/HexPlane)       |      | 32.68                            | 0.97                          | 0.02                            |
| [MSTH](https://github.com/masked-spacetime-hashing/msth)     |      | 31.34                            | 0.98                          | 0.02                            |
| [3D GS](https://github.com/graphdeco-inria/gaussian-splatting) | ✓    | 23.19                            | 0.93                          | 0.08                            |
| [4DGS](https://github.com/fudan-zvg/4d-gaussian-splatting)   | ✓    | 34.09                            | 0.98                          | -                               |
| [4D-GS](https://github.com/hustvl/4DGaussians)               | ✓    | 34.05                            | 0.98                          | 0.02                            |
| [GaGS](https://github.com/zhichengLuxx/GaGS)                 | ✓    | 37.36 | 0.99 | 0.01   |
| [D-3DGS](https://github.com/ingra14m/Deformable-3D-Gaussians) | ✓    | 39.51   | 0.99 | 0.02 |

---

## Table 4: Comparison of reconstruction methods on ZJU-MoCap

Comparison of reconstruction methods on ZJU-MoCap (avatar), in terms of PSNR, SSIM, and LPIPS\*. The numbers of non-GS methods are taken from GART.

| Method                                                       | GS   | PSNR↑                            | SSIM↑                         | LPIPS↓\*                         |
| ------------------------------------------------------------ | ---- | -------------------------------- | ----------------------------- | -------------------------------- |
| [NeuralBody](https://github.com/zju3dv/neuralbody)           |      | 29.03                            | 0.96                          | 42.47                            |
| [AnimNeRF](https://github.com/JanaldoChen/Anim-NeRF)         |      | 29.77                            | 0.96                          | 46.89                            |
| [PixelNeRF](https://github.com/sxyu/pixel-nerf)              |      | 24.71                            | 0.89                          | 121.86                           |
| [NHP](https://github.com/YoungJoongUNC/Neural_Human_Performer) |      | 28.25                            | 0.95                          | 64.77                            |
| [HumanNeRF](https://github.com/chungyiweng/humannerf)        |      | 30.66                            | 0.97                          | 33.38                            |
| [Instant-NVR](https://github.com/zju3dv/instant-nvr)         |      | 31.01                            | 0.97                          | 38.45                            |
| [GauHuman](https://github.com/skhu101/GauHuman)              | ✓    | 31.34  | 0.97                          | 30.51                            |
| [3DGS-Avatar](https://github.com/mikeqzy/3dgs-avatar-release) | ✓    | 30.61                            | 0.97                          | 29.58                            |
| [GART](https://github.com/JiahuiLei/GART)                    | ✓    | 32.22   | 0.98 | 29.21 |

---

## Table 5: Comparison of reconstruction methods on EndoNeRF

Comparison of reconstruction methods on EndoNeRF (surgical scenes), in terms of PSNR, SSIM, and LPIPS. The numbers of non-GS methods, FPS, and GPU usage (Mem.) are taken from . \* denotes numbers taken from . <sup>†</sup> denotes the average of the values reported in the original paper.

| Method                                                  | GS   | PSNR↑                            | SSIM↑                           | LPIPS↓                         | FPS↓   | Mem.↓ |
| ------------------------------------------------------- | ---- | -------------------------------- | ------------------------------- | ------------------------------ | ------ | ----- |
| [EndoNeRF](https://github.com/med-air/EndoNeRF)         |      | 36.06                            | 0.93                            | 0.09                           | 0.04   | 19GB  |
| [EndoSurf](https://github.com/Ruyi-Zha/endosurf)        |      | 36.53                            | 0.95                            | 0.07                           | 0.04   | 17GB  |
| [LerPlane-9k](https://github.com/Loping151/ForPlane)    |      | 35.00                            | 0.93                            | 0.08                           | 0.91   | 20GB  |
| [LerPlane-32k](https://github.com/Loping151/ForPlane)   |      | 37.38 | 0.95                            | 0.05                           | 0.87   | 20GB  |
| [EndoGS](https://github.com/HKU-MedAI/EndoGS)           | ✓    | 36.84                            | 0.96                            | 0.04 | -      | -     |
| [Endo-4DGS](https://github.com/lastbasket/Endo-4DGS)    | ✓    | 37.00                            | 0.96 | 0.05                           | -      | 4GB   |
| [EndoGaussian](https://github.com/CUHK-AIM-Group/EndoGaussian) | ✓    | 37.85  | 0.96 | 0.05                           | 195.09 | 2GB   |
| [HFGS](https://github.com/Maxwell-Zhao/HFGS)                                                    | ✓    | 38.14   | 0.97   | 0.03  | -      | -     |
