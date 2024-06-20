
# Pystats results

- benchmark: richards
- fork: python
- ref: 15fbd53ba96be4b6a5abd94ceada684493c36bdd
- commit hash: 15fbd53
- commit date: 2024-04-20T17:46:52+01:00

## Execution counts

<details>
<summary> Execution counts for Tier 1 instructions. </summary>


The "miss ratio" column shows the percentage of times the instruction
executed that it deoptimized. When this happens, the base unspecialized
instruction is not counted.

<table>
<thead>
<tr>
<th align="left">Name</th>
<th align="right">Count</th>
<th align="right">Self</th>
<th align="right">Cumulative</th>
<th align="right">Miss ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">500,104,940</td>
<td align="right">25.3%</td>
<td align="right">25.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">191,633,760</td>
<td align="right">9.7%</td>
<td align="right">35.0%</td>
<td align="right">24.4%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">145,322,140</td>
<td align="right">7.3%</td>
<td align="right">42.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">118,276,000</td>
<td align="right">6.0%</td>
<td align="right">48.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">116,879,840</td>
<td align="right">5.9%</td>
<td align="right">54.2%</td>
<td align="right">14.8%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">105,058,400</td>
<td align="right">5.3%</td>
<td align="right">59.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">78,259,680</td>
<td align="right">4.0%</td>
<td align="right">63.5%</td>
<td align="right">31.2%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">78,066,240</td>
<td align="right">3.9%</td>
<td align="right">67.4%</td>
<td align="right">18.0%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">77,810,600</td>
<td align="right">3.9%</td>
<td align="right">71.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">70,535,560</td>
<td align="right">3.6%</td>
<td align="right">74.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">61,509,760</td>
<td align="right">3.1%</td>
<td align="right">78.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">61,453,660</td>
<td align="right">3.1%</td>
<td align="right">81.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">58,790,760</td>
<td align="right">3.0%</td>
<td align="right">84.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">50,201,900</td>
<td align="right">2.5%</td>
<td align="right">86.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">40,939,840</td>
<td align="right">2.1%</td>
<td align="right">88.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">31,848,160</td>
<td align="right">1.6%</td>
<td align="right">90.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">26,032,100</td>
<td align="right">1.3%</td>
<td align="right">91.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">21,055,700</td>
<td align="right">1.1%</td>
<td align="right">92.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">21,053,080</td>
<td align="right">1.1%</td>
<td align="right">93.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">21,052,720</td>
<td align="right">1.1%</td>
<td align="right">94.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">15,981,120</td>
<td align="right">0.8%</td>
<td align="right">95.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">15,960,880</td>
<td align="right">0.8%</td>
<td align="right">96.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">14,825,020</td>
<td align="right">0.7%</td>
<td align="right">97.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">13,908,380</td>
<td align="right">0.7%</td>
<td align="right">97.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT</td>
<td align="right">13,614,360</td>
<td align="right">0.7%</td>
<td align="right">98.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">8,562,080</td>
<td align="right">0.4%</td>
<td align="right">99.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">8,002,520</td>
<td align="right">0.4%</td>
<td align="right">99.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">3,890,440</td>
<td align="right">0.2%</td>
<td align="right">99.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">3,718,160</td>
<td align="right">0.2%</td>
<td align="right">99.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">1,490,500</td>
<td align="right">0.1%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">745,040</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">692,360</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">10,880</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">9,820</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">7,800</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">7,800</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">5,880</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">4,560</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">3,560</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">3,520</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">2,560</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">1,320</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">960</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">840</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">740</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">640</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">600</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">440</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">360</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">160</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">120</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">120</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">80</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">80</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">80</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">80</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">60</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
</tbody>
</table>


</details>

## Pair counts

<details>
<summary> Pair counts for top 100 opcode pairs </summary>


Pairs of specialized operations that deoptimize and are then followed by
the corresponding unspecialized instruction are not counted as pairs.

