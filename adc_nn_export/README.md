# ADC 神经网络校准项目导出

这里是本次对话生成的完整项目文件。

- [下载完整项目 ZIP](./ADC_NN_COMPLETE_EXPORT.zip?raw=true)：37 个文件，约 1.9 MB，包含 MATLAB 代码、CSV 模板、交接文档、PDF/HTML 图文说明、配图及参考验证脚本。
- [在线阅读交接 Markdown](./CODEX_HANDOFF.md)：迁移到另一个 Codex 环境时先读。
- [查看图文说明 PDF](./NN_training_guide.pdf)：面向 AI 初学者，9 页。
- [SHA-256 校验值](./SHA256SUMS.txt)。

## 开始使用

1. 下载并解压 ZIP。
2. 阅读 `adc_nn_matlab/CODEX_HANDOFF.md` 和 `README.md`。
3. 在有 Deep Learning Toolbox 的 MATLAB 中进入 `adc_nn_matlab`，运行 `demo_adc_nn`。
4. 准备真实 Virtuoso 保持电压 CSV 后，使用 `manifest_user_496MHz.csv` 和 `run_virtuoso_data`。

代码针对 1 GS/s 差分采样网络，用户首轮输入频率为 496.09375 MHz；近 Nyquist 的实现差异见交接文档。

## 当前验证边界

交付的 `.m` 程序此前只完成语法解析和对应数学流程的 NumPy 检查，尚未在 MATLAB 原生执行，也未训练用户真实电路数据。图文说明中的曲线来自合成参考实验。

本包不包含原论文 PDF、PDK、用户网表或真实电路 CSV。参考检查脚本来自上一运行环境，迁移后请先检查路径与依赖，再运行；不要假设原绝对路径仍有效。
