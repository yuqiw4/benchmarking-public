
# Pystats results

- benchmark: deltablue
- fork: python
- ref: 51aefc5bf907ddffaaf083ded0de773adcdf08c8
- commit hash: 51aefc5
- commit date: 2024-04-27T11:36:06+01:00

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
<td align="right">296,175,580</td>
<td align="right">18.8%</td>
<td align="right">18.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">231,347,040</td>
<td align="right">14.7%</td>
<td align="right">33.5%</td>
<td align="right">1.5%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">122,711,280</td>
<td align="right">7.8%</td>
<td align="right">41.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">115,836,420</td>
<td align="right">7.4%</td>
<td align="right">48.7%</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">82,722,920</td>
<td align="right">5.3%</td>
<td align="right">54.0%</td>
<td align="right">6.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">78,936,220</td>
<td align="right">5.0%</td>
<td align="right">59.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">76,766,880</td>
<td align="right">4.9%</td>
<td align="right">63.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">76,376,400</td>
<td align="right">4.9%</td>
<td align="right">68.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">72,302,320</td>
<td align="right">4.6%</td>
<td align="right">73.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">65,885,540</td>
<td align="right">4.2%</td>
<td align="right">77.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">55,572,460</td>
<td align="right">3.5%</td>
<td align="right">81.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">53,091,440</td>
<td align="right">3.4%</td>
<td align="right">84.4%</td>
<td align="right">3.5%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">52,570,600</td>
<td align="right">3.3%</td>
<td align="right">87.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">50,564,680</td>
<td align="right">3.2%</td>
<td align="right">91.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">20,108,300</td>
<td align="right">1.3%</td>
<td align="right">92.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">14,162,900</td>
<td align="right">0.9%</td>
<td align="right">93.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">13,416,260</td>
<td align="right">0.9%</td>
<td align="right">94.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">7,871,600</td>
<td align="right">0.5%</td>
<td align="right">94.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">6,969,880</td>
<td align="right">0.4%</td>
<td align="right">95.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">6,656,660</td>
<td align="right">0.4%</td>
<td align="right">95.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">6,021,020</td>
<td align="right">0.4%</td>
<td align="right">95.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">5,997,860</td>
<td align="right">0.4%</td>
<td align="right">96.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_INT</td>
<td align="right">5,857,980</td>
<td align="right">0.4%</td>
<td align="right">96.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">5,831,540</td>
<td align="right">0.4%</td>
<td align="right">96.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">5,351,160</td>
<td align="right">0.3%</td>
<td align="right">97.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">5,145,740</td>
<td align="right">0.3%</td>
<td align="right">97.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">4,644,040</td>
<td align="right">0.3%</td>
<td align="right">97.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">4,446,600</td>
<td align="right">0.3%</td>
<td align="right">98.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">4,446,600</td>
<td align="right">0.3%</td>
<td align="right">98.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">3,981,820</td>
<td align="right">0.3%</td>
<td align="right">98.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">3,702,580</td>
<td align="right">0.2%</td>
<td align="right">98.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">3,402,320</td>
<td align="right">0.2%</td>
<td align="right">99.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">3,402,020</td>
<td align="right">0.2%</td>
<td align="right">99.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">3,185,780</td>
<td align="right">0.2%</td>
<td align="right">99.5%</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">2,688,600</td>
<td align="right">0.2%</td>
<td align="right">99.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">1,318,140</td>
<td align="right">0.1%</td>
<td align="right">99.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">1,318,140</td>
<td align="right">0.1%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">796,160</td>
<td align="right">0.1%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">345,000</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">271,360</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">261,380</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">89,540</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">35,120</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">26,020</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">22,980</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">18,120</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">10,780</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">10,400</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">9,600</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">8,060</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_GLOBAL</td>
<td align="right">5,120</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">4,080</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">3,480</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">2,560</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">2,560</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">2,540</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">2,200</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BUILD_CONST_KEY_MAP</td>
<td align="right">1,620</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_DICT</td>
<td align="right">1,600</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">1,280</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">1,200</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right">58.3%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">720</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">520</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR</td>
<td align="right">440</td>
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
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">120</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">NOP</td>
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
<td align="left">BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">60</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">40</td>
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
<td align="right">156,205,540</td>
<td align="right">9.9%</td>
<td align="right">9.9%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK LOAD_FAST</td>
<td align="right">115,754,000</td>
<td align="right">7.4%</td>
<td align="right">17.3%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS RESUME_CHECK</td>
<td align="right">113,954,640</td>
<td align="right">7.2%</td>
<td align="right">24.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">77,160,860</td>
<td align="right">4.9%</td>
<td align="right">29.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES CALL_PY_EXACT_ARGS</td>
<td align="right">72,537,080</td>
<td align="right">4.6%</td>
<td align="right">34.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE LOAD_ATTR_CLASS</td>
<td align="right">65,885,300</td>
<td align="right">4.2%</td>
<td align="right">38.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE LOAD_GLOBAL_MODULE</td>
<td align="right">63,614,480</td>
<td align="right">4.0%</td>
<td align="right">42.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS COMPARE_OP_INT</td>
<td align="right">63,609,400</td>
<td align="right">4.0%</td>
<td align="right">46.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE RETURN_VALUE</td>
<td align="right">54,859,840</td>
<td align="right">3.5%</td>
<td align="right">49.8%</td>
</tr>
<tr>
<td align="left">RETURN_CONST POP_TOP</td>
<td align="right">47,396,340</td>
<td align="right">3.0%</td>
<td align="right">52.8%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE LOAD_FAST</td>
<td align="right">46,512,100</td>
<td align="right">3.0%</td>
<td align="right">55.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE LOAD_FAST</td>
<td align="right">45,397,880</td>
<td align="right">2.9%</td>
<td align="right">58.7%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT POP_JUMP_IF_FALSE</td>
<td align="right">42,096,240</td>
<td align="right">2.7%</td>
<td align="right">61.4%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE RETURN_CONST</td>
<td align="right">36,711,000</td>
<td align="right">2.3%</td>
<td align="right">63.7%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR CALL_PY_EXACT_ARGS</td>
<td align="right">31,316,720</td>
<td align="right">2.0%</td>
<td align="right">65.7%</td>
</tr>
<tr>
<td align="left">POP_TOP ENTER_EXECUTOR</td>
<td align="right">31,246,240</td>
<td align="right">2.0%</td>
<td align="right">67.7%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">28,510,600</td>
<td align="right">1.8%</td>
<td align="right">69.5%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">27,723,020</td>
<td align="right">1.8%</td>
<td align="right">71.2%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT ENTER_EXECUTOR</td>
<td align="right">25,125,000</td>
<td align="right">1.6%</td>
<td align="right">72.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">23,467,520</td>
<td align="right">1.5%</td>
<td align="right">74.3%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">21,840,780</td>
<td align="right">1.4%</td>
<td align="right">75.7%</td>
</tr>
<tr>
<td align="left">STORE_FAST LOAD_FAST</td>
<td align="right">17,426,000</td>
<td align="right">1.1%</td>
<td align="right">76.8%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR RETURN_VALUE</td>
<td align="right">12,379,380</td>
<td align="right">0.8%</td>
<td align="right">77.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">11,079,200</td>
<td align="right">0.7%</td>
<td align="right">78.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST CALL_PY_EXACT_ARGS</td>
<td align="right">10,372,020</td>
<td align="right">0.7%</td>
<td align="right">79.0%</td>
</tr>
<tr>
<td align="left">POP_TOP LOAD_FAST</td>
<td align="right">9,147,340</td>
<td align="right">0.6%</td>
<td align="right">79.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES LOAD_FAST</td>
<td align="right">9,069,620</td>
<td align="right">0.6%</td>
<td align="right">80.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL POP_JUMP_IF_FALSE</td>
<td align="right">9,006,780</td>
<td align="right">0.6%</td>
<td align="right">80.7%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE LOAD_FAST</td>
<td align="right">8,312,940</td>
<td align="right">0.5%</td>
<td align="right">81.2%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE STORE_FAST</td>
<td align="right">8,191,720</td>
<td align="right">0.5%</td>
<td align="right">81.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST ENTER_EXECUTOR</td>
<td align="right">8,105,120</td>
<td align="right">0.5%</td>
<td align="right">82.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">6,998,880</td>
<td align="right">0.4%</td>
<td align="right">82.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE STORE_FAST</td>
<td align="right">6,840,840</td>
<td align="right">0.4%</td>
<td align="right">83.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">6,458,100</td>
<td align="right">0.4%</td>
<td align="right">83.6%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE TO_BOOL_BOOL</td>
<td align="right">6,387,520</td>
<td align="right">0.4%</td>
<td align="right">84.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT LOAD_FAST</td>
<td align="right">5,854,780</td>
<td align="right">0.4%</td>
<td align="right">84.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_INT LOAD_FAST</td>
<td align="right">5,854,780</td>
<td align="right">0.4%</td>
<td align="right">84.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE BINARY_OP_ADD_INT</td>
<td align="right">5,854,760</td>
<td align="right">0.4%</td>
<td align="right">85.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE BINARY_OP_MULTIPLY_INT</td>
<td align="right">5,854,760</td>
<td align="right">0.4%</td>
<td align="right">85.5%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS RESUME_CHECK</td>
<td align="right">5,351,160</td>
<td align="right">0.3%</td>
<td align="right">85.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE LOAD_ATTR</td>
<td align="right">4,894,280</td>
<td align="right">0.3%</td>
<td align="right">86.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL POP_JUMP_IF_TRUE</td>
<td align="right">4,882,720</td>
<td align="right">0.3%</td>
<td align="right">86.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST COMPARE_OP_INT</td>
<td align="right">4,870,420</td>
<td align="right">0.3%</td>
<td align="right">86.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_LAZY_DICT LOAD_FAST</td>
<td align="right">4,699,160</td>
<td align="right">0.3%</td>
<td align="right">87.0%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE LOAD_FAST</td>
<td align="right">4,650,340</td>
<td align="right">0.3%</td>
<td align="right">87.3%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN LOAD_FAST</td>
<td align="right">4,456,820</td>
<td align="right">0.3%</td>
<td align="right">87.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT POP_JUMP_IF_FALSE</td>
<td align="right">4,446,600</td>
<td align="right">0.3%</td>
<td align="right">87.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST CALL_LEN</td>
<td align="right">4,446,480</td>
<td align="right">0.3%</td>
<td align="right">88.2%</td>
</tr>
<tr>
<td align="left">CALL_LEN TO_BOOL_INT</td>
<td align="right">4,446,480</td>
<td align="right">0.3%</td>
<td align="right">88.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST CALL_LIST_APPEND</td>
<td align="right">4,174,300</td>
<td align="right">0.3%</td>
<td align="right">88.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR LOAD_FAST</td>
<td align="right">4,094,800</td>
<td align="right">0.3%</td>
<td align="right">89.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT RETURN_VALUE</td>
<td align="right">4,048,800</td>
<td align="right">0.3%</td>
<td align="right">89.2%</td>
</tr>
<tr>
<td align="left">POP_TOP RETURN_CONST</td>
<td align="right">3,911,800</td>
<td align="right">0.2%</td>
<td align="right">89.5%</td>
</tr>
<tr>
<td align="left">COPY TO_BOOL_BOOL</td>
<td align="right">3,847,720</td>
<td align="right">0.2%</td>
<td align="right">89.7%</td>
</tr>
<tr>
<td align="left">POP_TOP LOAD_FAST_LOAD_FAST</td>
<td align="right">3,801,440</td>
<td align="right">0.2%</td>
<td align="right">90.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE LOAD_FAST</td>
<td align="right">3,690,200</td>
<td align="right">0.2%</td>
<td align="right">90.2%</td>
</tr>
<tr>
<td align="left">GET_ITER ENTER_EXECUTOR</td>
<td align="right">3,682,340</td>
<td align="right">0.2%</td>
<td align="right">90.4%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR RETURN_CONST</td>
<td align="right">3,464,680</td>
<td align="right">0.2%</td>
<td align="right">90.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">3,417,320</td>
<td align="right">0.2%</td>
<td align="right">90.9%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS RESUME_CHECK</td>
<td align="right">3,402,080</td>
<td align="right">0.2%</td>
<td align="right">91.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST LOAD_SUPER_ATTR_METHOD</td>
<td align="right">3,401,800</td>
<td align="right">0.2%</td>
<td align="right">91.3%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN LOAD_GLOBAL_MODULE</td>
<td align="right">3,401,800</td>
<td align="right">0.2%</td>
<td align="right">91.5%</td>
</tr>
<tr>
<td align="left">LOAD_CONST LOAD_FAST</td>
<td align="right">3,385,280</td>
<td align="right">0.2%</td>
<td align="right">91.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST RETURN_VALUE</td>
<td align="right">3,372,980</td>
<td align="right">0.2%</td>
<td align="right">92.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE COMPARE_OP_INT</td>
<td align="right">3,299,320</td>
<td align="right">0.2%</td>
<td align="right">92.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">3,299,080</td>
<td align="right">0.2%</td>
<td align="right">92.4%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK LOAD_GLOBAL_BUILTIN</td>
<td align="right">3,145,840</td>
<td align="right">0.2%</td>
<td align="right">92.6%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST STORE_FAST</td>
<td align="right">3,125,700</td>
<td align="right">0.2%</td>
<td align="right">92.8%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE LOAD_GLOBAL_MODULE</td>
<td align="right">3,098,940</td>
<td align="right">0.2%</td>
<td align="right">93.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE COPY</td>
<td align="right">3,074,700</td>
<td align="right">0.2%</td>
<td align="right">93.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST POP_JUMP_IF_NONE</td>
<td align="right">2,678,360</td>
<td align="right">0.2%</td>
<td align="right">93.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST GET_ITER</td>
<td align="right">2,621,520</td>
<td align="right">0.2%</td>
<td align="right">93.5%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE LOAD_CONST</td>
<td align="right">2,608,480</td>
<td align="right">0.2%</td>
<td align="right">93.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">2,603,400</td>
<td align="right">0.2%</td>
<td align="right">93.8%</td>
</tr>
<tr>
<td align="left">POP_TOP LOAD_GLOBAL_BUILTIN</td>
<td align="right">2,603,360</td>
<td align="right">0.2%</td>
<td align="right">94.0%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND RETURN_CONST</td>
<td align="right">2,593,240</td>
<td align="right">0.2%</td>
<td align="right">94.2%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE ENTER_EXECUTOR</td>
<td align="right">2,409,300</td>
<td align="right">0.2%</td>
<td align="right">94.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST LOAD_GLOBAL_MODULE</td>
<td align="right">2,362,020</td>
<td align="right">0.2%</td>
<td align="right">94.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE TO_BOOL_BOOL</td>
<td align="right">2,323,180</td>
<td align="right">0.1%</td>
<td align="right">94.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE POP_TOP</td>
<td align="right">2,301,640</td>
<td align="right">0.1%</td>
<td align="right">94.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS LOAD_FAST</td>
<td align="right">2,276,060</td>
<td align="right">0.1%</td>
<td align="right">94.9%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE RETURN_CONST</td>
<td align="right">2,097,200</td>
<td align="right">0.1%</td>
<td align="right">95.1%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE LOAD_FAST_LOAD_FAST</td>
<td align="right">2,058,140</td>
<td align="right">0.1%</td>
<td align="right">95.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST LOAD_ATTR</td>
<td align="right">2,057,780</td>
<td align="right">0.1%</td>
<td align="right">95.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR LOAD_FAST_LOAD_FAST</td>
<td align="right">2,051,960</td>
<td align="right">0.1%</td>
<td align="right">95.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">2,051,900</td>
<td align="right">0.1%</td>
<td align="right">95.6%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR ENTER_EXECUTOR</td>
<td align="right">1,854,180</td>
<td align="right">0.1%</td>
<td align="right">95.7%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE CALL</td>
<td align="right">1,852,340</td>
<td align="right">0.1%</td>
<td align="right">95.8%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND ENTER_EXECUTOR</td>
<td align="right">1,826,460</td>
<td align="right">0.1%</td>
<td align="right">95.9%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS COPY_FREE_VARS</td>
<td align="right">1,825,180</td>
<td align="right">0.1%</td>
<td align="right">96.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">1,821,540</td>
<td align="right">0.1%</td>
<td align="right">96.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">1,817,360</td>
<td align="right">0.1%</td>
<td align="right">96.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">1,810,740</td>
<td align="right">0.1%</td>
<td align="right">96.4%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">1,803,540</td>
<td align="right">0.1%</td>
<td align="right">96.5%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE LOAD_GLOBAL_MODULE</td>
<td align="right">1,790,280</td>
<td align="right">0.1%</td>
<td align="right">96.6%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK LOAD_GLOBAL_MODULE</td>
<td align="right">1,763,220</td>
<td align="right">0.1%</td>
<td align="right">96.7%</td>
</tr>
<tr>
<td align="left">CALL STORE_FAST</td>
<td align="right">1,605,420</td>
<td align="right">0.1%</td>
<td align="right">96.8%</td>
</tr>
<tr>
<td align="left">RETURN_CONST TO_BOOL_BOOL</td>
<td align="right">1,583,560</td>
<td align="right">0.1%</td>
<td align="right">96.9%</td>
</tr>
<tr>
<td align="left">CALL POP_TOP</td>
<td align="right">1,579,920</td>
<td align="right">0.1%</td>
<td align="right">97.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD CALL</td>
<td align="right">1,576,900</td>
<td align="right">0.1%</td>
<td align="right">97.1%</td>
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
<td align="left">COPY_FREE_VARS</td>
<td align="right">258,820</td>
<td align="right">99.0%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">2,540</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">20</td>
<td align="right">0.0%</td>
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
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">3,240</td>
<td align="right">93.1%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">200</td>
<td align="right">5.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">20</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">20</td>
<td align="right">0.6%</td>
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
<td align="right">3,160</td>
<td align="right">90.8%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">200</td>
<td align="right">5.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">80</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">20</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_DICT</td>
<td align="right">20</td>
<td align="right">0.6%</td>
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
<td align="right">1,318,140</td>
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
<td align="right">1,318,140</td>
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
<td align="left">LOAD_FAST</td>
<td align="right">2,621,520</td>
<td align="right">70.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">1,057,960</td>
<td align="right">28.6%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">22,920</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">120</td>
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
<td align="left">ENTER_EXECUTOR</td>
<td align="right">3,682,340</td>
<td align="right">99.5%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">12,040</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">7,940</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">260</td>
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
<td align="right">261,380</td>
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
<td align="left">POP_TOP</td>
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
<td align="left">LOAD_DEREF</td>
<td align="right">80</td>
<td align="right">100.0%</td>
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
<td align="left">RETURN_CONST</td>
<td align="right">47,396,340</td>
<td align="right">90.2%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">2,301,640</td>
<td align="right">4.4%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">1,579,920</td>
<td align="right">3.0%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">770,480</td>
<td align="right">1.5%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">512,000</td>
<td align="right">1.0%</td>
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
<td align="right">31,246,240</td>
<td align="right">59.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">9,147,340</td>
<td align="right">17.4%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">3,911,800</td>
<td align="right">7.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">3,801,440</td>
<td align="right">7.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">2,603,360</td>
<td align="right">5.0%</td>
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
<td align="right">560</td>
<td align="right">77.8%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">80</td>
<td align="right">11.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">60</td>
<td align="right">8.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">20</td>
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
<td align="left">CALL</td>
<td align="right">640</td>
<td align="right">88.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">80</td>
<td align="right">11.1%</td>
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
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">54,859,840</td>
<td align="right">71.5%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">12,379,380</td>
<td align="right">16.1%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">4,048,800</td>
<td align="right">5.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">3,372,980</td>
<td align="right">4.4%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">1,318,140</td>
<td align="right">1.7%</td>
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
<td align="right">28,510,600</td>
<td align="right">37.1%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">27,723,020</td>
<td align="right">36.1%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">8,191,720</td>
<td align="right">10.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">6,387,520</td>
<td align="right">8.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">4,650,340</td>
<td align="right">6.1%</td>
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
<td align="left">RETURN_VALUE</td>
<td align="right">540</td>
<td align="right">42.2%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">160</td>
<td align="right">12.5%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">140</td>
<td align="right">10.9%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">120</td>
<td align="right">9.4%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">120</td>
<td align="right">9.4%</td>
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
<td align="right">520</td>
<td align="right">40.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">460</td>
<td align="right">35.9%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">160</td>
<td align="right">12.5%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">120</td>
<td align="right">9.4%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">20</td>
<td align="right">1.6%</td>
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
<td align="right">271,340</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
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
<td align="left">LOAD_FAST</td>
<td align="right">271,360</td>
<td align="right">100.0%</td>
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
<td align="left">LOAD_FAST</td>
<td align="right">259,400</td>
<td align="right">75.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">84,520</td>
<td align="right">24.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">680</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">320</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
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
<td align="right">342,220</td>
<td align="right">99.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">1,700</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">680</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">100</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">60</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### BUILD_CONST_KEY_MAP

