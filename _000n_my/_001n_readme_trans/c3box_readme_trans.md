<p align="center">
<img src="../../resources/logo.png"  width="800px">
</p>

<p align="center">
  <a href="#-项目简介">🎉项目简介</a> •
  <a href="#-已复现的方法">🌟已复现的方法</a> •
  <a href="#-最新动态">📰最新动态</a> •
  <a href="#%EF%B8%8F-使用方法">☄️使用方法</a> •
  <a href="#-致谢">👨‍🏫致谢</a> •
  <a href="#-联系方式">🤗联系方式</a>
</p>

---

## 🎉 项目简介

欢迎使用 C3Box——一个基于 CLIP 的持续学习工具箱 <a href="https://arxiv.org/abs/2601.20852">[论文]</a>。一方面，C3Box 实现了若干先进的基于 CLIP 的类增量学习算法，例如 CLG-CBM、PROOF 和 ENGINE。另一方面，C3Box 也对典型的类增量学习算法（*例如* FOSTER 和 MEMO）以及基于 ViT 的类增量学习算法（*例如* L2P 和 DualPrompt）进行了适配，以评估它们的有效性。

**如果您在工作中使用了本仓库的任何内容，请引用以下参考文献条目：**

    @article{sun2026c3box,
        title={C3Box: A CLIP-based Class-Incremental Learning Toolbox},
        author={Sun, Hao and Zhou, Da-Wei},
        journal={arXiv preprint arXiv:2601.20852},
        year={2026}
    }
    
    @inproceedings{zhou2024continual,
        title={Continual learning with pre-trained models: A survey},
        author={Zhou, Da-Wei and Sun, Hai-Long and Ning, Jingyi and Ye, Han-Jia and Zhan, De-Chuan},
        booktitle={IJCAI},
        pages={8363-8371},
        year={2024}
    }

    @article{zhou2024class,
        author = {Zhou, Da-Wei and Wang, Qi-Wei and Qi, Zhi-Hong and Ye, Han-Jia and Zhan, De-Chuan and Liu, Ziwei},
        title = {Class-Incremental Learning: A Survey},
        journal={IEEE Transactions on Pattern Analysis and Machine Intelligence},
        volume={46},
        number={12},
        pages={9851--9873},
        year = {2024}
    }

## 📰 最新动态

- [2026-01]🌟 C3Box 初始版本已发布 <a href="https://arxiv.org/abs/2601.20852">[论文]</a>。
- [2026-01]🌟 代码已发布。

## 🌟 已复现的方法

