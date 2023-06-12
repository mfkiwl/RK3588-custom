1、查看以下文件选择版本：
hardware/rockchip/camera/SiliconImage/include/isp_cam_api/cam_api/cam_engine_interface.h

如果是下面宏定义，则选择camerahal1-isplib-2.4这包软件
#define CONFIG_SILICONIMAGE_LIBISP_VERSION KERNEL_VERSION(2, 0x04, 0)
如果是是下面宏定义，则选择camerahal1-isplib-3.1这包软件
#define CONFIG_SILICONIMAGE_LIBISP_VERSION KERNEL_VERSION(3, 0x1, 0)   
如果文件不存在（ANDROID9.0及更高版本），则选择camerahal3这包软件

2、rk356x_HAL3_support_rgb2yuv_patch.rar 的用途
适用于RK3568+RK628+HDMI2CSI的应用场景，用于规避HDMI2CSI的色偏问题，对其他芯片方案无效，其使用说明在补丁包里，该补丁包根据需求来决定是否需要。
对于ANDROID12版本的R10/R11版本则可以直接打补丁0001-rkisp2-add-rgb2yuv-base-android12-R11.patch。

3、3dlut目录用途
适用于RK3399+RK628+HDMI2GVI的应用场景，用于调整色温和画质，具体使用说明在补丁包里，该补丁包根据需求来决定是否需要。