<details>
<summary> Successors and predecessors for BUILD_CONST_KEY_MAP </summary>

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
<td align="right">1,620</td>
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
<td align="left">STORE_FAST</td>
<td align="right">1,620</td>
<td align="right">100.0%</td>
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
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">1,852,340</td>
<td align="right">46.5%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">1,576,900</td>
<td align="right">39.6%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">541,500</td>
<td align="right">13.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">3,560</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">3,420</td>
<td align="right">0.1%</td>
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
<td align="right">1,605,420</td>
<td align="right">40.3%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">1,579,920</td>
<td align="right">39.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">788,560</td>
<td align="right">19.8%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">3,420</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">1,520</td>
<td align="right">0.0%</td>
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
<td align="left">LOAD_ATTR</td>
<td align="right">15,480</td>
<td align="right">44.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">12,220</td>
<td align="right">34.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">3,660</td>
<td align="right">10.4%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">2,680</td>
<td align="right">7.6%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">880</td>
<td align="right">2.5%</td>
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
<td align="right">19,820</td>
<td align="right">56.4%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">10,240</td>
<td align="right">29.2%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">3,680</td>
<td align="right">10.5%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">880</td>
<td align="right">2.5%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">420</td>
<td align="right">1.2%</td>
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
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">3,074,700</td>
<td align="right">66.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">796,160</td>
<td align="right">17.1%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">773,100</td>
<td align="right">16.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">60</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
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
<td align="left">TO_BOOL_BOOL</td>
<td align="right">3,847,720</td>
<td align="right">82.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">796,120</td>
<td align="right">17.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">160</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">40</td>
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
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">1,825,180</td>
<td align="right">53.6%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">1,318,140</td>
<td align="right">38.7%</td>
</tr>
<tr>
<td align="left">CACHE</td>
<td align="right">258,820</td>
<td align="right">7.6%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">100</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
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
<td align="left">RESUME_CHECK</td>
<td align="right">3,402,080</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">240</td>
<td align="right">0.0%</td>
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
<td align="left">POP_TOP</td>
<td align="right">31,246,240</td>
<td align="right">40.9%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">25,125,000</td>
<td align="right">32.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">8,105,120</td>
<td align="right">10.6%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">3,682,340</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">2,409,300</td>
<td align="right">3.2%</td>
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
<td align="right">31,316,720</td>
<td align="right">41.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">21,840,780</td>
<td align="right">28.6%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">12,379,380</td>
<td align="right">16.2%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">3,464,680</td>
<td align="right">4.5%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">1,854,180</td>
<td align="right">2.4%</td>
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
<td align="right">260</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">260</td>
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
<td align="left">STORE_FAST</td>
<td align="right">260</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">140</td>
<td align="right">26.9%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">120</td>
<td align="right">23.1%</td>
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
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">2,440</td>
<td align="right">30.3%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">1,660</td>
<td align="right">20.6%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">1,520</td>
<td align="right">18.9%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">1,300</td>
<td align="right">16.1%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">740</td>
<td align="right">9.2%</td>
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
<td align="left">FOR_ITER_LIST</td>
<td align="right">2,500</td>
<td align="right">31.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">2,140</td>
<td align="right">26.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,360</td>
<td align="right">16.9%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">1,200</td>
<td align="right">14.9%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">300</td>
<td align="right">3.7%</td>
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
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">10,740</td>
<td align="right">99.6%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
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
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">5,580</td>
<td align="right">51.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">5,200</td>
<td align="right">48.2%</td>
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
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">4,894,280</td>
<td align="right">70.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,057,780</td>
<td align="right">29.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">9,600</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">6,380</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">760</td>
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
<td align="right">4,094,800</td>
<td align="right">58.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">2,051,960</td>
<td align="right">29.4%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">783,120</td>
<td align="right">11.2%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">15,480</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">10,340</td>
<td align="right">0.1%</td>
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
<td align="right">2,608,480</td>
<td align="right">44.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">1,321,860</td>
<td align="right">22.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">801,220</td>
<td align="right">13.7%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">286,720</td>
<td align="right">4.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">279,800</td>
<td align="right">4.8%</td>
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
<td align="right">3,385,280</td>
<td align="right">58.1%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">1,321,800</td>
<td align="right">22.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">801,800</td>
<td align="right">13.7%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">261,080</td>
<td align="right">4.5%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">12,800</td>
<td align="right">0.2%</td>
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
<td align="left">RESUME_CHECK</td>
<td align="right">115,754,000</td>
<td align="right">39.1%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">46,512,100</td>
<td align="right">15.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">45,397,880</td>
<td align="right">15.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">17,426,000</td>
<td align="right">5.9%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">9,147,340</td>
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
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">156,205,540</td>
<td align="right">52.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">77,160,860</td>
<td align="right">26.1%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">11,079,200</td>
<td align="right">3.7%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">10,372,020</td>
<td align="right">3.5%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">8,105,120</td>
<td align="right">2.7%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_FAST_CHECK

