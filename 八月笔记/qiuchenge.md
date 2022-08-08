# runtime

## 测试
### 测试环境
* 内网, 远程青岛的电脑/在北京弄一台内网的电脑装上vivado
### 测试流程
1. vivado 下载bitstream
2. sdk 选中工程 run as system debugger
### 根据需要选择版本工程版本和配置
* 单张图片 与 连续多张 -> USE_PCIE
* 硬件单双核:
  * 单核单ddr -> test_app, hw
  * 双核单ddr(可能会卡住) -> test_app_core_v2(优化后) 或 test_app_2_core, hw_2core
  * 双核双ddr -> test_app_2core_2ddr, hw_2core_2ddr
## 遗留问题
* 卡住, 加上print就好了, 不能确定时runtime还是硬件的问题
  * 单核重复推理开启pingpong的情况下
  * 多核卡住不分第几次, 应该和ddr有关
## 读代码
后续有需要时能够修改

# compiler
* 读懂代码, 为了后续优化时可以修改