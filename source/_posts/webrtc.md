---
title: webrtc
date: 2021-08-02 15:58:43
tags:
---

# 源码
`git clone https://webrtc.googlesource.com/src`


# ADM: audio device module模块
```
webrtc

WebRtcVoiceEngine::Init() 的时候初始化 
    adm_ = webrtc::AudioDeviceModule::Create(
        webrtc::AudioDeviceModule::kPlatformDefaultAudio, task_queue_factory_);

class AudioDeviceModuleIOS sdk/objc/native/src/audio/audio_device_module_ios.mm
    继承 class AudioDeviceModuleIOS : public AudioDeviceModule
    这里使用 std::unique_ptr<AudioDeviceIOS> audio_device_;

    还有其他的 AndroidAudioDeviceModule WindowsAudioDeviceModule 都继承public AudioDeviceModule

class AudioDeviceIOS sdk/objc/native/src/audio/audio_device_ios.mm
    这里使用  std::unique_ptr<VoiceProcessingAudioUnit> audio_unit_;

class VoiceProcessingAudioUnit sdk/objc/native/src/audio/voice_processing_audio_unit.mm
    主要在这里 AudioUnitSetProperty

```
可以参考源码中的文档
modules/audio_device/g3doc/audio_device_module.md
ADM: audio device module

另外一些分析ADM文章：https://blog.piasy.com/2018/09/14/WebRTC-ADM/index.html
# 一些refercence
 * Official web site: http://www.webrtc.org
 * Master source code repo: https://webrtc.googlesource.com/src
 * Samples and reference apps: https://github.com/webrtc
 * Mailing list: http://groups.google.com/group/discuss-webrtc
 * Continuous build: https://ci.chromium.org/p/webrtc/g/ci/console
 * [Coding style guide](g3doc/style-guide.md)
 * [Code of conduct](CODE_OF_CONDUCT.md)
 * [Reporting bugs](docs/bug-reporting.md)