<details>
<summary> Successors and predecessors for LOAD_FAST_CHECK </summary>

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
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">2,520</td>
<td align="right">98.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">40</td>
<td align="right">1.6%</td>
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
<td align="left">POP_TOP</td>
<td align="right">3,801,440</td>
<td align="right">28.3%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">2,058,140</td>
<td align="right">15.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">2,051,960</td>
<td align="right">15.3%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">1,297,920</td>
<td align="right">9.7%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">1,024,880</td>
<td align="right">7.6%</td>
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
<td align="right">6,458,100</td>
<td align="right">48.1%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">2,051,900</td>
<td align="right">15.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">1,810,740</td>
<td align="right">13.5%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">1,286,580</td>
<td align="right">9.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">518,620</td>
<td align="right">3.9%</td>
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
<td align="left">STORE_FAST</td>
<td align="right">680</td>
<td align="right">16.7%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">560</td>
<td align="right">13.7%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">500</td>
<td align="right">12.3%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">380</td>
<td align="right">9.3%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">380</td>
<td align="right">9.3%</td>
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
<td align="right">1,560</td>
<td align="right">38.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">760</td>
<td align="right">18.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">660</td>
<td align="right">16.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">480</td>
<td align="right">11.8%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">240</td>
<td align="right">5.9%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_SUPER_ATTR

<details>
<summary> Successors and predecessors for LOAD_SUPER_ATTR </summary>

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
<td align="right">440</td>
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
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">220</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">100</td>
<td align="right">22.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">60</td>
<td align="right">13.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">60</td>
<td align="right">13.6%</td>
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
<td align="right">42,096,240</td>
<td align="right">75.8%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">9,006,780</td>
<td align="right">16.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">4,446,600</td>
<td align="right">8.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">19,820</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">2,540</td>
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
<td align="right">46,512,100</td>
<td align="right">83.7%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">2,409,300</td>
<td align="right">4.3%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">2,301,640</td>
<td align="right">4.1%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">2,097,200</td>
<td align="right">3.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">1,790,280</td>
<td align="right">3.2%</td>
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
<td align="right">2,678,360</td>
<td align="right">99.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">10,220</td>
<td align="right">0.4%</td>
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
<td align="left">RETURN_CONST</td>
<td align="right">783,360</td>
<td align="right">29.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">599,480</td>
<td align="right">22.3%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">561,040</td>
<td align="right">20.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">488,320</td>
<td align="right">18.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">255,960</td>
<td align="right">9.5%</td>
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
<td align="right">4,882,720</td>
<td align="right">94.9%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">259,180</td>
<td align="right">5.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">3,680</td>
<td align="right">0.1%</td>
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
<td align="left">ENTER_EXECUTOR</td>
<td align="right">1,304,020</td>
<td align="right">25.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">1,297,920</td>
<td align="right">25.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,256,240</td>
<td align="right">24.4%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">773,120</td>
<td align="right">15.0%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">512,000</td>
<td align="right">9.9%</td>
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
<td align="right">36,711,000</td>
<td align="right">72.6%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">3,911,800</td>
<td align="right">7.7%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">3,464,680</td>
<td align="right">6.9%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">2,593,240</td>
<td align="right">5.1%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">2,097,200</td>
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
<td align="left">POP_TOP</td>
<td align="right">47,396,340</td>
<td align="right">93.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">1,583,560</td>
<td align="right">3.1%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">1,318,140</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">261,380</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">5,120</td>
<td align="right">0.0%</td>
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
<td align="right">1,220</td>
<td align="right">55.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">540</td>
<td align="right">24.5%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">120</td>
<td align="right">5.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">120</td>
<td align="right">5.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">120</td>
<td align="right">5.5%</td>
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
<td align="right">1,020</td>
<td align="right">46.4%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">380</td>
<td align="right">17.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">320</td>
<td align="right">14.5%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">160</td>
<td align="right">7.3%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">140</td>
<td align="right">6.4%</td>
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
<td align="left">RETURN_VALUE</td>
<td align="right">8,191,720</td>
<td align="right">40.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">6,840,840</td>
<td align="right">34.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">3,125,700</td>
<td align="right">15.5%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">1,605,420</td>
<td align="right">8.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">276,480</td>
<td align="right">1.4%</td>
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
<td align="right">17,426,000</td>
<td align="right">86.7%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">2,362,020</td>
<td align="right">11.7%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">259,440</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">30,520</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">14,480</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>


