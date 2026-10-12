# TH08 Presentation Lab

独立诊断工作台使用锁定 common 的 RuntimeDriverV1、ObservationAdapterV1 与 controller。生产 Runtime 不暴露诊断控制。

TH08 有固定步、只绘制扫描和 Replay 遍历适配。各类结果依其实际观察覆盖解释。

先在环境中明确 `EMSDK` 和 `EAGLER_FONT_ROOT`，再从本游戏根目录执行：

```text
node portable/presentation-lab/start-lab.mjs --build --port=8132
```

只启动已有诊断产物时省略 `--build`。服务只监听本机，不自动打开浏览器。TH08 可用 --snapshot=NAME 选择合法快照名。

固定步必须推进全部真实所有者；只绘制不能改变下一步输入、RNG、计时器和音频。原版绘制参考独立于待测插值。报告记录源码、工具链、输入、代次和覆盖；诊断 WASM 不进入正式 Runtime Release。

共同约定见锁定依赖的 `testkit/presentation-lab/`。本轮普通构建通过，不等同于 Lab 构建或物理手机验收。
