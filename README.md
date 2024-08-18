# Deep-Live-Cam-all-in-one-package环境整合包
Deep-Live-Cam-all-in-one-package


# Deep-Live-Cam 与 DeepFaceLive 的比较评测

最近，**deep-live-cam** 项目（下文简称 **DLC**）也火了一把。它只需一张图就能实现实时换脸，完全不需要训练自己的模型，直接开箱就能使用。文末我会提供本地运行的整合包下载链接。

## 软件提供的功能

- 图片换脸
- 摄像头实时换脸
- 带人脸清晰化的换脸

还有一个知名的项目叫 **DeepFaceLive**，也是用于实时换脸。巧合的是，我也是 DeepFaceLive 项目的参与者，因此我对这两个同类软件做了个比较评测，分以下几个方面进行对比。

## 易用度

- **deep-live-cam:** ★★★★☆
- **deepfacelive:** ★☆☆☆☆

在这方面，毫无疑问是 DLC 胜出。DLC 无需训练，只需要一张照片就能直接进行换脸。而 DeepFaceLive（以下简称 **DFL**）由于算法不同，需要针对每个要换脸的形象单独训练一个模型，使用过程相对繁琐。训练时间从几天到几周不等，想快速图个新鲜好玩的用户显然不适合 DFL。

虽然 DLC 的算法方便了使用，但目前用户界面和操作流程仍然比较原始，各种 bug 也比较多，因此只能给 4 星。

## 功能丰富度

- **deep-live-cam:** ★☆☆☆☆
- **deepfacelive:** ★★★★☆

DLC 虽然简单，但也丧失了很多操控性，比如输入来源、颜色控制、边缘融合处理、人脸大小控制、多人脸筛选控制等，基本没有这些实际商用会遇到的功能需求。甚至不如使用同一个算法的 **Rope** 项目，Rope 项目的功能也比 DLC 更丰富。

DFL 相对成熟，功能较多。

## 清晰度

- **deep-live-cam:** ★☆☆☆☆-★★★☆☆
- **deepfacelive:** ★★★☆☆-★★★★★

DLC 的清晰度是其一大弱点，因为其基础模型只有 128x128 的人脸分辨率，比微信视频的画质还要差，具体可见我发的视频，像素格子肉眼可见。虽然软件内自带了 **GFPGAN** 来做人脸清晰化处理，但加了超分算法后，一方面处理速度下降，另一方面超分后的人脸会显得失真，尤其在牙齿等区域会显得非常不稳定，时而 2 门牙，时而 3 门牙，不停变化。

DFL 的清晰度理论上可以做到很高，比如《流浪地球》里的吴京和刘德华年轻化就是 DFL（DeepFaceLab）配合后期实现的。不过理论归理论，实践中考虑模型训练时间和成本，一般使用 256x256 分辨率的人脸模型，远看可以做到毫无破绽，但近距离特写还是会露馅。此外，模型的训练方法和技巧也会直接影响训练效果。

## 逼真度

- **deep-live-cam:** ★★★★☆
- **deepfacelive:** ★★★★☆

在这方面，两者可以打平手，前提是 DFL 模型训练得比较到位。

两者都能较好还原目标人物的特征，但也都不能改变脸型，因此当脸型差异过大时，逼真度会明显下降。

## 抗遮挡

- **deep-live-cam:** ★☆☆☆☆
- **deepfacelive:** ★★★★☆

DLC 可以说完全没做这方面的优化，稍微挡住一点画面就露馅。我在视频里也有演示。

DFL 在这方面的优化做得比较好，在训练模型时，可以结合 **Xseg** 遮挡算法进行遮挡区域的学习，使得实际推理时能自行预测出被遮挡的部分进行蒙版处理。

## 光影适配度

- **deep-live-cam:** ★★★★★
- **deepfacelive:** ★★★☆☆-★★★★★

这是 DLC 的另一个大优势，下方 GIF 图有展示，在环境光源变化时，模型可以做到跟随光影变化而变化。

DFL 也能做到这个效果，但对模型训练要求就高了很多，需要拿目标人物大量不同光影角度的素材进行训练。如果训练素材里的光影丰富度不足，就会产生类似面具感的瑕疵，面部的光影和环境会有色差。

## 下载链接