</details>

### STORE_FAST_STORE_FAST

<details>
<summary> Successors and predecessors for STORE_FAST_STORE_FAST </summary>

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
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">2,540</td>
<td align="right">99.2%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">20</td>
<td align="right">0.8%</td>
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
<td align="right">2,560</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### STORE_GLOBAL

<details>
<summary> Successors and predecessors for STORE_GLOBAL </summary>

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
<td align="right">5,080</td>
<td align="right">99.2%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">40</td>
<td align="right">0.8%</td>
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
<td align="right">2,560</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">2,520</td>
<td align="right">49.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">40</td>
<td align="right">0.8%</td>
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
<td align="right">796,140</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
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
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">796,120</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">40</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### UNPACK_SEQUENCE

<details>
<summary> Successors and predecessors for UNPACK_SEQUENCE </summary>

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
<td align="right">40</td>
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
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">20</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">20</td>
<td align="right">50.0%</td>
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
<td align="right">740</td>
<td align="right">61.7%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">240</td>
<td align="right">20.0%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">200</td>
<td align="right">16.7%</td>
</tr>
<tr>
<td align="left">CACHE</td>
<td align="right">20</td>
<td align="right">1.7%</td>
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
<td align="right">640</td>
<td align="right">53.3%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">380</td>
<td align="right">31.7%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">120</td>
<td align="right">10.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">40</td>
<td align="right">3.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">20</td>
<td align="right">1.7%</td>
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
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">5,854,760</td>
<td align="right">88.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">801,800</td>
<td align="right">12.0%</td>
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
<td align="left">LOAD_FAST</td>
<td align="right">5,854,780</td>
<td align="right">88.0%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">796,140</td>
<td align="right">12.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">3,160</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">2,520</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">40</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_OP_MULTIPLY_INT

<details>
<summary> Successors and predecessors for BINARY_OP_MULTIPLY_INT </summary>

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
<td align="right">5,854,760</td>
<td align="right">99.9%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">3,160</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
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
<td align="right">5,854,780</td>
<td align="right">99.9%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">3,200</td>
<td align="right">0.1%</td>
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
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">84,440</td>
<td align="right">94.3%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">5,040</td>
<td align="right">5.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">60</td>
<td align="right">0.1%</td>
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
<td align="right">84,460</td>
<td align="right">94.3%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">5,040</td>
<td align="right">5.6%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">40</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_SUBSCR_DICT

<details>
<summary> Successors and predecessors for BINARY_SUBSCR_DICT </summary>

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
<td align="right">1,580</td>
<td align="right">98.8%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">20</td>
<td align="right">1.2%</td>
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
<td align="right">1,600</td>
<td align="right">100.0%</td>
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
<td align="left">LOAD_ATTR</td>
<td align="right">783,120</td>
<td align="right">59.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">257,600</td>
<td align="right">19.5%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">254,240</td>
<td align="right">19.3%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">17,800</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">5,040</td>
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
<td align="left">COPY_FREE_VARS</td>
<td align="right">1,318,140</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### CALL_BOUND_METHOD_EXACT_ARGS

<details>
<summary> Successors and predecessors for CALL_BOUND_METHOD_EXACT_ARGS </summary>

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
<td align="right">3,299,080</td>
<td align="right">61.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">2,051,900</td>
<td align="right">38.3%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">180</td>
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
<td align="left">RESUME_CHECK</td>
<td align="right">5,351,160</td>
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
<td align="left">LOAD_CONST</td>
<td align="right">12,720</td>
<td align="right">55.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">5,040</td>
<td align="right">21.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,560</td>
<td align="right">11.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">2,520</td>
<td align="right">11.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">140</td>
<td align="right">0.6%</td>
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
<td align="right">22,920</td>
<td align="right">99.7%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">60</td>
<td align="right">0.3%</td>
</tr>
</tbody>
</table>


</details>

### CALL_LEN

<details>
<summary> Successors and predecessors for CALL_LEN </summary>

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
<td align="right">4,446,480</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">120</td>
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
<td align="left">TO_BOOL_INT</td>
<td align="right">4,446,480</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">120</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### CALL_LIST_APPEND

<details>
<summary> Successors and predecessors for CALL_LIST_APPEND </summary>

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
<td align="right">4,174,300</td>
<td align="right">69.6%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">1,308,920</td>
<td align="right">21.8%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">514,420</td>
<td align="right">8.6%</td>
</tr>
<tr>
<td align="left">CALL</td>
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
<td align="left">RETURN_CONST</td>
<td align="right">2,593,240</td>
<td align="right">43.2%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">1,826,460</td>
<td align="right">30.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">1,308,080</td>
<td align="right">21.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">268,680</td>
<td align="right">4.5%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">1,300</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### CALL_METHOD_DESCRIPTOR_FAST

<details>
<summary> Successors and predecessors for CALL_METHOD_DESCRIPTOR_FAST </summary>

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
<td align="left">ENTER_EXECUTOR</td>
<td align="right">1,803,540</td>
<td align="right">56.6%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">1,321,800</td>
<td align="right">41.5%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">60,080</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">300</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
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
<td align="right">3,125,700</td>
<td align="right">98.1%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">60,080</td>
<td align="right">1.9%</td>
</tr>
</tbody>
</table>


</details>

### CALL_METHOD_DESCRIPTOR_O

<details>
<summary> Successors and predecessors for CALL_METHOD_DESCRIPTOR_O </summary>

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
<td align="right">10,200</td>
<td align="right">98.1%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">180</td>
<td align="right">1.7%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">20</td>
<td align="right">0.2%</td>
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
<td align="left">POP_TOP</td>
<td align="right">10,220</td>
<td align="right">98.3%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">180</td>
<td align="right">1.7%</td>
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
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">72,537,080</td>
<td align="right">62.6%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">31,316,720</td>
<td align="right">27.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">10,372,020</td>
<td align="right">9.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">1,286,580</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">255,960</td>
<td align="right">0.2%</td>
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
<td align="right">113,954,640</td>
<td align="right">98.4%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">1,825,180</td>
<td align="right">1.6%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">56,400</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">200</td>
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
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">63,609,400</td>
<td align="right">88.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">4,870,420</td>
<td align="right">6.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">3,299,320</td>
<td align="right">4.6%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">261,080</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">258,520</td>
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
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">42,096,240</td>
<td align="right">58.2%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">25,125,000</td>
<td align="right">34.7%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">4,048,800</td>
<td align="right">5.6%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">773,100</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">259,180</td>
<td align="right">0.4%</td>
</tr>
</tbody>
</table>


</details>

### FOR_ITER_LIST

<details>
<summary> Successors and predecessors for FOR_ITER_LIST </summary>

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
<td align="right">12,040</td>
<td align="right">46.3%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">11,360</td>
<td align="right">43.7%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">2,500</td>
<td align="right">9.6%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">120</td>
<td align="right">0.5%</td>
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
<td align="right">13,080</td>
<td align="right">50.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">8,400</td>
<td align="right">32.3%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">2,880</td>
<td align="right">11.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">1,620</td>
<td align="right">6.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">40</td>
<td align="right">0.2%</td>
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
<td align="right">7,940</td>
<td align="right">43.8%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">7,900</td>
<td align="right">43.6%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">2,140</td>
<td align="right">11.8%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">140</td>
<td align="right">0.8%</td>
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
<td align="right">10,160</td>
<td align="right">56.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">3,840</td>
<td align="right">21.2%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">2,620</td>
<td align="right">14.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,380</td>
<td align="right">7.6%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">120</td>
<td align="right">0.7%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_ATTR_CLASS

<details>
<summary> Successors and predecessors for LOAD_ATTR_CLASS </summary>

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
<td align="right">65,885,300</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">240</td>
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
<td align="left">COMPARE_OP_INT</td>
<td align="right">63,609,400</td>
<td align="right">96.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,276,060</td>
<td align="right">3.5%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">80</td>
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
<td align="right">156,205,540</td>
<td align="right">67.5%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">28,510,600</td>
<td align="right">12.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">23,467,520</td>
<td align="right">10.1%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">21,840,780</td>
<td align="right">9.4%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">796,120</td>
<td align="right">0.3%</td>
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
<td align="right">63,614,480</td>
<td align="right">27.5%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">54,859,840</td>
<td align="right">23.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">45,397,880</td>
<td align="right">19.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">23,467,520</td>
<td align="right">10.1%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">6,998,880</td>
<td align="right">3.0%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_ATTR_METHOD_LAZY_DICT

<details>
<summary> Successors and predecessors for LOAD_ATTR_METHOD_LAZY_DICT </summary>

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
<td align="right">3,417,320</td>
<td align="right">56.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">2,603,400</td>
<td align="right">43.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">300</td>
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
<td align="right">4,699,160</td>
<td align="right">78.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">1,321,860</td>
<td align="right">22.0%</td>
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
<td align="right">77,160,860</td>
<td align="right">93.3%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">1,821,540</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">1,817,360</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">1,810,740</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">100,060</td>
<td align="right">0.1%</td>
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
<td align="right">72,537,080</td>
<td align="right">87.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">9,069,620</td>
<td align="right">11.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">1,015,320</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">100,060</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">840</td>
<td align="right">0.0%</td>
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