<table>
<thead>
<tr>
<th align="left">Pair</th>
<th align="right">Count</th>
<th align="right">Self</th>
<th align="right">Cumulative</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">123,922,100</td>
<td align="right">6.3%</td>
<td align="right">6.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">88,147,120</td>
<td align="right">4.5%</td>
<td align="right">10.7%</td>
</tr>
<tr>
<td align="left">STORE_FAST LOAD_FAST</td>
<td align="right">85,831,920</td>
<td align="right">4.3%</td>
<td align="right">15.1%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE LOAD_FAST</td>
<td align="right">81,292,940</td>
<td align="right">4.1%</td>
<td align="right">19.2%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS RESUME_CHECK</td>
<td align="right">77,801,760</td>
<td align="right">3.9%</td>
<td align="right">23.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">77,793,460</td>
<td align="right">3.9%</td>
<td align="right">27.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST LOAD_FAST</td>
<td align="right">58,272,000</td>
<td align="right">2.9%</td>
<td align="right">30.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE LOAD_FAST</td>
<td align="right">50,838,080</td>
<td align="right">2.6%</td>
<td align="right">32.6%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE RETURN_VALUE</td>
<td align="right">49,544,320</td>
<td align="right">2.5%</td>
<td align="right">35.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST POP_JUMP_IF_NOT_NONE</td>
<td align="right">46,631,040</td>
<td align="right">2.4%</td>
<td align="right">37.4%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE TO_BOOL_BOOL</td>
<td align="right">46,473,860</td>
<td align="right">2.4%</td>
<td align="right">39.8%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK LOAD_FAST</td>
<td align="right">42,868,880</td>
<td align="right">2.2%</td>
<td align="right">41.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST RETURN_VALUE</td>
<td align="right">42,594,640</td>
<td align="right">2.2%</td>
<td align="right">44.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE LOAD_FAST</td>
<td align="right">40,829,780</td>
<td align="right">2.1%</td>
<td align="right">46.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE STORE_FAST</td>
<td align="right">36,437,740</td>
<td align="right">1.8%</td>
<td align="right">48.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE CALL_PY_EXACT_ARGS</td>
<td align="right">34,927,800</td>
<td align="right">1.8%</td>
<td align="right">49.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST POP_JUMP_IF_NONE</td>
<td align="right">31,848,160</td>
<td align="right">1.6%</td>
<td align="right">51.4%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE STORE_FAST</td>
<td align="right">31,693,600</td>
<td align="right">1.6%</td>
<td align="right">53.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE LOAD_FAST</td>
<td align="right">31,245,460</td>
<td align="right">1.6%</td>
<td align="right">54.6%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE LOAD_CONST</td>
<td align="right">30,775,280</td>
<td align="right">1.6%</td>
<td align="right">56.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES LOAD_FAST_LOAD_FAST</td>
<td align="right">28,491,480</td>
<td align="right">1.4%</td>
<td align="right">57.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES LOAD_FAST</td>
<td align="right">28,234,020</td>
<td align="right">1.4%</td>
<td align="right">59.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST LOAD_GLOBAL_MODULE</td>
<td align="right">27,558,080</td>
<td align="right">1.4%</td>
<td align="right">60.4%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT POP_JUMP_IF_FALSE</td>
<td align="right">26,032,100</td>
<td align="right">1.3%</td>
<td align="right">61.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE RETURN_VALUE</td>
<td align="right">25,870,100</td>
<td align="right">1.3%</td>
<td align="right">63.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL ENTER_EXECUTOR</td>
<td align="right">25,418,520</td>
<td align="right">1.3%</td>
<td align="right">64.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE LOAD_CONST</td>
<td align="right">24,703,300</td>
<td align="right">1.2%</td>
<td align="right">65.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST STORE_FAST</td>
<td align="right">24,402,240</td>
<td align="right">1.2%</td>
<td align="right">66.8%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL POP_JUMP_IF_FALSE</td>
<td align="right">24,051,660</td>
<td align="right">1.2%</td>
<td align="right">68.0%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR RETURN_VALUE</td>
<td align="right">21,564,460</td>
<td align="right">1.1%</td>
<td align="right">69.1%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK LOAD_CONST</td>
<td align="right">21,321,080</td>
<td align="right">1.1%</td>
<td align="right">70.2%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE ENTER_EXECUTOR</td>
<td align="right">21,057,400</td>
<td align="right">1.1%</td>
<td align="right">71.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL POP_JUMP_IF_TRUE</td>
<td align="right">21,055,600</td>
<td align="right">1.1%</td>
<td align="right">72.3%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN LOAD_FAST</td>
<td align="right">21,053,080</td>
<td align="right">1.1%</td>
<td align="right">73.4%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE LOAD_FAST</td>
<td align="right">21,052,800</td>
<td align="right">1.1%</td>
<td align="right">74.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">21,052,760</td>
<td align="right">1.1%</td>
<td align="right">75.5%</td>
</tr>
<tr>
<td align="left">STORE_FAST LOAD_GLOBAL_BUILTIN</td>
<td align="right">21,052,640</td>
<td align="right">1.1%</td>
<td align="right">76.6%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE TO_BOOL_BOOL</td>
<td align="right">21,052,640</td>
<td align="right">1.1%</td>
<td align="right">77.6%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE CALL_ISINSTANCE</td>
<td align="right">21,052,640</td>
<td align="right">1.1%</td>
<td align="right">78.7%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">19,171,920</td>
<td align="right">1.0%</td>
<td align="right">79.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES CALL_PY_EXACT_ARGS</td>
<td align="right">17,874,140</td>
<td align="right">0.9%</td>
<td align="right">80.6%</td>
</tr>
<tr>
<td align="left">COPY LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">15,960,680</td>
<td align="right">0.8%</td>
<td align="right">81.4%</td>
</tr>
<tr>
<td align="left">SWAP STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">15,960,680</td>
<td align="right">0.8%</td>
<td align="right">82.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE POP_JUMP_IF_NOT_NONE</td>
<td align="right">14,878,680</td>
<td align="right">0.8%</td>
<td align="right">82.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST CALL_PY_EXACT_ARGS</td>
<td align="right">14,358,760</td>
<td align="right">0.7%</td>
<td align="right">83.7%</td>
</tr>
<tr>
<td align="left">LOAD_CONST BINARY_OP_ADD_INT</td>
<td align="right">14,134,480</td>
<td align="right">0.7%</td>
<td align="right">84.4%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE POP_TOP</td>
<td align="right">13,878,280</td>
<td align="right">0.7%</td>
<td align="right">85.1%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK LOAD_GLOBAL_MODULE</td>
<td align="right">13,617,600</td>
<td align="right">0.7%</td>
<td align="right">85.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST BINARY_SUBSCR_LIST_INT</td>
<td align="right">13,614,320</td>
<td align="right">0.7%</td>
<td align="right">86.4%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE LOAD_CONST</td>
<td align="right">13,614,080</td>
<td align="right">0.7%</td>
<td align="right">87.1%</td>
</tr>
<tr>
<td align="left">LOAD_CONST STORE_FAST</td>
<td align="right">13,613,120</td>
<td align="right">0.7%</td>
<td align="right">87.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">12,441,600</td>
<td align="right">0.6%</td>
<td align="right">88.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT SWAP</td>
<td align="right">11,158,580</td>
<td align="right">0.6%</td>
<td align="right">89.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE COMPARE_OP_INT</td>
<td align="right">10,964,360</td>
<td align="right">0.6%</td>
<td align="right">89.6%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">10,642,960</td>
<td align="right">0.5%</td>
<td align="right">90.1%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT STORE_FAST</td>
<td align="right">10,638,380</td>
<td align="right">0.5%</td>
<td align="right">90.6%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE COPY</td>
<td align="right">10,413,720</td>
<td align="right">0.5%</td>
<td align="right">91.2%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR POP_JUMP_IF_FALSE</td>
<td align="right">8,706,620</td>
<td align="right">0.4%</td>
<td align="right">91.6%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD LOAD_FAST</td>
<td align="right">8,189,600</td>
<td align="right">0.4%</td>
<td align="right">92.0%</td>
</tr>
<tr>
<td align="left">POP_TOP JUMP_FORWARD</td>
<td align="right">8,184,640</td>
<td align="right">0.4%</td>
<td align="right">92.4%</td>
</tr>
<tr>
<td align="left">LOAD_CONST BINARY_OP</td>
<td align="right">7,997,040</td>
<td align="right">0.4%</td>
<td align="right">92.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE COMPARE_OP_INT</td>
<td align="right">7,922,480</td>
<td align="right">0.4%</td>
<td align="right">93.2%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE LOAD_FAST_LOAD_FAST</td>
<td align="right">7,697,600</td>
<td align="right">0.4%</td>
<td align="right">93.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE LOAD_FAST</td>
<td align="right">7,549,440</td>
<td align="right">0.4%</td>
<td align="right">94.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST LOAD_GLOBAL_MODULE</td>
<td align="right">7,441,200</td>
<td align="right">0.4%</td>
<td align="right">94.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST CALL_PY_EXACT_ARGS</td>
<td align="right">7,440,440</td>
<td align="right">0.4%</td>
<td align="right">94.8%</td>
</tr>
<tr>
<td align="left">LOAD_CONST COMPARE_OP_INT</td>
<td align="right">7,145,040</td>
<td align="right">0.4%</td>
<td align="right">95.1%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE RETURN_VALUE</td>
<td align="right">5,735,000</td>
<td align="right">0.3%</td>
<td align="right">95.4%</td>
</tr>
<tr>
<td align="left">POP_TOP LOAD_FAST</td>
<td align="right">5,719,180</td>
<td align="right">0.3%</td>
<td align="right">95.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST COPY</td>
<td align="right">5,547,120</td>
<td align="right">0.3%</td>
<td align="right">96.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP LOAD_CONST</td>
<td align="right">4,797,140</td>
<td align="right">0.2%</td>
<td align="right">96.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE LOAD_GLOBAL_MODULE</td>
<td align="right">4,465,200</td>
<td align="right">0.2%</td>
<td align="right">96.5%</td>
</tr>
<tr>
<td align="left">LOAD_CONST BINARY_OP_SUBTRACT_INT</td>
<td align="right">3,890,400</td>
<td align="right">0.2%</td>
<td align="right">96.7%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE LOAD_FAST</td>
<td align="right">3,726,400</td>
<td align="right">0.2%</td>
<td align="right">96.8%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE LOAD_GLOBAL_MODULE</td>
<td align="right">3,722,100</td>
<td align="right">0.2%</td>
<td align="right">97.0%</td>
</tr>
<tr>
<td align="left">NOP LOAD_FAST</td>
<td align="right">3,718,080</td>
<td align="right">0.2%</td>
<td align="right">97.2%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE NOP</td>
<td align="right">3,718,080</td>
<td align="right">0.2%</td>
<td align="right">97.4%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE LOAD_FAST_LOAD_FAST</td>
<td align="right">3,240,640</td>
<td align="right">0.2%</td>
<td align="right">97.6%</td>
</tr>
<tr>
<td align="left">STORE_FAST LOAD_CONST</td>
<td align="right">3,200,000</td>
<td align="right">0.2%</td>
<td align="right">97.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT SWAP</td>
<td align="right">3,199,980</td>
<td align="right">0.2%</td>
<td align="right">97.9%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE CALL_PY_EXACT_ARGS</td>
<td align="right">3,199,880</td>
<td align="right">0.2%</td>
<td align="right">98.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES LOAD_GLOBAL_MODULE</td>
<td align="right">3,199,600</td>
<td align="right">0.2%</td>
<td align="right">98.2%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE ENTER_EXECUTOR</td>
<td align="right">3,019,260</td>
<td align="right">0.2%</td>
<td align="right">98.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE TO_BOOL_BOOL</td>
<td align="right">2,978,940</td>
<td align="right">0.2%</td>
<td align="right">98.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST LOAD_CONST</td>
<td align="right">2,976,400</td>
<td align="right">0.2%</td>
<td align="right">98.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT LOAD_FAST</td>
<td align="right">2,975,980</td>
<td align="right">0.2%</td>
<td align="right">98.8%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT LOAD_FAST</td>
<td align="right">2,975,980</td>
<td align="right">0.2%</td>
<td align="right">99.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE LOAD_CONST</td>
<td align="right">2,974,080</td>
<td align="right">0.2%</td>
<td align="right">99.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP SWAP</td>
<td align="right">1,602,320</td>
<td align="right">0.1%</td>
<td align="right">99.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP LOAD_FAST</td>
<td align="right">1,600,040</td>
<td align="right">0.1%</td>
<td align="right">99.3%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE LOAD_GLOBAL_MODULE</td>
<td align="right">1,436,380</td>
<td align="right">0.1%</td>
<td align="right">99.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">882,240</td>
<td align="right">0.0%</td>
<td align="right">99.4%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE LOAD_FAST_LOAD_FAST</td>
<td align="right">756,500</td>
<td align="right">0.0%</td>
<td align="right">99.4%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE STORE_FAST</td>
<td align="right">745,460</td>
<td align="right">0.0%</td>
<td align="right">99.5%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE LOAD_FAST</td>
<td align="right">744,720</td>
<td align="right">0.0%</td>
<td align="right">99.5%</td>
</tr>
<tr>
<td align="left">GET_ITER FOR_ITER_RANGE</td>
<td align="right">744,680</td>
<td align="right">0.0%</td>
<td align="right">99.6%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE GET_ITER</td>
<td align="right">744,620</td>
<td align="right">0.0%</td>
<td align="right">99.6%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE STORE_FAST</td>
<td align="right">744,600</td>
<td align="right">0.0%</td>
<td align="right">99.6%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR FOR_ITER_RANGE</td>
<td align="right">744,540</td>
<td align="right">0.0%</td>
<td align="right">99.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST STORE_SUBSCR_LIST_INT</td>
<td align="right">692,320</td>
<td align="right">0.0%</td>
<td align="right">99.7%</td>
</tr>
</tbody>
</table>


</details>

## Predecessor/Successor Pairs

<details>
<summary> Top 5 predecessors and successors of each Tier 1 opcode. </summary>


This does not include the unspecialized instructions that occur after a
specialized instruction deoptimizes.

### CACHE

<details>
<summary> Successors and predecessors for CACHE </summary>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">620</td>
<td align="right">73.8%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">220</td>
<td align="right">26.2%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_SUBSCR

<details>
<summary> Successors and predecessors for BINARY_SUBSCR </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">80</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT</td>
<td align="right">40</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">20</td>
<td align="right">25.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">20</td>
<td align="right">25.0%</td>
</tr>
</tbody>
</table>


</details>

### EXIT_INIT_CHECK

<details>
<summary> Successors and predecessors for EXIT_INIT_CHECK </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">7,800</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">7,800</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### GET_ITER

<details>
<summary> Successors and predecessors for GET_ITER </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">744,620</td>
<td align="right">99.9%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">300</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">80</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">20</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">20</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">744,680</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">320</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">40</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### INTERPRETER_EXIT

<details>
<summary> Successors and predecessors for INTERPRETER_EXIT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">840</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### NOP

<details>
<summary> Successors and predecessors for NOP </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">3,718,080</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">80</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">3,718,080</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">80</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### POP_TOP

