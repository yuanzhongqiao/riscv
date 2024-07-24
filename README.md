<div class="Box-sc-g0xbh4-0 bJMeLZ js-snippet-clipboard-copy-unpositioned" data-hpc="true"><article class="markdown-body entry-content container-lg" itemprop="text"><div class="markdown-heading" dir="auto"><h1 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">RISC-V 核心</font></font></h1><a id="user-content-risc-v-core" class="anchor" aria-label="永久链接：RISC-V 核心" href="#risc-v-core"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Github：</font></font><a href="http://github.com/ultraembedded/riscv"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">http://github.com/ultraembedded/riscv</font></font></a></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">用 Verilog 编写的 32 位 RISC-V 内核和支持 RV32IM 的指令集模拟器。</font></font><br><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">
该内核已针对联合仿真模型进行了测试，并在 FPGA 上进行了测试。</font></font></p>
<p dir="auto"><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">对于具有分支预测功能的更高性能双发射 CPU，请参阅我的最新 RISC-V 核心；</font></font></strong>
<a href="http://github.com/ultraembedded/biriscv"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">http://github.com/ultraembedded/biriscv</font></font></a></p>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">概述</font></font></h2><a id="user-content-overview" class="anchor" aria-label="固定链接：概述" href="#overview"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><a target="_blank" rel="noopener noreferrer" href="/ultraembedded/riscv/blob/master/doc/overview.png"><img src="/ultraembedded/riscv/raw/master/doc/overview.png" alt="" style="max-width: 100%;"></a></p>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">特征</font></font></h2><a id="user-content-features" class="anchor" aria-label="固定链接：功能" href="#features"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ul dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">32 位 RISC-V ISA CPU 内核。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持RISC-V整数（I）、乘法和除法（M）以及CSR指令（Z）扩展（RV32IMZicsr）。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持用户、主管和机器模式特权级别。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">基本 MMU 支持 - 能够使用原子（RV-A）SW 仿真启动 Linux。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">实现基本 ISA 规范</font></font><a href="https://github.com/ultraembedded/riscv/tree/master/doc/riscv_isa_spec.pdf"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">v2.1</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">和特权 ISA 规范</font></font><a href="https://github.com/ultraembedded/riscv/tree/master/doc/riscv_privileged_spec.pdf"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">v1.11</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">使用</font></font><a href="https://github.com/google/riscv-dv"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Google 的 RISCV-DV</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">随机指令序列与</font></font><a href="https://github.com/ultraembedded/exactstep"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">C++ ISA 模型</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">进行联合仿真进行验证。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持指令/数据缓存、AXI总线接口或紧密耦合的存储器。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">可配置的管道阶段数量和结果转发选项。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">可合成的 Verilog 2001、Verilator 和 FPGA 友好。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Coremark：   </font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">2.94 CoreMark/MHz</font></font></strong></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Dhrystone：</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">1.25 DMIPS/MHz</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">（“合法编译选项”/每次迭代 337 条指令）</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">想要更高的性能（</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">4.1CM/MHz</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;"> / </font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">1.9DMIPS/MHz</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">） - 请参阅</font></font><a href="http://github.com/ultraembedded/biriscv"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">我改进的核心</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></li>
</ul>
<div class="markdown-heading" dir="auto"><h4 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">配置</font></font></h4><a id="user-content-configuration" class="anchor" aria-label="固定链接：配置" href="#configuration"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<markdown-accessiblity-table data-catalyst=""><table>
<thead>
<tr>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">参数名称</font></font></th>
<th align="center"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">有效范围</font></font></th>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">描述</font></font></th>
</tr>
</thead>
<tbody>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持_超级</font></font></td>
<td align="center"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">1/0</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">启用主管/用户权限级别。</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持 MMU</font></font></td>
<td align="center"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">1/0</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">启用基本内存管理单元。</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持多路复用 (SUPPORT_MULDIV)</font></font></td>
<td align="center"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">1/0</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">启用硬件乘法/除法（RV-M）。</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持加载绕过</font></font></td>
<td align="center"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">1/0</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持加载结果绕行路径。</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持多路复用 (MUL_BYPASS)</font></font></td>
<td align="center"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">1/0</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持多结果旁路路径。</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持_REGFILE_XILINX</font></font></td>
<td align="center"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">1/0</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持Xilinx优化的寄存器文件。</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">额外解码阶段</font></font></td>
<td align="center"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">1/0</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">额外的解码管道阶段可改善时序。</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">内存缓存地址</font></font></td>
<td align="center"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">32'h0-32'hffffffff</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">最低可缓存内存地址。</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">内存缓存地址 (MEM_CACHE_ADDR)</font></font></td>
<td align="center"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">32'h0-32'hffffffff</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">最高可缓存内存地址。</font></font></td>
</tr>
</tbody>
</table></markdown-accessiblity-table>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">目录</font></font></h2><a id="user-content-directories" class="anchor" aria-label="永久链接：目录" href="#directories"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<markdown-accessiblity-table data-catalyst=""><table>
<thead>
<tr>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">姓名</font></font></th>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">内容</font></font></th>
</tr>
</thead>
<tbody>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">核心/riscv</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">RISC-V 流水线 RV32IM CPU 核心 (Verilog)</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">isa_sim</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">指令集模拟器（C）</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">top_tcm_axi/src_v</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">具有 64KB DP-RAM 和 AXI 接口的示例</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">top_tcm_axi/tb</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">核心的 System-C 测试平台</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">top_cache_axi/src_v</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">具有指令和数据缓存的示例实例。</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">top_cache_axi/tb</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">核心的 System-C 测试平台</font></font></td>
</tr>
</tbody>
</table></markdown-accessiblity-table>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">示例核心实例（带 TCM 内存）</font></font></h2><a id="user-content-example-core-instance-with-tcm-memory" class="anchor" aria-label="永久链接：示例核心实例（带 TCM 内存）" href="#example-core-instance-with-tcm-memory"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">顶部（top_tcm_axi/src_v/riscv_tcm_top.v）包含；</font></font></p>
<ul dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">实例化上述核心之一，添加 RAM 和标准总线接口。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">64KB双端口RAM用于（I/D代码和数据）。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">AXI4 从属端口用于加载 RAM、DMA 访问等（包括支持突发访问）。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">AXI4-Lite 主端口用于 CPU 访问外围设备。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">将 CPU 核心单独复位至双端口 RAM / AXI 接口（以允许在 CPU 复位取消断言之前加载程序代码）。</font></font></li>
</ul>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">内存映射</font></font></h3><a id="user-content-memory-map" class="anchor" aria-label="永久链接：记忆地图" href="#memory-map"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<markdown-accessiblity-table data-catalyst=""><table>
<thead>
<tr>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">范围</font></font></th>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">描述</font></font></th>
</tr>
</thead>
<tbody>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">0x0000_0000—0x0000_ffff</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">64KB TCM 内存</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">0x0000_2000</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">启动地址（可配置，参见 RISCV_BOOT_ADDRESS）</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">0x8000_0000——0xffff_ffff</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">外设地址空间（来自 AXI4-L 端口）</font></font></td>
</tr>
</tbody>
</table></markdown-accessiblity-table>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">接口</font></font></h3><a id="user-content-interfaces" class="anchor" aria-label="永久链接：接口" href="#interfaces"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<markdown-accessiblity-table data-catalyst=""><table>
<thead>
<tr>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">姓名</font></font></th>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">描述</font></font></th>
</tr>
</thead>
<tbody>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">clk_i</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">时钟输入</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">rst_i</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">异步复位，高电平有效。复位内存/AXI 接口。</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">rst_cpu_i</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">异步复位，高电平有效。复位 CPU 内核（不包括 AXI/内存）。</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">axi_t_*</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">AXI4 从属接口用于访问 64KB TCM 内存。</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">axi_i_*</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">AXI4-Lite 主接口用于 CPU 访问外设。</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">内参</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">高电平有效中断输入（用于连接外部中断控制器）。</font></font></td>
</tr>
</tbody>
</table></markdown-accessiblity-table>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">试验台</font></font></h3><a id="user-content-testbench" class="anchor" aria-label="永久链接：测试台" href="#testbench"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">提供了基于基本 System-C / Verilator 的核心测试平台。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">依赖项；</font></font></p>
<ul dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">海湾合作委员会</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">制作</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">诽谤</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">System-C（使用 SYSTEMC_HOME 指定路径）</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Verilator（使用 VERILATOR_SRC 指定路径）</font></font></li>
</ul>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">建立测试平台；</font></font></p>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>cd top_tcm_axi/tb
make
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="cd top_tcm_axi/tb
make" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">运行提供的测试可执行文件；</font></font></p>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>cd top_tcm_axi/tb
make run
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="cd top_tcm_axi/tb
make run" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">核心实例示例（带缓存）</font></font></h2><a id="user-content-example-core-instance-with-caches" class="anchor" aria-label="永久链接：核心实例示例（带缓存）" href="#example-core-instance-with-caches"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">顶部（top_cache_axi/src_v/riscv_top.v）包含；</font></font></p>
<ul dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">实例化上述核心之一，添加 RAM 和标准总线接口。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">16KB 2 路组相联指令缓存</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">16KB 双向组相联数据缓存，具有写回和写入时分配功能。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">2 x AXI4 主端口用于 CPU 访问指令/数据/外围设备。</font></font></li>
</ul>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">接口</font></font></h3><a id="user-content-interfaces-1" class="anchor" aria-label="永久链接：接口" href="#interfaces-1"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<markdown-accessiblity-table data-catalyst=""><table>
<thead>
<tr>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">姓名</font></font></th>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">描述</font></font></th>
</tr>
</thead>
<tbody>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">clk_i</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">时钟输入</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">rst_i</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">异步复位，高电平有效。复位内存/AXI 接口。</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">axi_i_*</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">AXI4 主接口，用于 CPU 访问指令存储器。</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">axi_d_*</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">AXI4 主接口，用于 CPU 访问数据/外围存储器。</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">内参</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">高电平有效中断输入（用于连接外部中断控制器）。</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">重置向量</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">引导向量。</font></font></td>
</tr>
</tbody>
</table></markdown-accessiblity-table>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">执行示例</font></font></h2><a id="user-content-execution-example" class="anchor" aria-label="永久链接：执行示例" href="#execution-example"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><a target="_blank" rel="noopener noreferrer" href="/ultraembedded/riscv/blob/master/doc/core_exec.png"><img src="/ultraembedded/riscv/raw/master/doc/core_exec.png" alt="" style="max-width: 100%;"></a></p>
</article></div>