### LOAD_ATTR_SLOT

<details>
<summary> Successors and predecessors for LOAD_ATTR_SLOT </summary>

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
<td align="right">9,480</td>
<td align="right">98.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">120</td>
<td align="right">1.2%</td>
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
<td align="left">LOAD_ATTR</td>
<td align="right">9,600</td>
<td align="right">100.0%</td>
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
<td align="left">RESUME_CHECK</td>
<td align="right">3,145,840</td>
<td align="right">40.0%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">2,603,360</td>
<td align="right">33.1%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">1,308,080</td>
<td align="right">16.6%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">525,700</td>
<td align="right">6.7%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">255,960</td>
<td align="right">3.3%</td>
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
<td align="right">4,456,820</td>
<td align="right">56.6%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">3,401,800</td>
<td align="right">43.2%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">12,760</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">220</td>
<td align="right">0.0%</td>
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
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">63,614,480</td>
<td align="right">80.6%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">3,401,800</td>
<td align="right">4.3%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">3,098,940</td>
<td align="right">3.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">2,362,020</td>
<td align="right">3.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">1,790,280</td>
<td align="right">2.3%</td>
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
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">65,885,300</td>
<td align="right">83.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">4,894,280</td>
<td align="right">6.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">3,690,200</td>
<td align="right">4.7%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">1,852,340</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">1,821,540</td>
<td align="right">2.3%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_SUPER_ATTR_METHOD

<details>
<summary> Successors and predecessors for LOAD_SUPER_ATTR_METHOD </summary>

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
<td align="right">3,401,800</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR</td>
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
<td align="left">CALL</td>
<td align="right">1,576,900</td>
<td align="right">46.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,041,860</td>
<td align="right">30.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">527,300</td>
<td align="right">15.5%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">255,960</td>
<td align="right">7.5%</td>
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
<td align="right">113,954,640</td>
<td align="right">92.9%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">5,351,160</td>
<td align="right">4.4%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">3,402,080</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">CACHE</td>
<td align="right">2,540</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">860</td>
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
<td align="right">115,754,000</td>
<td align="right">94.3%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">3,145,840</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">1,763,220</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">1,024,880</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">997,400</td>
<td align="right">0.8%</td>
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
<td align="left">RETURN_VALUE</td>
<td align="right">27,723,020</td>
<td align="right">52.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">11,079,200</td>
<td align="right">20.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">6,998,880</td>
<td align="right">13.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">6,458,100</td>
<td align="right">12.2%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">796,120</td>
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
<td align="left">RETURN_CONST</td>
<td align="right">36,711,000</td>
<td align="right">69.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">8,312,940</td>
<td align="right">15.7%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">3,098,940</td>
<td align="right">5.8%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">2,608,480</td>
<td align="right">4.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">2,058,140</td>
<td align="right">3.9%</td>
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
<td align="right">6,387,520</td>
<td align="right">45.1%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">3,847,720</td>
<td align="right">27.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">2,323,180</td>
<td align="right">16.4%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">1,583,560</td>
<td align="right">11.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">20,400</td>
<td align="right">0.1%</td>
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
<td align="right">9,006,780</td>
<td align="right">63.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">4,882,720</td>
<td align="right">34.5%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">271,340</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">2,060</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### TO_BOOL_INT

<details>
<summary> Successors and predecessors for TO_BOOL_INT </summary>

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
<td align="left">CALL_LEN</td>
<td align="right">4,446,480</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">120</td>
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
<td align="right">4,446,600</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### UNPACK_SEQUENCE_TUPLE

<details>
<summary> Successors and predecessors for UNPACK_SEQUENCE_TUPLE </summary>

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
<td align="right">2,520</td>
<td align="right">99.2%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">20</td>
<td align="right">0.8%</td>
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
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">2,540</td>
<td align="right">100.0%</td>
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
<td align="right">344,080</td>
<td align="right">2.7%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">12,604,240</td>
<td align="right">97.3%</td>
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
<td align="right">240</td>
<td align="right">26.1%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">680</td>
<td align="right">73.9%</td>
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
<td align="left">remainder</td>
<td align="right">460</td>
<td align="right">67.6%</td>
</tr>
<tr>
<td align="left">true divide other</td>
<td align="right">220</td>
<td align="right">32.4%</td>
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
<td align="right">3,260</td>
<td align="right">64.2%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,600</td>
<td align="right">31.5%</td>
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
<td align="right">20</td>
<td align="right">9.1%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">200</td>
<td align="right">90.9%</td>
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
<td align="left">buffer int</td>
<td align="right">200</td>
<td align="right">100.0%</td>
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
<td align="right">10,052,080</td>
<td align="right">6.9%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">135,327,640</td>
<td align="right">93.0%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">6,192,860</td>
<td align="right">4.3%</td>
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
<td align="right">119,180</td>
<td align="right">97.2%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">3,420</td>
<td align="right">2.8%</td>
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
<td align="left">class mutable</td>
<td align="right">1,920</td>
<td align="right">56.1%</td>
</tr>
<tr>
<td align="left">operator wrapper</td>
<td align="right">1,060</td>
<td align="right">31.0%</td>
</tr>
<tr>
<td align="left">wrong number arguments</td>
<td align="right">260</td>
<td align="right">7.6%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">120</td>
<td align="right">3.5%</td>
</tr>
<tr>
<td align="left">cfunc noargs</td>
<td align="right">60</td>
<td align="right">1.8%</td>
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
<td align="right">33,820</td>
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
<td align="right">72,302,320</td>
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
<td align="right">420</td>
<td align="right">32.3%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">880</td>
<td align="right">67.7%</td>
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
<td align="left">baseobject</td>
<td align="right">700</td>
<td align="right">79.5%</td>
</tr>
<tr>
<td align="left">float long</td>
<td align="right">120</td>
<td align="right">13.6%</td>
</tr>
<tr>
<td align="left">different types</td>
<td align="right">60</td>
<td align="right">6.8%</td>
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
<td align="right">260</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">44,140</td>
<td align="right">98.8%</td>
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
<td align="right">260</td>
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
<td align="right">15,503,000</td>
<td align="right">3.9%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">377,279,240</td>
<td align="right">96.0%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">8,707,000</td>
<td align="right">2.2%</td>
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
<td align="right">168,220</td>
<td align="right">96.7%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">5,660</td>
<td align="right">3.3%</td>
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
<td align="left">class method obj</td>
<td align="right">2,880</td>
<td align="right">50.9%</td>
</tr>
<tr>
<td align="left">mutable class</td>
<td align="right">2,780</td>
<td align="right">49.1%</td>
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
<td align="right">2,040</td>
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
<td align="right">86,807,820</td>
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
<td align="right">2,040</td>
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

### LOAD_SUPER_ATTR

<details>
<summary> specialization stats for LOAD_SUPER_ATTR family </summary>

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
<td align="right">3,402,020</td>
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

### POP_JUMP_IF_FALSE

<details>
<summary> specialization stats for POP_JUMP_IF_FALSE family </summary>


</details>

### POP_JUMP_IF_NONE

<details>
<summary> specialization stats for POP_JUMP_IF_NONE family </summary>


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
<td align="right">1,829,980</td>
<td align="right">3.4%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">51,227,500</td>
<td align="right">96.5%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">1,863,940</td>
<td align="right">3.5%</td>
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
<td align="right">36,120</td>
<td align="right">99.9%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">40</td>
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
<td align="right">40</td>
<td align="right">100.0%</td>
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
<td align="right">640</td>
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
<td align="right">18,609,500</td>
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
<td align="right">640</td>
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

### UNPACK_SEQUENCE

<details>
<summary> specialization stats for UNPACK_SEQUENCE family </summary>

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
<td align="right">20</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">2,540</td>
<td align="right">98.4%</td>
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
<td align="right">20</td>
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
<td align="right">606,239,160</td>
<td align="right">38.5%</td>
</tr>
<tr>
<td align="left">
Not specialized
<details>
<summary>ⓘ</summary>

Instructions that could be specialized but aren't, e.g. `LOAD_ATTR`, `BINARY_SLICE`.
</details>
</td>
<td align="right">74,750,660</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">
Specialized hits
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that complete.
</details>
</td>
<td align="right">874,967,980</td>
<td align="right">55.6%</td>
</tr>
<tr>
<td align="left">
Specialized misses
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that deopt.
</details>
</td>
<td align="right">16,764,500</td>
<td align="right">1.1%</td>
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
<td align="right">15,503,000</td>
<td align="right">55.8%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">10,052,080</td>
<td align="right">36.2%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">1,829,980</td>
<td align="right">6.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">344,080</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">33,820</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">3,260</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">2,040</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">640</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">260</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR</td>
<td align="right">220</td>
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
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">5,309,580</td>
<td align="right">31.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">3,397,420</td>
<td align="right">20.3%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">3,185,780</td>
<td align="right">19.0%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">2,996,680</td>
<td align="right">17.9%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">1,863,940</td>
<td align="right">11.1%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">10,400</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">700</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">700</td>
<td align="right">0.0%</td>
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
<td align="right">261,380</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">Calls to Python functions inlined</td>
<td align="right">131,376,460</td>
<td align="right">99.8%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">261,380</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (vector)</td>
<td align="right">261,380</td>
<td align="right">0.2%</td>
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
<td align="right">261,380</td>
<td align="right">0.2%</td>
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
<td align="right">132,955,980</td>
<td align="right">101.0%</td>
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
<td align="right">1,929,740</td>
<td align="right">7.0%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">1,930,360</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">25,777,220</td>
<td align="right">93.0%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">25,775,700</td>
<td align="right">93.0%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">1,280</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Allocations over 4 kbytes</td>
<td align="right">240</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">27,226,279</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Inline values</td>
<td align="right">1,576,960</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Interpreter increfs</td>
<td align="right">1,028,554,560</td>
<td align="right">91.6%</td>
</tr>
<tr>
<td align="left">Interpreter decrefs</td>
<td align="right">1,096,223,720</td>
<td align="right">95.5%</td>
</tr>
<tr>
<td align="left">Increfs</td>
<td align="right">94,064,137</td>
<td align="right">8.4%</td>
</tr>
<tr>
<td align="left">Decrefs</td>
<td align="right">51,726,459</td>
<td align="right">4.5%</td>
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
<td align="right">68,000,296</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Method cache misses</td>
<td align="right">11,024</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">10,184</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">766,440</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Method cache dunder misses</td>
<td align="right">340</td>
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
<td align="right">1,788,240</td>
<td align="right">34,558,780</td>
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
<td align="right">13,480</td>
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
<td align="right">1,940</td>
<td align="right">14.4%</td>
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
<td align="right">9,880</td>
<td align="right">73.3%</td>
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
<td align="right">11,540</td>
<td align="right">85.6%</td>
</tr>
<tr>
<td align="left">
Inner loop found
<details>
<summary>ⓘ</summary>