<details>
<summary> Successors and predecessors for POP_TOP </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">13,878,280</td>
<td align="right">99.8%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">21,900</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">2,880</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">2,560</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">2,240</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">8,184,640</td>
<td align="right">58.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">5,719,180</td>
<td align="right">41.1%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">1,920</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">1,680</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">320</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### PUSH_NULL

<details>
<summary> Successors and predecessors for PUSH_NULL </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">480</td>
<td align="right">75.0%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">80</td>
<td align="right">12.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">60</td>
<td align="right">9.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">20</td>
<td align="right">3.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL</td>
<td align="right">560</td>
<td align="right">87.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">80</td>
<td align="right">12.5%</td>
</tr>
</tbody>
</table>


</details>

### RETURN_VALUE

<details>
<summary> Successors and predecessors for RETURN_VALUE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">49,544,320</td>
<td align="right">34.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">42,594,640</td>
<td align="right">29.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">25,870,100</td>
<td align="right">17.8%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">21,564,460</td>
<td align="right">14.8%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">5,735,000</td>
<td align="right">3.9%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">49,544,320</td>
<td align="right">34.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">46,473,860</td>
<td align="right">32.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">31,693,600</td>
<td align="right">21.8%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">13,878,280</td>
<td align="right">9.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">3,726,400</td>
<td align="right">2.6%</td>
</tr>
</tbody>
</table>


</details>

### STORE_SUBSCR

<details>
<summary> Successors and predecessors for STORE_SUBSCR </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">80</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">40</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">20</td>
<td align="right">25.0%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">20</td>
<td align="right">25.0%</td>
</tr>
</tbody>
</table>


</details>

### TO_BOOL

<details>
<summary> Successors and predecessors for TO_BOOL </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">COPY</td>
<td align="right">160</td>
<td align="right">26.7%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">80</td>
<td align="right">13.3%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">80</td>
<td align="right">13.3%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">80</td>
<td align="right">13.3%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">60</td>
<td align="right">10.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">300</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">160</td>
<td align="right">26.7%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">100</td>
<td align="right">16.7%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">40</td>
<td align="right">6.7%</td>
</tr>
</tbody>
</table>


</details>

### UNARY_NOT

<details>
<summary> Successors and predecessors for UNARY_NOT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">9,780</td>
<td align="right">99.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">40</td>
<td align="right">0.4%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">5,660</td>
<td align="right">57.6%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">4,160</td>
<td align="right">42.4%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_OP

<details>
<summary> Successors and predecessors for BINARY_OP </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">7,997,040</td>
<td align="right">99.9%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">2,840</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">2,540</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">40</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">20</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">4,797,140</td>
<td align="right">59.9%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">1,602,320</td>
<td align="right">20.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,600,040</td>
<td align="right">20.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">2,840</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">100</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### BUILD_LIST

<details>
<summary> Successors and predecessors for BUILD_LIST </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">2,560</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">2,520</td>
<td align="right">98.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">40</td>
<td align="right">1.6%</td>
</tr>
</tbody>
</table>


</details>

### CALL

<details>
<summary> Successors and predecessors for CALL </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">560</td>
<td align="right">15.7%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">540</td>
<td align="right">15.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">540</td>
<td align="right">15.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">500</td>
<td align="right">14.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">400</td>
<td align="right">11.2%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">800</td>
<td align="right">22.5%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">520</td>
<td align="right">14.6%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">520</td>
<td align="right">14.6%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">440</td>
<td align="right">12.4%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">360</td>
<td align="right">10.1%</td>
</tr>
</tbody>
</table>


</details>

### CALL_FUNCTION_EX

<details>
<summary> Successors and predecessors for CALL_FUNCTION_EX </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">80</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">80</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### COMPARE_OP

<details>
<summary> Successors and predecessors for COMPARE_OP </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">240</td>
<td align="right">54.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">60</td>
<td align="right">13.6%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">60</td>
<td align="right">13.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">40</td>
<td align="right">9.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">40</td>
<td align="right">9.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">220</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">220</td>
<td align="right">50.0%</td>
</tr>
</tbody>
</table>


</details>

### COPY

<details>
<summary> Successors and predecessors for COPY </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">10,413,720</td>
<td align="right">65.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">5,547,120</td>
<td align="right">34.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">16,020</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">4,160</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">60</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">15,960,680</td>
<td align="right">99.9%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">20,080</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">200</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">160</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### COPY_FREE_VARS

<details>
<summary> Successors and predecessors for COPY_FREE_VARS </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">80</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">60</td>
<td align="right">75.0%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">20</td>
<td align="right">25.0%</td>
</tr>
</tbody>
</table>


</details>

### ENTER_EXECUTOR

<details>
<summary> Successors and predecessors for ENTER_EXECUTOR </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">25,418,520</td>
<td align="right">50.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">21,057,400</td>
<td align="right">41.9%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">3,019,260</td>
<td align="right">6.0%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">690,140</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">11,460</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">21,564,460</td>
<td align="right">43.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">19,171,920</td>
<td align="right">38.2%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">8,706,620</td>
<td align="right">17.3%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">744,540</td>
<td align="right">1.5%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">5,120</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### EXTENDED_ARG

<details>
<summary> Successors and predecessors for EXTENDED_ARG </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">GET_ITER</td>
<td align="right">320</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">320</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">320</td>
<td align="right">33.3%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">600</td>
<td align="right">62.5%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">320</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">40</td>
<td align="right">4.2%</td>
</tr>
</tbody>
</table>


</details>

### FOR_ITER

<details>
<summary> Successors and predecessors for FOR_ITER </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">GET_ITER</td>
<td align="right">40</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">40</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">40</td>
<td align="right">33.3%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">60</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">60</td>
<td align="right">50.0%</td>
</tr>
</tbody>
</table>


</details>

### JUMP_BACKWARD

<details>
<summary> Successors and predecessors for JUMP_BACKWARD </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">340</td>
<td align="right">25.8%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">320</td>
<td align="right">24.2%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">320</td>
<td align="right">24.2%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">320</td>
<td align="right">24.2%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">20</td>
<td align="right">1.5%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">620</td>
<td align="right">47.0%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">320</td>
<td align="right">24.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">300</td>
<td align="right">22.7%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">40</td>
<td align="right">3.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">20</td>
<td align="right">1.5%</td>
</tr>
</tbody>
</table>


</details>

### JUMP_FORWARD

<details>
<summary> Successors and predecessors for JUMP_FORWARD </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_TOP</td>
<td align="right">8,184,640</td>
<td align="right">95.6%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">377,440</td>
<td align="right">4.4%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">8,189,600</td>
<td align="right">95.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">372,480</td>
<td align="right">4.4%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_ATTR

<details>
<summary> Successors and predecessors for LOAD_ATTR </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,880</td>
<td align="right">49.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">2,000</td>
<td align="right">34.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">280</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">240</td>
<td align="right">4.1%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">200</td>
<td align="right">3.4%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">1,960</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">1,100</td>
<td align="right">18.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">700</td>
<td align="right">11.9%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">500</td>
<td align="right">8.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">440</td>
<td align="right">7.5%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_CONST

<details>
<summary> Successors and predecessors for LOAD_CONST </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">30,775,280</td>
<td align="right">29.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">24,703,300</td>
<td align="right">23.5%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">21,321,080</td>
<td align="right">20.3%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">13,614,080</td>
<td align="right">13.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">4,797,140</td>
<td align="right">4.6%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">58,272,000</td>
<td align="right">55.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">14,134,480</td>
<td align="right">13.5%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">13,613,120</td>
<td align="right">13.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">7,997,040</td>
<td align="right">7.6%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">7,145,040</td>
<td align="right">6.8%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_DEREF

<details>
<summary> Successors and predecessors for LOAD_DEREF </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">NOP</td>
<td align="right">80</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">80</td>
<td align="right">50.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">80</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">80</td>
<td align="right">50.0%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_FAST

<details>
<summary> Successors and predecessors for LOAD_FAST </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">85,831,920</td>
<td align="right">17.2%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">81,292,940</td>
<td align="right">16.3%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">58,272,000</td>
<td align="right">11.7%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">50,838,080</td>
<td align="right">10.2%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">42,868,880</td>
<td align="right">8.6%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">123,922,100</td>
<td align="right">24.8%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">88,147,120</td>
<td align="right">17.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">77,793,460</td>
<td align="right">15.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">46,631,040</td>
<td align="right">9.3%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">42,594,640</td>
<td align="right">8.5%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_FAST_LOAD_FAST

<details>
<summary> Successors and predecessors for LOAD_FAST_LOAD_FAST </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">28,491,480</td>
<td align="right">69.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">7,697,600</td>
<td align="right">18.8%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">3,240,640</td>
<td align="right">7.9%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">756,500</td>
<td align="right">1.8%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">372,480</td>
<td align="right">0.9%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">21,052,760</td>
<td align="right">51.4%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">12,441,600</td>
<td align="right">30.4%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">7,440,440</td>
<td align="right">18.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">3,200</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">1,280</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_GLOBAL

<details>
<summary> Successors and predecessors for LOAD_GLOBAL </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">640</td>
<td align="right">18.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">560</td>
<td align="right">15.9%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">280</td>
<td align="right">8.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">280</td>
<td align="right">8.0%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">240</td>
<td align="right">6.8%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">1,640</td>
<td align="right">46.6%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">540</td>
<td align="right">15.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">260</td>
<td align="right">7.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">240</td>
<td align="right">6.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">240</td>
<td align="right">6.8%</td>
</tr>
</tbody>
</table>


</details>

### POP_JUMP_IF_FALSE