- `FineTune`：仅在新任务上更新参数的基线方法。
- `ZS-CLIP`：作为预训练 CLIP 在下游任务上的性能基准的基线方法。
- `FOSTER`：用于类增量学习的特征增强与压缩。ECCV 2022 [[论文](https://arxiv.org/abs/2204.04662)]
- `MEMO`：一个模型还是 603 个样本：迈向内存高效的类增量学习。ICLR 2023 Spotlight [[论文](https://openreview.net/forum?id=S07feAlQHgM)]
- `L2P`：学习用于持续学习的提示。CVPR 2022 [[论文](https://arxiv.org/abs/2112.08654)]
- `DualPrompt`：DualPrompt：用于无回放持续学习的互补提示。ECCV 2022 [[论文](https://arxiv.org/abs/2204.04799)]
- `CODA-Prompt`：CODA-Prompt：用于无回放持续学习的持续分解式注意力提示。CVPR 2023 [[论文](https://arxiv.org/abs/2211.13218)]
- `Ease`：用于基于预训练模型的类增量学习的可扩展子空间集成。CVPR 2024 [[论文](https://arxiv.org/abs/2403.12030)]
- `SimpleCIL`：重新审视基于预训练模型的类增量学习：泛化性与适应性就是你所需要的一切。IJCV 2024 [[论文](https://arxiv.org/abs/2303.07338)]
- `APER`：重新审视基于预训练模型的类增量学习：泛化性与适应性就是你所需要的一切。IJCV 2024 [[论文](https://arxiv.org/abs/2303.07338)]
- `TUNA`：为基于预训练模型的类增量学习整合任务专用适配器与通用适配器。ICCV 2025 [[论文](https://arxiv.org/abs/2508.08165)]
- `RAPF`：使用 CLIP 的类增量学习：自适应表示调整与参数融合。ECCV 2024 [[论文](https://arxiv.org/abs/2407.14143)]
- `MG-CLIP`：弥合差距：在基于 CLIP 的持续学习中保留并补偿模态差距。ICCV 2025 [[论文](https://arxiv.org/abs/2507.09118)]
- `CLG-CBM`：用于可解释持续学习的语言引导概念瓶颈模型。CVPR 2025 [[论文](https://arxiv.org/abs/2503.23283)]
- `PROOF`：视觉语言模型的无遗忘学习。TPAMI 2025 [[论文](https://arxiv.org/abs/2305.19270)]
- `ENGINE`：用于基于 CLIP 的类增量学习的外部知识注入。ICCV 2025 [[论文](https://arxiv.org/abs/2503.08510)]
- `BOFA`：BOFA：用于基于 CLIP 的类增量学习的桥接层正交低秩融合。AAAI 2026 [[论文](https://arxiv.org/abs/2511.11421)]

## ☄️ 使用方法

### 🕹️ 克隆仓库

克隆此 GitHub 仓库：

```
git clone https://github.com/LAMDA-CL/C3Box
cd LAMDA-C3Box
```

### 🗂️ 依赖项

1. [torch 2.0.1](https://github.com/pytorch/pytorch)
2. [torchvision 0.15.2](https://github.com/pytorch/vision)
3. [timm 0.6.12](https://github.com/huggingface/pytorch-image-models)
4. [tqdm](https://github.com/tqdm/tqdm)
5. [numpy](https://github.com/numpy/numpy)
6. [scipy](https://github.com/scipy/scipy)
7. [easydict](https://github.com/makinacorpus/easydict)
8. [open-clip 2.17.1](https://github.com/mlfoundations/open_clip/releases/tag/v2.17.1)



### 🔑 运行实验

1. 编辑 `[MODEL NAME].json` 文件，设置全局配置和超参数。
2. 运行：

    ```bash
    python main.py --config=./exps/[MODEL NAME].json
    ```

3. `超参数`

    使用 C3Box 时，可以在相应的 JSON 文件中编辑全局参数和算法专用超参数。

    这些参数包括：

   - **model_name**：模型名称应从上述 11 种方法中选择，即 `finetune`、`zs_clip`、`foster`、`memo`、`simplecil`、`l2p`、`dual`、`coda`、`ease`、`aper`、`tuna`、`rapf`、`clg_cbm`、`mg_clip`、`proof`、`engine` 和 `bofa`。
   - **init_cls**：初始增量阶段的类别数量。由于类增量学习配置包含多种初始类别数量不同的设置，因此本框架支持以多种方式定义初始阶段。
   - **increment**：第 $i$ 个增量阶段（$i$ > 1）的类别数量。默认情况下，所有增量阶段的类别数量均相同。
   - **backbone_type**：增量模型的骨干网络。对于采用 **ViT-B/16** 的 CLIP，可以从 Timm 库提供的多种预训练模型中选择，例如 **LAION-400M** 和 **OpenAI**。
   - **seed**：用于打乱类别顺序的随机种子。按照 iCaRL 的基准设置，其默认值为 1993。
   - **fixed_memory**：布尔参数。设置为 true 时，模型会为每个类别保留固定数量的存储样本；设置为 false 时，模型会为每个类别采用动态的存储分配方式。
   - **memory_size**：增量学习过程中保留的样本总数。如果将 `fixed_memory` 设置为 false，假设当前阶段共有 $K$ 个类别，则模型会为每个类别保留 $\left[\frac{{memory-size}}{K}\right]$ 个样本。**ZS-CLIP、SimpleCIL、ADAM、EASE、TUNA、CLG_CBM、MG_CLIP、ENGINE 和 BOFA 不需要样本。** 因此，与样本有关的参数不会被使用。
   - **memory_per_class**：如果将 `fixed memory` 设置为 true，模型会为每个类别保留固定数量的 `memory_per_class` 个样本。

### 🔎 数据集

我们已经对以下数据集进行了预处理：

- **CIFAR100**：代码会自动下载该数据集。
- **CUB200**：Google Drive：[链接](https://drive.google.com/file/d/1XbUpnWpJPnItt5zQ6sHJnsjPncnNLvWb/view?usp=sharing)，或 OneDrive：[链接](https://entuedu-my.sharepoint.com/:u:/g/personal/n2207876b_e_ntu_edu_sg/EVV4pT9VJ9pBrVs2x0lcwd0BlVQCtSrdbLVfhuajMry-lA?e=L6Wjsc)
- **ImageNet-R**：Google Drive：[链接](https://drive.google.com/file/d/1SG4TbiL8_DooekztyCVK8mPmfhMo8fkR/view?usp=sharing)，或 Onedrive：[链接](https://entuedu-my.sharepoint.com/:u:/g/personal/n2207876b_e_ntu_edu_sg/EU4jyLL29CtBsZkB6y-JSbgBzWF5YHhBAUz1Qw8qM2954A?e=hlWpNW)
- **ObjectNet**：Onedrive：[链接](https://entuedu-my.sharepoint.com/:u:/g/personal/n2207876b_e_ntu_edu_sg/EZFv9uaaO1hBj7Y40KoCvYkBnuUZHnHnjMda6obiDpiIWw?e=4n8Kpy)。如果文件过大而无法下载，也可以参考该[文件列表](https://drive.google.com/file/d/147Mta-HcENF6IhZ8dvPnZ93Romcie7T6/view?usp=sharing)和处理[代码](https://github.com/zhoudw-zdw/RevisitingCIL/issues/2#issuecomment-2280462493)。
- **Cars**：Google Drive：[链接](https://drive.google.com/file/d/1D8ReAuOPenWi6SMNUrOZhbm6ViyhDHbL/view?usp=sharing  )，或 OneDrive：[链接](https://njuedu-my.sharepoint.cn/:u:/g/personal/ky2409911_365_nju_edu_cn/EbT1XAstg51Mpy82uHM0D2EBJLrtzmr_V64jeBRjqyyTnQ?e=h6g1rM)
- **UCF**：Google Drive：[链接](https://drive.google.com/file/d/1Ng4w310_VDqpKbc7eYaumXTOiDxI02Wc/view?usp=sharing)，或 OneDrive：[链接](https://njuedu-my.sharepoint.cn/:u:/g/personal/ky2409911_365_nju_edu_cn/EU2qHQXjASdLh1jIl6ihZmcB6G2KvqmSw-sTlZKDE6xPbg?e=7ezvTr)
- **Aircraft**：Google Drive：[链接](https://drive.google.com/file/d/1xI5r1fU0d6Nff51HuOo5w-e4sGEP46Z2/view?usp=drive_link)，或 OneDrive：[链接](https://njuedu-my.sharepoint.cn/:u:/g/personal/ky2409911_365_nju_edu_cn/ETVliZnmPY9AvZZgcFFJ6jMB2c7TRvcq7-gso2Aqvdl_VQ?e=pWXqdP)
- **Food**：Google Drive：[链接](https://drive.google.com/file/d/1rupzXpwrbxki4l-RVmsRawhz1Cm0lDY5/view?usp=drive_link)，或 OneDrive：[链接](https://njuedu-my.sharepoint.cn/:u:/g/personal/ky2409911_365_nju_edu_cn/Eb4xfptD4L5Egus-SiYxrIcBDH1VewLGp4kzyACGF_Na_w?e=duA3Ia)
- **SUN**：OneDrive：[链接](https://njuedu-my.sharepoint.cn/:u:/g/personal/ky2409911_365_nju_edu_cn/EcQq1-1pFulKstYtdknB4O8BGo0hnlDRarAwB4wFEgkx0Q?e=YZ0xYV)
- **TV100**：OneDrive：[链接](https://njuedu-my.sharepoint.cn/:u:/r/personal/ky2409911_365_nju_edu_cn/Documents/TV100/TV100.zip?csf=1&web=1&e=XNpitj)


> 这些子集均采样自原始数据集。请注意，我无权分发这些数据集。如果这种分发方式违反了许可协议，我将改为提供文件名。

使用 `CIFAR100` 以外的数据集进行训练时，需要在 `utils/data.py` 中指定数据集所在的文件夹。

```python
    def download_data(self):
        assert 0,"You should specify the folder of your dataset"
        train_dir = '[DATA-PATH]/train/'
        test_dir = '[DATA-PATH]/val/'
```

## 👨‍🏫 致谢

感谢以下代码仓库为我们的工作提供了有用的组件和函数。

- [PyCIL](https://github.com/G-U-N/PyCIL)
- [PILOT](https://github.com/LAMDA-CL/LAMDA-PILOT)


## 🤗 联系方式

如有任何问题，欢迎通过创建 Issue 提议新功能，或联系作者：**Hao Sun**（[sunhao@lamda.nju.edu.cn](mailto:sunhl@lamda.nju.edu.cn)）和 **Da-Wei Zhou**（[zhoudw@lamda.nju.edu.cn](mailto:zhoudw@lamda.nju.edu.cn)）。祝您使用愉快。