A trace is truncated because it has an inner loop
</details>
</td>
<td align="right">320</td>
<td align="right">2.4%</td>
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
<td align="right">140</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">
Executors invalidated
<details>
<summary>ⓘ</summary>

The number of executors that were invalidated due to watched dictionary changes.
</details>
</td>
<td align="right">820</td>
<td align="right">42.3%</td>
</tr>
<tr>
<td align="left">
Traces executed
<details>
<summary>ⓘ</summary>

The number of traces that were executed
</details>
</td>
<td align="right">152,015,720</td>
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
<td align="right">1,132,470,860</td>
<td align="right">745.0%</td>
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
<td align="right">1,940</td>
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
<td align="right">1,940</td>
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
<td align="right">180</td>
<td align="right">9.3%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">420</td>
<td align="right">21.6%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">380</td>
<td align="right">19.6%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">300</td>
<td align="right">15.5%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">420</td>
<td align="right">21.6%</td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">240</td>
<td align="right">12.4%</td>
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
<td align="right">120</td>
<td align="right">6.2%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">420</td>
<td align="right">21.6%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">440</td>
<td align="right">22.7%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">200</td>
<td align="right">10.3%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">360</td>
<td align="right">18.6%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">280</td>
<td align="right">14.4%</td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">120</td>
<td align="right">6.2%</td>
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
<td align="right">2,307,720</td>
<td align="right">1.5%</td>
</tr>
<tr>
<td align="left"><= 4</td>
<td align="right">4,001,200</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left"><= 8</td>
<td align="right">88,523,000</td>
<td align="right">58.2%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">9,854,720</td>
<td align="right">6.5%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">7,034,280</td>
<td align="right">4.6%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">1,522,540</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">613,740</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">504,540</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">4,320</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left"><= 1,024</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left"><= 2,048</td>
<td align="right">40</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left"><= 4,096</td>
<td align="right">10,200</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left"><= 8,192</td>
<td align="right">2,000</td>
<td align="right">0.0%</td>
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
<td align="left">_START_EXECUTOR</td>
<td align="right">114,378,300</td>
<td align="right">10.1%</td>
<td align="right">10.1%</td>
<td align="right">2.0%</td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION</td>
<td align="right">94,595,960</td>
<td align="right">8.4%</td>
<td align="right">18.5%</td>
<td align="right">57.0%</td>
</tr>
<tr>
<td align="left">_SIDE_EXIT</td>
<td align="right">75,637,080</td>
<td align="right">6.7%</td>
<td align="right">25.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_SET_IP</td>
<td align="right">68,151,120</td>
<td align="right">6.0%</td>
<td align="right">31.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_0</td>
<td align="right">47,705,120</td>
<td align="right">4.2%</td>
<td align="right">35.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR</td>
<td align="right">41,850,600</td>
<td align="right">3.7%</td>
<td align="right">39.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_EXACT_ARGS</td>
<td align="right">40,242,140</td>
<td align="right">3.6%</td>
<td align="right">42.6%</td>
<td align="right">77.8%</td>
</tr>
<tr>
<td align="left">_DEOPT</td>
<td align="right">38,741,220</td>
<td align="right">3.4%</td>
<td align="right">46.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COLD_EXIT</td>
<td align="right">37,637,420</td>
<td align="right">3.3%</td>
<td align="right">49.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_IS_TRUE_POP</td>
<td align="right">37,630,060</td>
<td align="right">3.3%</td>
<td align="right">52.7%</td>
<td align="right">3.3%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_1</td>
<td align="right">35,878,900</td>
<td align="right">3.2%</td>
<td align="right">55.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_LIST</td>
<td align="right">34,188,500</td>
<td align="right">3.0%</td>
<td align="right">58.9%</td>
<td align="right">3.6%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_LIST</td>
<td align="right">34,188,500</td>
<td align="right">3.0%</td>
<td align="right">61.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_ITER_NEXT_LIST</td>
<td align="right">32,972,640</td>
<td align="right">2.9%</td>
<td align="right">64.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_1</td>
<td align="right">31,617,460</td>
<td align="right">2.8%</td>
<td align="right">67.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY_AND_SET_IP</td>
<td align="right">31,589,140</td>
<td align="right">2.8%</td>
<td align="right">70.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_MANAGED_OBJECT_HAS_VALUES</td>
<td align="right">29,077,400</td>
<td align="right">2.6%</td>
<td align="right">72.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE_0</td>
<td align="right">29,077,400</td>
<td align="right">2.6%</td>
<td align="right">75.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY</td>
<td align="right">22,068,360</td>
<td align="right">1.9%</td>
<td align="right">77.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_EXIT_TRACE</td>
<td align="right">15,570,920</td>
<td align="right">1.4%</td>
<td align="right">78.8%</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_INT</td>
<td align="right">15,502,780</td>
<td align="right">1.4%</td>
<td align="right">80.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_GLOBALS_VERSION</td>
<td align="right">15,023,160</td>
<td align="right">1.3%</td>
<td align="right">81.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_MODULE</td>
<td align="right">15,023,160</td>
<td align="right">1.3%</td>
<td align="right">82.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_INT</td>
<td align="right">14,497,400</td>
<td align="right">1.3%</td>
<td align="right">84.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_CLASS</td>
<td align="right">12,859,820</td>
<td align="right">1.1%</td>
<td align="right">85.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_CLASS_0</td>
<td align="right">12,859,820</td>
<td align="right">1.1%</td>
<td align="right">86.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_5</td>
<td align="right">11,936,540</td>
<td align="right">1.1%</td>
<td align="right">87.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_FOR_ITER_TIER_TWO</td>
<td align="right">8,980,780</td>
<td align="right">0.8%</td>
<td align="right">88.3%</td>
<td align="right">44.9%</td>
</tr>
<tr>
<td align="left">_RESUME_CHECK</td>
<td align="right">8,925,360</td>
<td align="right">0.8%</td>
<td align="right">89.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_PUSH_FRAME</td>
<td align="right">8,925,360</td>
<td align="right">0.8%</td>
<td align="right">89.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_SAVE_RETURN_OFFSET</td>
<td align="right">8,925,360</td>
<td align="right">0.8%</td>
<td align="right">90.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_5</td>
<td align="right">7,621,520</td>
<td align="right">0.7%</td>
<td align="right">91.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_IS_FALSE_POP</td>
<td align="right">7,271,360</td>
<td align="right">0.6%</td>
<td align="right">91.9%</td>
<td align="right">39.4%</td>
</tr>
<tr>
<td align="left">_GUARD_DORV_VALUES_INST_ATTR_FROM_DICT</td>
<td align="right">6,414,740</td>
<td align="right">0.6%</td>
<td align="right">92.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_KEYS_VERSION</td>
<td align="right">6,414,740</td>
<td align="right">0.6%</td>
<td align="right">93.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">6,414,740</td>
<td align="right">0.6%</td>
<td align="right">93.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_3</td>
<td align="right">6,237,940</td>
<td align="right">0.6%</td>
<td align="right">94.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_0</td>
<td align="right">5,849,660</td>
<td align="right">0.5%</td>
<td align="right">94.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_POP_FRAME</td>
<td align="right">5,624,420</td>
<td align="right">0.5%</td>
<td align="right">95.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COMPARE_OP</td>
<td align="right">5,475,720</td>
<td align="right">0.5%</td>
<td align="right">95.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE_OPERAND</td>
<td align="right">5,009,300</td>
<td align="right">0.4%</td>
<td align="right">96.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_JUMP_TO_TOP</td>
<td align="right">4,855,900</td>
<td align="right">0.4%</td>
<td align="right">96.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_2</td>
<td align="right">4,166,320</td>
<td align="right">0.4%</td>
<td align="right">96.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_METHOD_LAZY_DICT</td>
<td align="right">3,112,760</td>
<td align="right">0.3%</td>
<td align="right">97.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">3,112,760</td>
<td align="right">0.3%</td>
<td align="right">97.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW</td>
<td align="right">2,919,600</td>
<td align="right">0.3%</td>
<td align="right">97.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_DORV_NO_DICT</td>
<td align="right">1,997,880</td>
<td align="right">0.2%</td>
<td align="right">97.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">1,997,880</td>
<td align="right">0.2%</td>
<td align="right">98.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_4</td>
<td align="right">1,905,660</td>
<td align="right">0.2%</td>
<td align="right">98.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_2</td>
<td align="right">1,886,760</td>
<td align="right">0.2%</td>
<td align="right">98.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">1,803,840</td>
<td align="right">0.2%</td>
<td align="right">98.6%</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">_CHECK_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">1,604,180</td>
<td align="right">0.1%</td>
<td align="right">98.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">1,604,180</td>
<td align="right">0.1%</td>
<td align="right">98.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE</td>
<td align="right">1,521,420</td>
<td align="right">0.1%</td>
<td align="right">99.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_NOS_INT</td>
<td align="right">1,259,900</td>
<td align="right">0.1%</td>
<td align="right">99.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_1</td>
<td align="right">1,188,940</td>
<td align="right">0.1%</td>
<td align="right">99.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_RANGE</td>
<td align="right">1,130,680</td>
<td align="right">0.1%</td>
<td align="right">99.3%</td>
<td align="right">1.8%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_RANGE</td>
<td align="right">1,130,680</td>
<td align="right">0.1%</td>
<td align="right">99.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_ITER_NEXT_RANGE</td>
<td align="right">1,110,100</td>
<td align="right">0.1%</td>
<td align="right">99.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_6</td>
<td align="right">1,051,100</td>
<td align="right">0.1%</td>
<td align="right">99.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_POP_TOP</td>
<td align="right">542,960</td>
<td align="right">0.0%</td>
<td align="right">99.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_4</td>
<td align="right">519,820</td>
<td align="right">0.0%</td>
<td align="right">99.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP</td>
<td align="right">511,200</td>
<td align="right">0.0%</td>
<td align="right">99.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_INT</td>
<td align="right">508,680</td>
<td align="right">0.0%</td>
<td align="right">99.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_MULTIPLY_INT</td>
<td align="right">508,680</td>
<td align="right">0.0%</td>
<td align="right">99.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR</td>
<td align="right">503,640</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GET_ITER</td>
<td align="right">355,100</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST</td>
<td align="right">254,320</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_3</td>
<td align="right">192,340</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_2</td>
<td align="right">187,460</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL_BOOL</td>
<td align="right">125,760</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_IS_NOT_NONE_POP</td>
<td align="right">103,660</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right">48.3%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NONE_POP</td>
<td align="right">77,500</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_SLOT_0</td>
<td align="right">51,720</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION</td>
<td align="right">14,800</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_WITH_NULL</td>
<td align="right">12,940</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COPY</td>
<td align="right">12,600</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BUILD_CONST_KEY_MAP</td>
<td align="right">8,620</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_DICT</td>
<td align="right">8,620</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_6</td>
<td align="right">8,620</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_TOS_INT</td>
<td align="right">5,040</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_PUSH_NULL</td>
<td align="right">2,160</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_0</td>
<td align="right">2,160</td>
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
<td align="left">_GUARD_TYPE_VERSION _SIDE_EXIT</td>
<td align="right">53,941,460</td>
<td align="right">4.8%</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_0 _GUARD_TYPE_VERSION</td>
<td align="right">47,133,660</td>
<td align="right">4.2%</td>
<td align="right">8.9%</td>
</tr>
<tr>
<td align="left">_START_EXECUTOR _SET_IP</td>
<td align="right">45,095,080</td>
<td align="right">4.0%</td>
<td align="right">12.9%</td>
</tr>
<tr>
<td align="left">_SET_IP _LOAD_ATTR</td>
<td align="right">41,850,600</td>
<td align="right">3.7%</td>
<td align="right">16.6%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_LIST _GUARD_NOT_EXHAUSTED_LIST</td>
<td align="right">34,188,500</td>
<td align="right">3.0%</td>
<td align="right">19.6%</td>
</tr>
<tr>
<td align="left">_START_EXECUTOR _ITER_CHECK_LIST</td>
<td align="right">33,312,060</td>
<td align="right">2.9%</td>
<td align="right">22.6%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_LIST _ITER_NEXT_LIST</td>
<td align="right">32,972,640</td>
<td align="right">2.9%</td>
<td align="right">25.5%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_1 _GUARD_TYPE_VERSION</td>
<td align="right">32,739,420</td>
<td align="right">2.9%</td>
<td align="right">28.4%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_TRUE_POP _LOAD_FAST_0</td>
<td align="right">32,130,800</td>
<td align="right">2.8%</td>
<td align="right">31.2%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY_AND_SET_IP _CHECK_FUNCTION_EXACT_ARGS</td>
<td align="right">31,589,140</td>
<td align="right">2.8%</td>
<td align="right">34.0%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR _CHECK_VALIDITY_AND_SET_IP</td>
<td align="right">31,589,140</td>
<td align="right">2.8%</td>
<td align="right">36.8%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_1 _LOAD_FAST_1</td>
<td align="right">31,137,560</td>
<td align="right">2.7%</td>
<td align="right">39.5%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_LIST _STORE_FAST_1</td>
<td align="right">31,123,020</td>
<td align="right">2.7%</td>
<td align="right">42.3%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_EXACT_ARGS _DEOPT</td>
<td align="right">30,592,880</td>
<td align="right">2.7%</td>
<td align="right">45.0%</td>
</tr>
<tr>
<td align="left">_CHECK_MANAGED_OBJECT_HAS_VALUES _LOAD_ATTR_INSTANCE_VALUE_0</td>
<td align="right">29,077,400</td>
<td align="right">2.6%</td>
<td align="right">47.5%</td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION _CHECK_MANAGED_OBJECT_HAS_VALUES</td>
<td align="right">29,077,400</td>
<td align="right">2.6%</td>
<td align="right">50.1%</td>
</tr>
<tr>
<td align="left">_START_EXECUTOR _GUARD_IS_TRUE_POP</td>
<td align="right">25,601,740</td>
<td align="right">2.3%</td>
<td align="right">52.4%</td>
</tr>
<tr>
<td align="left">_EXIT_TRACE _SIDE_EXIT</td>
<td align="right">15,570,920</td>
<td align="right">1.4%</td>
<td align="right">53.8%</td>
</tr>
<tr>
<td align="left">_GUARD_GLOBALS_VERSION _LOAD_GLOBAL_MODULE</td>
<td align="right">15,023,160</td>
<td align="right">1.3%</td>
<td align="right">55.1%</td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_INT _COMPARE_OP_INT</td>
<td align="right">14,492,360</td>
<td align="right">1.3%</td>
<td align="right">56.4%</td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_CLASS _LOAD_ATTR_CLASS_0</td>
<td align="right">12,859,820</td>
<td align="right">1.1%</td>
<td align="right">57.5%</td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_MODULE _CHECK_ATTR_CLASS</td>
<td align="right">12,385,280</td>
<td align="right">1.1%</td>
<td align="right">58.6%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_CLASS_0 _GUARD_BOTH_INT</td>
<td align="right">11,800,360</td>
<td align="right">1.0%</td>
<td align="right">59.6%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE_0 _EXIT_TRACE</td>
<td align="right">11,052,040</td>
<td align="right">1.0%</td>
<td align="right">60.6%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR _CHECK_VALIDITY</td>
<td align="right">10,261,460</td>
<td align="right">0.9%</td>
<td align="right">61.5%</td>
</tr>
<tr>
<td align="left">_SET_IP _FOR_ITER_TIER_TWO</td>
<td align="right">8,980,780</td>
<td align="right">0.8%</td>
<td align="right">62.3%</td>
</tr>
<tr>
<td align="left">_PUSH_FRAME _RESUME_CHECK</td>
<td align="right">8,925,360</td>
<td align="right">0.8%</td>
<td align="right">63.1%</td>
</tr>
<tr>
<td align="left">_SAVE_RETURN_OFFSET _PUSH_FRAME</td>
<td align="right">8,925,360</td>
<td align="right">0.8%</td>
<td align="right">63.9%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_INT _GUARD_IS_TRUE_POP</td>
<td align="right">8,281,220</td>
<td align="right">0.7%</td>
<td align="right">64.6%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY _GUARD_GLOBALS_VERSION</td>
<td align="right">7,967,580</td>
<td align="right">0.7%</td>
<td align="right">65.3%</td>
</tr>
<tr>
<td align="left">_SET_IP _CHECK_FUNCTION_EXACT_ARGS</td>
<td align="right">7,048,820</td>
<td align="right">0.6%</td>
<td align="right">65.9%</td>
</tr>
<tr>
<td align="left">_RESUME_CHECK _LOAD_FAST_0</td>
<td align="right">6,802,360</td>
<td align="right">0.6%</td>
<td align="right">66.5%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_5 _LOAD_FAST_5</td>
<td align="right">6,505,900</td>
<td align="right">0.6%</td>
<td align="right">67.1%</td>
</tr>
<tr>
<td align="left">_GUARD_DORV_VALUES_INST_ATTR_FROM_DICT _GUARD_KEYS_VERSION</td>
<td align="right">6,414,740</td>
<td align="right">0.6%</td>
<td align="right">67.7%</td>
</tr>
<tr>
<td align="left">_GUARD_KEYS_VERSION _LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">6,414,740</td>
<td align="right">0.6%</td>
<td align="right">68.2%</td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION _GUARD_DORV_VALUES_INST_ATTR_FROM_DICT</td>
<td align="right">6,414,740</td>
<td align="right">0.6%</td>
<td align="right">68.8%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_0 _SAVE_RETURN_OFFSET</td>
<td align="right">5,849,660</td>
<td align="right">0.5%</td>
<td align="right">69.3%</td>
</tr>
<tr>
<td align="left">_SET_IP _COMPARE_OP</td>
<td align="right">5,475,720</td>
<td align="right">0.5%</td>
<td align="right">69.8%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP _CHECK_VALIDITY</td>
<td align="right">5,475,720</td>
<td align="right">0.5%</td>
<td align="right">70.3%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY _GUARD_IS_FALSE_POP</td>
<td align="right">5,472,040</td>
<td align="right">0.5%</td>
<td align="right">70.8%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY _STORE_FAST_5</td>
<td align="right">5,172,760</td>
<td align="right">0.5%</td>
<td align="right">71.2%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_WITH_VALUES _SET_IP</td>
<td align="right">5,114,980</td>
<td align="right">0.5%</td>
<td align="right">71.7%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_EXACT_ARGS _CHECK_STACK_SPACE_OPERAND</td>
<td align="right">5,009,300</td>
<td align="right">0.4%</td>
<td align="right">72.1%</td>
</tr>
<tr>
<td align="left">_FOR_ITER_TIER_TWO _CHECK_VALIDITY</td>
<td align="right">4,944,000</td>
<td align="right">0.4%</td>
<td align="right">72.6%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_3 _SET_IP</td>
<td align="right">4,424,620</td>
<td align="right">0.4%</td>
<td align="right">73.0%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_5 _LOAD_FAST_3</td>
<td align="right">4,424,620</td>
<td align="right">0.4%</td>
<td align="right">73.3%</td>
</tr>
<tr>
<td align="left">_JUMP_TO_TOP _SET_IP</td>
<td align="right">4,080,400</td>
<td align="right">0.4%</td>
<td align="right">73.7%</td>
</tr>
<tr>
<td align="left">_FOR_ITER_TIER_TWO _DEOPT</td>
<td align="right">4,036,780</td>
<td align="right">0.4%</td>
<td align="right">74.1%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_INT _POP_FRAME</td>
<td align="right">3,901,240</td>
<td align="right">0.3%</td>
<td align="right">74.4%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE_0 _GUARD_TYPE_VERSION</td>
<td align="right">3,725,120</td>
<td align="right">0.3%</td>
<td align="right">74.7%</td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE_OPERAND _INIT_CALL_PY_EXACT_ARGS_0</td>
<td align="right">3,673,460</td>
<td align="right">0.3%</td>
<td align="right">75.1%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_2 _GUARD_TYPE_VERSION</td>
<td align="right">3,641,100</td>
<td align="right">0.3%</td>
<td align="right">75.4%</td>
</tr>
<tr>
<td align="left">_POP_FRAME _GUARD_IS_TRUE_POP</td>
<td align="right">3,638,200</td>
<td align="right">0.3%</td>
<td align="right">75.7%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_FALSE_POP _JUMP_TO_TOP</td>
<td align="right">3,615,920</td>
<td align="right">0.3%</td>
<td align="right">76.0%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_5 _GUARD_TYPE_VERSION</td>
<td align="right">3,401,560</td>
<td align="right">0.3%</td>
<td align="right">76.3%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE_0 _GUARD_GLOBALS_VERSION</td>
<td align="right">3,370,200</td>
<td align="right">0.3%</td>
<td align="right">76.6%</td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_METHOD_LAZY_DICT _LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">3,112,760</td>
<td align="right">0.3%</td>
<td align="right">76.9%</td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION _CHECK_ATTR_METHOD_LAZY_DICT</td>
<td align="right">3,112,760</td>
<td align="right">0.3%</td>
<td align="right">77.2%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_FALSE_POP _SIDE_EXIT</td>
<td align="right">2,861,660</td>
<td align="right">0.3%</td>
<td align="right">77.4%</td>
</tr>
<tr>
<td align="left">_START_EXECUTOR _LOAD_FAST_0</td>
<td align="right">2,495,460</td>
<td align="right">0.2%</td>
<td align="right">77.6%</td>
</tr>
<tr>
<td align="left">_START_EXECUTOR _DEOPT</td>
<td align="right">2,307,720</td>
<td align="right">0.2%</td>
<td align="right">77.8%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_EXACT_ARGS _INIT_CALL_PY_EXACT_ARGS_0</td>
<td align="right">2,176,200</td>
<td align="right">0.2%</td>
<td align="right">78.0%</td>
</tr>
<tr>
<td align="left">_GUARD_DORV_NO_DICT _STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">1,997,880</td>
<td align="right">0.2%</td>
<td align="right">78.2%</td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION _GUARD_DORV_NO_DICT</td>
<td align="right">1,997,880</td>
<td align="right">0.2%</td>
<td align="right">78.4%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE_0 _SET_IP</td>
<td align="right">1,961,600</td>
<td align="right">0.2%</td>
<td align="right">78.6%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_2 _SAVE_RETURN_OFFSET</td>
<td align="right">1,886,760</td>
<td align="right">0.2%</td>
<td align="right">78.7%</td>
</tr>
<tr>
<td align="left">_START_EXECUTOR _LOAD_FAST_5</td>
<td align="right">1,869,320</td>
<td align="right">0.2%</td>
<td align="right">78.9%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_LIST _STORE_FAST_5</td>
<td align="right">1,849,620</td>
<td align="right">0.2%</td>
<td align="right">79.1%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_TRUE_POP _GUARD_GLOBALS_VERSION</td>
<td align="right">1,824,800</td>
<td align="right">0.2%</td>
<td align="right">79.2%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_5 _EXIT_TRACE</td>
<td align="right">1,806,280</td>
<td align="right">0.2%</td>
<td align="right">79.4%</td>
</tr>
<tr>
<td align="left">_SET_IP _CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">1,803,840</td>
<td align="right">0.2%</td>
<td align="right">79.5%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST _DEOPT</td>
<td align="right">1,803,840</td>
<td align="right">0.2%</td>
<td align="right">79.7%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_LAZY_DICT _LOAD_CONST_INLINE_BORROW</td>
<td align="right">1,803,840</td>
<td align="right">0.2%</td>
<td align="right">79.9%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW _SET_IP</td>
<td align="right">1,803,840</td>
<td align="right">0.2%</td>
<td align="right">80.0%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_INT _EXIT_TRACE</td>
<td align="right">1,800,940</td>
<td align="right">0.2%</td>
<td align="right">80.2%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE_0 _LOAD_FAST_0</td>
<td align="right">1,796,300</td>
<td align="right">0.2%</td>
<td align="right">80.3%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY _LOAD_FAST_0</td>
<td align="right">1,640,980</td>
<td align="right">0.1%</td>
<td align="right">80.5%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_3 _GUARD_TYPE_VERSION</td>
<td align="right">1,618,820</td>
<td align="right">0.1%</td>
<td align="right">80.6%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE_0 _LOAD_FAST_1</td>
<td align="right">1,607,200</td>
<td align="right">0.1%</td>
<td align="right">80.8%</td>
</tr>
<tr>
<td align="left">_SET_IP _CHECK_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">1,604,180</td>
<td align="right">0.1%</td>
<td align="right">80.9%</td>
</tr>
<tr>
<td align="left">_CHECK_CALL_BOUND_METHOD_EXACT_ARGS _INIT_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">1,604,180</td>
<td align="right">0.1%</td>
<td align="right">81.1%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_BOUND_METHOD_EXACT_ARGS _CHECK_FUNCTION_EXACT_ARGS</td>
<td align="right">1,604,180</td>
<td align="right">0.1%</td>
<td align="right">81.2%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE_0 _LOAD_FAST_2</td>
<td align="right">1,604,180</td>
<td align="right">0.1%</td>
<td align="right">81.3%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE_0 _GUARD_BOTH_INT</td>
<td align="right">1,602,920</td>
<td align="right">0.1%</td>
<td align="right">81.5%</td>
</tr>
<tr>
<td align="left">_RESUME_CHECK _LOAD_FAST_1</td>
<td align="right">1,599,540</td>
<td align="right">0.1%</td>
<td align="right">81.6%</td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_MODULE _SET_IP</td>
<td align="right">1,576,100</td>
<td align="right">0.1%</td>
<td align="right">81.8%</td>
</tr>
<tr>
<td align="left">_START_EXECUTOR _LOAD_FAST_3</td>
<td align="right">1,540,160</td>
<td align="right">0.1%</td>
<td align="right">81.9%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_INT _GUARD_IS_FALSE_POP</td>
<td align="right">1,519,380</td>
<td align="right">0.1%</td>
<td align="right">82.0%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_1 _SET_IP</td>
<td align="right">1,421,220</td>
<td align="right">0.1%</td>
<td align="right">82.2%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_LAZY_DICT _LOAD_FAST_5</td>
<td align="right">1,297,740</td>
<td align="right">0.1%</td>
<td align="right">82.3%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_TRUE_POP _SIDE_EXIT</td>
<td align="right">1,251,920</td>
<td align="right">0.1%</td>
<td align="right">82.4%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_EXACT_ARGS _INIT_CALL_PY_EXACT_ARGS_2</td>
<td align="right">1,229,240</td>
<td align="right">0.1%</td>
<td align="right">82.5%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_LIST _SIDE_EXIT</td>
<td align="right">1,215,860</td>
<td align="right">0.1%</td>
<td align="right">82.6%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_1 _SAVE_RETURN_OFFSET</td>
<td align="right">1,188,940</td>
<td align="right">0.1%</td>
<td align="right">82.7%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE_0 _POP_FRAME</td>
<td align="right">1,177,900</td>
<td align="right">0.1%</td>
<td align="right">82.8%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_RANGE _GUARD_NOT_EXHAUSTED_RANGE</td>
<td align="right">1,130,680</td>
<td align="right">0.1%</td>
<td align="right">82.9%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_RANGE _ITER_NEXT_RANGE</td>
<td align="right">1,110,100</td>
<td align="right">0.1%</td>
<td align="right">83.0%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_1 _GUARD_BOTH_INT</td>
<td align="right">1,094,120</td>
<td align="right">0.1%</td>
<td align="right">83.1%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_CLASS_0 _LOAD_FAST_0</td>
<td align="right">1,059,460</td>
<td align="right">0.1%</td>
<td align="right">83.2%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_5 _LOAD_FAST_6</td>
<td align="right">1,042,480</td>
<td align="right">0.1%</td>
<td align="right">83.3%</td>
</tr>
</tbody>
</table>


</details>

### Unsupported opcodes

<details>
<summary> unsupported opcodes </summary>

<table>
<thead>
<tr>
<th align="left">Opcode</th>
<th align="right">Count</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL</td>
<td align="right">2,220</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">300</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">100</td>
</tr>
</tbody>
</table>


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
<td align="right">120</td>
</tr>
<tr>
<td align="left">
watched globals modification
<details>
<summary>ⓘ</summary>

A watched `globals()` dict has been modified
</details>
</td>
<td align="right">120</td>
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
Stats gathered on: 2024-04-28