<details>
<summary> Successors and predecessors for POP_JUMP_IF_FALSE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">26,032,100</td>
<td align="right">44.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">24,051,660</td>
<td align="right">40.9%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">8,706,620</td>
<td align="right">14.8%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">220</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">160</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">31,245,460</td>
<td align="right">53.1%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">13,614,080</td>
<td align="right">23.2%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">5,735,000</td>
<td align="right">9.8%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">3,718,080</td>
<td align="right">6.3%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">3,019,260</td>
<td align="right">5.1%</td>
</tr>
</tbody>
</table>


</details>

### POP_JUMP_IF_NONE

<details>
<summary> Successors and predecessors for POP_JUMP_IF_NONE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">31,848,160</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">21,057,400</td>
<td align="right">66.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">7,549,440</td>
<td align="right">23.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">3,240,640</td>
<td align="right">10.2%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">340</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">300</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### POP_JUMP_IF_NOT_NONE

<details>
<summary> Successors and predecessors for POP_JUMP_IF_NOT_NONE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">46,631,040</td>
<td align="right">75.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">14,878,680</td>
<td align="right">24.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">40</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">50,838,080</td>
<td align="right">82.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">7,697,600</td>
<td align="right">12.5%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">2,974,080</td>
<td align="right">4.8%</td>
</tr>
</tbody>
</table>


</details>

### POP_JUMP_IF_TRUE

<details>
<summary> Successors and predecessors for POP_JUMP_IF_TRUE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">21,055,600</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">100</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">21,052,800</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">2,880</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">20</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### RETURN_CONST

<details>
<summary> Successors and predecessors for RETURN_CONST </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">6,280</td>
<td align="right">57.7%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">1,920</td>
<td align="right">17.6%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">1,900</td>
<td align="right">17.5%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">320</td>
<td align="right">2.9%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">300</td>
<td align="right">2.8%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">7,800</td>
<td align="right">71.7%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">2,240</td>
<td align="right">20.6%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">840</td>
<td align="right">7.7%</td>
</tr>
</tbody>
</table>


</details>

### STORE_ATTR

<details>
<summary> Successors and predecessors for STORE_ATTR </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,640</td>
<td align="right">57.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">1,280</td>
<td align="right">28.1%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">320</td>
<td align="right">7.0%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">200</td>
<td align="right">4.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">60</td>
<td align="right">1.3%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,380</td>
<td align="right">30.3%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">1,320</td>
<td align="right">28.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">940</td>
<td align="right">20.6%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">400</td>
<td align="right">8.8%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">320</td>
<td align="right">7.0%</td>
</tr>
</tbody>
</table>


</details>

### STORE_FAST

<details>
<summary> Successors and predecessors for STORE_FAST </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">36,437,740</td>
<td align="right">30.8%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">31,693,600</td>
<td align="right">26.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">24,402,240</td>
<td align="right">20.6%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">13,613,120</td>
<td align="right">11.5%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT</td>
<td align="right">10,638,380</td>
<td align="right">9.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">85,831,920</td>
<td align="right">72.6%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">21,052,640</td>
<td align="right">17.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">7,441,200</td>
<td align="right">6.3%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">3,200,000</td>
<td align="right">2.7%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">377,440</td>
<td align="right">0.3%</td>
</tr>
</tbody>
</table>


</details>

### SWAP

<details>
<summary> Successors and predecessors for SWAP </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">11,158,580</td>
<td align="right">69.9%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">3,199,980</td>
<td align="right">20.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">1,602,320</td>
<td align="right">10.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">15,960,680</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">200</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### RESUME

<details>
<summary> Successors and predecessors for RESUME </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL</td>
<td align="right">440</td>
<td align="right">59.5%</td>
</tr>
<tr>
<td align="left">CACHE</td>
<td align="right">220</td>
<td align="right">29.7%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">60</td>
<td align="right">8.1%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">20</td>
<td align="right">2.7%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">300</td>
<td align="right">40.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">220</td>
<td align="right">29.7%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">200</td>
<td align="right">27.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">20</td>
<td align="right">2.7%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_OP_ADD_INT

<details>
<summary> Successors and predecessors for BINARY_OP_ADD_INT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">14,134,480</td>
<td align="right">95.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">690,440</td>
<td align="right">4.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">100</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">SWAP</td>
<td align="right">11,158,580</td>
<td align="right">75.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,975,980</td>
<td align="right">20.1%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">690,460</td>
<td align="right">4.7%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_OP_SUBTRACT_FLOAT

<details>
<summary> Successors and predecessors for BINARY_OP_SUBTRACT_FLOAT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">40</td>
<td align="right">66.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">20</td>
<td align="right">33.3%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">60</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_OP_SUBTRACT_INT

<details>
<summary> Successors and predecessors for BINARY_OP_SUBTRACT_INT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">3,890,400</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">40</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">SWAP</td>
<td align="right">3,199,980</td>
<td align="right">82.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">690,460</td>
<td align="right">17.7%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_SUBSCR_LIST_INT

<details>
<summary> Successors and predecessors for BINARY_SUBSCR_LIST_INT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">13,614,320</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">40</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">10,638,380</td>
<td align="right">78.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,975,980</td>
<td align="right">21.9%</td>
</tr>
</tbody>
</table>


</details>

### CALL_ALLOC_AND_ENTER_INIT

<details>
<summary> Successors and predecessors for CALL_ALLOC_AND_ENTER_INIT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">5,600</td>
<td align="right">71.8%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">1,680</td>
<td align="right">21.5%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">520</td>
<td align="right">6.7%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">7,800</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### CALL_BUILTIN_CLASS

<details>
<summary> Successors and predecessors for CALL_BUILTIN_CLASS </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">320</td>
<td align="right">88.9%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">40</td>
<td align="right">11.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">GET_ITER</td>
<td align="right">300</td>
<td align="right">83.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">60</td>
<td align="right">16.7%</td>
</tr>
</tbody>
</table>


</details>

### CALL_ISINSTANCE

<details>
<summary> Successors and predecessors for CALL_ISINSTANCE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">21,052,640</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">80</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">21,052,640</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">80</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### CALL_PY_EXACT_ARGS

<details>
<summary> Successors and predecessors for CALL_PY_EXACT_ARGS </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">34,927,800</td>
<td align="right">44.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">17,874,140</td>
<td align="right">22.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">14,358,760</td>
<td align="right">18.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">7,440,440</td>
<td align="right">9.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">3,199,880</td>
<td align="right">4.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">77,801,760</td>
<td align="right">99.7%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">264,420</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">60</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### COMPARE_OP_INT

<details>
<summary> Successors and predecessors for COMPARE_OP_INT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">10,964,360</td>
<td align="right">42.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">7,922,480</td>
<td align="right">30.4%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">7,145,040</td>
<td align="right">27.4%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">220</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">26,032,100</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### FOR_ITER_RANGE

<details>
<summary> Successors and predecessors for FOR_ITER_RANGE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">GET_ITER</td>
<td align="right">744,680</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">744,540</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">620</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">600</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">60</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">745,460</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">744,720</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">320</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_ATTR_INSTANCE_VALUE

<details>
<summary> Successors and predecessors for LOAD_ATTR_INSTANCE_VALUE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">123,922,100</td>
<td align="right">64.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">21,052,760</td>
<td align="right">11.0%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">19,171,920</td>
<td align="right">10.0%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">15,960,680</td>
<td align="right">8.3%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">10,642,960</td>
<td align="right">5.6%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">40,829,780</td>
<td align="right">21.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">36,437,740</td>
<td align="right">19.0%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">34,927,800</td>
<td align="right">18.2%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">25,870,100</td>
<td align="right">13.5%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">24,703,300</td>
<td align="right">12.9%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_ATTR_METHOD_WITH_VALUES

<details>
<summary> Successors and predecessors for LOAD_ATTR_METHOD_WITH_VALUES </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">77,793,460</td>
<td align="right">99.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">460,000</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">3,820</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">1,680</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">700</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">28,491,480</td>
<td align="right">36.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">28,234,020</td>
<td align="right">36.1%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">17,874,140</td>
<td align="right">22.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">3,199,600</td>
<td align="right">4.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">460,000</td>
<td align="right">0.6%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_ATTR_MODULE

<details>
<summary> Successors and predecessors for LOAD_ATTR_MODULE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">80</td>
<td align="right">66.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">40</td>
<td align="right">33.3%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">60</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">60</td>
<td align="right">50.0%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_GLOBAL_BUILTIN

<details>
<summary> Successors and predecessors for LOAD_GLOBAL_BUILTIN </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">21,052,640</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">280</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">120</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">40</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">21,053,080</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_GLOBAL_MODULE

<details>
<summary> Successors and predecessors for LOAD_GLOBAL_MODULE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">27,558,080</td>
<td align="right">44.8%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">13,617,600</td>
<td align="right">22.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">7,441,200</td>
<td align="right">12.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">4,465,200</td>
<td align="right">7.3%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">3,722,100</td>
<td align="right">6.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">21,052,640</td>
<td align="right">34.3%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">10,964,360</td>
<td align="right">17.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">10,642,960</td>
<td align="right">17.3%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">10,413,720</td>
<td align="right">16.9%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">3,199,880</td>
<td align="right">5.2%</td>
</tr>
</tbody>
</table>


</details>

### RESUME_CHECK

<details>
<summary> Successors and predecessors for RESUME_CHECK </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">77,801,760</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">7,800</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CACHE</td>
<td align="right">620</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">360</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">60</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">42,868,880</td>
<td align="right">55.1%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">21,321,080</td>
<td align="right">27.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">13,617,600</td>
<td align="right">17.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">2,540</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">280</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### STORE_ATTR_INSTANCE_VALUE