**Windows 环境整合包下载地址：**  
[下载链接](https://pan.baidu.com/s/1GmFBm3NXDN-rXTbACy74kg?pwd=u98q)  
**提取码：** u98q

直接解压，双击启动 `.exe` 即可使用。

### 硬件要求

需有支持 CUDA 的 NVIDIA 显卡。

如果硬件不符合要求也不用急，软件也有对应的 Mac 版本和 Windows 非 N 卡版本。我还没做成整合包，有需求的请先点赞评论，如果人数多的话我再考虑制作其他硬件下的整合包。

# Deep-Live-Cam vs. DeepFaceLive: A Comparative Evaluation

Recently, the **deep-live-cam** project (hereinafter referred to as **DLC**) has gained significant attention. It allows real-time face swapping with just one image, without the need to train your own model; you can use it straight out of the box. At the end of this article, I will provide a download link for the local running package.

## Features Offered by the Software

- Image face swapping
- Real-time face swapping using a camera
- Face swapping with face clarification

There is also a well-known project called **DeepFaceLive** for real-time face swapping. Coincidentally, I am also a participant in the DeepFaceLive project, so I have made a comparative evaluation of these two similar software programs, focusing on several aspects.

## Ease of Use

- **deep-live-cam:** ★★★★☆
- **deepfacelive:** ★☆☆☆☆

In this aspect, there is no doubt that DLC wins. DLC requires no training and can perform face swapping directly with just one photo. On the other hand, DeepFaceLive (hereinafter referred to as **DFL**) requires a separate model to be trained for each face to be swapped due to different algorithms, making the process much more cumbersome. Training can take anywhere from days to weeks, which is not suitable for users looking for quick and fun results.

Although the DLC algorithm makes it easier to use, the current user interface and operation process are still quite primitive, with many bugs, so I can only give it 4 stars.

## Feature Richness

- **deep-live-cam:** ★☆☆☆☆
- **deepfacelive:** ★★★★☆

While DLC is simple, it also lacks many controls, such as input sources, color control, edge blending, face size control, and multi-face filtering, which are essential for practical commercial use. It is even less functional than the **Rope** project, which uses the same algorithm but offers more features.

DFL is more mature and has a wider range of functionalities.

## Clarity

- **deep-live-cam:** ★☆☆☆☆-★★★☆☆
- **deepfacelive:** ★★★☆☆-★★★★★

The clarity of DLC is one of its major weaknesses, as its base model has a face resolution of only 128x128, which is worse than the quality of WeChat video calls. You can see this clearly in the video I posted, with visible pixelation. Although the software includes **GFPGAN** for face clarification, the processing speed decreases with the super-resolution algorithm, and the upscaled faces often appear distorted, especially in areas like teeth, where they can look unstable—sometimes showing two front teeth and sometimes three, constantly changing.

In theory, DFL can achieve very high clarity. For example, the youthful appearances of Wu Jing and Andy Lau in "The Wandering Earth" were achieved using DFL (DeepFaceLab) in combination with post-production. However, in practice, considering the time and cost of model training, a resolution of 256x256 is generally used, which can look flawless from a distance but may show flaws in close-ups. Additionally, the training methods and techniques will directly affect the training results.

## Realism

- **deep-live-cam:** ★★★★☆
- **deepfacelive:** ★★★★☆

In this aspect, both can be considered equal, provided that the DFL model is well-trained.

Both can effectively replicate the target person's features, but neither can change the face shape. Therefore, when there is a significant difference in face shape, the realism will noticeably decrease.

## Occlusion Resistance

- **deep-live-cam:** ★☆☆☆☆
- **deepfacelive:** ★★★★☆

DLC has not optimized this aspect at all; even a slight obstruction in the frame reveals the swap. I demonstrated this in the video.

DFL has made good optimizations in this regard. When training the model, it can incorporate the **Xseg** occlusion algorithm to learn about occluded areas, allowing it to predict and mask those areas during actual inference.

## Light and Shadow Adaptability

- **deep-live-cam:** ★★★★★
- **deepfacelive:** ★★★☆☆-★★★★★

This is another significant advantage of DLC. The GIF below demonstrates that the model can adapt to changes in ambient light.

DFL can also achieve this effect, but it requires much higher training standards. It needs a large amount of material with different lighting angles of the target person for training. If the training materials lack sufficient lighting variety, it can result in a mask-like flaw, with discrepancies between the face's lighting and the environment.

## Download Link

**Download link for the Windows environment integration package:**  
[Download Here](https://pan.baidu.com/s/1GmFBm3NXDN-rXTbACy74kg?pwd=u98q)  
**Extract code:** u98q

Simply unzip and double-click the `.exe` file to use it.

### Hardware Requirements

Must have an NVIDIA graphics card that supports CUDA.

If your hardware does not meet the requirements, don't worry. The software also has corresponding versions for Mac and non-NVIDIA Windows. I haven't created an integration package for those yet, but if there's demand, please like and comment. If there are enough requests, I will consider making integration packages for other hardware.
