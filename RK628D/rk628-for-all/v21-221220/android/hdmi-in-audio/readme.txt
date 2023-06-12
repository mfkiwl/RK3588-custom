1. src-rkCamera2-v13-with-audio-210924.tar.gz  是包含了音频部分的rkCamera2的源码包，其代码可以放置在packages/apps/rkCamera2 目录下面编译出APK。

2. patch_rk628-android9-audio-v10-210924.tar.gz 是HDMI-IN的AUDIO补丁包，可以用于ANDROID7/8/9版本，ANDROID10/11版本需要的修改较少，可以采用patch_rk628-android11-audio-v10-210924.tar.gz补丁包即可。

patch_rk628-android9-audio-v10-210924
├── device
│   └── rockchip
│       └── common
│           └── 0001-add-hdmi-in-audio-policy-configuration.patch
├── frameworks
│   └── av
│       └── 0001-add-hdmi-in-audio-support.patch
├── hardware
│   └── rockchip
│       └── audio
│           ├── 0001-support-RT5640-hdmiin-capture-route-config.patch
│           ├── 0002-support-HDMIIn-capture-mode.patch
│           └── 0003-audio-hal-use-levenshtein-distance-for-sound-card-ma.patch
└── tags_name.txt

3. src_rk628-android9-audio-v10-210924.tar.gz 是HDMI-IN audio补丁对应的源码，对于ANDROID7/8/9代码可以源码覆盖。

./src_rk628-android9-audio-v10-210924/
├── device
│   └── rockchip
│       └── common
│           └── audio_policy_configuration.xml
├── filename.txt
├── filepath.txt
├── frameworks
│   └── av
│       └── services
│           └── audiopolicy
│               └── enginedefault
│                   └── src
│                       └── Engine.cpp
├── grepname.txt
└── hardware
    └── rockchip
        └── audio
            └── tinyalsa_hal
                ├── alsa_audio.h
                ├── alsa_route.c
                ├── audio_hw.c
                ├── audio_hw.h
                └── codec_config
                    ├── config.h
                    └── rt5640_config.h

14 directories, 11 files

4. 如果 hardware/rockchip/audio补丁不好打，ANDROID7/8/9直接采用源码 src-hardware-rockchip-audio-210926.tar.gz 覆盖即可。