<details>
<summary> Successors and predecessors for STORE_ATTR_INSTANCE_VALUE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">88,147,120</td>
<td align="right">75.4%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">15,960,680</td>
<td align="right">13.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">12,441,600</td>
<td align="right">10.6%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">326,680</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">2,440</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">81,292,940</td>
<td align="right">69.6%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">30,775,280</td>
<td align="right">26.3%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">3,722,100</td>
<td align="right">3.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">756,500</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">326,680</td>
<td align="right">0.3%</td>
</tr>
</tbody>
</table>


</details>

### STORE_SUBSCR_LIST_INT

<details>
<summary> Successors and predecessors for STORE_SUBSCR_LIST_INT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">692,320</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">40</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">690,140</td>
<td align="right">99.7%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">1,900</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">320</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### TO_BOOL_BOOL

<details>
<summary> Successors and predecessors for TO_BOOL_BOOL </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">46,473,860</td>
<td align="right">65.9%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">21,052,640</td>
<td align="right">29.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">2,978,940</td>
<td align="right">4.2%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">20,080</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">9,740</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">25,418,520</td>
<td align="right">36.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">24,051,660</td>
<td align="right">34.1%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">21,055,600</td>
<td align="right">29.9%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">9,780</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>


</details>

## Specialization stats

<details>
<summary> Specialization stats by family </summary>

### BINARY_OP

<details>
<summary> specialization stats for BINARY_OP family </summary>

<table>
<thead>
<tr>
<th align="left">Kind</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">7,999,520</td>
<td align="right">29.9%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">18,715,520</td>
<td align="right">70.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">160</td>
<td align="right">5.3%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">2,840</td>
<td align="right">94.7%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">floor divide</td>
<td align="right">1,160</td>
<td align="right">40.8%</td>
</tr>
<tr>
<td align="left">and int</td>
<td align="right">980</td>
<td align="right">34.5%</td>
</tr>
<tr>
<td align="left">xor</td>
<td align="right">580</td>
<td align="right">20.4%</td>
</tr>
<tr>
<td align="left">multiply different types</td>
<td align="right">120</td>
<td align="right">4.2%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_SUBSCR

<details>
<summary> specialization stats for BINARY_SUBSCR family </summary>

<table>
<thead>
<tr>
<th align="left">Kind</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">40</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">13,614,360</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">40</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### CALL

<details>
<summary> specialization stats for CALL family </summary>

<table>
<thead>
<tr>
<th align="left">Kind</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">13,752,300</td>
<td align="right">13.9%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">85,112,400</td>
<td align="right">85.9%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">14,014,720</td>
<td align="right">14.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">265,860</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">120</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">other</td>
<td align="right">60</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">cfunc noargs</td>
<td align="right">60</td>
<td align="right">50.0%</td>
</tr>
</tbody>
</table>


</details>

### COMPARE_OP

<details>
<summary> specialization stats for COMPARE_OP family </summary>

<table>
<thead>
<tr>
<th align="left">Kind</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">220</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">26,032,100</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">220</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### FOR_ITER

<details>
<summary> specialization stats for FOR_ITER family </summary>

<table>
<thead>
<tr>
<th align="left">Kind</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">60</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,490,500</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">60</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_ATTR

<details>
<summary> specialization stats for LOAD_ATTR family </summary>

<table>
<thead>
<tr>
<th align="left">Kind</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">69,808,640</td>
<td align="right">25.9%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">198,746,440</td>
<td align="right">73.6%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">71,147,120</td>
<td align="right">26.4%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">1,344,080</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">280</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">metaclass attribute</td>
<td align="right">280</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_GLOBAL

<details>
<summary> specialization stats for LOAD_GLOBAL family </summary>

<table>
<thead>
<tr>
<th align="left">Kind</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">1,760</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">82,506,740</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">1,760</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### POP_JUMP_IF_FALSE

<details>
<summary> specialization stats for POP_JUMP_IF_FALSE family </summary>


</details>

### POP_JUMP_IF_NONE

<details>
<summary> specialization stats for POP_JUMP_IF_NONE family </summary>


</details>

### POP_JUMP_IF_NOT_NONE

<details>
<summary> specialization stats for POP_JUMP_IF_NOT_NONE family </summary>


</details>

### POP_JUMP_IF_TRUE

<details>
<summary> specialization stats for POP_JUMP_IF_TRUE family </summary>


</details>

### STORE_ATTR

<details>
<summary> specialization stats for STORE_ATTR family </summary>

<table>
<thead>
<tr>
<th align="left">Kind</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">16,995,660</td>
<td align="right">14.5%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">99,560,420</td>
<td align="right">85.2%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">17,319,420</td>
<td align="right">14.8%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">328,000</td>
<td align="right">99.9%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">320</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">not in keys</td>
<td align="right">320</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### STORE_SUBSCR

<details>
<summary> specialization stats for STORE_SUBSCR family </summary>

<table>
<thead>
<tr>
<th align="left">Kind</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">40</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">692,360</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">40</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### TO_BOOL

<details>
<summary> specialization stats for TO_BOOL family </summary>

<table>
<thead>
<tr>
<th align="left">Kind</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">300</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">70,535,560</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">300</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>


</details>

## Specialization effectiveness

<details>
<summary> specialization effectiveness </summary>


All entries are execution counts. Should add up to the total number of
Tier 1 instructions executed.

<table>
<thead>
<tr>
<th align="left">Instructions</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
Basic
<details>
<summary>ⓘ</summary>

Instructions that are not and cannot be specialized, e.g. `LOAD_FAST`.
</details>
</td>
<td align="right">1,018,814,760</td>
<td align="right">51.5%</td>
</tr>
<tr>
<td align="left">
Not specialized
<details>
<summary>ⓘ</summary>

Instructions that could be specialized but aren't, e.g. `LOAD_ATTR`, `BINARY_SLICE`.
</details>
</td>
<td align="right">181,225,740</td>
<td align="right">9.2%</td>
</tr>
<tr>
<td align="left">
Specialized hits
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that complete.
</details>
</td>
<td align="right">674,817,000</td>
<td align="right">34.1%</td>
</tr>
<tr>
<td align="left">
Specialized misses
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that deopt.
</details>
</td>
<td align="right">102,481,260</td>
<td align="right">5.2%</td>
</tr>
</tbody>
</table>

### Deferred by instruction

<details>
<summary> Breakdown of deferred (not specialized) instruction counts by family </summary>

<table>
<thead>
<tr>
<th align="left">Name</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">69,808,640</td>
<td align="right">64.3%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">16,995,660</td>
<td align="right">15.7%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">13,752,300</td>
<td align="right">12.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">7,999,520</td>
<td align="right">7.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">1,760</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">300</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">220</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">60</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">40</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">40</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### Misses by instruction

<details>
<summary> Breakdown of misses (specialized deopts) instruction counts by family </summary>

<table>
<thead>
<tr>
<th align="left">Name</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">46,764,400</td>
<td align="right">45.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">24,382,720</td>
<td align="right">23.8%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">17,319,420</td>
<td align="right">16.9%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">14,014,720</td>
<td align="right">13.7%</td>
</tr>
<tr>
<td align="left">CACHE</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>


</details>

## Call stats

<details>
<summary> Inlined calls and frame stats </summary>


This shows what fraction of calls to Python functions are inlined (i.e.
not having a call at the C level) and for those that are not, where the
call comes from.  The various categories overlap.

Also includes the count of frame objects created.

<table>
<thead>
<tr>
<th align="left"></th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Calls to PyEval_EvalDefault</td>
<td align="right">840</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls to Python functions inlined</td>
<td align="right">154,030,920</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">840</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (vector)</td>
<td align="right">840</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (generator)</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (legacy)</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function vectorcall)</td>
<td align="right">840</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (build class)</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (slot)</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function ex)</td>
<td align="right">80</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (api)</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (method)</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Frame objects created</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Frames pushed</td>
<td align="right">154,039,560</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

## Object stats

<details>
<summary> Allocations, frees and dict materializatons </summary>


Below, "allocations" means "allocations that are not from a freelist".
Total allocations = "Allocations from freelist" + "Allocations".

"Inline values" is the number of values arrays inlined into objects.

The cache hit/miss numbers are for the MRO cache, split into dunder and
other names.

<table>
<thead>
<tr>
<th align="left"></th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Allocations from freelist</td>
<td align="right">3,260</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">2,940</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">18,894,140</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">18,893,940</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">200</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Allocations over 4 kbytes</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">18,882,249</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Inline values</td>
<td align="right">8,320</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Interpreter increfs</td>
<td align="right">1,357,781,960</td>
<td align="right">91.8%</td>
</tr>
<tr>
<td align="left">Interpreter decrefs</td>
<td align="right">1,476,014,280</td>
<td align="right">98.6%</td>
</tr>
<tr>
<td align="left">Increfs</td>
<td align="right">120,660,951</td>
<td align="right">8.2%</td>
</tr>
<tr>
<td align="left">Decrefs</td>
<td align="right">21,299,471</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">Materialize dict (on request)</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Materialize dict (new key)</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Materialize dict (too big)</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Materialize dict (str subclass)</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Method cache hits</td>
<td align="right">161,365,389</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Method cache misses</td>
<td align="right">1,971</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">1,288</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">4,740</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Method cache dunder misses</td>
<td align="right">420</td>
<td align="right"></td>
</tr>
</tbody>
</table>


</details>

## GC stats

<details>
<summary> GC collections and effectiveness </summary>


Collected/visits gives some measure of efficiency.

<table>
<thead>
<tr>
<th align="right">Generation</th>
<th align="right">Collections</th>
<th align="right">Objects collected</th>
<th align="right">Object visits</th>
</tr>
</thead>
<tbody>
<tr>
<td align="right">0</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right">0</td>
</tr>
<tr>
<td align="right">1</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right">0</td>
</tr>
<tr>
<td align="right">2</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right">0</td>
</tr>
</tbody>
</table>


</details>

## Optimization (Tier 2) stats

<details>
<summary> statistics about the Tier 2 optimizer </summary>

<table>
<thead>
<tr>
<th align="left"></th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
Optimization attempts
<details>
<summary>ⓘ</summary>

The number of times a potential trace is identified.  Specifically, this occurs in the JUMP BACKWARD instruction when the counter reaches a threshold.
</details>
</td>
<td align="right">13,740</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">
Traces created
<details>
<summary>ⓘ</summary>

The number of traces that were successfully created.
</details>
</td>
<td align="right">340</td>
<td align="right">2.5%</td>
</tr>
<tr>
<td align="left">
Trace stack overflow
<details>
<summary>ⓘ</summary>

A trace is truncated because it would require more than 5 stack frames.
</details>
</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">
Trace stack underflow
<details>
<summary>ⓘ</summary>

A potential trace is abandoned because it pops more frames than it pushes.
</details>
</td>
<td align="right">13,540</td>
<td align="right">98.5%</td>
</tr>
<tr>
<td align="left">
Trace too long
<details>
<summary>ⓘ</summary>

A trace is truncated because it is longer than the instruction buffer.
</details>
</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">
Trace too short
<details>
<summary>ⓘ</summary>

A potential trace is abandoced because it it too short.
</details>
</td>
<td align="right">13,400</td>
<td align="right">97.5%</td>
</tr>
<tr>
<td align="left">
Inner loop found
<details>
<summary>ⓘ</summary>

A trace is truncated because it has an inner loop
</details>
</td>
<td align="right">60</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">
Recursive call
<details>
<summary>ⓘ</summary>

A trace is truncated because it has a recursive call.
</details>
</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">
Low confidence
<details>
<summary>ⓘ</summary>

A trace is abandoned because the likelihood of the jump to top being taken is too low.
</details>
</td>
<td align="right">120</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">
Executors invalidated
<details>
<summary>ⓘ</summary>

The number of executors that were invalidated due to watched dictionary changes.
</details>
</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">
Traces executed
<details>
<summary>ⓘ</summary>

The number of traces that were executed
</details>
</td>
<td align="right">217,866,520</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">
Uops executed
<details>
<summary>ⓘ</summary>

The total number of uops (micro-operations) that were executed
</details>
</td>
<td align="right">2,528,304,120</td>
<td align="right">1,160.5%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left"></th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
Optimizer attempts
<details>
<summary>ⓘ</summary>

The number of times the trace optimizer (_Py_uop_analyze_and_optimize) was run.
</details>
</td>
<td align="right">340</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">
Optimizer successes
<details>
<summary>ⓘ</summary>

The number of traces that were successfully optimized.
</details>
</td>
<td align="right">340</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">
Optimizer no memory
<details>
<summary>ⓘ</summary>

The number of optimizations that failed due to no memory.
</details>
</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">
Remove globals builtins changed
<details>
<summary>ⓘ</summary>

The builtins changed during optimization
</details>
</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">
Remove globals incorrect keys
<details>
<summary>ⓘ</summary>

The keys in the globals dictionary aren't what was expected
</details>
</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

### Trace length histogram

<details>
<summary> trace length histogram </summary>

<table>
<thead>
<tr>
<th align="left">Range</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left"><= 1</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left"><= 2</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left"><= 4</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left"><= 8</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">120</td>
<td align="right">35.3%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">60</td>
<td align="right">17.6%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">100</td>
<td align="right">29.4%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">60</td>
<td align="right">17.6%</td>
</tr>
</tbody>
</table>


</details>

### Optimized trace length histogram

<details>
<summary> optimized trace length histogram </summary>

<table>
<thead>
<tr>
<th align="left">Range</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left"><= 1</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left"><= 2</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left"><= 4</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left"><= 8</td>
<td align="right">80</td>
<td align="right">23.5%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">100</td>
<td align="right">29.4%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">40</td>
<td align="right">11.8%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">100</td>
<td align="right">29.4%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">20</td>
<td align="right">5.9%</td>
</tr>
</tbody>
</table>


</details>

### Trace run length histogram

<details>
<summary> trace run length histogram </summary>

<table>
<thead>
<tr>
<th align="left">Range</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left"><= 1</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left"><= 2</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left"><= 4</td>
<td align="right">18,718,460</td>
<td align="right">8.6%</td>
</tr>
<tr>
<td align="left"><= 8</td>
<td align="right">49,362,220</td>
<td align="right">22.7%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">50,644,040</td>
<td align="right">23.2%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">31,254,160</td>
<td align="right">14.3%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">17,685,320</td>
<td align="right">8.1%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">57,280</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">687,280</td>
<td align="right">0.3%</td>
</tr>
</tbody>
</table>


</details>

### Uop execution stats

<details>
<summary> uop execution stats </summary>

<table>
<thead>
<tr>
<th align="left">Name</th>
<th align="right">Count</th>
<th align="right">Self</th>
<th align="right">Cumulative</th>
<th align="right">Miss ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">_LOAD_FAST_0</td>
<td align="right">229,632,260</td>
<td align="right">9.1%</td>
<td align="right">9.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION</td>
<td align="right">227,951,220</td>
<td align="right">9.0%</td>
<td align="right">18.1%</td>
<td align="right">40.4%</td>
</tr>
<tr>
<td align="left">_START_EXECUTOR</td>
<td align="right">168,408,760</td>
<td align="right">6.7%</td>
<td align="right">24.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_SIDE_EXIT</td>
<td align="right">167,664,200</td>
<td align="right">6.6%</td>
<td align="right">31.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL_BOOL</td>
<td align="right">140,444,500</td>
<td align="right">5.6%</td>
<td align="right">36.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_SET_IP</td>
<td align="right">113,159,580</td>
<td align="right">4.5%</td>
<td align="right">41.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_MANAGED_OBJECT_HAS_VALUES</td>
<td align="right">103,070,060</td>
<td align="right">4.1%</td>
<td align="right">45.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE_0</td>
<td align="right">103,070,060</td>
<td align="right">4.1%</td>
<td align="right">49.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COPY</td>
<td align="right">102,907,040</td>
<td align="right">4.1%</td>
<td align="right">53.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_IS_FALSE_POP</td>
<td align="right">80,586,240</td>
<td align="right">3.2%</td>
<td align="right">56.8%</td>
<td align="right">20.2%</td>
</tr>
<tr>
<td align="left">_RESUME_CHECK</td>
<td align="right">76,220,420</td>
<td align="right">3.0%</td>
<td align="right">59.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_EXACT_ARGS</td>
<td align="right">76,220,420</td>
<td align="right">3.0%</td>
<td align="right">62.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_0</td>
<td align="right">76,220,420</td>
<td align="right">3.0%</td>
<td align="right">65.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_PUSH_FRAME</td>
<td align="right">76,220,420</td>
<td align="right">3.0%</td>
<td align="right">68.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_SAVE_RETURN_OFFSET</td>
<td align="right">76,220,420</td>
<td align="right">3.0%</td>
<td align="right">71.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR</td>
<td align="right">72,892,620</td>
<td align="right">2.9%</td>
<td align="right">74.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_POP_TOP</td>
<td align="right">72,094,580</td>
<td align="right">2.9%</td>
<td align="right">77.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE_OPERAND</td>
<td align="right">65,810,140</td>
<td align="right">2.6%</td>
<td align="right">80.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION</td>
<td align="right">57,464,220</td>
<td align="right">2.3%</td>
<td align="right">82.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COLD_EXIT</td>
<td align="right">49,457,760</td>
<td align="right">2.0%</td>
<td align="right">84.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_IS_TRUE_POP</td>
<td align="right">47,739,240</td>
<td align="right">1.9%</td>
<td align="right">86.4%</td>
<td align="right">25.9%</td>
</tr>
<tr>
<td align="left">_EXIT_TRACE</td>
<td align="right">46,948,040</td>
<td align="right">1.9%</td>
<td align="right">88.2%</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY_AND_SET_IP</td>
<td align="right">45,741,540</td>
<td align="right">1.8%</td>
<td align="right">90.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNARY_NOT</td>
<td align="right">39,771,140</td>
<td align="right">1.6%</td>
<td align="right">91.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_DORV_VALUES_INST_ATTR_FROM_DICT</td>
<td align="right">30,478,880</td>
<td align="right">1.2%</td>
<td align="right">92.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_KEYS_VERSION</td>
<td align="right">30,478,880</td>
<td align="right">1.2%</td>
<td align="right">94.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">30,478,880</td>
<td align="right">1.2%</td>
<td align="right">95.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY</td>
<td align="right">27,151,080</td>
<td align="right">1.1%</td>
<td align="right">96.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_IS_NOT_NONE_POP</td>
<td align="right">13,069,920</td>
<td align="right">0.5%</td>
<td align="right">96.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_0</td>
<td align="right">13,069,920</td>
<td align="right">0.5%</td>
<td align="right">97.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW</td>
<td align="right">9,155,200</td>
<td align="right">0.4%</td>
<td align="right">97.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_POP_FRAME</td>
<td align="right">8,706,540</td>
<td align="right">0.3%</td>
<td align="right">98.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_3</td>
<td align="right">6,867,120</td>
<td align="right">0.3%</td>
<td align="right">98.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_INT</td>
<td align="right">6,755,440</td>
<td align="right">0.3%</td>
<td align="right">98.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_INT</td>
<td align="right">4,521,760</td>
<td align="right">0.2%</td>
<td align="right">98.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_RANGE</td>
<td align="right">2,978,240</td>
<td align="right">0.1%</td>
<td align="right">98.9%</td>
<td align="right">25.0%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_RANGE</td>
<td align="right">2,978,240</td>
<td align="right">0.1%</td>
<td align="right">99.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_DORV_NO_DICT</td>
<td align="right">2,345,360</td>
<td align="right">0.1%</td>
<td align="right">99.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">2,345,360</td>
<td align="right">0.1%</td>
<td align="right">99.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_LIST_INT</td>
<td align="right">2,288,080</td>
<td align="right">0.1%</td>
<td align="right">99.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBTRACT_INT</td>
<td align="right">2,288,080</td>
<td align="right">0.1%</td>
<td align="right">99.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_1</td>
<td align="right">2,288,080</td>
<td align="right">0.1%</td>
<td align="right">99.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_5</td>
<td align="right">2,288,080</td>
<td align="right">0.1%</td>
<td align="right">99.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_SWAP</td>
<td align="right">2,233,680</td>
<td align="right">0.1%</td>
<td align="right">99.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COMPARE_OP_INT</td>
<td align="right">2,233,680</td>
<td align="right">0.1%</td>
<td align="right">99.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_ITER_NEXT_RANGE</td>
<td align="right">2,233,680</td>
<td align="right">0.1%</td>
<td align="right">99.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_5</td>
<td align="right">2,233,680</td>
<td align="right">0.1%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_JUMP_TO_TOP</td>
<td align="right">2,176,400</td>
<td align="right">0.1%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_DEOPT</td>
<td align="right">744,560</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
</tbody>
</table>


</details>

### Pair counts

<details>
<summary> Pair counts for top 100 Non-JIT uop pairs </summary>


Pairs of specialized operations that deoptimize and are then followed by
the corresponding unspecialized instruction are not counted as pairs.

<table>
<thead>
<tr>
<th align="left">Pair</th>
<th align="right">Count</th>
<th align="right">Self</th>
<th align="right">Cumulative</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">_LOAD_FAST_0 _GUARD_TYPE_VERSION</td>
<td align="right">216,562,340</td>
<td align="right">8.6%</td>
<td align="right">8.6%</td>
</tr>
<tr>
<td align="left">_CHECK_MANAGED_OBJECT_HAS_VALUES _LOAD_ATTR_INSTANCE_VALUE_0</td>
<td align="right">103,070,060</td>
<td align="right">4.1%</td>
<td align="right">12.6%</td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION _CHECK_MANAGED_OBJECT_HAS_VALUES</td>
<td align="right">103,070,060</td>
<td align="right">4.1%</td>
<td align="right">16.7%</td>
</tr>
<tr>
<td align="left">_COPY _TO_BOOL_BOOL</td>
<td align="right">100,673,360</td>
<td align="right">4.0%</td>
<td align="right">20.7%</td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION _SIDE_EXIT</td>
<td align="right">92,056,920</td>
<td align="right">3.6%</td>
<td align="right">24.3%</td>
</tr>
<tr>
<td align="left">_RESUME_CHECK _LOAD_FAST_0</td>
<td align="right">76,220,420</td>
<td align="right">3.0%</td>
<td align="right">27.4%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_0 _SAVE_RETURN_OFFSET</td>
<td align="right">76,220,420</td>
<td align="right">3.0%</td>
<td align="right">30.4%</td>
</tr>
<tr>
<td align="left">_PUSH_FRAME _RESUME_CHECK</td>
<td align="right">76,220,420</td>
<td align="right">3.0%</td>
<td align="right">33.4%</td>
</tr>
<tr>
<td align="left">_SAVE_RETURN_OFFSET _PUSH_FRAME</td>
<td align="right">76,220,420</td>
<td align="right">3.0%</td>
<td align="right">36.4%</td>
</tr>
<tr>
<td align="left">_START_EXECUTOR _SET_IP</td>
<td align="right">73,694,460</td>
<td align="right">2.9%</td>
<td align="right">39.3%</td>
</tr>
<tr>
<td align="left">_SET_IP _LOAD_ATTR</td>
<td align="right">72,892,620</td>
<td align="right">2.9%</td>
<td align="right">42.2%</td>
</tr>
<tr>
<td align="left">_POP_TOP _LOAD_FAST_0</td>
<td align="right">72,094,580</td>
<td align="right">2.9%</td>
<td align="right">45.0%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_EXACT_ARGS _CHECK_STACK_SPACE_OPERAND</td>
<td align="right">65,810,140</td>
<td align="right">2.6%</td>
<td align="right">47.7%</td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE_OPERAND _INIT_CALL_PY_EXACT_ARGS_0</td>
<td align="right">65,810,140</td>
<td align="right">2.6%</td>
<td align="right">50.3%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE_0 _COPY</td>
<td align="right">56,503,020</td>
<td align="right">2.2%</td>
<td align="right">52.5%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION _LOAD_FAST_0</td>
<td align="right">55,176,140</td>
<td align="right">2.2%</td>
<td align="right">54.7%</td>
</tr>
<tr>
<td align="left">_EXIT_TRACE _SIDE_EXIT</td>
<td align="right">46,948,040</td>
<td align="right">1.9%</td>
<td align="right">56.5%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY_AND_SET_IP _CHECK_FUNCTION_EXACT_ARGS</td>
<td align="right">45,741,540</td>
<td align="right">1.8%</td>
<td align="right">58.3%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR _CHECK_VALIDITY_AND_SET_IP</td>
<td align="right">45,741,540</td>
<td align="right">1.8%</td>
<td align="right">60.1%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_BOOL _GUARD_IS_FALSE_POP</td>
<td align="right">44,230,980</td>
<td align="right">1.7%</td>
<td align="right">61.9%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_BOOL _UNARY_NOT</td>
<td align="right">39,771,140</td>
<td align="right">1.6%</td>
<td align="right">63.5%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_BOOL _GUARD_IS_TRUE_POP</td>
<td align="right">38,816,820</td>
<td align="right">1.5%</td>
<td align="right">65.0%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_TRUE_POP _POP_TOP</td>
<td align="right">35,396,120</td>
<td align="right">1.4%</td>
<td align="right">66.4%</td>
</tr>
<tr>
<td align="left">_START_EXECUTOR _CHECK_FUNCTION</td>
<td align="right">34,127,040</td>
<td align="right">1.3%</td>
<td align="right">67.8%</td>
</tr>
<tr>
<td align="left">_START_EXECUTOR _GUARD_IS_FALSE_POP</td>
<td align="right">34,121,580</td>
<td align="right">1.3%</td>
<td align="right">69.1%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_FALSE_POP _POP_TOP</td>
<td align="right">32,338,080</td>
<td align="right">1.3%</td>
<td align="right">70.4%</td>
</tr>
<tr>
<td align="left">_UNARY_NOT _COPY</td>
<td align="right">32,336,800</td>
<td align="right">1.3%</td>
<td align="right">71.7%</td>
</tr>
<tr>
<td align="left">_SET_IP _CHECK_FUNCTION_EXACT_ARGS</td>
<td align="right">30,478,880</td>
<td align="right">1.2%</td>
<td align="right">72.9%</td>
</tr>
<tr>
<td align="left">_GUARD_DORV_VALUES_INST_ATTR_FROM_DICT _GUARD_KEYS_VERSION</td>
<td align="right">30,478,880</td>
<td align="right">1.2%</td>
<td align="right">74.1%</td>
</tr>
<tr>
<td align="left">_GUARD_KEYS_VERSION _LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">30,478,880</td>
<td align="right">1.2%</td>
<td align="right">75.3%</td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION _GUARD_DORV_VALUES_INST_ATTR_FROM_DICT</td>
<td align="right">30,478,880</td>
<td align="right">1.2%</td>
<td align="right">76.5%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_WITH_VALUES _SET_IP</td>
<td align="right">30,478,880</td>
<td align="right">1.2%</td>
<td align="right">77.7%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE_0 _TO_BOOL_BOOL</td>
<td align="right">29,880,260</td>
<td align="right">1.2%</td>
<td align="right">78.9%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR _CHECK_VALIDITY</td>
<td align="right">27,151,080</td>
<td align="right">1.1%</td>
<td align="right">79.9%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_FALSE_POP _CHECK_FUNCTION</td>
<td align="right">23,225,500</td>
<td align="right">0.9%</td>
<td align="right">80.9%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_BOOL _EXIT_TRACE</td>
<td align="right">17,625,560</td>
<td align="right">0.7%</td>
<td align="right">81.6%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_FALSE_POP _SIDE_EXIT</td>
<td align="right">16,315,820</td>
<td align="right">0.6%</td>
<td align="right">82.2%</td>
</tr>
<tr>
<td align="left">_START_EXECUTOR _LOAD_FAST_0</td>
<td align="right">13,071,200</td>
<td align="right">0.5%</td>
<td align="right">82.7%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_0 _GUARD_IS_NOT_NONE_POP</td>
<td align="right">13,069,920</td>
<td align="right">0.5%</td>
<td align="right">83.2%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_0 _LOAD_FAST_0</td>
<td align="right">13,069,920</td>
<td align="right">0.5%</td>
<td align="right">83.8%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NOT_NONE_POP _EXIT_TRACE</td>
<td align="right">13,069,620</td>
<td align="right">0.5%</td>
<td align="right">84.3%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_TRUE_POP _SIDE_EXIT</td>
<td align="right">12,343,120</td>
<td align="right">0.5%</td>
<td align="right">84.8%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY _COPY</td>
<td align="right">11,833,540</td>
<td align="right">0.5%</td>
<td align="right">85.2%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_EXACT_ARGS _INIT_CALL_PY_EXACT_ARGS_0</td>
<td align="right">10,410,280</td>
<td align="right">0.4%</td>
<td align="right">85.6%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY _TO_BOOL_BOOL</td>
<td align="right">9,890,880</td>
<td align="right">0.4%</td>
<td align="right">86.0%</td>
</tr>
<tr>
<td align="left">_START_EXECUTOR _GUARD_IS_TRUE_POP</td>
<td align="right">8,922,420</td>
<td align="right">0.4%</td>
<td align="right">86.4%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_FALSE_POP _POP_FRAME</td>
<td align="right">8,706,540</td>
<td align="right">0.3%</td>
<td align="right">86.7%</td>
</tr>
<tr>
<td align="left">_POP_FRAME _EXIT_TRACE</td>
<td align="right">8,706,540</td>
<td align="right">0.3%</td>
<td align="right">87.1%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE_0 _STORE_FAST_0</td>
<td align="right">7,643,260</td>
<td align="right">0.3%</td>
<td align="right">87.4%</td>
</tr>
<tr>
<td align="left">_UNARY_NOT _EXIT_TRACE</td>
<td align="right">7,434,340</td>
<td align="right">0.3%</td>
<td align="right">87.7%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY _STORE_FAST_0</td>
<td align="right">5,426,660</td>
<td align="right">0.2%</td>
<td align="right">87.9%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_3 _GUARD_TYPE_VERSION</td>
<td align="right">4,633,440</td>
<td align="right">0.2%</td>
<td align="right">88.1%</td>
</tr>
<tr>
<td align="left">_SET_IP _GUARD_BOTH_INT</td>
<td align="right">4,521,760</td>
<td align="right">0.2%</td>
<td align="right">88.2%</td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_INT _BINARY_OP_ADD_INT</td>
<td align="right">4,521,760</td>
<td align="right">0.2%</td>
<td align="right">88.4%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW _SET_IP</td>
<td align="right">4,521,760</td>
<td align="right">0.2%</td>
<td align="right">88.6%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE_0 _LOAD_CONST_INLINE_BORROW</td>
<td align="right">4,467,360</td>
<td align="right">0.2%</td>
<td align="right">88.8%</td>
</tr>
<tr>
<td align="left">_START_EXECUTOR _POP_TOP</td>
<td align="right">4,360,380</td>
<td align="right">0.2%</td>
<td align="right">89.0%</td>
</tr>
<tr>
<td align="left">_SET_IP _ITER_CHECK_RANGE</td>
<td align="right">2,978,240</td>
<td align="right">0.1%</td>
<td align="right">89.1%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_RANGE _GUARD_NOT_EXHAUSTED_RANGE</td>
<td align="right">2,978,240</td>
<td align="right">0.1%</td>
<td align="right">89.2%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW _LOAD_FAST_3</td>
<td align="right">2,399,760</td>
<td align="right">0.1%</td>
<td align="right">89.3%</td>
</tr>
<tr>
<td align="left">_GUARD_DORV_NO_DICT _STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">2,345,360</td>
<td align="right">0.1%</td>
<td align="right">89.4%</td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION _GUARD_DORV_NO_DICT</td>
<td align="right">2,345,360</td>
<td align="right">0.1%</td>
<td align="right">89.5%</td>
</tr>
<tr>
<td align="left">_SET_IP _BINARY_OP_SUBTRACT_INT</td>
<td align="right">2,288,080</td>
<td align="right">0.1%</td>
<td align="right">89.6%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_INT _LOAD_CONST_INLINE_BORROW</td>
<td align="right">2,288,080</td>
<td align="right">0.1%</td>
<td align="right">89.7%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBTRACT_INT _LOAD_FAST_1</td>
<td align="right">2,288,080</td>
<td align="right">0.1%</td>
<td align="right">89.7%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION _LOAD_CONST_INLINE_BORROW</td>
<td align="right">2,288,080</td>
<td align="right">0.1%</td>
<td align="right">89.8%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE_0 _SET_IP</td>
<td align="right">2,288,080</td>
<td align="right">0.1%</td>
<td align="right">89.9%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE_0 _LOAD_FAST_5</td>
<td align="right">2,288,080</td>
<td align="right">0.1%</td>
<td align="right">90.0%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_1 _GUARD_TYPE_VERSION</td>
<td align="right">2,288,080</td>
<td align="right">0.1%</td>
<td align="right">90.1%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_5 _STORE_SUBSCR_LIST_INT</td>
<td align="right">2,288,080</td>
<td align="right">0.1%</td>
<td align="right">90.2%</td>
</tr>
<tr>
<td align="left">_COPY _GUARD_TYPE_VERSION</td>
<td align="right">2,233,680</td>
<td align="right">0.1%</td>
<td align="right">90.3%</td>
</tr>
<tr>
<td align="left">_SWAP _GUARD_TYPE_VERSION</td>
<td align="right">2,233,680</td>
<td align="right">0.1%</td>
<td align="right">90.4%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_INT _SWAP</td>
<td align="right">2,233,680</td>
<td align="right">0.1%</td>
<td align="right">90.5%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_INT _GUARD_IS_FALSE_POP</td>
<td align="right">2,233,680</td>
<td align="right">0.1%</td>
<td align="right">90.5%</td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_INT _COMPARE_OP_INT</td>
<td align="right">2,233,680</td>
<td align="right">0.1%</td>
<td align="right">90.6%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_RANGE _ITER_NEXT_RANGE</td>
<td align="right">2,233,680</td>
<td align="right">0.1%</td>
<td align="right">90.7%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_RANGE _STORE_FAST_5</td>
<td align="right">2,233,680</td>
<td align="right">0.1%</td>
<td align="right">90.8%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW _GUARD_BOTH_INT</td>
<td align="right">2,233,680</td>
<td align="right">0.1%</td>
<td align="right">90.9%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_3 _COPY</td>
<td align="right">2,233,680</td>
<td align="right">0.1%</td>
<td align="right">91.0%</td>
</tr>
<tr>
<td align="left">_STORE_ATTR_INSTANCE_VALUE _LOAD_FAST_3</td>
<td align="right">2,233,680</td>
<td align="right">0.1%</td>
<td align="right">91.1%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_5 _LOAD_FAST_3</td>
<td align="right">2,233,680</td>
<td align="right">0.1%</td>
<td align="right">91.2%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_LIST_INT _JUMP_TO_TOP</td>
<td align="right">2,176,400</td>
<td align="right">0.1%</td>
<td align="right">91.3%</td>
</tr>
<tr>
<td align="left">_JUMP_TO_TOP _SET_IP</td>
<td align="right">2,176,400</td>
<td align="right">0.1%</td>
<td align="right">91.3%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_RANGE _DEOPT</td>
<td align="right">744,560</td>
<td align="right">0.0%</td>
<td align="right">91.4%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_LIST_INT _EXIT_TRACE</td>
<td align="right">111,680</td>
<td align="right">0.0%</td>
<td align="right">91.4%</td>
</tr>
<tr>
<td align="left">_START_EXECUTOR _LOAD_CONST_INLINE_BORROW</td>
<td align="right">111,680</td>
<td align="right">0.0%</td>
<td align="right">91.4%</td>
</tr>
<tr>
<td align="left">_STORE_ATTR_INSTANCE_VALUE _CHECK_FUNCTION</td>
<td align="right">111,680</td>
<td align="right">0.0%</td>
<td align="right">91.4%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_FALSE_POP _EXIT_TRACE</td>
<td align="right">300</td>
<td align="right">0.0%</td>
<td align="right">91.4%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NOT_NONE_POP _SIDE_EXIT</td>
<td align="right">300</td>
<td align="right">0.0%</td>
<td align="right">91.4%</td>
</tr>
</tbody>
</table>


</details>

### Unsupported opcodes

<details>
<summary> unsupported opcodes </summary>


</details>

### Optimizer errored out with opcode

<details>
<summary> Optimization stopped after encountering this opcode </summary>


</details>


</details>

## Rare events

<details>
<summary> Counts of rare/unlikely events </summary>

<table>
<thead>
<tr>
<th align="left">Event</th>
<th align="right">Count</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
set class
<details>
<summary>ⓘ</summary>

Setting an object's class, `obj.__class__ = ...`
</details>
</td>
<td align="right">0</td>
</tr>
<tr>
<td align="left">
set bases
<details>
<summary>ⓘ</summary>

Setting the bases of a class, `cls.__bases__ = ...`
</details>
</td>
<td align="right">0</td>
</tr>
<tr>
<td align="left">
set eval frame func
<details>
<summary>ⓘ</summary>

Setting the PEP 523 frame eval function `_PyInterpreterState_SetFrameEvalFunc()`
</details>
</td>
<td align="right">0</td>
</tr>
<tr>
<td align="left">
builtin dict
<details>
<summary>ⓘ</summary>

Modifying the builtins, `__builtins__.__dict__[var] = ...`
</details>
</td>
<td align="right">0</td>
</tr>
<tr>
<td align="left">
func modification
<details>
<summary>ⓘ</summary>

Modifying a function, e.g. `func.__defaults__ = ...`, etc.
</details>
</td>
<td align="right">0</td>
</tr>
<tr>
<td align="left">
watched dict modification
<details>
<summary>ⓘ</summary>

A watched dict has been modified
</details>
</td>
<td align="right">0</td>
</tr>
<tr>
<td align="left">
watched globals modification
<details>
<summary>ⓘ</summary>

A watched `globals()` dict has been modified
</details>
</td>
<td align="right">0</td>
</tr>
</tbody>
</table>


</details>

## Meta stats

<details>
<summary> Meta statistics </summary>

<table>
<thead>
<tr>
<th align="left"></th>
<th align="right">Count</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Number of data files</td>
<td align="right">20</td>
</tr>
</tbody>
</table>


</details>

---
Stats gathered on: 2024-04-21
