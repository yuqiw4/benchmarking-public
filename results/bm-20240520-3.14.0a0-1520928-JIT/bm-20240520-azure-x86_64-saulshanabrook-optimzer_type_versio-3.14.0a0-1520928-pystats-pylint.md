
# Pystats results

- benchmark: pylint
- fork: saulshanabrook
- ref: optimzer-type-version
- commit hash: 1520928
- commit date: 2024-05-20T16:55:29-04:00

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
<td align="right">267,930,491</td>
<td align="right">16.1%</td>
<td align="right">16.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">85,357,776</td>
<td align="right">5.1%</td>
<td align="right">21.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">69,151,929</td>
<td align="right">4.2%</td>
<td align="right">25.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">64,689,610</td>
<td align="right">3.9%</td>
<td align="right">29.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">61,050,953</td>
<td align="right">3.7%</td>
<td align="right">32.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">59,926,186</td>
<td align="right">3.6%</td>
<td align="right">36.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">54,456,482</td>
<td align="right">3.3%</td>
<td align="right">39.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">52,960,260</td>
<td align="right">3.2%</td>
<td align="right">43.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">50,509,653</td>
<td align="right">3.0%</td>
<td align="right">46.0%</td>
<td align="right">9.5%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">50,035,840</td>
<td align="right">3.0%</td>
<td align="right">49.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">46,084,416</td>
<td align="right">2.8%</td>
<td align="right">51.8%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">43,712,178</td>
<td align="right">2.6%</td>
<td align="right">54.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">41,020,991</td>
<td align="right">2.5%</td>
<td align="right">56.9%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">40,661,106</td>
<td align="right">2.4%</td>
<td align="right">59.4%</td>
<td align="right">19.9%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">35,905,797</td>
<td align="right">2.2%</td>
<td align="right">61.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">32,133,248</td>
<td align="right">1.9%</td>
<td align="right">63.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">30,946,946</td>
<td align="right">1.9%</td>
<td align="right">65.3%</td>
<td align="right">47.3%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">29,260,640</td>
<td align="right">1.8%</td>
<td align="right">67.1%</td>
<td align="right">40.4%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">27,234,867</td>
<td align="right">1.6%</td>
<td align="right">68.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">26,109,200</td>
<td align="right">1.6%</td>
<td align="right">70.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">23,113,048</td>
<td align="right">1.4%</td>
<td align="right">71.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">21,720,035</td>
<td align="right">1.3%</td>
<td align="right">73.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">21,499,300</td>
<td align="right">1.3%</td>
<td align="right">74.3%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">21,378,642</td>
<td align="right">1.3%</td>
<td align="right">75.5%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">19,767,300</td>
<td align="right">1.2%</td>
<td align="right">76.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">16,459,420</td>
<td align="right">1.0%</td>
<td align="right">77.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">16,456,580</td>
<td align="right">1.0%</td>
<td align="right">78.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">16,129,240</td>
<td align="right">1.0%</td>
<td align="right">79.7%</td>
<td align="right">21.0%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">15,435,940</td>
<td align="right">0.9%</td>
<td align="right">80.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">12,359,123</td>
<td align="right">0.7%</td>
<td align="right">81.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">12,203,741</td>
<td align="right">0.7%</td>
<td align="right">82.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">END_SEND</td>
<td align="right">10,600,500</td>
<td align="right">0.6%</td>
<td align="right">82.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">10,495,860</td>
<td align="right">0.6%</td>
<td align="right">83.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">GET_YIELD_FROM_ITER</td>
<td align="right">10,136,220</td>
<td align="right">0.6%</td>
<td align="right">84.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">10,002,040</td>
<td align="right">0.6%</td>
<td align="right">84.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">9,469,300</td>
<td align="right">0.6%</td>
<td align="right">85.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">9,281,940</td>
<td align="right">0.6%</td>
<td align="right">85.7%</td>
<td align="right">7.7%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">8,509,520</td>
<td align="right">0.5%</td>
<td align="right">86.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">8,222,634</td>
<td align="right">0.5%</td>
<td align="right">86.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">8,140,660</td>
<td align="right">0.5%</td>
<td align="right">87.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">6,862,740</td>
<td align="right">0.4%</td>
<td align="right">87.6%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">6,857,680</td>
<td align="right">0.4%</td>
<td align="right">88.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">6,333,760</td>
<td align="right">0.4%</td>
<td align="right">88.4%</td>
<td align="right">6.7%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_DICT</td>
<td align="right">6,287,840</td>
<td align="right">0.4%</td>
<td align="right">88.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">END_FOR</td>
<td align="right">6,239,340</td>
<td align="right">0.4%</td>
<td align="right">89.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">6,127,900</td>
<td align="right">0.4%</td>
<td align="right">89.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">5,986,820</td>
<td align="right">0.4%</td>
<td align="right">89.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">5,739,659</td>
<td align="right">0.3%</td>
<td align="right">90.2%</td>
<td align="right">8.9%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">5,418,906</td>
<td align="right">0.3%</td>
<td align="right">90.5%</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">5,002,140</td>
<td align="right">0.3%</td>
<td align="right">90.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">4,975,280</td>
<td align="right">0.3%</td>
<td align="right">91.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">4,879,520</td>
<td align="right">0.3%</td>
<td align="right">91.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">4,805,060</td>
<td align="right">0.3%</td>
<td align="right">91.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">4,709,600</td>
<td align="right">0.3%</td>
<td align="right">92.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">3,996,680</td>
<td align="right">0.2%</td>
<td align="right">92.2%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">3,963,226</td>
<td align="right">0.2%</td>
<td align="right">92.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">3,827,720</td>
<td align="right">0.2%</td>
<td align="right">92.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">3,819,220</td>
<td align="right">0.2%</td>
<td align="right">92.9%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">3,760,350</td>
<td align="right">0.2%</td>
<td align="right">93.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">3,603,053</td>
<td align="right">0.2%</td>
<td align="right">93.4%</td>
<td align="right">11.5%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT</td>
<td align="right">3,561,208</td>
<td align="right">0.2%</td>
<td align="right">93.6%</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">3,555,480</td>
<td align="right">0.2%</td>
<td align="right">93.8%</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">3,493,040</td>
<td align="right">0.2%</td>
<td align="right">94.0%</td>
<td align="right">58.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">3,446,780</td>
<td align="right">0.2%</td>
<td align="right">94.2%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">3,189,400</td>
<td align="right">0.2%</td>
<td align="right">94.4%</td>
<td align="right">51.1%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">3,065,020</td>
<td align="right">0.2%</td>
<td align="right">94.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">3,050,100</td>
<td align="right">0.2%</td>
<td align="right">94.8%</td>
<td align="right">70.4%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">3,035,380</td>
<td align="right">0.2%</td>
<td align="right">95.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">3,018,982</td>
<td align="right">0.2%</td>
<td align="right">95.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">3,009,560</td>
<td align="right">0.2%</td>
<td align="right">95.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">2,908,926</td>
<td align="right">0.2%</td>
<td align="right">95.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FORMAT_SIMPLE</td>
<td align="right">2,888,300</td>
<td align="right">0.2%</td>
<td align="right">95.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">2,660,140</td>
<td align="right">0.2%</td>
<td align="right">95.8%</td>
<td align="right">3.2%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">2,595,420</td>
<td align="right">0.2%</td>
<td align="right">96.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">2,483,760</td>
<td align="right">0.1%</td>
<td align="right">96.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">2,479,580</td>
<td align="right">0.1%</td>
<td align="right">96.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">2,364,756</td>
<td align="right">0.1%</td>
<td align="right">96.4%</td>
<td align="right">4.2%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">2,328,342</td>
<td align="right">0.1%</td>
<td align="right">96.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CONTAINS_OP_SET</td>
<td align="right">2,298,601</td>
<td align="right">0.1%</td>
<td align="right">96.7%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">2,269,200</td>
<td align="right">0.1%</td>
<td align="right">96.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">2,253,560</td>
<td align="right">0.1%</td>
<td align="right">97.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">2,245,260</td>
<td align="right">0.1%</td>
<td align="right">97.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">2,142,820</td>
<td align="right">0.1%</td>
<td align="right">97.2%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">2,036,380</td>
<td align="right">0.1%</td>
<td align="right">97.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">1,906,300</td>
<td align="right">0.1%</td>
<td align="right">97.5%</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">1,817,222</td>
<td align="right">0.1%</td>
<td align="right">97.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">1,795,240</td>
<td align="right">0.1%</td>
<td align="right">97.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">1,788,300</td>
<td align="right">0.1%</td>
<td align="right">97.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">1,743,802</td>
<td align="right">0.1%</td>
<td align="right">97.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">1,721,172</td>
<td align="right">0.1%</td>
<td align="right">98.0%</td>
<td align="right">4.3%</td>
</tr>
<tr>
<td align="left">DICT_MERGE</td>
<td align="right">1,639,280</td>
<td align="right">0.1%</td>
<td align="right">98.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">1,545,198</td>
<td align="right">0.1%</td>
<td align="right">98.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BUILD_STRING</td>
<td align="right">1,504,200</td>
<td align="right">0.1%</td>
<td align="right">98.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CHECK_EXC_MATCH</td>
<td align="right">1,468,620</td>
<td align="right">0.1%</td>
<td align="right">98.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">RERAISE</td>
<td align="right">1,362,060</td>
<td align="right">0.1%</td>
<td align="right">98.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">1,345,160</td>
<td align="right">0.1%</td>
<td align="right">98.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">1,316,140</td>
<td align="right">0.1%</td>
<td align="right">98.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">1,308,520</td>
<td align="right">0.1%</td>
<td align="right">98.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">1,278,540</td>
<td align="right">0.1%</td>
<td align="right">98.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">1,248,740</td>
<td align="right">0.1%</td>
<td align="right">98.9%</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">CALL_TYPE_1</td>
<td align="right">1,228,260</td>
<td align="right">0.1%</td>
<td align="right">98.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">1,002,406</td>
<td align="right">0.1%</td>
<td align="right">99.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">939,600</td>
<td align="right">0.1%</td>
<td align="right">99.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">903,500</td>
<td align="right">0.1%</td>
<td align="right">99.1%</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">898,740</td>
<td align="right">0.1%</td>
<td align="right">99.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">866,020</td>
<td align="right">0.1%</td>
<td align="right">99.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_TUPLE_INT</td>
<td align="right">825,460</td>
<td align="right">0.0%</td>
<td align="right">99.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">792,600</td>
<td align="right">0.0%</td>
<td align="right">99.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">692,980</td>
<td align="right">0.0%</td>
<td align="right">99.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">649,487</td>
<td align="right">0.0%</td>
<td align="right">99.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">642,020</td>
<td align="right">0.0%</td>
<td align="right">99.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">588,160</td>
<td align="right">0.0%</td>
<td align="right">99.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right">565,820</td>
<td align="right">0.0%</td>
<td align="right">99.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">515,340</td>
<td align="right">0.0%</td>
<td align="right">99.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">513,920</td>
<td align="right">0.0%</td>
<td align="right">99.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">483,820</td>
<td align="right">0.0%</td>
<td align="right">99.6%</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">459,240</td>
<td align="right">0.0%</td>
<td align="right">99.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">448,260</td>
<td align="right">0.0%</td>
<td align="right">99.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">431,040</td>
<td align="right">0.0%</td>
<td align="right">99.7%</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">DELETE_ATTR</td>
<td align="right">381,680</td>
<td align="right">0.0%</td>
<td align="right">99.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">359,440</td>
<td align="right">0.0%</td>
<td align="right">99.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">347,960</td>
<td align="right">0.0%</td>
<td align="right">99.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">321,792</td>
<td align="right">0.0%</td>
<td align="right">99.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_STR_INT</td>
<td align="right">307,897</td>
<td align="right">0.0%</td>
<td align="right">99.8%</td>
<td align="right">2.0%</td>
</tr>
<tr>
<td align="left">BEFORE_WITH</td>
<td align="right">282,500</td>
<td align="right">0.0%</td>
<td align="right">99.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">278,246</td>
<td align="right">0.0%</td>
<td align="right">99.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">RAISE_VARARGS</td>
<td align="right">264,460</td>
<td align="right">0.0%</td>
<td align="right">99.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_ATTR</td>
<td align="right">250,780</td>
<td align="right">0.0%</td>
<td align="right">99.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">246,320</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BUILD_CONST_KEY_MAP</td>
<td align="right">220,700</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">196,240</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">190,180</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_GENERAL</td>
<td align="right">188,900</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right">72.2%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">165,660</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CLEANUP_THROW</td>
<td align="right">149,920</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">119,200</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">DELETE_SUBSCR</td>
<td align="right">112,020</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">109,940</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_STR_1</td>
<td align="right">106,360</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right">12.0%</td>
</tr>
<tr>
<td align="left">CONVERT_VALUE</td>
<td align="right">101,100</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">97,900</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">SET_UPDATE</td>
<td align="right">91,340</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_GETATTRIBUTE_OVERRIDDEN</td>
<td align="right">90,000</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right">63.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">77,460</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">68,780</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">DELETE_FAST</td>
<td align="right">68,380</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">59,520</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right">5.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">40,800</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right">2.0%</td>
</tr>
<tr>
<td align="left">SET_ADD</td>
<td align="right">35,280</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_GETITEM</td>
<td align="right">30,308</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right">4.2%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_WITH_HINT</td>
<td align="right">27,360</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">BUILD_SLICE</td>
<td align="right">18,520</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_INT</td>
<td align="right">13,260</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">11,620</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">11,560</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">LOAD_BUILD_CLASS</td>
<td align="right">10,600</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">MAP_ADD</td>
<td align="right">8,960</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">UNARY_NEGATIVE</td>
<td align="right">8,760</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">WITH_EXCEPT_START</td>
<td align="right">8,220</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">COMPARE_OP_FLOAT</td>
<td align="right">6,480</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right">7.1%</td>
</tr>
<tr>
<td align="left">STORE_SLICE</td>
<td align="right">4,720</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_LIST</td>
<td align="right">4,400</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR</td>
<td align="right">4,060</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">UNARY_INVERT</td>
<td align="right">3,380</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">SETUP_ANNOTATIONS</td>
<td align="right">980</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">DICT_UPDATE</td>
<td align="right">740</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_GLOBAL</td>
<td align="right">360</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FORMAT_WITH_SPEC</td>
<td align="right">240</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">DELETE_NAME</td>
<td align="right">200</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">120</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_FLOAT</td>
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
<td align="left">RESUME_CHECK LOAD_FAST</td>
<td align="right">46,013,480</td>
<td align="right">2.8%</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">44,372,073</td>
<td align="right">2.7%</td>
<td align="right">5.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL POP_JUMP_IF_FALSE</td>
<td align="right">38,346,128</td>
<td align="right">2.3%</td>
<td align="right">7.7%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN LOAD_FAST</td>
<td align="right">26,525,763</td>
<td align="right">1.6%</td>
<td align="right">9.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST LOAD_FAST</td>
<td align="right">26,313,077</td>
<td align="right">1.6%</td>
<td align="right">10.9%</td>
</tr>
<tr>
<td align="left">CACHE RESUME_CHECK</td>
<td align="right">25,501,228</td>
<td align="right">1.5%</td>
<td align="right">12.4%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE LOAD_FAST</td>
<td align="right">23,383,802</td>
<td align="right">1.4%</td>
<td align="right">13.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">21,696,646</td>
<td align="right">1.3%</td>
<td align="right">15.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE LOAD_ATTR_MODULE</td>
<td align="right">20,586,240</td>
<td align="right">1.2%</td>
<td align="right">16.4%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE TO_BOOL_BOOL</td>
<td align="right">20,255,908</td>
<td align="right">1.2%</td>
<td align="right">17.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">19,779,840</td>
<td align="right">1.2%</td>
<td align="right">18.8%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS RESUME_CHECK</td>
<td align="right">19,514,826</td>
<td align="right">1.2%</td>
<td align="right">20.0%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE INTERPRETER_EXIT</td>
<td align="right">17,334,288</td>
<td align="right">1.0%</td>
<td align="right">21.0%</td>
</tr>
<tr>
<td align="left">POP_TOP RETURN_CONST</td>
<td align="right">16,922,960</td>
<td align="right">1.0%</td>
<td align="right">22.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE LOAD_FAST</td>
<td align="right">16,760,188</td>
<td align="right">1.0%</td>
<td align="right">23.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST LOAD_ATTR</td>
<td align="right">16,396,240</td>
<td align="right">1.0%</td>
<td align="right">24.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST LOAD_CONST</td>
<td align="right">15,992,489</td>
<td align="right">1.0%</td>
<td align="right">25.0%</td>
</tr>
<tr>
<td align="left">COPY TO_BOOL_BOOL</td>
<td align="right">15,622,880</td>
<td align="right">0.9%</td>
<td align="right">25.9%</td>
</tr>
<tr>
<td align="left">POP_TOP RESUME_CHECK</td>
<td align="right">15,512,020</td>
<td align="right">0.9%</td>
<td align="right">26.9%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE NOP</td>
<td align="right">14,904,200</td>
<td align="right">0.9%</td>
<td align="right">27.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST LOAD_ATTR_WITH_HINT</td>
<td align="right">12,981,420</td>
<td align="right">0.8%</td>
<td align="right">28.5%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE RETURN_VALUE</td>
<td align="right">12,783,160</td>
<td align="right">0.8%</td>
<td align="right">29.3%</td>
</tr>
<tr>
<td align="left">POP_TOP ENTER_EXECUTOR</td>
<td align="right">12,637,280</td>
<td align="right">0.8%</td>
<td align="right">30.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST COMPARE_OP_STR</td>
<td align="right">12,514,760</td>
<td align="right">0.8%</td>
<td align="right">30.8%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR COPY</td>
<td align="right">12,508,240</td>
<td align="right">0.8%</td>
<td align="right">31.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST CALL_PY_EXACT_ARGS</td>
<td align="right">12,129,380</td>
<td align="right">0.7%</td>
<td align="right">32.3%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE RETURN_VALUE</td>
<td align="right">12,071,080</td>
<td align="right">0.7%</td>
<td align="right">33.0%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE STORE_FAST</td>
<td align="right">11,961,797</td>
<td align="right">0.7%</td>
<td align="right">33.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE CALL_ISINSTANCE</td>
<td align="right">11,893,940</td>
<td align="right">0.7%</td>
<td align="right">34.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST LOAD_GLOBAL_MODULE</td>
<td align="right">11,742,983</td>
<td align="right">0.7%</td>
<td align="right">35.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES LOAD_FAST</td>
<td align="right">11,244,060</td>
<td align="right">0.7%</td>
<td align="right">35.8%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL POP_JUMP_IF_TRUE</td>
<td align="right">10,974,412</td>
<td align="right">0.7%</td>
<td align="right">36.5%</td>
</tr>
<tr>
<td align="left">RETURN_CONST POP_TOP</td>
<td align="right">10,952,957</td>
<td align="right">0.7%</td>
<td align="right">37.2%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE LOAD_GLOBAL_BUILTIN</td>
<td align="right">10,781,864</td>
<td align="right">0.6%</td>
<td align="right">37.8%</td>
</tr>
<tr>
<td align="left">NOP LOAD_FAST_LOAD_FAST</td>
<td align="right">10,728,920</td>
<td align="right">0.6%</td>
<td align="right">38.4%</td>
</tr>
<tr>
<td align="left">END_SEND POP_TOP</td>
<td align="right">10,600,500</td>
<td align="right">0.6%</td>
<td align="right">39.1%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK LOAD_GLOBAL_BUILTIN</td>
<td align="right">10,433,636</td>
<td align="right">0.6%</td>
<td align="right">39.7%</td>
</tr>
<tr>
<td align="left">GET_YIELD_FROM_ITER LOAD_CONST</td>
<td align="right">10,136,220</td>
<td align="right">0.6%</td>
<td align="right">40.3%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR RETURN_VALUE</td>
<td align="right">9,875,160</td>
<td align="right">0.6%</td>
<td align="right">40.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST POP_JUMP_IF_NOT_NONE</td>
<td align="right">9,686,983</td>
<td align="right">0.6%</td>
<td align="right">41.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST LOAD_FAST</td>
<td align="right">9,600,560</td>
<td align="right">0.6%</td>
<td align="right">42.1%</td>
</tr>
<tr>
<td align="left">LOAD_CONST LOAD_FAST</td>
<td align="right">9,411,386</td>
<td align="right">0.6%</td>
<td align="right">42.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">9,182,080</td>
<td align="right">0.6%</td>
<td align="right">43.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST STORE_ATTR_SLOT</td>
<td align="right">8,960,040</td>
<td align="right">0.5%</td>
<td align="right">43.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR LOAD_FAST</td>
<td align="right">8,857,320</td>
<td align="right">0.5%</td>
<td align="right">44.3%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS RETURN_GENERATOR</td>
<td align="right">8,553,080</td>
<td align="right">0.5%</td>
<td align="right">44.8%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE STORE_FAST</td>
<td align="right">8,546,560</td>
<td align="right">0.5%</td>
<td align="right">45.3%</td>
</tr>
<tr>
<td align="left">RETURN_CONST INTERPRETER_EXIT</td>
<td align="right">8,523,060</td>
<td align="right">0.5%</td>
<td align="right">45.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES CALL_PY_EXACT_ARGS</td>
<td align="right">8,498,380</td>
<td align="right">0.5%</td>
<td align="right">46.3%</td>
</tr>
<tr>
<td align="left">LOAD_CONST COMPARE_OP_STR</td>
<td align="right">8,214,182</td>
<td align="right">0.5%</td>
<td align="right">46.8%</td>
</tr>
<tr>
<td align="left">POP_TOP LOAD_FAST</td>
<td align="right">8,071,320</td>
<td align="right">0.5%</td>
<td align="right">47.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST LOAD_GLOBAL_BUILTIN</td>
<td align="right">8,052,703</td>
<td align="right">0.5%</td>
<td align="right">47.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST LOAD_ATTR_SLOT</td>
<td align="right">7,993,060</td>
<td align="right">0.5%</td>
<td align="right">48.3%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS ENTER_EXECUTOR</td>
<td align="right">7,741,520</td>
<td align="right">0.5%</td>
<td align="right">48.7%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE LOAD_FAST</td>
<td align="right">7,493,570</td>
<td align="right">0.5%</td>
<td align="right">49.2%</td>
</tr>
<tr>
<td align="left">LOAD_CONST CALL_KW</td>
<td align="right">7,319,760</td>
<td align="right">0.4%</td>
<td align="right">49.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST RETURN_VALUE</td>
<td align="right">7,258,157</td>
<td align="right">0.4%</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE LOAD_FAST</td>
<td align="right">7,226,583</td>
<td align="right">0.4%</td>
<td align="right">50.5%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE ENTER_EXECUTOR</td>
<td align="right">6,992,959</td>
<td align="right">0.4%</td>
<td align="right">50.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE LOAD_GLOBAL_MODULE</td>
<td align="right">6,973,960</td>
<td align="right">0.4%</td>
<td align="right">51.3%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN POP_TOP</td>
<td align="right">6,777,160</td>
<td align="right">0.4%</td>
<td align="right">51.7%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR CALL_PY_EXACT_ARGS</td>
<td align="right">6,715,740</td>
<td align="right">0.4%</td>
<td align="right">52.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES LOAD_FAST_LOAD_FAST</td>
<td align="right">6,703,000</td>
<td align="right">0.4%</td>
<td align="right">52.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST CALL_PY_EXACT_ARGS</td>
<td align="right">6,558,960</td>
<td align="right">0.4%</td>
<td align="right">52.9%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR GET_ITER</td>
<td align="right">6,458,500</td>
<td align="right">0.4%</td>
<td align="right">53.3%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK LOAD_FAST_LOAD_FAST</td>
<td align="right">6,383,240</td>
<td align="right">0.4%</td>
<td align="right">53.7%</td>
</tr>
<tr>
<td align="left">GET_ITER FOR_ITER_GEN</td>
<td align="right">6,257,280</td>
<td align="right">0.4%</td>
<td align="right">54.1%</td>
</tr>
<tr>
<td align="left">END_FOR POP_TOP</td>
<td align="right">6,237,780</td>
<td align="right">0.4%</td>
<td align="right">54.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">6,209,354</td>
<td align="right">0.4%</td>
<td align="right">54.8%</td>
</tr>
<tr>
<td align="left">RETURN_CONST END_FOR</td>
<td align="right">6,188,240</td>
<td align="right">0.4%</td>
<td align="right">55.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN LOAD_FAST_LOAD_FAST</td>
<td align="right">6,109,260</td>
<td align="right">0.4%</td>
<td align="right">55.6%</td>
</tr>
<tr>
<td align="left">PUSH_NULL LOAD_FAST</td>
<td align="right">6,041,300</td>
<td align="right">0.4%</td>
<td align="right">55.9%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK LOAD_GLOBAL_MODULE</td>
<td align="right">5,945,880</td>
<td align="right">0.4%</td>
<td align="right">56.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST LOAD_FAST_LOAD_FAST</td>
<td align="right">5,922,500</td>
<td align="right">0.4%</td>
<td align="right">56.6%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE INTERPRETER_EXIT</td>
<td align="right">5,842,800</td>
<td align="right">0.4%</td>
<td align="right">57.0%</td>
</tr>
<tr>
<td align="left">NOP LOAD_CONST</td>
<td align="right">5,613,160</td>
<td align="right">0.3%</td>
<td align="right">57.3%</td>
</tr>
<tr>
<td align="left">SEND END_SEND</td>
<td align="right">5,417,340</td>
<td align="right">0.3%</td>
<td align="right">57.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST CALL_ISINSTANCE</td>
<td align="right">5,349,500</td>
<td align="right">0.3%</td>
<td align="right">58.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST SEND_GEN</td>
<td align="right">5,281,100</td>
<td align="right">0.3%</td>
<td align="right">58.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT LOAD_FAST</td>
<td align="right">5,183,559</td>
<td align="right">0.3%</td>
<td align="right">58.6%</td>
</tr>
<tr>
<td align="left">RETURN_CONST END_SEND</td>
<td align="right">5,182,960</td>
<td align="right">0.3%</td>
<td align="right">58.9%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR POP_JUMP_IF_FALSE</td>
<td align="right">5,136,922</td>
<td align="right">0.3%</td>
<td align="right">59.2%</td>
</tr>
<tr>
<td align="left">SEND_GEN POP_TOP</td>
<td align="right">5,037,160</td>
<td align="right">0.3%</td>
<td align="right">59.5%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR GET_YIELD_FROM_ITER</td>
<td align="right">5,021,120</td>
<td align="right">0.3%</td>
<td align="right">59.8%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT NOP</td>
<td align="right">5,019,120</td>
<td align="right">0.3%</td>
<td align="right">60.1%</td>
</tr>
<tr>
<td align="left">LOAD_CONST SEND</td>
<td align="right">4,855,120</td>
<td align="right">0.3%</td>
<td align="right">60.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE LOAD_ATTR</td>
<td align="right">4,812,560</td>
<td align="right">0.3%</td>
<td align="right">60.7%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE RETURN_CONST</td>
<td align="right">4,791,980</td>
<td align="right">0.3%</td>
<td align="right">61.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE RETURN_CONST</td>
<td align="right">4,773,100</td>
<td align="right">0.3%</td>
<td align="right">61.3%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">4,594,380</td>
<td align="right">0.3%</td>
<td align="right">61.6%</td>
</tr>
<tr>
<td align="left">LOAD_CONST LOAD_CONST</td>
<td align="right">4,568,827</td>
<td align="right">0.3%</td>
<td align="right">61.8%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK POP_TOP</td>
<td align="right">4,496,820</td>
<td align="right">0.3%</td>
<td align="right">62.1%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE TO_BOOL_BOOL</td>
<td align="right">4,424,060</td>
<td align="right">0.3%</td>
<td align="right">62.4%</td>
</tr>
<tr>
<td align="left">CALL_KW RESUME_CHECK</td>
<td align="right">4,327,100</td>
<td align="right">0.3%</td>
<td align="right">62.6%</td>
</tr>
<tr>
<td align="left">NOP LOAD_FAST</td>
<td align="right">4,262,167</td>
<td align="right">0.3%</td>
<td align="right">62.9%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF LOAD_FAST</td>
<td align="right">4,198,320</td>
<td align="right">0.3%</td>
<td align="right">63.1%</td>
</tr>
<tr>
<td align="left">LOAD_CONST BINARY_SUBSCR_DICT</td>
<td align="right">4,102,140</td>
<td align="right">0.2%</td>
<td align="right">63.4%</td>
</tr>
<tr>
<td align="left">BUILD_MAP LOAD_FAST</td>
<td align="right">3,981,160</td>
<td align="right">0.2%</td>
<td align="right">63.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE PUSH_NULL</td>
<td align="right">3,960,900</td>
<td align="right">0.2%</td>
<td align="right">63.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST ENTER_EXECUTOR</td>
<td align="right">3,944,140</td>
<td align="right">0.2%</td>
<td align="right">64.1%</td>
</tr>
</tbody>
</table>


</details>

## Predecessor/Successor Pairs

<details>
<summary> Top 5 predecessors and successors of each Tier 1 opcode. </summary>


This does not include the unspecialized instructions that occur after a
specialized instruction deoptimizes.

### BINARY_SLICE

<details>
<summary> Successors and predecessors for BINARY_SLICE </summary>

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
<td align="right">556,007</td>
<td align="right">85.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">31,580</td>
<td align="right">4.9%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">27,840</td>
<td align="right">4.3%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_TUPLE_INT</td>
<td align="right">14,680</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">9,800</td>
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
<td align="left">LOAD_FAST</td>
<td align="right">149,340</td>
<td align="right">23.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">141,347</td>
<td align="right">21.8%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">101,640</td>
<td align="right">15.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">88,340</td>
<td align="right">13.6%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">63,620</td>
<td align="right">9.8%</td>
</tr>
</tbody>
</table>


</details>

### STORE_SLICE

<details>
<summary> Successors and predecessors for STORE_SLICE </summary>

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
<td align="right">4,140</td>
<td align="right">87.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">580</td>
<td align="right">12.3%</td>
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
<td align="right">3,980</td>
<td align="right">84.3%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">480</td>
<td align="right">10.2%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">160</td>
<td align="right">3.4%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">100</td>
<td align="right">2.1%</td>
</tr>
</tbody>
</table>


</details>

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
<td align="right">25,501,228</td>
<td align="right">77.5%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">3,702,220</td>
<td align="right">11.2%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">2,827,600</td>
<td align="right">8.6%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">365,920</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">175,080</td>
<td align="right">0.5%</td>
</tr>
</tbody>
</table>


</details>

### BEFORE_WITH

<details>
<summary> Successors and predecessors for BEFORE_WITH </summary>

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
<td align="right">127,520</td>
<td align="right">45.1%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">125,320</td>
<td align="right">44.4%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">15,300</td>
<td align="right">5.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">8,760</td>
<td align="right">3.1%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">4,300</td>
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
<td align="left">POP_TOP</td>
<td align="right">273,180</td>
<td align="right">96.7%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">9,320</td>
<td align="right">3.3%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_OP_INPLACE_ADD_UNICODE

<details>
<summary> Successors and predecessors for BINARY_OP_INPLACE_ADD_UNICODE </summary>

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
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">74,540</td>
<td align="right">96.2%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">1,460</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">500</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">BUILD_STRING</td>
<td align="right">440</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">420</td>
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
<td align="left">ENTER_EXECUTOR</td>
<td align="right">74,840</td>
<td align="right">96.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,180</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">240</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">140</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">40</td>
<td align="right">0.1%</td>
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
<td align="left">LOAD_CONST</td>
<td align="right">769,360</td>
<td align="right">60.2%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">93,120</td>
<td align="right">7.3%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">90,600</td>
<td align="right">7.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">85,180</td>
<td align="right">6.7%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">84,460</td>
<td align="right">6.6%</td>
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
<td align="right">296,100</td>
<td align="right">23.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">278,580</td>
<td align="right">21.8%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">229,100</td>
<td align="right">17.9%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">131,220</td>
<td align="right">10.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">101,400</td>
<td align="right">7.9%</td>
</tr>
</tbody>
</table>


</details>

### CHECK_EXC_MATCH

<details>
<summary> Successors and predecessors for CHECK_EXC_MATCH </summary>

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
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">990,520</td>
<td align="right">67.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">390,520</td>
<td align="right">26.6%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">61,200</td>
<td align="right">4.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">23,820</td>
<td align="right">1.6%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">2,020</td>
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
<td align="right">1,468,600</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">20</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### CLEANUP_THROW

<details>
<summary> Successors and predecessors for CLEANUP_THROW </summary>

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
<td align="left">CACHE</td>
<td align="right">149,920</td>
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
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">120,040</td>
<td align="right">80.1%</td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">29,880</td>
<td align="right">19.9%</td>
</tr>
</tbody>
</table>


</details>

### DELETE_SUBSCR

<details>
<summary> Successors and predecessors for DELETE_SUBSCR </summary>

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
<td align="right">100,720</td>
<td align="right">89.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">8,560</td>
<td align="right">7.6%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">2,540</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">120</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">BUILD_SLICE</td>
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
<td align="left">ENTER_EXECUTOR</td>
<td align="right">98,940</td>
<td align="right">88.3%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">4,320</td>
<td align="right">3.9%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">3,920</td>
<td align="right">3.5%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">3,880</td>
<td align="right">3.5%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">580</td>
<td align="right">0.5%</td>
</tr>
</tbody>
</table>


</details>

### END_FOR

<details>
<summary> Successors and predecessors for END_FOR </summary>

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
<td align="right">6,188,240</td>
<td align="right">99.2%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">51,100</td>
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
<td align="left">POP_TOP</td>
<td align="right">6,237,780</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">1,560</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### END_SEND

<details>
<summary> Successors and predecessors for END_SEND </summary>

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
<td align="left">SEND</td>
<td align="right">5,417,340</td>
<td align="right">51.1%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">5,182,960</td>
<td align="right">48.9%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">200</td>
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
<td align="left">POP_TOP</td>
<td align="right">10,600,500</td>
<td align="right">100.0%</td>
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
<td align="right">898,740</td>
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
<td align="right">898,740</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### FORMAT_SIMPLE

<details>
<summary> Successors and predecessors for FORMAT_SIMPLE </summary>

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
<td align="right">1,269,700</td>
<td align="right">44.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">1,034,440</td>
<td align="right">35.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">238,360</td>
<td align="right">8.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">120,780</td>
<td align="right">4.2%</td>
</tr>
<tr>
<td align="left">CONVERT_VALUE</td>
<td align="right">101,100</td>
<td align="right">3.5%</td>
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
<td align="right">1,492,640</td>
<td align="right">51.7%</td>
</tr>
<tr>
<td align="left">BUILD_STRING</td>
<td align="right">1,375,500</td>
<td align="right">47.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">17,760</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">2,400</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>


</details>

### FORMAT_WITH_SPEC

<details>
<summary> Successors and predecessors for FORMAT_WITH_SPEC </summary>

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
<td align="left">LOAD_CONST</td>
<td align="right">240</td>
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
<td align="left">RETURN_GENERATOR</td>
<td align="right">6,458,500</td>
<td align="right">39.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">3,862,480</td>
<td align="right">23.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">1,000,820</td>
<td align="right">6.1%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">866,400</td>
<td align="right">5.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">863,160</td>
<td align="right">5.2%</td>
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
<td align="left">FOR_ITER_GEN</td>
<td align="right">6,257,280</td>
<td align="right">38.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">2,591,680</td>
<td align="right">15.7%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">2,242,760</td>
<td align="right">13.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">1,719,100</td>
<td align="right">10.4%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">1,648,860</td>
<td align="right">10.0%</td>
</tr>
</tbody>
</table>


</details>

### GET_YIELD_FROM_ITER

<details>
<summary> Successors and predecessors for GET_YIELD_FROM_ITER </summary>

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
<td align="left">RETURN_GENERATOR</td>
<td align="right">5,021,120</td>
<td align="right">49.5%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">2,803,300</td>
<td align="right">27.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">1,097,400</td>
<td align="right">10.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">574,780</td>
<td align="right">5.7%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_DICT</td>
<td align="right">273,520</td>
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
<td align="left">LOAD_CONST</td>
<td align="right">10,136,220</td>
<td align="right">100.0%</td>
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
<td align="left">RETURN_VALUE</td>
<td align="right">17,334,288</td>
<td align="right">53.9%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">8,523,060</td>
<td align="right">26.5%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">5,842,800</td>
<td align="right">18.2%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">433,100</td>
<td align="right">1.3%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_BUILD_CLASS

<details>
<summary> Successors and predecessors for LOAD_BUILD_CLASS </summary>

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
<td align="left">STORE_NAME</td>
<td align="right">8,860</td>
<td align="right">83.6%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">600</td>
<td align="right">5.7%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">420</td>
<td align="right">4.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">220</td>
<td align="right">2.1%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">120</td>
<td align="right">1.1%</td>
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
<td align="right">10,600</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### MAKE_FUNCTION

<details>
<summary> Successors and predecessors for MAKE_FUNCTION </summary>

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
<td align="right">2,479,580</td>
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
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">2,159,960</td>
<td align="right">87.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">249,780</td>
<td align="right">10.1%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">25,360</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">17,180</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">10,900</td>
<td align="right">0.4%</td>
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
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">14,904,200</td>
<td align="right">54.7%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">5,019,120</td>
<td align="right">18.4%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">2,071,820</td>
<td align="right">7.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">1,329,627</td>
<td align="right">4.9%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">1,322,540</td>
<td align="right">4.9%</td>
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
<td align="right">10,728,920</td>
<td align="right">39.4%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">5,613,160</td>
<td align="right">20.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">4,262,167</td>
<td align="right">15.6%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">2,597,060</td>
<td align="right">9.5%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">2,125,380</td>
<td align="right">7.8%</td>
</tr>
</tbody>
</table>


</details>

### POP_EXCEPT

<details>
<summary> Successors and predecessors for POP_EXCEPT </summary>

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
<td align="right">567,700</td>
<td align="right">43.4%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">304,680</td>
<td align="right">23.3%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">241,720</td>
<td align="right">18.5%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">99,160</td>
<td align="right">7.6%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">75,440</td>
<td align="right">5.8%</td>
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
<td align="left">RERAISE</td>
<td align="right">304,680</td>
<td align="right">23.3%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">287,240</td>
<td align="right">22.0%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">246,480</td>
<td align="right">18.8%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">227,480</td>
<td align="right">17.4%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">93,880</td>
<td align="right">7.2%</td>
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
<td align="right">10,952,957</td>
<td align="right">18.3%</td>
</tr>
<tr>
<td align="left">END_SEND</td>
<td align="right">10,600,500</td>
<td align="right">17.7%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">6,777,160</td>
<td align="right">11.3%</td>
</tr>
<tr>
<td align="left">END_FOR</td>
<td align="right">6,237,780</td>
<td align="right">10.4%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">5,037,160</td>
<td align="right">8.4%</td>
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
<td align="right">16,922,960</td>
<td align="right">28.2%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">15,512,020</td>
<td align="right">25.9%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">12,637,280</td>
<td align="right">21.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">8,071,320</td>
<td align="right">13.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">1,686,000</td>
<td align="right">2.8%</td>
</tr>
</tbody>
</table>


</details>

### PUSH_EXC_INFO

<details>
<summary> Successors and predecessors for PUSH_EXC_INFO </summary>

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
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">262,880</td>
<td align="right">20.0%</td>
</tr>
<tr>
<td align="left">RAISE_VARARGS</td>
<td align="right">198,900</td>
<td align="right">15.1%</td>
</tr>
<tr>
<td align="left">CACHE</td>
<td align="right">175,080</td>
<td align="right">13.3%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">144,140</td>
<td align="right">11.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">113,960</td>
<td align="right">8.7%</td>
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
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">937,580</td>
<td align="right">71.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">351,900</td>
<td align="right">26.7%</td>
</tr>
<tr>
<td align="left">WITH_EXCEPT_START</td>
<td align="right">8,220</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">6,520</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">5,220</td>
<td align="right">0.4%</td>
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
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">3,960,900</td>
<td align="right">48.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,868,240</td>
<td align="right">22.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">1,430,800</td>
<td align="right">17.6%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">434,740</td>
<td align="right">5.3%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_ATTR</td>
<td align="right">243,040</td>
<td align="right">3.0%</td>
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
<td align="right">6,041,300</td>
<td align="right">74.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">863,500</td>
<td align="right">10.6%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">797,000</td>
<td align="right">9.8%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">117,120</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">112,400</td>
<td align="right">1.4%</td>
</tr>
</tbody>
</table>


</details>

### RETURN_GENERATOR

<details>
<summary> Successors and predecessors for RETURN_GENERATOR </summary>

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
<td align="right">8,553,080</td>
<td align="right">55.4%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">2,383,640</td>
<td align="right">15.4%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">1,193,360</td>
<td align="right">7.7%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">1,036,280</td>
<td align="right">6.7%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">874,040</td>
<td align="right">5.7%</td>
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
<td align="right">6,458,500</td>
<td align="right">41.8%</td>
</tr>
<tr>
<td align="left">GET_YIELD_FROM_ITER</td>
<td align="right">5,021,120</td>
<td align="right">32.5%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">1,975,740</td>
<td align="right">12.8%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">565,680</td>
<td align="right">3.7%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">433,100</td>
<td align="right">2.8%</td>
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
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">12,783,160</td>
<td align="right">20.9%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">12,071,080</td>
<td align="right">19.8%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">9,875,160</td>
<td align="right">16.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">7,258,157</td>
<td align="right">11.9%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_DICT</td>
<td align="right">1,645,260</td>
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
<td align="left">INTERPRETER_EXIT</td>
<td align="right">17,334,288</td>
<td align="right">28.4%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">12,071,080</td>
<td align="right">19.8%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">11,961,797</td>
<td align="right">19.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">4,424,060</td>
<td align="right">7.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,992,246</td>
<td align="right">3.3%</td>
</tr>
</tbody>
</table>


</details>

### SETUP_ANNOTATIONS

<details>
<summary> Successors and predecessors for SETUP_ANNOTATIONS </summary>

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
<td align="left">STORE_NAME</td>
<td align="right">580</td>
<td align="right">59.2%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">400</td>
<td align="right">40.8%</td>
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
<td align="right">860</td>
<td align="right">87.8%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">120</td>
<td align="right">12.2%</td>
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
<td align="left">SWAP</td>
<td align="right">93,120</td>
<td align="right">78.1%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">8,580</td>
<td align="right">7.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">8,020</td>
<td align="right">6.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">4,740</td>
<td align="right">4.0%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">1,440</td>
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
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">77,600</td>
<td align="right">65.1%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">21,920</td>
<td align="right">18.4%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">6,020</td>
<td align="right">5.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">2,000</td>
<td align="right">1.7%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">1,700</td>
<td align="right">1.4%</td>
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
<td align="right">695,120</td>
<td align="right">69.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">158,066</td>
<td align="right">15.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">25,420</td>
<td align="right">2.5%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">20,700</td>
<td align="right">2.1%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">19,740</td>
<td align="right">2.0%</td>
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
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">707,006</td>
<td align="right">70.5%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">222,580</td>
<td align="right">22.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">34,260</td>
<td align="right">3.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">12,760</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">7,140</td>
<td align="right">0.7%</td>
</tr>
</tbody>
</table>


</details>

### UNARY_INVERT

<details>
<summary> Successors and predecessors for UNARY_INVERT </summary>

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
<td align="right">2,840</td>
<td align="right">84.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">540</td>
<td align="right">16.0%</td>
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
<td align="left">BINARY_OP</td>
<td align="right">3,380</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### UNARY_NEGATIVE

<details>
<summary> Successors and predecessors for UNARY_NEGATIVE </summary>

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
<td align="right">7,800</td>
<td align="right">89.0%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">940</td>
<td align="right">10.7%</td>
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
<td align="left">BINARY_SLICE</td>
<td align="right">5,520</td>
<td align="right">63.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">1,640</td>
<td align="right">18.7%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">920</td>
<td align="right">10.5%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">640</td>
<td align="right">7.3%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">40</td>
<td align="right">0.5%</td>
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
<td align="right">216,320</td>
<td align="right">87.8%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">12,940</td>
<td align="right">5.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">6,560</td>
<td align="right">2.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">6,120</td>
<td align="right">2.5%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">3,760</td>
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
<td align="left">COPY</td>
<td align="right">114,720</td>
<td align="right">46.6%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">97,760</td>
<td align="right">39.7%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">22,920</td>
<td align="right">9.3%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">6,200</td>
<td align="right">2.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">4,320</td>
<td align="right">1.8%</td>
</tr>
</tbody>
</table>


</details>

### WITH_EXCEPT_START

<details>
<summary> Successors and predecessors for WITH_EXCEPT_START </summary>

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
<td align="left">PUSH_EXC_INFO</td>
<td align="right">8,220</td>
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
<td align="left">TO_BOOL_BOOL</td>
<td align="right">7,620</td>
<td align="right">92.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">320</td>
<td align="right">3.9%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">280</td>
<td align="right">3.4%</td>
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
<td align="left">BUILD_CONST_KEY_MAP</td>
<td align="right">186,000</td>
<td align="right">19.8%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">110,180</td>
<td align="right">11.7%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">101,020</td>
<td align="right">10.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">94,740</td>
<td align="right">10.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">93,420</td>
<td align="right">9.9%</td>
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
<td align="right">376,440</td>
<td align="right">40.1%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">194,320</td>
<td align="right">20.7%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">93,100</td>
<td align="right">9.9%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">86,080</td>
<td align="right">9.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">76,160</td>
<td align="right">8.1%</td>
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
<td align="right">220,700</td>
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
<td align="left">BINARY_OP</td>
<td align="right">186,000</td>
<td align="right">84.3%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">10,640</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">7,180</td>
<td align="right">3.3%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">5,840</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">5,640</td>
<td align="right">2.6%</td>
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
<td align="left">SWAP</td>
<td align="right">1,658,200</td>
<td align="right">27.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">879,420</td>
<td align="right">14.4%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">644,240</td>
<td align="right">10.5%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">624,640</td>
<td align="right">10.2%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">459,880</td>
<td align="right">7.5%</td>
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
<td align="right">1,761,080</td>
<td align="right">28.7%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">1,690,600</td>
<td align="right">27.6%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">1,660,080</td>
<td align="right">27.1%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">610,700</td>
<td align="right">10.0%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">123,560</td>
<td align="right">2.0%</td>
</tr>
</tbody>
</table>


</details>

### BUILD_MAP

<details>
<summary> Successors and predecessors for BUILD_MAP </summary>

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
<td align="right">2,125,380</td>
<td align="right">42.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,215,020</td>
<td align="right">24.3%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">601,940</td>
<td align="right">12.0%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">363,860</td>
<td align="right">7.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">286,440</td>
<td align="right">5.7%</td>
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
<td align="right">3,981,160</td>
<td align="right">79.6%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">697,300</td>
<td align="right">13.9%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">212,360</td>
<td align="right">4.2%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">28,680</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">27,480</td>
<td align="right">0.5%</td>
</tr>
</tbody>
</table>


</details>

### BUILD_SET

<details>
<summary> Successors and predecessors for BUILD_SET </summary>

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
<td align="right">432,800</td>
<td align="right">76.5%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">90,440</td>
<td align="right">16.0%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">33,420</td>
<td align="right">5.9%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">5,240</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">1,580</td>
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
<td align="left">STORE_FAST</td>
<td align="right">438,000</td>
<td align="right">77.4%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">91,480</td>
<td align="right">16.2%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">35,000</td>
<td align="right">6.2%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_SET</td>
<td align="right">700</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">220</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### BUILD_SLICE

<details>
<summary> Successors and predecessors for BUILD_SLICE </summary>

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
<td align="right">18,520</td>
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
<td align="left">BINARY_SUBSCR</td>
<td align="right">18,460</td>
<td align="right">99.7%</td>
</tr>
<tr>
<td align="left">DELETE_SUBSCR</td>
<td align="right">60</td>
<td align="right">0.3%</td>
</tr>
</tbody>
</table>


</details>

### BUILD_STRING

<details>
<summary> Successors and predecessors for BUILD_STRING </summary>

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
<td align="left">FORMAT_SIMPLE</td>
<td align="right">1,375,500</td>
<td align="right">91.4%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">128,700</td>
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
<td align="left">RETURN_VALUE</td>
<td align="right">1,326,160</td>
<td align="right">88.2%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">97,380</td>
<td align="right">6.5%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">17,840</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">15,640</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">9,840</td>
<td align="right">0.7%</td>
</tr>
</tbody>
</table>


</details>

### BUILD_TUPLE

<details>
<summary> Successors and predecessors for BUILD_TUPLE </summary>

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
<td align="right">2,612,546</td>
<td align="right">31.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">1,392,142</td>
<td align="right">16.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">1,000,540</td>
<td align="right">12.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">704,080</td>
<td align="right">8.6%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">620,260</td>
<td align="right">7.5%</td>
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
<td align="right">2,120,540</td>
<td align="right">25.8%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">1,530,660</td>
<td align="right">18.6%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">1,098,440</td>
<td align="right">13.4%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">611,540</td>
<td align="right">7.4%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">601,940</td>
<td align="right">7.3%</td>
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
<td align="left">LOAD_FAST</td>
<td align="right">103,860</td>
<td align="right">17.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">69,420</td>
<td align="right">11.8%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">64,620</td>
<td align="right">11.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">62,340</td>
<td align="right">10.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">52,140</td>
<td align="right">8.9%</td>
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
<td align="right">117,140</td>
<td align="right">19.9%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">96,340</td>
<td align="right">16.4%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">58,180</td>
<td align="right">9.9%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">35,140</td>
<td align="right">6.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">32,880</td>
<td align="right">5.6%</td>
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
<td align="left">DICT_MERGE</td>
<td align="right">1,637,520</td>
<td align="right">91.6%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">89,800</td>
<td align="right">5.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">45,640</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">BUILD_CONST_KEY_MAP</td>
<td align="right">10,640</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">4,160</td>
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
<td align="left">RETURN_GENERATOR</td>
<td align="right">539,200</td>
<td align="right">30.2%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">433,040</td>
<td align="right">24.2%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">261,520</td>
<td align="right">14.6%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">260,060</td>
<td align="right">14.5%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">199,280</td>
<td align="right">11.1%</td>
</tr>
</tbody>
</table>


</details>

### CALL_INTRINSIC_1

<details>
<summary> Successors and predecessors for CALL_INTRINSIC_1 </summary>

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
<td align="left">CACHE</td>
<td align="right">365,920</td>
<td align="right">46.2%</td>
</tr>
<tr>
<td align="left">RERAISE</td>
<td align="right">247,580</td>
<td align="right">31.2%</td>
</tr>
<tr>
<td align="left">CLEANUP_THROW</td>
<td align="right">120,040</td>
<td align="right">15.1%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">19,280</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">16,900</td>
<td align="right">2.1%</td>
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
<td align="left">RERAISE</td>
<td align="right">767,840</td>
<td align="right">96.9%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">7,440</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">7,380</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">4,920</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">4,160</td>
<td align="right">0.5%</td>
</tr>
</tbody>
</table>


</details>

### CALL_KW

<details>
<summary> Successors and predecessors for CALL_KW </summary>

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
<td align="right">7,319,760</td>
<td align="right">77.3%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">2,149,420</td>
<td align="right">22.7%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
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
<td align="left">RESUME_CHECK</td>
<td align="right">4,327,100</td>
<td align="right">45.7%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">2,168,080</td>
<td align="right">22.9%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">941,140</td>
<td align="right">9.9%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">874,040</td>
<td align="right">9.2%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">319,860</td>
<td align="right">3.4%</td>
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
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">2,181,700</td>
<td align="right">55.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">1,238,180</td>
<td align="right">31.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">191,946</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">96,700</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">84,020</td>
<td align="right">2.1%</td>
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
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">2,333,666</td>
<td align="right">58.9%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">1,575,000</td>
<td align="right">39.7%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">23,320</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">9,700</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">7,920</td>
<td align="right">0.2%</td>
</tr>
</tbody>
</table>


</details>

### CONTAINS_OP

<details>
<summary> Successors and predecessors for CONTAINS_OP </summary>

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
<td align="left">BUILD_TUPLE</td>
<td align="right">611,540</td>
<td align="right">30.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">278,360</td>
<td align="right">13.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">165,780</td>
<td align="right">8.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">149,700</td>
<td align="right">7.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">149,560</td>
<td align="right">7.3%</td>
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
<td align="right">1,275,560</td>
<td align="right">62.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">290,480</td>
<td align="right">14.3%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">200,420</td>
<td align="right">9.8%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">159,900</td>
<td align="right">7.9%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">86,140</td>
<td align="right">4.2%</td>
</tr>
</tbody>
</table>


</details>

### CONVERT_VALUE

<details>
<summary> Successors and predecessors for CONVERT_VALUE </summary>

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
<td align="right">99,080</td>
<td align="right">98.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">1,980</td>
<td align="right">2.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
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
<td align="left">FORMAT_SIMPLE</td>
<td align="right">101,100</td>
<td align="right">100.0%</td>
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
<td align="left">COMPARE_OP_STR</td>
<td align="right">12,508,240</td>
<td align="right">63.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,216,940</td>
<td align="right">11.2%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">1,811,580</td>
<td align="right">9.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">626,820</td>
<td align="right">3.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">411,620</td>
<td align="right">2.1%</td>
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
<td align="right">15,622,880</td>
<td align="right">79.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">871,800</td>
<td align="right">4.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">695,120</td>
<td align="right">3.5%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">624,840</td>
<td align="right">3.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">536,300</td>
<td align="right">2.7%</td>
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
<td align="left">CACHE</td>
<td align="right">2,827,600</td>
<td align="right">47.2%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">2,698,800</td>
<td align="right">45.1%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">187,960</td>
<td align="right">3.1%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">126,200</td>
<td align="right">2.1%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">67,200</td>
<td align="right">1.1%</td>
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
<td align="right">3,600,200</td>
<td align="right">60.1%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">2,383,640</td>
<td align="right">39.8%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">2,600</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">380</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### DELETE_ATTR

<details>
<summary> Successors and predecessors for DELETE_ATTR </summary>

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
<td align="right">381,680</td>
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
<td align="left">LOAD_FAST</td>
<td align="right">254,400</td>
<td align="right">66.7%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">127,200</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">80</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### DELETE_FAST

<details>
<summary> Successors and predecessors for DELETE_FAST </summary>

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
<td align="right">68,380</td>
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
<td align="left">RERAISE</td>
<td align="right">43,960</td>
<td align="right">64.3%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">14,000</td>
<td align="right">20.5%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">10,200</td>
<td align="right">14.9%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">200</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">20</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### DELETE_NAME

<details>
<summary> Successors and predecessors for DELETE_NAME </summary>

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
<td align="left">DELETE_NAME</td>
<td align="right">120</td>
<td align="right">60.0%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">20</td>
<td align="right">10.0%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">20</td>
<td align="right">10.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">20</td>
<td align="right">10.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">20</td>
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
<td align="left">DELETE_NAME</td>
<td align="right">120</td>
<td align="right">60.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">40</td>
<td align="right">20.0%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">40</td>
<td align="right">20.0%</td>
</tr>
</tbody>
</table>


</details>

### DICT_MERGE

<details>
<summary> Successors and predecessors for DICT_MERGE </summary>

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
<td align="right">1,630,060</td>
<td align="right">99.4%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">3,840</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_TUPLE_INT</td>
<td align="right">1,780</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">BUILD_CONST_KEY_MAP</td>
<td align="right">1,760</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">1,720</td>
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
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">1,637,520</td>
<td align="right">99.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,760</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>


</details>

### DICT_UPDATE

<details>
<summary> Successors and predecessors for DICT_UPDATE </summary>

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
<td align="left">BUILD_CONST_KEY_MAP</td>
<td align="right">260</td>
<td align="right">35.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">240</td>
<td align="right">32.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">120</td>
<td align="right">16.2%</td>
</tr>
<tr>
<td align="left">MAP_ADD</td>
<td align="right">40</td>
<td align="right">5.4%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">40</td>
<td align="right">5.4%</td>
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
<td align="left">STORE_NAME</td>
<td align="right">280</td>
<td align="right">37.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">160</td>
<td align="right">21.6%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">100</td>
<td align="right">13.5%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">100</td>
<td align="right">13.5%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">80</td>
<td align="right">10.8%</td>
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
<td align="right">12,637,280</td>
<td align="right">28.9%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">7,741,520</td>
<td align="right">17.7%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">6,992,959</td>
<td align="right">16.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">3,944,140</td>
<td align="right">9.0%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">2,538,800</td>
<td align="right">5.8%</td>
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
<td align="right">9,875,160</td>
<td align="right">22.6%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">6,715,740</td>
<td align="right">15.4%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">3,830,824</td>
<td align="right">8.8%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">3,734,363</td>
<td align="right">8.5%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">3,495,380</td>
<td align="right">8.0%</td>
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
<td align="left">COMPARE_OP_STR</td>
<td align="right">2,301,540</td>
<td align="right">60.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">491,980</td>
<td align="right">12.9%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">452,820</td>
<td align="right">11.8%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">199,860</td>
<td align="right">5.2%</td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">93,880</td>
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
<td align="right">3,144,980</td>
<td align="right">82.2%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">276,020</td>
<td align="right">7.2%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">176,240</td>
<td align="right">4.6%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">92,640</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">65,060</td>
<td align="right">1.7%</td>
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
<td align="right">1,648,860</td>
<td align="right">73.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">426,500</td>
<td align="right">19.0%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">85,320</td>
<td align="right">3.8%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">45,260</td>
<td align="right">2.0%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">24,820</td>
<td align="right">1.1%</td>
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
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">781,580</td>
<td align="right">34.8%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">691,080</td>
<td align="right">30.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">341,460</td>
<td align="right">15.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">226,780</td>
<td align="right">10.1%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">76,780</td>
<td align="right">3.4%</td>
</tr>
</tbody>
</table>


</details>

### IMPORT_FROM

<details>
<summary> Successors and predecessors for IMPORT_FROM </summary>

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
<td align="left">IMPORT_NAME</td>
<td align="right">504,000</td>
<td align="right">97.8%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">10,800</td>
<td align="right">2.1%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">500</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
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
<td align="right">461,980</td>
<td align="right">89.6%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">29,140</td>
<td align="right">5.7%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">24,160</td>
<td align="right">4.7%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">40</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">20</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### IMPORT_NAME

<details>
<summary> Successors and predecessors for IMPORT_NAME </summary>

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
<td align="right">498,560</td>
<td align="right">97.0%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">15,360</td>
<td align="right">3.0%</td>
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
<td align="left">IMPORT_FROM</td>
<td align="right">504,000</td>
<td align="right">98.1%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">8,820</td>
<td align="right">1.7%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">900</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">140</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">40</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### IS_OP

<details>
<summary> Successors and predecessors for IS_OP </summary>

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
<td align="right">962,160</td>
<td align="right">31.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">942,020</td>
<td align="right">31.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">591,822</td>
<td align="right">19.6%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">186,600</td>
<td align="right">6.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">139,840</td>
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
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">1,941,342</td>
<td align="right">64.3%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">676,460</td>
<td align="right">22.4%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">203,700</td>
<td align="right">6.7%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">98,180</td>
<td align="right">3.3%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">79,040</td>
<td align="right">2.6%</td>
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
<td align="left">POP_TOP</td>
<td align="right">80,240</td>
<td align="right">28.8%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">57,886</td>
<td align="right">20.8%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">37,760</td>
<td align="right">13.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">27,840</td>
<td align="right">10.0%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">21,880</td>
<td align="right">7.9%</td>
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
<td align="right">100,366</td>
<td align="right">36.1%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">45,260</td>
<td align="right">16.3%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">37,860</td>
<td align="right">13.6%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">33,660</td>
<td align="right">12.1%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">31,760</td>
<td align="right">11.4%</td>
</tr>
</tbody>
</table>


</details>

### JUMP_BACKWARD_NO_INTERRUPT

<details>
<summary> Successors and predecessors for JUMP_BACKWARD_NO_INTERRUPT </summary>

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
<td align="right">4,594,380</td>
<td align="right">92.3%</td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">287,240</td>
<td align="right">5.8%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">92,640</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">1,000</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DELETE_FAST</td>
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
<td align="left">SEND</td>
<td align="right">3,019,640</td>
<td align="right">60.7%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">1,575,740</td>
<td align="right">31.7%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">201,740</td>
<td align="right">4.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">167,880</td>
<td align="right">3.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">5,940</td>
<td align="right">0.1%</td>
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
<td align="left">STORE_FAST</td>
<td align="right">1,384,300</td>
<td align="right">47.6%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">381,160</td>
<td align="right">13.1%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">374,166</td>
<td align="right">12.9%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">165,040</td>
<td align="right">5.7%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_DICT</td>
<td align="right">113,940</td>
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
<td align="left">LOAD_FAST</td>
<td align="right">1,755,506</td>
<td align="right">60.3%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">248,720</td>
<td align="right">8.6%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">169,760</td>
<td align="right">5.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">162,380</td>
<td align="right">5.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">157,520</td>
<td align="right">5.4%</td>
</tr>
</tbody>
</table>


</details>

### LIST_APPEND

<details>
<summary> Successors and predecessors for LIST_APPEND </summary>

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
<td align="right">1,677,200</td>
<td align="right">64.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">351,380</td>
<td align="right">13.5%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">146,300</td>
<td align="right">5.6%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">114,340</td>
<td align="right">4.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">82,800</td>
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
<td align="left">ENTER_EXECUTOR</td>
<td align="right">2,538,800</td>
<td align="right">97.8%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">37,760</td>
<td align="right">1.5%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">8,260</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">7,820</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">2,000</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>


</details>

### LIST_EXTEND

<details>
<summary> Successors and predecessors for LIST_EXTEND </summary>

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
<td align="right">46,920</td>
<td align="right">42.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">26,760</td>
<td align="right">24.3%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">24,760</td>
<td align="right">22.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">7,480</td>
<td align="right">6.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">3,360</td>
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
<td align="left">RETURN_VALUE</td>
<td align="right">46,980</td>
<td align="right">42.7%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">26,960</td>
<td align="right">24.5%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">16,900</td>
<td align="right">15.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">9,900</td>
<td align="right">9.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">7,220</td>
<td align="right">6.6%</td>
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
<td align="right">16,396,240</td>
<td align="right">62.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">4,812,560</td>
<td align="right">18.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">1,448,540</td>
<td align="right">5.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">940,400</td>
<td align="right">3.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">727,980</td>
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
<td align="left">LOAD_FAST</td>
<td align="right">8,857,320</td>
<td align="right">33.9%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">1,430,800</td>
<td align="right">5.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">1,384,240</td>
<td align="right">5.3%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">1,271,380</td>
<td align="right">4.9%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">1,238,180</td>
<td align="right">4.7%</td>
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
<td align="left">LOAD_FAST</td>
<td align="right">15,992,489</td>
<td align="right">23.1%</td>
</tr>
<tr>
<td align="left">GET_YIELD_FROM_ITER</td>
<td align="right">10,136,220</td>
<td align="right">14.7%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">5,613,160</td>
<td align="right">8.1%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">4,568,827</td>
<td align="right">6.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">3,753,460</td>
<td align="right">5.4%</td>
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
<td align="right">9,411,386</td>
<td align="right">13.6%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">8,214,182</td>
<td align="right">11.9%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">7,319,760</td>
<td align="right">10.6%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">5,281,100</td>
<td align="right">7.6%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">4,855,120</td>
<td align="right">7.0%</td>
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
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">3,726,660</td>
<td align="right">35.5%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">1,715,940</td>
<td align="right">16.3%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">1,036,100</td>
<td align="right">9.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">844,820</td>
<td align="right">8.0%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">672,600</td>
<td align="right">6.4%</td>
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
<td align="right">4,198,320</td>
<td align="right">40.0%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">944,780</td>
<td align="right">9.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">892,640</td>
<td align="right">8.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">732,100</td>
<td align="right">7.0%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">560,340</td>
<td align="right">5.3%</td>
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
<td align="right">46,013,480</td>
<td align="right">17.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">26,525,763</td>
<td align="right">9.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">26,313,077</td>
<td align="right">9.8%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">23,383,802</td>
<td align="right">8.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">16,760,188</td>
<td align="right">6.3%</td>
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
<td align="right">44,372,073</td>
<td align="right">16.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">21,696,646</td>
<td align="right">8.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">16,396,240</td>
<td align="right">6.1%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">15,992,489</td>
<td align="right">6.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">12,981,420</td>
<td align="right">4.8%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_FAST_AND_CLEAR

<details>
<summary> Successors and predecessors for LOAD_FAST_AND_CLEAR </summary>

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
<td align="right">1,719,100</td>
<td align="right">95.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">76,140</td>
<td align="right">4.2%</td>
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
<td align="right">1,719,100</td>
<td align="right">95.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">76,140</td>
<td align="right">4.2%</td>
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
<td align="left">PUSH_NULL</td>
<td align="right">112,400</td>
<td align="right">32.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">103,980</td>
<td align="right">29.9%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">103,540</td>
<td align="right">29.8%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">15,900</td>
<td align="right">4.6%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">6,180</td>
<td align="right">1.8%</td>
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
<td align="right">112,440</td>
<td align="right">32.3%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_SET</td>
<td align="right">100,840</td>
<td align="right">29.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">100,840</td>
<td align="right">29.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">14,600</td>
<td align="right">4.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">3,160</td>
<td align="right">0.9%</td>
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
<td align="left">NOP</td>
<td align="right">10,728,920</td>
<td align="right">19.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">6,703,000</td>
<td align="right">12.3%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">6,383,240</td>
<td align="right">11.7%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">6,109,260</td>
<td align="right">11.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">5,922,500</td>
<td align="right">10.9%</td>
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
<td align="right">19,779,840</td>
<td align="right">36.3%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">6,558,960</td>
<td align="right">12.0%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">5,349,500</td>
<td align="right">9.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,647,180</td>
<td align="right">4.9%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">2,292,840</td>
<td align="right">4.2%</td>
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
<td align="right">34,300</td>
<td align="right">17.5%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">30,860</td>
<td align="right">15.7%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">29,920</td>
<td align="right">15.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">12,980</td>
<td align="right">6.6%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">12,140</td>
<td align="right">6.2%</td>
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
<td align="right">55,940</td>
<td align="right">28.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">39,540</td>
<td align="right">20.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">37,880</td>
<td align="right">19.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">35,560</td>
<td align="right">18.1%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">6,620</td>
<td align="right">3.4%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_NAME

<details>
<summary> Successors and predecessors for LOAD_NAME </summary>

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
<td align="right">26,780</td>
<td align="right">27.4%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">25,760</td>
<td align="right">26.3%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">14,680</td>
<td align="right">15.0%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">10,080</td>
<td align="right">10.3%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">4,880</td>
<td align="right">5.0%</td>
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
<td align="right">19,220</td>
<td align="right">19.6%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">14,680</td>
<td align="right">15.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">13,440</td>
<td align="right">13.7%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">12,380</td>
<td align="right">12.6%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">9,340</td>
<td align="right">9.5%</td>
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
<td align="right">4,060</td>
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
<td align="right">1,740</td>
<td align="right">42.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,420</td>
<td align="right">35.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_ATTR</td>
<td align="right">260</td>
<td align="right">6.4%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">240</td>
<td align="right">5.9%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">200</td>
<td align="right">4.9%</td>
</tr>
</tbody>
</table>


</details>

### MAKE_CELL

<details>
<summary> Successors and predecessors for MAKE_CELL </summary>

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
<td align="right">1,953,840</td>
<td align="right">40.7%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">1,923,780</td>
<td align="right">40.0%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">752,840</td>
<td align="right">15.7%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">101,420</td>
<td align="right">2.1%</td>
</tr>
<tr>
<td align="left">CACHE</td>
<td align="right">41,800</td>
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
<td align="left">RESUME_CHECK</td>
<td align="right">2,606,080</td>
<td align="right">54.2%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">1,923,780</td>
<td align="right">40.0%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">271,640</td>
<td align="right">5.7%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">3,560</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>


</details>

### MAP_ADD

<details>
<summary> Successors and predecessors for MAP_ADD </summary>

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
<td align="right">5,360</td>
<td align="right">59.8%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">1,360</td>
<td align="right">15.2%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">620</td>
<td align="right">6.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">480</td>
<td align="right">5.4%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">400</td>
<td align="right">4.5%</td>
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
<td align="right">6,240</td>
<td align="right">69.6%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">2,300</td>
<td align="right">25.7%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">200</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">80</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">40</td>
<td align="right">0.4%</td>
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
<td align="left">TO_BOOL_BOOL</td>
<td align="right">38,346,128</td>
<td align="right">59.3%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">5,136,922</td>
<td align="right">7.9%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">3,144,980</td>
<td align="right">4.9%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">2,682,830</td>
<td align="right">4.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">2,131,294</td>
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
<td align="right">23,383,802</td>
<td align="right">36.1%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">12,783,160</td>
<td align="right">19.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">10,781,864</td>
<td align="right">16.7%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">4,791,980</td>
<td align="right">7.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">2,976,907</td>
<td align="right">4.6%</td>
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
<td align="right">3,052,340</td>
<td align="right">64.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">723,060</td>
<td align="right">15.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">567,180</td>
<td align="right">12.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">221,660</td>
<td align="right">4.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">125,680</td>
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
<td align="right">3,260,720</td>
<td align="right">69.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">1,068,900</td>
<td align="right">22.7%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">94,300</td>
<td align="right">2.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">70,300</td>
<td align="right">1.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">66,740</td>
<td align="right">1.4%</td>
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
<td align="right">9,686,983</td>
<td align="right">78.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">1,649,620</td>
<td align="right">13.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">777,200</td>
<td align="right">6.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">149,880</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">40,240</td>
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
<td align="left">LOAD_FAST</td>
<td align="right">7,226,583</td>
<td align="right">58.5%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">1,322,540</td>
<td align="right">10.7%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">881,820</td>
<td align="right">7.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">754,800</td>
<td align="right">6.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">725,500</td>
<td align="right">5.9%</td>
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
<td align="right">10,974,412</td>
<td align="right">50.5%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">2,333,666</td>
<td align="right">10.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">1,634,840</td>
<td align="right">7.5%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">1,455,899</td>
<td align="right">6.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">1,287,492</td>
<td align="right">5.9%</td>
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
<td align="right">7,493,570</td>
<td align="right">34.5%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">6,992,959</td>
<td align="right">32.2%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">1,931,500</td>
<td align="right">8.9%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">1,890,240</td>
<td align="right">8.7%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">1,285,860</td>
<td align="right">5.9%</td>
</tr>
</tbody>
</table>


</details>

### RAISE_VARARGS

<details>
<summary> Successors and predecessors for RAISE_VARARGS </summary>

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
<td align="left">CALL_KW</td>
<td align="right">179,900</td>
<td align="right">68.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">38,040</td>
<td align="right">14.4%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">12,000</td>
<td align="right">4.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">8,400</td>
<td align="right">3.2%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">7,560</td>
<td align="right">2.9%</td>
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
<td align="left">PUSH_EXC_INFO</td>
<td align="right">198,900</td>
<td align="right">77.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">43,960</td>
<td align="right">17.0%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">8,900</td>
<td align="right">3.4%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">6,460</td>
<td align="right">2.5%</td>
</tr>
</tbody>
</table>


</details>

### RERAISE

<details>
<summary> Successors and predecessors for RERAISE </summary>

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
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">767,840</td>
<td align="right">56.4%</td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">304,680</td>
<td align="right">22.4%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">227,820</td>
<td align="right">16.7%</td>
</tr>
<tr>
<td align="left">DELETE_FAST</td>
<td align="right">43,960</td>
<td align="right">3.2%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">8,160</td>
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
<td align="left">COPY</td>
<td align="right">294,920</td>
<td align="right">46.9%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">247,580</td>
<td align="right">39.4%</td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">84,360</td>
<td align="right">13.4%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">1,320</td>
<td align="right">0.2%</td>
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
<td align="left">POP_TOP</td>
<td align="right">16,922,960</td>
<td align="right">47.1%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">4,791,980</td>
<td align="right">13.3%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">4,773,100</td>
<td align="right">13.3%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">2,605,117</td>
<td align="right">7.3%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">1,931,500</td>
<td align="right">5.4%</td>
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
<td align="right">10,952,957</td>
<td align="right">30.5%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">8,523,060</td>
<td align="right">23.7%</td>
</tr>
<tr>
<td align="left">END_FOR</td>
<td align="right">6,188,240</td>
<td align="right">17.2%</td>
</tr>
<tr>
<td align="left">END_SEND</td>
<td align="right">5,182,960</td>
<td align="right">14.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">2,673,360</td>
<td align="right">7.4%</td>
</tr>
</tbody>
</table>


</details>

### SEND

<details>
<summary> Successors and predecessors for SEND </summary>

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
<td align="right">4,855,120</td>
<td align="right">57.1%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">3,019,640</td>
<td align="right">35.5%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">625,600</td>
<td align="right">7.4%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">9,160</td>
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
<td align="left">END_SEND</td>
<td align="right">5,417,340</td>
<td align="right">63.7%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">3,081,340</td>
<td align="right">36.2%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">9,160</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">840</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">800</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### SET_ADD

<details>
<summary> Successors and predecessors for SET_ADD </summary>

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
<td align="right">28,380</td>
<td align="right">80.4%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_TUPLE_INT</td>
<td align="right">3,180</td>
<td align="right">9.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">1,820</td>
<td align="right">5.2%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">920</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">460</td>
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
<td align="left">ENTER_EXECUTOR</td>
<td align="right">32,080</td>
<td align="right">90.9%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">3,160</td>
<td align="right">9.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">20</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">20</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>


</details>

### SET_FUNCTION_ATTRIBUTE

<details>
<summary> Successors and predecessors for SET_FUNCTION_ATTRIBUTE </summary>

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
<td align="left">MAKE_FUNCTION</td>
<td align="right">2,159,960</td>
<td align="right">95.8%</td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">93,600</td>
<td align="right">4.2%</td>
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
<td align="right">1,636,980</td>
<td align="right">72.6%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">186,740</td>
<td align="right">8.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">129,040</td>
<td align="right">5.7%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">125,600</td>
<td align="right">5.6%</td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">93,600</td>
<td align="right">4.2%</td>
</tr>
</tbody>
</table>


</details>

### SET_UPDATE

<details>
<summary> Successors and predecessors for SET_UPDATE </summary>

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
<td align="right">91,320</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
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
<td align="left">STORE_FAST</td>
<td align="right">90,480</td>
<td align="right">99.1%</td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right">300</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">260</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">260</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">20</td>
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
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">2,292,840</td>
<td align="right">74.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">455,880</td>
<td align="right">14.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">294,140</td>
<td align="right">9.6%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">14,040</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">5,940</td>
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
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">1,459,460</td>
<td align="right">47.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">742,000</td>
<td align="right">24.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">337,360</td>
<td align="right">11.0%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">252,640</td>
<td align="right">8.2%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">216,600</td>
<td align="right">7.1%</td>
</tr>
</tbody>
</table>


</details>

### STORE_DEREF

<details>
<summary> Successors and predecessors for STORE_DEREF </summary>

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
<td align="left">YIELD_VALUE</td>
<td align="right">292,060</td>
<td align="right">45.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">95,700</td>
<td align="right">14.9%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">70,880</td>
<td align="right">11.0%</td>
</tr>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">29,140</td>
<td align="right">4.5%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">19,940</td>
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
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">384,960</td>
<td align="right">60.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">106,960</td>
<td align="right">16.7%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">66,560</td>
<td align="right">10.4%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">29,140</td>
<td align="right">4.5%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">21,080</td>
<td align="right">3.3%</td>
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
<td align="right">11,961,797</td>
<td align="right">22.6%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">8,546,560</td>
<td align="right">16.1%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">3,143,169</td>
<td align="right">5.9%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">2,638,867</td>
<td align="right">5.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">2,299,780</td>
<td align="right">4.3%</td>
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
<td align="right">26,313,077</td>
<td align="right">49.7%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">8,052,703</td>
<td align="right">15.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">5,922,500</td>
<td align="right">11.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">2,276,240</td>
<td align="right">4.3%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">2,071,820</td>
<td align="right">3.9%</td>
</tr>
</tbody>
</table>


</details>

### STORE_FAST_LOAD_FAST

<details>
<summary> Successors and predecessors for STORE_FAST_LOAD_FAST </summary>

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
<td align="left">FOR_ITER_LIST</td>
<td align="right">843,240</td>
<td align="right">62.7%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">291,940</td>
<td align="right">21.7%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">113,960</td>
<td align="right">8.5%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">76,780</td>
<td align="right">5.7%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">18,560</td>
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
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">473,900</td>
<td align="right">35.2%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">263,320</td>
<td align="right">19.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">177,420</td>
<td align="right">13.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">171,600</td>
<td align="right">12.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">107,120</td>
<td align="right">8.0%</td>
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
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">1,694,682</td>
<td align="right">93.3%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">39,440</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">30,560</td>
<td align="right">1.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">21,740</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">13,440</td>
<td align="right">0.7%</td>
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
<td align="right">1,048,382</td>
<td align="right">57.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">550,700</td>
<td align="right">30.3%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">59,860</td>
<td align="right">3.3%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">47,980</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">38,500</td>
<td align="right">2.1%</td>
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
<td align="left">LOAD_CONST</td>
<td align="right">260</td>
<td align="right">72.2%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">40</td>
<td align="right">11.1%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">20</td>
<td align="right">5.6%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">20</td>
<td align="right">5.6%</td>
</tr>
<tr>
<td align="left">STORE_GLOBAL</td>
<td align="right">20</td>
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
<td align="left">LOAD_CONST</td>
<td align="right">280</td>
<td align="right">77.8%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">20</td>
<td align="right">5.6%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">20</td>
<td align="right">5.6%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">20</td>
<td align="right">5.6%</td>
</tr>
<tr>
<td align="left">STORE_GLOBAL</td>
<td align="right">20</td>
<td align="right">5.6%</td>
</tr>
</tbody>
</table>


</details>

### STORE_NAME

<details>
<summary> Successors and predecessors for STORE_NAME </summary>

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
<td align="right">51,920</td>
<td align="right">27.3%</td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">28,480</td>
<td align="right">15.0%</td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">25,360</td>
<td align="right">13.3%</td>
</tr>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">24,160</td>
<td align="right">12.7%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">22,000</td>
<td align="right">11.6%</td>
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
<td align="right">107,380</td>
<td align="right">56.5%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">25,760</td>
<td align="right">13.5%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">13,360</td>
<td align="right">7.0%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">11,960</td>
<td align="right">6.3%</td>
</tr>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">10,800</td>
<td align="right">5.7%</td>
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
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">1,719,100</td>
<td align="right">35.2%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">1,660,080</td>
<td align="right">34.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">250,520</td>
<td align="right">5.1%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">185,040</td>
<td align="right">3.8%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">160,100</td>
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
<td align="left">BUILD_LIST</td>
<td align="right">1,658,200</td>
<td align="right">34.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">1,326,060</td>
<td align="right">27.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">495,020</td>
<td align="right">10.1%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">258,520</td>
<td align="right">5.3%</td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">241,720</td>
<td align="right">5.0%</td>
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
<td align="left">FOR_ITER</td>
<td align="right">3,740</td>
<td align="right">32.2%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">1,960</td>
<td align="right">16.9%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">1,860</td>
<td align="right">16.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">1,520</td>
<td align="right">13.1%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">760</td>
<td align="right">6.5%</td>
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
<td align="right">6,600</td>
<td align="right">56.8%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">3,640</td>
<td align="right">31.3%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">340</td>
<td align="right">2.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">320</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">320</td>
<td align="right">2.8%</td>
</tr>
</tbody>
</table>


</details>

### YIELD_VALUE

<details>
<summary> Successors and predecessors for YIELD_VALUE </summary>

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
<td align="right">3,495,380</td>
<td align="right">21.2%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">3,081,340</td>
<td align="right">18.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,051,440</td>
<td align="right">12.5%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">1,663,960</td>
<td align="right">10.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">1,149,980</td>
<td align="right">7.0%</td>
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
<td align="right">8,546,560</td>
<td align="right">51.9%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">5,842,800</td>
<td align="right">35.5%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">1,663,960</td>
<td align="right">10.1%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">292,060</td>
<td align="right">1.8%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">113,960</td>
<td align="right">0.7%</td>
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
<td align="left">CACHE</td>
<td align="right">18,620</td>
<td align="right">31.3%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">16,500</td>
<td align="right">27.7%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">6,120</td>
<td align="right">10.3%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">5,320</td>
<td align="right">8.9%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">3,560</td>
<td align="right">6.0%</td>
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
<td align="right">19,780</td>
<td align="right">33.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">12,140</td>
<td align="right">20.4%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">10,080</td>
<td align="right">16.9%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">5,440</td>
<td align="right">9.1%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">4,360</td>
<td align="right">7.3%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_OP_ADD_FLOAT

<details>
<summary> Successors and predecessors for BINARY_OP_ADD_FLOAT </summary>

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
<td align="left">CALL_BUILTIN_CLASS</td>
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
<td align="left">SWAP</td>
<td align="right">60</td>
<td align="right">100.0%</td>
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
<td align="right">523,460</td>
<td align="right">60.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">248,380</td>
<td align="right">28.7%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_TUPLE_INT</td>
<td align="right">63,360</td>
<td align="right">7.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_INT</td>
<td align="right">8,340</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">8,200</td>
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
<td align="left">STORE_FAST</td>
<td align="right">190,720</td>
<td align="right">22.0%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">134,660</td>
<td align="right">15.5%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">112,040</td>
<td align="right">12.9%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT</td>
<td align="right">96,440</td>
<td align="right">11.1%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">92,200</td>
<td align="right">10.6%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_OP_ADD_UNICODE

<details>
<summary> Successors and predecessors for BINARY_OP_ADD_UNICODE </summary>

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
<td align="right">129,400</td>
<td align="right">40.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">97,340</td>
<td align="right">30.2%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">59,260</td>
<td align="right">18.4%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">21,432</td>
<td align="right">6.7%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT</td>
<td align="right">6,480</td>
<td align="right">2.0%</td>
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
<td align="left">CALL_LIST_APPEND</td>
<td align="right">90,360</td>
<td align="right">28.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">74,540</td>
<td align="right">23.2%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">56,500</td>
<td align="right">17.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">46,560</td>
<td align="right">14.5%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">20,140</td>
<td align="right">6.3%</td>
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
<td align="left">BINARY_SUBSCR_TUPLE_INT</td>
<td align="right">8,340</td>
<td align="right">62.9%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">4,040</td>
<td align="right">30.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">640</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">220</td>
<td align="right">1.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
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
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">8,340</td>
<td align="right">62.9%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">2,080</td>
<td align="right">15.7%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">1,880</td>
<td align="right">14.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">660</td>
<td align="right">5.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">220</td>
<td align="right">1.7%</td>
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
<td align="left">BINARY_OP</td>
<td align="right">40</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">40</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
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
<td align="left">BINARY_OP</td>
<td align="right">60</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">60</td>
<td align="right">50.0%</td>
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
<td align="right">631,220</td>
<td align="right">91.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">37,560</td>
<td align="right">5.4%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">15,860</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">3,700</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">2,920</td>
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
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">180,560</td>
<td align="right">26.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">164,060</td>
<td align="right">23.7%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">131,100</td>
<td align="right">18.9%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">85,180</td>
<td align="right">12.3%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">47,640</td>
<td align="right">6.9%</td>
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
<td align="left">LOAD_CONST</td>
<td align="right">4,102,140</td>
<td align="right">65.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,517,500</td>
<td align="right">24.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">200,500</td>
<td align="right">3.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">191,900</td>
<td align="right">3.1%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">121,340</td>
<td align="right">1.9%</td>
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
<td align="right">3,453,240</td>
<td align="right">54.9%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">1,645,260</td>
<td align="right">26.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">350,440</td>
<td align="right">5.6%</td>
</tr>
<tr>
<td align="left">GET_YIELD_FROM_ITER</td>
<td align="right">273,520</td>
<td align="right">4.3%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">113,940</td>
<td align="right">1.8%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_SUBSCR_GETITEM

<details>
<summary> Successors and predecessors for BINARY_SUBSCR_GETITEM </summary>

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
<td align="right">20,148</td>
<td align="right">66.5%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">7,780</td>
<td align="right">25.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">1,640</td>
<td align="right">5.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">500</td>
<td align="right">1.6%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">180</td>
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
<td align="left">RESUME_CHECK</td>
<td align="right">28,108</td>
<td align="right">92.7%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">1,060</td>
<td align="right">3.5%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">940</td>
<td align="right">3.1%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">80</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">60</td>
<td align="right">0.2%</td>
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
<td align="left">LOAD_CONST</td>
<td align="right">2,046,340</td>
<td align="right">57.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">674,828</td>
<td align="right">18.9%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">514,760</td>
<td align="right">14.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">147,840</td>
<td align="right">4.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">96,440</td>
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
<td align="left">RETURN_VALUE</td>
<td align="right">1,094,408</td>
<td align="right">30.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">726,000</td>
<td align="right">20.5%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">425,940</td>
<td align="right">12.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">207,300</td>
<td align="right">5.8%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">169,880</td>
<td align="right">4.8%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_SUBSCR_STR_INT

<details>
<summary> Successors and predecessors for BINARY_SUBSCR_STR_INT </summary>

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
<td align="right">284,897</td>
<td align="right">92.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">15,220</td>
<td align="right">4.9%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">5,980</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">1,320</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">360</td>
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
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">110,000</td>
<td align="right">35.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">55,240</td>
<td align="right">17.9%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_DICT</td>
<td align="right">36,120</td>
<td align="right">11.7%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">35,677</td>
<td align="right">11.6%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">29,960</td>
<td align="right">9.7%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_SUBSCR_TUPLE_INT

<details>
<summary> Successors and predecessors for BINARY_SUBSCR_TUPLE_INT </summary>

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
<td align="right">823,920</td>
<td align="right">99.8%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">1,540</td>
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
<td align="left">LOAD_CONST</td>
<td align="right">307,980</td>
<td align="right">37.3%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">102,340</td>
<td align="right">12.4%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">70,180</td>
<td align="right">8.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">65,520</td>
<td align="right">7.9%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">63,360</td>
<td align="right">7.7%</td>
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
<td align="right">667,100</td>
<td align="right">73.8%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">92,260</td>
<td align="right">10.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">65,880</td>
<td align="right">7.3%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">33,260</td>
<td align="right">3.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">33,000</td>
<td align="right">3.7%</td>
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
<td align="right">831,800</td>
<td align="right">92.1%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">67,200</td>
<td align="right">7.4%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">4,040</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">400</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">60</td>
<td align="right">0.0%</td>
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
<td align="left">ENTER_EXECUTOR</td>
<td align="right">1,393,620</td>
<td align="right">39.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">801,120</td>
<td align="right">22.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">615,040</td>
<td align="right">17.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">355,740</td>
<td align="right">10.2%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">176,700</td>
<td align="right">5.1%</td>
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
<td align="right">2,083,600</td>
<td align="right">59.7%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">1,036,280</td>
<td align="right">29.7%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">145,860</td>
<td align="right">4.2%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">138,220</td>
<td align="right">4.0%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">35,640</td>
<td align="right">1.0%</td>
</tr>
</tbody>
</table>


</details>

### CALL_BOUND_METHOD_GENERAL

<details>
<summary> Successors and predecessors for CALL_BOUND_METHOD_GENERAL </summary>

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
<td align="right">121,600</td>
<td align="right">64.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">36,160</td>
<td align="right">19.1%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">11,540</td>
<td align="right">6.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">7,580</td>
<td align="right">4.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">4,960</td>
<td align="right">2.6%</td>
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
<td align="right">121,640</td>
<td align="right">64.4%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">50,480</td>
<td align="right">26.7%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">13,060</td>
<td align="right">6.9%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_GENERAL</td>
<td align="right">2,360</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">1,120</td>
<td align="right">0.6%</td>
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
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">1,204,280</td>
<td align="right">39.7%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">433,040</td>
<td align="right">14.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">358,400</td>
<td align="right">11.8%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">191,540</td>
<td align="right">6.3%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">131,060</td>
<td align="right">4.3%</td>
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
<td align="right">1,409,920</td>
<td align="right">46.4%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">866,400</td>
<td align="right">28.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">485,180</td>
<td align="right">16.0%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">166,420</td>
<td align="right">5.5%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_SET</td>
<td align="right">20,060</td>
<td align="right">0.7%</td>
</tr>
</tbody>
</table>


</details>

### CALL_BUILTIN_FAST

<details>
<summary> Successors and predecessors for CALL_BUILTIN_FAST </summary>

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
<td align="right">1,169,200</td>
<td align="right">29.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,143,920</td>
<td align="right">28.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">895,300</td>
<td align="right">22.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">268,440</td>
<td align="right">6.7%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">183,360</td>
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
<td align="left">RETURN_VALUE</td>
<td align="right">1,274,940</td>
<td align="right">32.1%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">765,320</td>
<td align="right">19.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">537,460</td>
<td align="right">13.5%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">395,120</td>
<td align="right">9.9%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">375,800</td>
<td align="right">9.5%</td>
</tr>
</tbody>
</table>


</details>

### CALL_BUILTIN_FAST_WITH_KEYWORDS

<details>
<summary> Successors and predecessors for CALL_BUILTIN_FAST_WITH_KEYWORDS </summary>

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
<td align="right">283,000</td>
<td align="right">65.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">86,080</td>
<td align="right">20.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">12,660</td>
<td align="right">2.9%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">12,180</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">12,080</td>
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
<td align="left">STORE_FAST</td>
<td align="right">208,600</td>
<td align="right">48.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">86,100</td>
<td align="right">20.0%</td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">50,880</td>
<td align="right">11.8%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">43,300</td>
<td align="right">10.0%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">17,580</td>
<td align="right">4.1%</td>
</tr>
</tbody>
</table>


</details>

### CALL_BUILTIN_O

<details>
<summary> Successors and predecessors for CALL_BUILTIN_O </summary>

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
<td align="left">RETURN_GENERATOR</td>
<td align="right">1,975,740</td>
<td align="right">74.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">534,740</td>
<td align="right">20.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">27,560</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_TUPLE_INT</td>
<td align="right">26,080</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">25,540</td>
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
<td align="left">RETURN_VALUE</td>
<td align="right">1,086,520</td>
<td align="right">40.8%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">881,700</td>
<td align="right">33.1%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">186,080</td>
<td align="right">7.0%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">149,700</td>
<td align="right">5.6%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">122,540</td>
<td align="right">4.6%</td>
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
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">11,893,940</td>
<td align="right">51.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">5,349,500</td>
<td align="right">23.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">2,754,600</td>
<td align="right">11.9%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">1,530,660</td>
<td align="right">6.6%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">893,248</td>
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
<td align="left">TO_BOOL_BOOL</td>
<td align="right">20,255,908</td>
<td align="right">87.6%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">1,811,580</td>
<td align="right">7.8%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">902,520</td>
<td align="right">3.9%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">87,380</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">20,860</td>
<td align="right">0.1%</td>
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
<td align="right">762,490</td>
<td align="right">49.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">336,548</td>
<td align="right">21.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">198,820</td>
<td align="right">12.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">189,100</td>
<td align="right">12.2%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">14,660</td>
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
<td align="left">LOAD_CONST</td>
<td align="right">711,970</td>
<td align="right">46.1%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">183,360</td>
<td align="right">11.9%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">172,260</td>
<td align="right">11.1%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">123,720</td>
<td align="right">8.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">82,160</td>
<td align="right">5.3%</td>
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
<td align="right">1,011,260</td>
<td align="right">43.4%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">885,820</td>
<td align="right">38.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">90,360</td>
<td align="right">3.9%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">61,722</td>
<td align="right">2.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">55,680</td>
<td align="right">2.4%</td>
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
<td align="right">623,600</td>
<td align="right">26.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">600,900</td>
<td align="right">25.8%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">432,962</td>
<td align="right">18.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">319,720</td>
<td align="right">13.7%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">117,400</td>
<td align="right">5.0%</td>
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
<td align="left">LOAD_CONST</td>
<td align="right">2,110,480</td>
<td align="right">36.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">659,500</td>
<td align="right">11.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">611,420</td>
<td align="right">10.7%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">610,700</td>
<td align="right">10.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">568,027</td>
<td align="right">9.9%</td>
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
<td align="right">2,638,867</td>
<td align="right">46.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">1,353,232</td>
<td align="right">23.6%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">724,180</td>
<td align="right">12.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">289,660</td>
<td align="right">5.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">131,060</td>
<td align="right">2.3%</td>
</tr>
</tbody>
</table>


</details>

### CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS

<details>
<summary> Successors and predecessors for CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS </summary>

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
<td align="right">407,540</td>
<td align="right">90.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">34,860</td>
<td align="right">7.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">3,240</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">1,160</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">820</td>
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
<td align="left">LOAD_CONST</td>
<td align="right">216,060</td>
<td align="right">48.2%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">96,200</td>
<td align="right">21.5%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">61,480</td>
<td align="right">13.7%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">39,920</td>
<td align="right">8.9%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">14,660</td>
<td align="right">3.3%</td>
</tr>
</tbody>
</table>


</details>

### CALL_METHOD_DESCRIPTOR_NOARGS

<details>
<summary> Successors and predecessors for CALL_METHOD_DESCRIPTOR_NOARGS </summary>

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
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">2,127,740</td>
<td align="right">99.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">6,020</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">5,800</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">2,500</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">360</td>
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
<td align="left">GET_ITER</td>
<td align="right">804,120</td>
<td align="right">37.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">704,080</td>
<td align="right">32.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">312,360</td>
<td align="right">14.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">133,500</td>
<td align="right">6.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">59,260</td>
<td align="right">2.8%</td>
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
<td align="right">771,620</td>
<td align="right">61.8%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">325,980</td>
<td align="right">26.1%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">81,380</td>
<td align="right">6.5%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">26,680</td>
<td align="right">2.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">13,720</td>
<td align="right">1.1%</td>
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
<td align="right">1,066,320</td>
<td align="right">85.4%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">68,840</td>
<td align="right">5.5%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">47,620</td>
<td align="right">3.8%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">19,200</td>
<td align="right">1.5%</td>
</tr>
<tr>
<td align="left">FORMAT_SIMPLE</td>
<td align="right">18,240</td>
<td align="right">1.5%</td>
</tr>
</tbody>
</table>


</details>

### CALL_NON_PY_GENERAL

<details>
<summary> Successors and predecessors for CALL_NON_PY_GENERAL </summary>

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
<td align="right">849,120</td>
<td align="right">23.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">608,440</td>
<td align="right">17.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">508,560</td>
<td align="right">14.3%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">503,860</td>
<td align="right">14.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">285,560</td>
<td align="right">8.0%</td>
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
<td align="right">1,178,320</td>
<td align="right">33.1%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">821,520</td>
<td align="right">23.1%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">662,840</td>
<td align="right">18.6%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">212,680</td>
<td align="right">6.0%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">139,780</td>
<td align="right">3.9%</td>
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
<td align="left">LOAD_FAST</td>
<td align="right">12,129,380</td>
<td align="right">29.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">8,498,380</td>
<td align="right">20.9%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">6,715,740</td>
<td align="right">16.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">6,558,960</td>
<td align="right">16.1%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">2,242,760</td>
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
<td align="left">RESUME_CHECK</td>
<td align="right">19,514,826</td>
<td align="right">48.0%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">8,553,080</td>
<td align="right">21.0%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">7,741,520</td>
<td align="right">19.0%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">2,698,800</td>
<td align="right">6.6%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">1,953,840</td>
<td align="right">4.8%</td>
</tr>
</tbody>
</table>


</details>

### CALL_PY_GENERAL

<details>
<summary> Successors and predecessors for CALL_PY_GENERAL </summary>

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
<td align="right">2,669,440</td>
<td align="right">42.1%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">1,475,020</td>
<td align="right">23.3%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">884,520</td>
<td align="right">14.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">514,880</td>
<td align="right">8.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">362,720</td>
<td align="right">5.7%</td>
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
<td align="right">2,535,200</td>
<td align="right">40.0%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">2,449,120</td>
<td align="right">38.7%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">752,840</td>
<td align="right">11.9%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">460,880</td>
<td align="right">7.3%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">126,200</td>
<td align="right">2.0%</td>
</tr>
</tbody>
</table>


</details>

### CALL_STR_1

<details>
<summary> Successors and predecessors for CALL_STR_1 </summary>

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
<td align="right">80,300</td>
<td align="right">75.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">23,920</td>
<td align="right">22.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">1,400</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">300</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">240</td>
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
<td align="left">STORE_FAST</td>
<td align="right">33,260</td>
<td align="right">31.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">24,820</td>
<td align="right">23.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">23,220</td>
<td align="right">21.8%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">12,440</td>
<td align="right">11.7%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">3,240</td>
<td align="right">3.0%</td>
</tr>
</tbody>
</table>


</details>

### CALL_TUPLE_1

<details>
<summary> Successors and predecessors for CALL_TUPLE_1 </summary>

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
<td align="right">287,820</td>
<td align="right">80.1%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">66,280</td>
<td align="right">18.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">3,580</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">1,180</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">360</td>
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
<td align="right">281,660</td>
<td align="right">78.4%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">64,940</td>
<td align="right">18.1%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">6,000</td>
<td align="right">1.7%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">3,360</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">2,660</td>
<td align="right">0.7%</td>
</tr>
</tbody>
</table>


</details>

### CALL_TYPE_1

<details>
<summary> Successors and predecessors for CALL_TYPE_1 </summary>

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
<td align="right">689,140</td>
<td align="right">56.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">534,320</td>
<td align="right">43.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">3,240</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">1,200</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">360</td>
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
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">670,920</td>
<td align="right">54.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">355,740</td>
<td align="right">29.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">125,420</td>
<td align="right">10.2%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_DICT</td>
<td align="right">34,400</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">18,660</td>
<td align="right">1.5%</td>
</tr>
</tbody>
</table>


</details>

### COMPARE_OP_FLOAT

<details>
<summary> Successors and predecessors for COMPARE_OP_FLOAT </summary>

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
<td align="right">6,460</td>
<td align="right">99.7%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">20</td>
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
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">6,460</td>
<td align="right">99.7%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">20</td>
<td align="right">0.3%</td>
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
<td align="left">LOAD_CONST</td>
<td align="right">1,050,050</td>
<td align="right">27.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">883,700</td>
<td align="right">23.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">719,500</td>
<td align="right">19.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">529,040</td>
<td align="right">14.1%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">172,260</td>
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
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">2,682,830</td>
<td align="right">71.3%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">601,100</td>
<td align="right">16.0%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">208,400</td>
<td align="right">5.5%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">90,840</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">90,380</td>
<td align="right">2.4%</td>
</tr>
</tbody>
</table>


</details>

### COMPARE_OP_STR

<details>
<summary> Successors and predecessors for COMPARE_OP_STR </summary>

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
<td align="right">12,514,760</td>
<td align="right">58.5%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">8,214,182</td>
<td align="right">38.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">183,100</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">152,440</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">93,300</td>
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
<td align="left">COPY</td>
<td align="right">12,508,240</td>
<td align="right">58.5%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">5,136,922</td>
<td align="right">24.0%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">2,301,540</td>
<td align="right">10.8%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">970,540</td>
<td align="right">4.5%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">238,740</td>
<td align="right">1.1%</td>
</tr>
</tbody>
</table>


</details>

### CONTAINS_OP_DICT

<details>
<summary> Successors and predecessors for CONTAINS_OP_DICT </summary>

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
<td align="right">786,100</td>
<td align="right">31.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">574,200</td>
<td align="right">23.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">293,020</td>
<td align="right">11.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">275,520</td>
<td align="right">11.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">205,100</td>
<td align="right">8.3%</td>
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
<td align="right">2,078,080</td>
<td align="right">83.7%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">199,860</td>
<td align="right">8.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">125,340</td>
<td align="right">5.0%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">48,080</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">26,880</td>
<td align="right">1.1%</td>
</tr>
</tbody>
</table>


</details>

### CONTAINS_OP_SET

<details>
<summary> Successors and predecessors for CONTAINS_OP_SET </summary>

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
<td align="right">775,940</td>
<td align="right">33.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">430,021</td>
<td align="right">18.7%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">365,700</td>
<td align="right">15.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">290,800</td>
<td align="right">12.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">198,240</td>
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
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">1,344,521</td>
<td align="right">58.5%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">557,260</td>
<td align="right">24.2%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">248,040</td>
<td align="right">10.8%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">94,060</td>
<td align="right">4.1%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">43,820</td>
<td align="right">1.9%</td>
</tr>
</tbody>
</table>


</details>

### FOR_ITER_GEN

<details>
<summary> Successors and predecessors for FOR_ITER_GEN </summary>

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
<td align="right">6,257,280</td>
<td align="right">91.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">360,000</td>
<td align="right">5.2%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">176,240</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">31,760</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">31,040</td>
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
<td align="left">POP_TOP</td>
<td align="right">6,777,160</td>
<td align="right">98.8%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">37,640</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">26,040</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">20,220</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">780</td>
<td align="right">0.0%</td>
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
<td align="right">2,591,680</td>
<td align="right">47.8%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">1,326,060</td>
<td align="right">24.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,104,220</td>
<td align="right">20.4%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">276,020</td>
<td align="right">5.1%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">100,366</td>
<td align="right">1.9%</td>
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
<td align="right">3,143,169</td>
<td align="right">58.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">843,240</td>
<td align="right">15.6%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">546,980</td>
<td align="right">10.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">382,417</td>
<td align="right">7.1%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">265,680</td>
<td align="right">4.9%</td>
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
<td align="right">133,960</td>
<td align="right">80.9%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">19,740</td>
<td align="right">11.9%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">6,880</td>
<td align="right">4.2%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">4,340</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">440</td>
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
<td align="left">STORE_FAST</td>
<td align="right">158,680</td>
<td align="right">95.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">5,720</td>
<td align="right">3.5%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">760</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">320</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">180</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>


</details>

### FOR_ITER_TUPLE

<details>
<summary> Successors and predecessors for FOR_ITER_TUPLE </summary>

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
<td align="right">1,138,580</td>
<td align="right">59.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">442,920</td>
<td align="right">23.2%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">258,520</td>
<td align="right">13.6%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">33,660</td>
<td align="right">1.8%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">23,740</td>
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
<td align="left">STORE_FAST</td>
<td align="right">1,044,300</td>
<td align="right">54.8%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">291,940</td>
<td align="right">15.3%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">160,100</td>
<td align="right">8.4%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">100,600</td>
<td align="right">5.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">99,200</td>
<td align="right">5.2%</td>
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
<td align="right">3,779,040</td>
<td align="right">98.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">32,940</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">4,080</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">2,280</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">840</td>
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
<td align="right">3,753,460</td>
<td align="right">98.3%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">22,080</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">11,120</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">10,440</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">8,920</td>
<td align="right">0.2%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_ATTR_GETATTRIBUTE_OVERRIDDEN

<details>
<summary> Successors and predecessors for LOAD_ATTR_GETATTRIBUTE_OVERRIDDEN </summary>

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
<td align="right">88,900</td>
<td align="right">98.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">1,080</td>
<td align="right">1.2%</td>
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
<td align="left">LOAD_ATTR</td>
<td align="right">56,160</td>
<td align="right">62.4%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">32,760</td>
<td align="right">36.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">1,080</td>
<td align="right">1.2%</td>
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
<td align="right">44,372,073</td>
<td align="right">87.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">2,946,220</td>
<td align="right">5.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">1,255,720</td>
<td align="right">2.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">560,640</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">487,380</td>
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
<td align="left">LOAD_FAST</td>
<td align="right">16,760,188</td>
<td align="right">33.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">6,973,960</td>
<td align="right">13.8%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">3,209,360</td>
<td align="right">6.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">2,946,220</td>
<td align="right">5.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">2,671,820</td>
<td align="right">5.3%</td>
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
<td align="right">9,700</td>
<td align="right">83.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">1,120</td>
<td align="right">9.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">420</td>
<td align="right">3.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">280</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">40</td>
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
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">6,020</td>
<td align="right">52.1%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">3,360</td>
<td align="right">29.1%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">1,000</td>
<td align="right">8.7%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">640</td>
<td align="right">5.5%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">260</td>
<td align="right">2.2%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_ATTR_METHOD_NO_DICT

<details>
<summary> Successors and predecessors for LOAD_ATTR_METHOD_NO_DICT </summary>

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
<td align="right">6,209,354</td>
<td align="right">50.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">1,758,520</td>
<td align="right">14.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">1,549,980</td>
<td align="right">12.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">1,065,540</td>
<td align="right">8.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">381,240</td>
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
<td align="left">LOAD_FAST</td>
<td align="right">5,183,559</td>
<td align="right">42.5%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">2,127,740</td>
<td align="right">17.4%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">1,873,860</td>
<td align="right">15.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">1,064,322</td>
<td align="right">8.7%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">687,500</td>
<td align="right">5.6%</td>
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
<td align="right">21,696,646</td>
<td align="right">70.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">2,671,820</td>
<td align="right">8.6%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">1,701,920</td>
<td align="right">5.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">1,651,540</td>
<td align="right">5.3%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">1,193,720</td>
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
<td align="left">LOAD_FAST</td>
<td align="right">11,244,060</td>
<td align="right">36.3%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">8,498,380</td>
<td align="right">27.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">6,703,000</td>
<td align="right">21.7%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">2,669,440</td>
<td align="right">8.6%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">923,060</td>
<td align="right">3.0%</td>
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
<td align="right">20,586,240</td>
<td align="right">95.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">585,820</td>
<td align="right">2.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">231,420</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">32,600</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">27,960</td>
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
<td align="left">CALL_ISINSTANCE</td>
<td align="right">11,893,940</td>
<td align="right">55.3%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">3,960,900</td>
<td align="right">18.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">1,920,940</td>
<td align="right">8.9%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">1,000,540</td>
<td align="right">4.7%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">719,500</td>
<td align="right">3.3%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_ATTR_NONDESCRIPTOR_NO_DICT

<details>
<summary> Successors and predecessors for LOAD_ATTR_NONDESCRIPTOR_NO_DICT </summary>

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
<td align="right">39,740</td>
<td align="right">97.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">460</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">400</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">200</td>
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
<td align="left">COMPARE_OP_INT</td>
<td align="right">34,720</td>
<td align="right">85.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">2,640</td>
<td align="right">6.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">1,020</td>
<td align="right">2.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">820</td>
<td align="right">2.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">500</td>
<td align="right">1.2%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES

<details>
<summary> Successors and predecessors for LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES </summary>

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
<td align="right">2,605,260</td>
<td align="right">85.4%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">136,400</td>
<td align="right">4.5%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">134,840</td>
<td align="right">4.4%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT</td>
<td align="right">61,880</td>
<td align="right">2.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">39,820</td>
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
<td align="left">TO_BOOL_BOOL</td>
<td align="right">1,535,620</td>
<td align="right">50.3%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">723,060</td>
<td align="right">23.7%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">363,100</td>
<td align="right">11.9%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">149,560</td>
<td align="right">4.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">99,100</td>
<td align="right">3.2%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_ATTR_PROPERTY

<details>
<summary> Successors and predecessors for LOAD_ATTR_PROPERTY </summary>

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
<td align="right">1,675,760</td>
<td align="right">48.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">725,780</td>
<td align="right">21.1%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">430,700</td>
<td align="right">12.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">200,640</td>
<td align="right">5.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">182,797</td>
<td align="right">5.3%</td>
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
<td align="right">3,436,700</td>
<td align="right">99.7%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">9,840</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">180</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">60</td>
<td align="right">0.0%</td>
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
<td align="right">7,993,060</td>
<td align="right">86.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">1,017,480</td>
<td align="right">11.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">148,140</td>
<td align="right">1.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">43,540</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">26,780</td>
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
<td align="left">LOAD_FAST</td>
<td align="right">3,358,680</td>
<td align="right">36.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">1,758,520</td>
<td align="right">18.9%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">1,174,840</td>
<td align="right">12.7%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">811,300</td>
<td align="right">8.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">727,980</td>
<td align="right">7.8%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_ATTR_WITH_HINT

<details>
<summary> Successors and predecessors for LOAD_ATTR_WITH_HINT </summary>

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
<td align="right">12,981,420</td>
<td align="right">80.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">1,203,320</td>
<td align="right">7.5%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">732,100</td>
<td align="right">4.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">471,240</td>
<td align="right">2.9%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">324,780</td>
<td align="right">2.0%</td>
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
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">1,651,540</td>
<td align="right">10.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">1,255,720</td>
<td align="right">7.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">1,203,320</td>
<td align="right">7.5%</td>
</tr>
<tr>
<td align="left">GET_YIELD_FROM_ITER</td>
<td align="right">1,097,400</td>
<td align="right">6.8%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">1,079,680</td>
<td align="right">6.7%</td>
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
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">10,781,864</td>
<td align="right">26.3%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">10,433,636</td>
<td align="right">25.4%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">8,052,703</td>
<td align="right">19.6%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">2,597,060</td>
<td align="right">6.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,735,708</td>
<td align="right">4.2%</td>
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
<td align="right">26,525,763</td>
<td align="right">64.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">6,109,260</td>
<td align="right">14.9%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">3,726,660</td>
<td align="right">9.1%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">1,204,280</td>
<td align="right">2.9%</td>
</tr>
<tr>
<td align="left">CHECK_EXC_MATCH</td>
<td align="right">990,520</td>
<td align="right">2.4%</td>
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
<td align="right">11,742,983</td>
<td align="right">25.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">6,973,960</td>
<td align="right">15.1%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">5,945,880</td>
<td align="right">12.9%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">2,976,907</td>
<td align="right">6.5%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">2,702,860</td>
<td align="right">5.9%</td>
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
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">20,586,240</td>
<td align="right">44.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">4,812,560</td>
<td align="right">10.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">3,779,040</td>
<td align="right">8.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,887,360</td>
<td align="right">6.3%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">2,754,600</td>
<td align="right">6.0%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_SUPER_ATTR_ATTR

<details>
<summary> Successors and predecessors for LOAD_SUPER_ATTR_ATTR </summary>

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
<td align="right">250,520</td>
<td align="right">99.9%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR</td>
<td align="right">260</td>
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
<td align="left">PUSH_NULL</td>
<td align="right">243,040</td>
<td align="right">96.9%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">3,360</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">3,040</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">1,320</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">20</td>
<td align="right">0.0%</td>
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
<td align="right">3,007,820</td>
<td align="right">99.9%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR</td>
<td align="right">1,740</td>
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
<td align="right">2,784,040</td>
<td align="right">92.5%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">97,080</td>
<td align="right">3.2%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">66,760</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">57,540</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">3,760</td>
<td align="right">0.1%</td>
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
<td align="left">CACHE</td>
<td align="right">25,501,228</td>
<td align="right">29.9%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">19,514,826</td>
<td align="right">22.9%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">15,512,020</td>
<td align="right">18.2%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">4,327,100</td>
<td align="right">5.1%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">3,830,824</td>
<td align="right">4.5%</td>
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
<td align="right">46,013,480</td>
<td align="right">53.9%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">10,433,636</td>
<td align="right">12.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">6,383,240</td>
<td align="right">7.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">5,945,880</td>
<td align="right">7.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">4,594,380</td>
<td align="right">5.4%</td>
</tr>
</tbody>
</table>


</details>

### SEND_GEN

<details>
<summary> Successors and predecessors for SEND_GEN </summary>

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
<td align="right">5,281,100</td>
<td align="right">77.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">1,575,740</td>
<td align="right">23.0%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">840</td>
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
<td align="left">POP_TOP</td>
<td align="right">5,037,160</td>
<td align="right">73.5%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">1,098,820</td>
<td align="right">16.0%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">721,220</td>
<td align="right">10.5%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">480</td>
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
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">19,779,840</td>
<td align="right">67.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">9,182,080</td>
<td align="right">31.4%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">222,240</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">49,040</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">11,440</td>
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
<td align="left">NOP</td>
<td align="right">14,904,200</td>
<td align="right">50.9%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">4,773,100</td>
<td align="right">16.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">3,465,220</td>
<td align="right">11.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">2,702,860</td>
<td align="right">9.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,513,580</td>
<td align="right">8.6%</td>
</tr>
</tbody>
</table>


</details>

### STORE_ATTR_SLOT

<details>
<summary> Successors and predecessors for STORE_ATTR_SLOT </summary>

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
<td align="right">8,960,040</td>
<td align="right">89.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">1,039,120</td>
<td align="right">10.4%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">1,160</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">1,080</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">640</td>
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
<td align="left">NOP</td>
<td align="right">5,019,120</td>
<td align="right">50.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">3,330,200</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">1,132,900</td>
<td align="right">11.3%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">381,160</td>
<td align="right">3.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">63,960</td>
<td align="right">0.6%</td>
</tr>
</tbody>
</table>


</details>

### STORE_ATTR_WITH_HINT

<details>
<summary> Successors and predecessors for STORE_ATTR_WITH_HINT </summary>

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
<td align="left">SWAP</td>
<td align="right">14,880</td>
<td align="right">54.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">6,920</td>
<td align="right">25.3%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">2,800</td>
<td align="right">10.2%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">1,520</td>
<td align="right">5.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">560</td>
<td align="right">2.0%</td>
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
<td align="right">17,660</td>
<td align="right">64.5%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">4,060</td>
<td align="right">14.8%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">3,920</td>
<td align="right">14.3%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">840</td>
<td align="right">3.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">380</td>
<td align="right">1.4%</td>
</tr>
</tbody>
</table>


</details>

### STORE_SUBSCR_DICT

<details>
<summary> Successors and predecessors for STORE_SUBSCR_DICT </summary>

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
<td align="right">917,520</td>
<td align="right">40.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">652,460</td>
<td align="right">28.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">558,180</td>
<td align="right">24.6%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">85,560</td>
<td align="right">3.8%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">30,200</td>
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
<td align="right">1,231,160</td>
<td align="right">54.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">552,980</td>
<td align="right">24.4%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">179,000</td>
<td align="right">7.9%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">149,820</td>
<td align="right">6.6%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">70,840</td>
<td align="right">3.1%</td>
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
<td align="left">LOAD_CONST</td>
<td align="right">300,580</td>
<td align="right">65.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">109,380</td>
<td align="right">23.8%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">34,680</td>
<td align="right">7.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">11,280</td>
<td align="right">2.5%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">3,160</td>
<td align="right">0.7%</td>
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
<td align="right">308,640</td>
<td align="right">67.2%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">146,960</td>
<td align="right">32.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">1,920</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,340</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">380</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>


</details>

### TO_BOOL_ALWAYS_TRUE

<details>
<summary> Successors and predecessors for TO_BOOL_ALWAYS_TRUE </summary>

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
<td align="right">1,265,040</td>
<td align="right">39.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">842,480</td>
<td align="right">26.4%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">525,840</td>
<td align="right">16.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">263,940</td>
<td align="right">8.3%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">160,480</td>
<td align="right">5.0%</td>
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
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">1,634,840</td>
<td align="right">51.3%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">1,500,460</td>
<td align="right">47.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">28,400</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">23,660</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">1,240</td>
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
<td align="left">CALL_ISINSTANCE</td>
<td align="right">20,255,908</td>
<td align="right">40.5%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">15,622,880</td>
<td align="right">31.2%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">4,424,060</td>
<td align="right">8.8%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">2,673,360</td>
<td align="right">5.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,888,640</td>
<td align="right">3.8%</td>
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
<td align="right">38,346,128</td>
<td align="right">76.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">10,974,412</td>
<td align="right">21.9%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">491,980</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">216,320</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">6,900</td>
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
<td align="left">LOAD_FAST</td>
<td align="right">245,580</td>
<td align="right">50.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">88,500</td>
<td align="right">18.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">76,160</td>
<td align="right">15.7%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">60,140</td>
<td align="right">12.4%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">4,380</td>
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
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">274,040</td>
<td align="right">56.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">195,940</td>
<td align="right">40.5%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">12,940</td>
<td align="right">2.7%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">820</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">40</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### TO_BOOL_LIST

<details>
<summary> Successors and predecessors for TO_BOOL_LIST </summary>

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
<td align="right">777,136</td>
<td align="right">32.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">640,060</td>
<td align="right">27.1%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">376,120</td>
<td align="right">15.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">340,760</td>
<td align="right">14.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">174,440</td>
<td align="right">7.4%</td>
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
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">1,214,720</td>
<td align="right">51.4%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">1,110,260</td>
<td align="right">47.0%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">26,500</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">6,560</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">4,976</td>
<td align="right">0.2%</td>
</tr>
</tbody>
</table>


</details>

### TO_BOOL_NONE

<details>
<summary> Successors and predecessors for TO_BOOL_NONE </summary>

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
<td align="right">1,793,967</td>
<td align="right">49.8%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">871,800</td>
<td align="right">24.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">394,960</td>
<td align="right">11.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">224,220</td>
<td align="right">6.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">212,180</td>
<td align="right">5.9%</td>
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
<td align="right">2,131,294</td>
<td align="right">59.2%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">1,455,899</td>
<td align="right">40.4%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">4,700</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">3,760</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">3,460</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>


</details>

### TO_BOOL_STR

<details>
<summary> Successors and predecessors for TO_BOOL_STR </summary>

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
<td align="right">909,932</td>
<td align="right">52.9%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">624,840</td>
<td align="right">36.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">142,600</td>
<td align="right">8.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">19,500</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">7,000</td>
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
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">1,287,492</td>
<td align="right">74.8%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">431,700</td>
<td align="right">25.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">1,340</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">620</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">20</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### UNPACK_SEQUENCE_LIST

<details>
<summary> Successors and predecessors for UNPACK_SEQUENCE_LIST </summary>

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
<td align="right">1,440</td>
<td align="right">32.7%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">1,020</td>
<td align="right">23.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">860</td>
<td align="right">19.5%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">660</td>
<td align="right">15.0%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">240</td>
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
<td align="left">STORE_FAST</td>
<td align="right">1,860</td>
<td align="right">42.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">1,480</td>
<td align="right">33.6%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">1,060</td>
<td align="right">24.1%</td>
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
<td align="left">RETURN_VALUE</td>
<td align="right">50,260</td>
<td align="right">73.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">7,840</td>
<td align="right">11.4%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">7,760</td>
<td align="right">11.3%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_TUPLE_INT</td>
<td align="right">1,340</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">480</td>
<td align="right">0.7%</td>
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
<td align="right">39,440</td>
<td align="right">57.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">26,700</td>
<td align="right">38.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,280</td>
<td align="right">3.3%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">360</td>
<td align="right">0.5%</td>
</tr>
</tbody>
</table>


</details>

### UNPACK_SEQUENCE_TWO_TUPLE

<details>
<summary> Successors and predecessors for UNPACK_SEQUENCE_TWO_TUPLE </summary>

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
<td align="left">FOR_ITER</td>
<td align="right">781,580</td>
<td align="right">44.8%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">357,982</td>
<td align="right">20.5%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">265,680</td>
<td align="right">15.2%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">139,180</td>
<td align="right">8.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">100,600</td>
<td align="right">5.8%</td>
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
<td align="right">1,694,682</td>
<td align="right">97.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">22,920</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">19,940</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">4,400</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,180</td>
<td align="right">0.1%</td>
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
<td align="right">927,640</td>
<td align="right">10.1%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">8,273,620</td>
<td align="right">89.8%</td>
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
<td align="right">3,280</td>
<td align="right">27.4%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">8,680</td>
<td align="right">72.6%</td>
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
<td align="left">add other</td>
<td align="right">3,300</td>
<td align="right">38.0%</td>
</tr>
<tr>
<td align="left">and int</td>
<td align="right">1,240</td>
<td align="right">14.3%</td>
</tr>
<tr>
<td align="left">or</td>
<td align="right">860</td>
<td align="right">9.9%</td>
</tr>
<tr>
<td align="left">remainder</td>
<td align="right">680</td>
<td align="right">7.8%</td>
</tr>
<tr>
<td align="left">add different types</td>
<td align="right">660</td>
<td align="right">7.6%</td>
</tr>
<tr>
<td align="left">multiply different types</td>
<td align="right">500</td>
<td align="right">5.8%</td>
</tr>
<tr>
<td align="left">xor</td>
<td align="right">400</td>
<td align="right">4.6%</td>
</tr>
<tr>
<td align="left">and other</td>
<td align="right">300</td>
<td align="right">3.5%</td>
</tr>
<tr>
<td align="left">true divide different types</td>
<td align="right">260</td>
<td align="right">3.0%</td>
</tr>
<tr>
<td align="left">lshift</td>
<td align="right">200</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">subtract other</td>
<td align="right">100</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">rshift</td>
<td align="right">60</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">and different types</td>
<td align="right">40</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">floor divide</td>
<td align="right">40</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">power</td>
<td align="right">20</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">true divide other</td>
<td align="right">20</td>
<td align="right">0.2%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_SLICE

<details>
<summary> specialization stats for BINARY_SLICE family </summary>


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
<td align="right">1,303,020</td>
<td align="right">6.6%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">18,532,976</td>
<td align="right">93.3%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">42,380</td>
<td align="right">0.2%</td>
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
<td align="right">9,420</td>
<td align="right">52.6%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">8,480</td>
<td align="right">47.4%</td>
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
<td align="left">out of range</td>
<td align="right">3,460</td>
<td align="right">40.8%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">2,580</td>
<td align="right">30.4%</td>
</tr>
<tr>
<td align="left">buffer int</td>
<td align="right">1,860</td>
<td align="right">21.9%</td>
</tr>
<tr>
<td align="left">code complex parameters</td>
<td align="right">260</td>
<td align="right">3.1%</td>
</tr>
<tr>
<td align="left">list slice</td>
<td align="right">180</td>
<td align="right">2.1%</td>
</tr>
<tr>
<td align="left">tuple slice</td>
<td align="right">100</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">buffer slice</td>
<td align="right">20</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">sequence int</td>
<td align="right">20</td>
<td align="right">0.2%</td>
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
<td align="right">11,648,580</td>
<td align="right">8.8%</td>
</tr>
<tr>
<td align="left">
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">10,260</td>
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
<td align="right">120,740,000</td>
<td align="right">91.0%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">11,375,900</td>
<td align="right">8.6%</td>
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
<td align="right">310,020</td>
<td align="right">98.3%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">5,460</td>
<td align="right">1.7%</td>
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
<td align="left">class no vectorcall</td>
<td align="right">4,840</td>
<td align="right">88.6%</td>
</tr>
<tr>
<td align="left">wrong number arguments</td>
<td align="right">620</td>
<td align="right">11.4%</td>
</tr>
<tr>
<td align="left">init not simple</td>
<td align="right">420</td>
<td align="right">7.7%</td>
</tr>
<tr>
<td align="left">init not inline values</td>
<td align="right">300</td>
<td align="right">5.5%</td>
</tr>
<tr>
<td align="left">init not python</td>
<td align="right">20</td>
<td align="right">0.4%</td>
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
<td align="right">3,967,926</td>
<td align="right">9.9%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">36,020,222</td>
<td align="right">90.0%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">26,920</td>
<td align="right">0.1%</td>
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
<td align="right">12,020</td>
<td align="right">54.1%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">10,200</td>
<td align="right">45.9%</td>
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
<td align="right">4,020</td>
<td align="right">39.4%</td>
</tr>
<tr>
<td align="left">different types</td>
<td align="right">3,360</td>
<td align="right">32.9%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">820</td>
<td align="right">8.0%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">720</td>
<td align="right">7.1%</td>
</tr>
<tr>
<td align="left">big int</td>
<td align="right">340</td>
<td align="right">3.3%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">340</td>
<td align="right">3.3%</td>
</tr>
<tr>
<td align="left">bool</td>
<td align="right">220</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">200</td>
<td align="right">2.0%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">160</td>
<td align="right">1.6%</td>
</tr>
<tr>
<td align="left">float long</td>
<td align="right">20</td>
<td align="right">0.2%</td>
</tr>
</tbody>
</table>


</details>

### CONTAINS_OP

<details>
<summary> specialization stats for CONTAINS_OP family </summary>

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
<td align="right">2,020,600</td>
<td align="right">20.2%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">7,952,440</td>
<td align="right">79.6%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">4,240</td>
<td align="right">0.0%</td>
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
<td align="right">4,180</td>
<td align="right">20.9%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">15,840</td>
<td align="right">79.1%</td>
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
<td align="left">tuple</td>
<td align="right">6,940</td>
<td align="right">43.8%</td>
</tr>
<tr>
<td align="left">str</td>
<td align="right">3,420</td>
<td align="right">21.6%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">3,280</td>
<td align="right">20.7%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">2,200</td>
<td align="right">13.9%</td>
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
<td align="right">2,283,760</td>
<td align="right">9.1%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">22,659,666</td>
<td align="right">90.7%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">66,920</td>
<td align="right">0.3%</td>
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
<td align="right">13,920</td>
<td align="right">49.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">14,500</td>
<td align="right">51.0%</td>
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
<td align="left">dict items</td>
<td align="right">3,780</td>
<td align="right">26.1%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">2,840</td>
<td align="right">19.6%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">2,680</td>
<td align="right">18.5%</td>
</tr>
<tr>
<td align="left">itertools</td>
<td align="right">1,680</td>
<td align="right">11.6%</td>
</tr>
<tr>
<td align="left">zip</td>
<td align="right">1,020</td>
<td align="right">7.0%</td>
</tr>
<tr>
<td align="left">dict values</td>
<td align="right">680</td>
<td align="right">4.7%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">600</td>
<td align="right">4.1%</td>
</tr>
<tr>
<td align="left">reversed list</td>
<td align="right">460</td>
<td align="right">3.2%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">380</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">140</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">map</td>
<td align="right">140</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">ascii string</td>
<td align="right">100</td>
<td align="right">0.7%</td>
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
<td align="right">51,129,879</td>
<td align="right">25.1%</td>
</tr>
<tr>
<td align="left">
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">319,260</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">151,977,955</td>
<td align="right">74.5%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">25,785,159</td>
<td align="right">12.6%</td>
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
<td align="right">607,440</td>
<td align="right">79.5%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">157,040</td>
<td align="right">20.5%</td>
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
<td align="left">not managed dict</td>
<td align="right">40,800</td>
<td align="right">26.0%</td>
</tr>
<tr>
<td align="left">shadowed</td>
<td align="right">32,460</td>
<td align="right">20.7%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">18,980</td>
<td align="right">12.1%</td>
</tr>
<tr>
<td align="left">mutable class</td>
<td align="right">13,540</td>
<td align="right">8.6%</td>
</tr>
<tr>
<td align="left">metaclass attribute</td>
<td align="right">13,480</td>
<td align="right">8.6%</td>
</tr>
<tr>
<td align="left">class attr descriptor</td>
<td align="right">11,120</td>
<td align="right">7.1%</td>
</tr>
<tr>
<td align="left">not in keys</td>
<td align="right">9,240</td>
<td align="right">5.9%</td>
</tr>
<tr>
<td align="left">module attr not found</td>
<td align="right">5,260</td>
<td align="right">3.3%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">4,220</td>
<td align="right">2.7%</td>
</tr>
<tr>
<td align="left">class method obj</td>
<td align="right">2,580</td>
<td align="right">1.6%</td>
</tr>
<tr>
<td align="left">non overriding descriptor</td>
<td align="right">1,920</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">wrong number arguments</td>
<td align="right">1,100</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">builtin class method</td>
<td align="right">840</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">820</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">non string or split</td>
<td align="right">320</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">not in dict</td>
<td align="right">320</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">expected error</td>
<td align="right">20</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">non object slot</td>
<td align="right">20</td>
<td align="right">0.0%</td>
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
<td align="right">224,460</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">1,860</td>
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
<td align="right">86,983,667</td>
<td align="right">99.6%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">125,940</td>
<td align="right">0.1%</td>
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
<td align="right">97,720</td>
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
<td align="right">2,060</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">3,260,340</td>
<td align="right">99.9%</td>
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
<td align="right">2,000</td>
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

### SEND

<details>
<summary> specialization stats for SEND family </summary>

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
<td align="right">8,499,520</td>
<td align="right">55.3%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">6,857,680</td>
<td align="right">44.6%</td>
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
<td align="right">840</td>
<td align="right">8.4%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">9,160</td>
<td align="right">91.6%</td>
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
<td align="left">list</td>
<td align="right">6,720</td>
<td align="right">73.4%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">2,220</td>
<td align="right">24.2%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">220</td>
<td align="right">2.4%</td>
</tr>
</tbody>
</table>


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
<td align="right">14,629,140</td>
<td align="right">33.9%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">28,215,620</td>
<td align="right">65.5%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">11,813,600</td>
<td align="right">27.4%</td>
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
<td align="right">235,280</td>
<td align="right">94.3%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">14,200</td>
<td align="right">5.7%</td>
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
<td align="left">not managed dict</td>
<td align="right">7,240</td>
<td align="right">51.0%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">3,160</td>
<td align="right">22.3%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">1,440</td>
<td align="right">10.1%</td>
</tr>
<tr>
<td align="left">not in keys</td>
<td align="right">760</td>
<td align="right">5.4%</td>
</tr>
<tr>
<td align="left">property</td>
<td align="right">460</td>
<td align="right">3.2%</td>
</tr>
<tr>
<td align="left">non string or split</td>
<td align="right">440</td>
<td align="right">3.1%</td>
</tr>
<tr>
<td align="left">no dict</td>
<td align="right">260</td>
<td align="right">1.8%</td>
</tr>
<tr>
<td align="left">overriding descriptor</td>
<td align="right">200</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">not in dict</td>
<td align="right">180</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">40</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">mutable class</td>
<td align="right">20</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>


</details>

### STORE_SLICE

<details>
<summary> specialization stats for STORE_SLICE family </summary>


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
<td align="right">115,920</td>
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
<td align="right">4,139,500</td>
<td align="right">97.2%</td>
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
<td align="right">1,840</td>
<td align="right">56.1%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">1,440</td>
<td align="right">43.9%</td>
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
<td align="left">dict subclass no override</td>
<td align="right">800</td>
<td align="right">55.6%</td>
</tr>
<tr>
<td align="left">bytearray int</td>
<td align="right">240</td>
<td align="right">16.7%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">160</td>
<td align="right">11.1%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">120</td>
<td align="right">8.3%</td>
</tr>
<tr>
<td align="left">py simple</td>
<td align="right">120</td>
<td align="right">8.3%</td>
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
<td align="right">3,128,686</td>
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
<td align="right">89,837,844</td>
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
<td align="right">2,230,460</td>
<td align="right">2.4%</td>
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
<td align="right">86,940</td>
<td align="right">83.5%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">17,240</td>
<td align="right">16.5%</td>
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
<td align="left">set</td>
<td align="right">11,100</td>
<td align="right">64.4%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">1,680</td>
<td align="right">9.7%</td>
</tr>
<tr>
<td align="left">mapping</td>
<td align="right">1,260</td>
<td align="right">7.3%</td>
</tr>
<tr>
<td align="left">dict</td>
<td align="right">1,220</td>
<td align="right">7.1%</td>
</tr>
<tr>
<td align="left">number</td>
<td align="right">1,000</td>
<td align="right">5.8%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">660</td>
<td align="right">3.8%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">200</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">sequence</td>
<td align="right">120</td>
<td align="right">0.7%</td>
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
<td align="right">7,160</td>
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
<td align="right">22,381,198</td>
<td align="right">99.9%</td>
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
<td align="right">4,140</td>
<td align="right">92.8%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">320</td>
<td align="right">7.2%</td>
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
<td align="left">sequence</td>
<td align="right">240</td>
<td align="right">75.0%</td>
</tr>
<tr>
<td align="left">iterator</td>
<td align="right">80</td>
<td align="right">25.0%</td>
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
<td align="right">910,006,941</td>
<td align="right">54.7%</td>
</tr>
<tr>
<td align="left">
Not specialized
<details>
<summary>ⓘ</summary>

Instructions that could be specialized but aren't, e.g. `LOAD_ATTR`, `BINARY_SLICE`.
</details>
</td>
<td align="right">154,201,007</td>
<td align="right">9.3%</td>
</tr>
<tr>
<td align="left">
Specialized hits
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that complete.
</details>
</td>
<td align="right">548,154,444</td>
<td align="right">32.9%</td>
</tr>
<tr>
<td align="left">
Specialized misses
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that deopt.
</details>
</td>
<td align="right">51,474,539</td>
<td align="right">3.1%</td>
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
<td align="right">51,129,879</td>
<td align="right">51.2%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">14,629,140</td>
<td align="right">14.6%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">11,648,580</td>
<td align="right">11.7%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">8,499,520</td>
<td align="right">8.5%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">3,967,926</td>
<td align="right">4.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">3,128,686</td>
<td align="right">3.1%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">2,283,760</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">2,020,600</td>
<td align="right">2.0%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">1,303,020</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">927,640</td>
<td align="right">0.9%</td>
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
<td align="right">14,631,160</td>
<td align="right">28.4%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">11,813,480</td>
<td align="right">22.9%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">8,084,840</td>
<td align="right">15.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">4,813,980</td>
<td align="right">9.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">3,382,020</td>
<td align="right">6.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">2,146,940</td>
<td align="right">4.2%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">2,046,320</td>
<td align="right">4.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">1,630,280</td>
<td align="right">3.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">712,580</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">512,940</td>
<td align="right">1.0%</td>
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
<td align="right">32,912,888</td>
<td align="right">25.2%</td>
</tr>
<tr>
<td align="left">Calls to Python functions inlined</td>
<td align="right">97,474,168</td>
<td align="right">74.8%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">32,912,888</td>
<td align="right">25.2%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (vector)</td>
<td align="right">24,046,248</td>
<td align="right">18.4%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (generator)</td>
<td align="right">8,866,640</td>
<td align="right">6.8%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (legacy)</td>
<td align="right">3,700</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function vectorcall)</td>
<td align="right">24,031,948</td>
<td align="right">18.4%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (build class)</td>
<td align="right">10,600</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (slot)</td>
<td align="right">879,148</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function ex)</td>
<td align="right">809,920</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (api)</td>
<td align="right">5,035,460</td>
<td align="right">3.9%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (method)</td>
<td align="right">860</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Frame objects created</td>
<td align="right">2,430,600</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">Frames pushed</td>
<td align="right">100,346,296</td>
<td align="right">77.0%</td>
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
<td align="right">58,219,322</td>
<td align="right">29.8%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">58,257,702</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">137,258,690</td>
<td align="right">70.2%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">136,505,590</td>
<td align="right">69.8%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">586,720</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">Allocations over 4 kbytes</td>
<td align="right">166,380</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">126,782,201</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Inline values</td>
<td align="right">3,679,480</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Interpreter increfs</td>
<td align="right">727,353,655</td>
<td align="right">43.8%</td>
</tr>
<tr>
<td align="left">Interpreter decrefs</td>
<td align="right">928,714,642</td>
<td align="right">51.4%</td>
</tr>
<tr>
<td align="left">Increfs</td>
<td align="right">933,123,023</td>
<td align="right">56.2%</td>
</tr>
<tr>
<td align="left">Decrefs</td>
<td align="right">879,821,008</td>
<td align="right">48.6%</td>
</tr>
<tr>
<td align="left">Materialize dict (on request)</td>
<td align="right">360,760</td>
<td align="right">9.8%</td>
</tr>
<tr>
<td align="left">Materialize dict (new key)</td>
<td align="right">25,720</td>
<td align="right">0.7%</td>
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
<td align="right">114,500,487</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Method cache misses</td>
<td align="right">3,483,867</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">4,311,913</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">58,551,769</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Method cache dunder misses</td>
<td align="right">856,847</td>
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
<td align="right">45,300</td>
<td align="right">321,734,440</td>
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
<td align="right">56,440</td>
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
<td align="right">23,280</td>
<td align="right">41.2%</td>
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
<td align="right">22,100</td>
<td align="right">39.2%</td>
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
<td align="right">33,160</td>
<td align="right">58.8%</td>
</tr>
<tr>
<td align="left">
Inner loop found
<details>
<summary>ⓘ</summary>

A trace is truncated because it has an inner loop
</details>
</td>
<td align="right">7,300</td>
<td align="right">12.9%</td>
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
<td align="right">600</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">
Executors invalidated
<details>
<summary>ⓘ</summary>

The number of executors that were invalidated due to watched dictionary changes.
</details>
</td>
<td align="right">480</td>
<td align="right">2.1%</td>
</tr>
<tr>
<td align="left">
Traces executed
<details>
<summary>ⓘ</summary>

The number of traces that were executed
</details>
</td>
<td align="right">149,504,363</td>
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
<td align="right">1,707,792,808</td>
<td align="right">1,142.3%</td>
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
<td align="right">23,280</td>
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
<td align="right">22,980</td>
<td align="right">98.7%</td>
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
<td align="right">240</td>
<td align="right">1.0%</td>
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
<td align="right">940</td>
<td align="right">4.0%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">5,100</td>
<td align="right">21.9%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">8,380</td>
<td align="right">36.0%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">6,840</td>
<td align="right">29.4%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">1,700</td>
<td align="right">7.3%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">300</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">20</td>
<td align="right">0.1%</td>
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
<td align="right">800</td>
<td align="right">3.4%</td>
</tr>
<tr>
<td align="left"><= 8</td>
<td align="right">3,520</td>
<td align="right">15.1%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">5,520</td>
<td align="right">23.7%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">9,740</td>
<td align="right">41.8%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">2,820</td>
<td align="right">12.1%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">540</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">40</td>
<td align="right">0.2%</td>
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
<td align="left">_SET_IP</td>
<td align="right">133,444,813</td>
<td align="right">7.8%</td>
<td align="right">7.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_START_EXECUTOR</td>
<td align="right">115,362,599</td>
<td align="right">6.8%</td>
<td align="right">14.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY</td>
<td align="right">100,577,279</td>
<td align="right">5.9%</td>
<td align="right">20.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_EXIT_TRACE</td>
<td align="right">90,844,165</td>
<td align="right">5.3%</td>
<td align="right">25.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TIER2_RESUME_CHECK</td>
<td align="right">76,421,018</td>
<td align="right">4.5%</td>
<td align="right">30.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_1</td>
<td align="right">70,581,558</td>
<td align="right">4.1%</td>
<td align="right">34.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION</td>
<td align="right">58,865,394</td>
<td align="right">3.4%</td>
<td align="right">37.8%</td>
<td align="right">52.0%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_4</td>
<td align="right">40,502,410</td>
<td align="right">2.4%</td>
<td align="right">40.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_IS_FALSE_POP</td>
<td align="right">38,842,794</td>
<td align="right">2.3%</td>
<td align="right">42.5%</td>
<td align="right">8.9%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR</td>
<td align="right">36,970,136</td>
<td align="right">2.2%</td>
<td align="right">44.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COLD_EXIT</td>
<td align="right">34,141,764</td>
<td align="right">2.0%</td>
<td align="right">46.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_0</td>
<td align="right">33,781,963</td>
<td align="right">2.0%</td>
<td align="right">48.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_ITER_CHECK_LIST</td>
<td align="right">32,579,778</td>
<td align="right">1.9%</td>
<td align="right">50.5%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_LIST</td>
<td align="right">32,543,218</td>
<td align="right">1.9%</td>
<td align="right">52.4%</td>
<td align="right">21.2%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW</td>
<td align="right">31,291,164</td>
<td align="right">1.8%</td>
<td align="right">54.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL_BOOL</td>
<td align="right">28,389,268</td>
<td align="right">1.7%</td>
<td align="right">55.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_LIST</td>
<td align="right">25,650,575</td>
<td align="right">1.5%</td>
<td align="right">57.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_PERIODIC</td>
<td align="right">24,256,977</td>
<td align="right">1.4%</td>
<td align="right">58.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_3</td>
<td align="right">23,577,113</td>
<td align="right">1.4%</td>
<td align="right">60.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_4</td>
<td align="right">22,793,396</td>
<td align="right">1.3%</td>
<td align="right">61.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_IS_NOT_NONE_POP</td>
<td align="right">22,720,843</td>
<td align="right">1.3%</td>
<td align="right">62.9%</td>
<td align="right">4.9%</td>
</tr>
<tr>
<td align="left">_PUSH_FRAME</td>
<td align="right">21,855,314</td>
<td align="right">1.3%</td>
<td align="right">64.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_PUSH_NULL</td>
<td align="right">21,398,060</td>
<td align="right">1.3%</td>
<td align="right">65.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">20,474,676</td>
<td align="right">1.2%</td>
<td align="right">66.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_DYNAMIC_EXIT</td>
<td align="right">19,993,274</td>
<td align="right">1.2%</td>
<td align="right">67.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_WITH_NULL</td>
<td align="right">19,965,755</td>
<td align="right">1.2%</td>
<td align="right">69.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION</td>
<td align="right">19,395,857</td>
<td align="right">1.1%</td>
<td align="right">70.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_JUMP_TO_TOP</td>
<td align="right">19,086,097</td>
<td align="right">1.1%</td>
<td align="right">71.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_EXACT_ARGS</td>
<td align="right">18,367,914</td>
<td align="right">1.1%</td>
<td align="right">72.3%</td>
<td align="right">31.4%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_TRUE_POP</td>
<td align="right">18,276,894</td>
<td align="right">1.1%</td>
<td align="right">73.4%</td>
<td align="right">11.8%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_2</td>
<td align="right">17,448,249</td>
<td align="right">1.0%</td>
<td align="right">74.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_IS_NOT_PY_CALLABLE</td>
<td align="right">17,414,776</td>
<td align="right">1.0%</td>
<td align="right">75.4%</td>
<td align="right">13.4%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_3</td>
<td align="right">16,901,715</td>
<td align="right">1.0%</td>
<td align="right">76.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_POP_TOP</td>
<td align="right">15,334,922</td>
<td align="right">0.9%</td>
<td align="right">77.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_NON_PY_GENERAL</td>
<td align="right">15,073,796</td>
<td align="right">0.9%</td>
<td align="right">78.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY_AND_SET_IP</td>
<td align="right">13,722,016</td>
<td align="right">0.8%</td>
<td align="right">79.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_SAVE_RETURN_OFFSET</td>
<td align="right">13,482,334</td>
<td align="right">0.8%</td>
<td align="right">79.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE</td>
<td align="right">12,763,828</td>
<td align="right">0.7%</td>
<td align="right">80.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_MANAGED_OBJECT_HAS_VALUES</td>
<td align="right">11,581,663</td>
<td align="right">0.7%</td>
<td align="right">81.2%</td>
<td align="right">8.4%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST</td>
<td align="right">11,041,988</td>
<td align="right">0.6%</td>
<td align="right">81.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE</td>
<td align="right">10,780,354</td>
<td align="right">0.6%</td>
<td align="right">82.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE_0</td>
<td align="right">10,605,463</td>
<td align="right">0.6%</td>
<td align="right">83.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_CALL_ISINSTANCE</td>
<td align="right">10,479,960</td>
<td align="right">0.6%</td>
<td align="right">83.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_2</td>
<td align="right">10,394,553</td>
<td align="right">0.6%</td>
<td align="right">84.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_7</td>
<td align="right">9,017,200</td>
<td align="right">0.5%</td>
<td align="right">84.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST</td>
<td align="right">8,766,582</td>
<td align="right">0.5%</td>
<td align="right">85.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_FOR_ITER_GEN_FRAME</td>
<td align="right">8,395,480</td>
<td align="right">0.5%</td>
<td align="right">85.9%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">_GUARD_DORV_VALUES_INST_ATTR_FROM_DICT</td>
<td align="right">8,127,574</td>
<td align="right">0.5%</td>
<td align="right">86.3%</td>
<td align="right">17.9%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_1</td>
<td align="right">7,969,360</td>
<td align="right">0.5%</td>
<td align="right">86.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_NOS_INT</td>
<td align="right">7,420,572</td>
<td align="right">0.4%</td>
<td align="right">87.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COMPARE_OP_INT</td>
<td align="right">7,234,152</td>
<td align="right">0.4%</td>
<td align="right">87.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_KEYS_VERSION</td>
<td align="right">6,669,154</td>
<td align="right">0.4%</td>
<td align="right">88.0%</td>
<td align="right">6.0%</td>
</tr>
<tr>
<td align="left">_TO_BOOL</td>
<td align="right">6,372,360</td>
<td align="right">0.4%</td>
<td align="right">88.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_FOR_ITER_TIER_TWO</td>
<td align="right">6,294,580</td>
<td align="right">0.4%</td>
<td align="right">88.8%</td>
<td align="right">19.8%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">6,237,994</td>
<td align="right">0.4%</td>
<td align="right">89.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_6</td>
<td align="right">6,233,860</td>
<td align="right">0.4%</td>
<td align="right">89.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_ITER_CHECK_TUPLE</td>
<td align="right">6,115,960</td>
<td align="right">0.4%</td>
<td align="right">89.9%</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_TUPLE</td>
<td align="right">6,072,040</td>
<td align="right">0.4%</td>
<td align="right">90.2%</td>
<td align="right">43.5%</td>
</tr>
<tr>
<td align="left">_LOAD_DEREF</td>
<td align="right">5,848,140</td>
<td align="right">0.3%</td>
<td align="right">90.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_5</td>
<td align="right">5,798,396</td>
<td align="right">0.3%</td>
<td align="right">90.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_SWAP</td>
<td align="right">5,772,580</td>
<td align="right">0.3%</td>
<td align="right">91.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GET_ITER</td>
<td align="right">5,677,480</td>
<td align="right">0.3%</td>
<td align="right">91.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_IS_NONE_POP</td>
<td align="right">5,163,840</td>
<td align="right">0.3%</td>
<td align="right">91.9%</td>
<td align="right">13.7%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_1</td>
<td align="right">4,990,134</td>
<td align="right">0.3%</td>
<td align="right">92.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_RESUME_CHECK</td>
<td align="right">4,989,180</td>
<td align="right">0.3%</td>
<td align="right">92.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_DEOPT</td>
<td align="right">4,379,420</td>
<td align="right">0.3%</td>
<td align="right">92.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">4,334,117</td>
<td align="right">0.3%</td>
<td align="right">93.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_UNICODE</td>
<td align="right">4,184,367</td>
<td align="right">0.2%</td>
<td align="right">93.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL_NONE</td>
<td align="right">4,156,649</td>
<td align="right">0.2%</td>
<td align="right">93.5%</td>
<td align="right">71.5%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_2</td>
<td align="right">4,123,160</td>
<td align="right">0.2%</td>
<td align="right">93.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_5</td>
<td align="right">4,075,216</td>
<td align="right">0.2%</td>
<td align="right">93.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_7</td>
<td align="right">3,963,880</td>
<td align="right">0.2%</td>
<td align="right">94.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_LIST_INT</td>
<td align="right">3,749,580</td>
<td align="right">0.2%</td>
<td align="right">94.4%</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_WITH_HINT</td>
<td align="right">3,746,480</td>
<td align="right">0.2%</td>
<td align="right">94.6%</td>
<td align="right">3.0%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_STR</td>
<td align="right">3,667,518</td>
<td align="right">0.2%</td>
<td align="right">94.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_WITH_HINT</td>
<td align="right">3,632,960</td>
<td align="right">0.2%</td>
<td align="right">95.0%</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST</td>
<td align="right">3,615,900</td>
<td align="right">0.2%</td>
<td align="right">95.3%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP</td>
<td align="right">3,579,698</td>
<td align="right">0.2%</td>
<td align="right">95.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_ITER_NEXT_TUPLE</td>
<td align="right">3,431,320</td>
<td align="right">0.2%</td>
<td align="right">95.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_INT</td>
<td align="right">3,334,940</td>
<td align="right">0.2%</td>
<td align="right">95.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_MAKE_CELL</td>
<td align="right">3,284,520</td>
<td align="right">0.2%</td>
<td align="right">96.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_6</td>
<td align="right">3,106,560</td>
<td align="right">0.2%</td>
<td align="right">96.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_0</td>
<td align="right">2,781,400</td>
<td align="right">0.2%</td>
<td align="right">96.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">2,654,600</td>
<td align="right">0.2%</td>
<td align="right">96.6%</td>
<td align="right">7.2%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">2,463,920</td>
<td align="right">0.1%</td>
<td align="right">96.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR</td>
<td align="right">2,385,420</td>
<td align="right">0.1%</td>
<td align="right">96.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BUILD_LIST</td>
<td align="right">2,331,200</td>
<td align="right">0.1%</td>
<td align="right">97.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">2,318,481</td>
<td align="right">0.1%</td>
<td align="right">97.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBTRACT_INT</td>
<td align="right">2,169,440</td>
<td align="right">0.1%</td>
<td align="right">97.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BUILD_TUPLE</td>
<td align="right">2,128,528</td>
<td align="right">0.1%</td>
<td align="right">97.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_IS_OP</td>
<td align="right">2,121,960</td>
<td align="right">0.1%</td>
<td align="right">97.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_AND_CLEAR</td>
<td align="right">1,747,300</td>
<td align="right">0.1%</td>
<td align="right">97.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_TUPLE_INT</td>
<td align="right">1,739,300</td>
<td align="right">0.1%</td>
<td align="right">97.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_DICT</td>
<td align="right">1,716,540</td>
<td align="right">0.1%</td>
<td align="right">97.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_INT</td>
<td align="right">1,699,280</td>
<td align="right">0.1%</td>
<td align="right">97.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_SET</td>
<td align="right">1,609,859</td>
<td align="right">0.1%</td>
<td align="right">98.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_DICT</td>
<td align="right">1,564,460</td>
<td align="right">0.1%</td>
<td align="right">98.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE</td>
<td align="right">1,543,840</td>
<td align="right">0.1%</td>
<td align="right">98.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE_OPERAND</td>
<td align="right">1,453,240</td>
<td align="right">0.1%</td>
<td align="right">98.3%</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">1,382,220</td>
<td align="right">0.1%</td>
<td align="right">98.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP</td>
<td align="right">1,380,680</td>
<td align="right">0.1%</td>
<td align="right">98.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL_LIST</td>
<td align="right">1,370,204</td>
<td align="right">0.1%</td>
<td align="right">98.5%</td>
<td align="right">3.3%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_SLOT_0</td>
<td align="right">1,299,760</td>
<td align="right">0.1%</td>
<td align="right">98.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_POP_FRAME</td>
<td align="right">1,279,586</td>
<td align="right">0.1%</td>
<td align="right">98.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_METHOD_VERSION</td>
<td align="right">1,226,860</td>
<td align="right">0.1%</td>
<td align="right">98.7%</td>
<td align="right">98.0%</td>
</tr>
<tr>
<td align="left">_CALL_LEN</td>
<td align="right">1,138,152</td>
<td align="right">0.1%</td>
<td align="right">98.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL</td>
<td align="right">1,082,800</td>
<td align="right">0.1%</td>
<td align="right">98.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_SLICE</td>
<td align="right">1,069,633</td>
<td align="right">0.1%</td>
<td align="right">98.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_LIST_INT</td>
<td align="right">1,015,200</td>
<td align="right">0.1%</td>
<td align="right">99.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_VERSION</td>
<td align="right">980,340</td>
<td align="right">0.1%</td>
<td align="right">99.0%</td>
<td align="right">10.5%</td>
</tr>
<tr>
<td align="left">_PY_FRAME_GENERAL</td>
<td align="right">901,700</td>
<td align="right">0.1%</td>
<td align="right">99.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_UNICODE</td>
<td align="right">797,348</td>
<td align="right">0.0%</td>
<td align="right">99.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL_INT</td>
<td align="right">780,140</td>
<td align="right">0.0%</td>
<td align="right">99.2%</td>
<td align="right">11.4%</td>
</tr>
<tr>
<td align="left">_REPLACE_WITH_TRUE</td>
<td align="right">760,760</td>
<td align="right">0.0%</td>
<td align="right">99.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">739,420</td>
<td align="right">0.0%</td>
<td align="right">99.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_GUARD_DORV_NO_DICT</td>
<td align="right">728,580</td>
<td align="right">0.0%</td>
<td align="right">99.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">728,580</td>
<td align="right">0.0%</td>
<td align="right">99.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL_STR</td>
<td align="right">717,128</td>
<td align="right">0.0%</td>
<td align="right">99.4%</td>
<td align="right">11.0%</td>
</tr>
<tr>
<td align="left">_COPY</td>
<td align="right">704,720</td>
<td align="right">0.0%</td>
<td align="right">99.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COPY_FREE_VARS</td>
<td align="right">666,960</td>
<td align="right">0.0%</td>
<td align="right">99.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GET_YIELD_FROM_ITER</td>
<td align="right">625,600</td>
<td align="right">0.0%</td>
<td align="right">99.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LIST_APPEND</td>
<td align="right">590,620</td>
<td align="right">0.0%</td>
<td align="right">99.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_TOS_INT</td>
<td align="right">589,260</td>
<td align="right">0.0%</td>
<td align="right">99.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_3</td>
<td align="right">573,900</td>
<td align="right">0.0%</td>
<td align="right">99.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_O</td>
<td align="right">468,080</td>
<td align="right">0.0%</td>
<td align="right">99.6%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_STR_INT</td>
<td align="right">448,343</td>
<td align="right">0.0%</td>
<td align="right">99.7%</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">397,460</td>
<td align="right">0.0%</td>
<td align="right">99.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_DICT</td>
<td align="right">395,860</td>
<td align="right">0.0%</td>
<td align="right">99.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW_WITH_NULL</td>
<td align="right">373,800</td>
<td align="right">0.0%</td>
<td align="right">99.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_ATTR</td>
<td align="right">356,380</td>
<td align="right">0.0%</td>
<td align="right">99.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_RANGE</td>
<td align="right">353,020</td>
<td align="right">0.0%</td>
<td align="right">99.8%</td>
<td align="right">30.1%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_RANGE</td>
<td align="right">353,020</td>
<td align="right">0.0%</td>
<td align="right">99.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_0</td>
<td align="right">326,120</td>
<td align="right">0.0%</td>
<td align="right">99.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_CLASS</td>
<td align="right">273,380</td>
<td align="right">0.0%</td>
<td align="right">99.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_ITER_NEXT_RANGE</td>
<td align="right">246,760</td>
<td align="right">0.0%</td>
<td align="right">99.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BUILD_MAP</td>
<td align="right">200,000</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COMPARE_OP</td>
<td align="right">179,840</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_SET_FUNCTION_ATTRIBUTE</td>
<td align="right">163,680</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">158,280</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_ERROR_POP_N</td>
<td align="right">145,740</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_MODULE</td>
<td align="right">139,860</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_MODULE</td>
<td align="right">139,860</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">133,340</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_MAKE_FUNCTION</td>
<td align="right">129,300</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR</td>
<td align="right">128,760</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_CHECK</td>
<td align="right">119,760</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_4</td>
<td align="right">107,300</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_CLASS</td>
<td align="right">96,500</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_CLASS_0</td>
<td align="right">96,480</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TUPLE</td>
<td align="right">87,540</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_RETURN_GENERATOR</td>
<td align="right">86,540</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_TUPLE_1</td>
<td align="right">85,300</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_DICT_MERGE</td>
<td align="right">84,480</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_DELETE_SUBSCR</td>
<td align="right">76,080</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_FORMAT_SIMPLE</td>
<td align="right">53,460</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LIST_EXTEND</td>
<td align="right">44,240</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_TYPE_1</td>
<td align="right">35,980</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_POP_TOP_LOAD_CONST_INLINE_BORROW</td>
<td align="right">34,400</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BUILD_STRING</td>
<td align="right">31,680</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">31,280</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_EXPAND_METHOD</td>
<td align="right">23,960</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNARY_NEGATIVE</td>
<td align="right">17,040</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_STR_1</td>
<td align="right">14,520</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BUILD_SLICE</td>
<td align="right">14,460</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_ATTR_SLOT</td>
<td align="right">10,600</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_SET_ADD</td>
<td align="right">8,920</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_POP_EXCEPT</td>
<td align="right">7,620</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNARY_NOT</td>
<td align="right">6,260</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_SLOT_1</td>
<td align="right">5,940</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS</td>
<td align="right">4,740</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_GLOBALS_VERSION</td>
<td align="right">4,200</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CONVERT_VALUE</td>
<td align="right">4,080</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_MAP_ADD</td>
<td align="right">3,000</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_INTRINSIC_1</td>
<td align="right">2,760</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_NAME</td>
<td align="right">2,560</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_BUILTINS_VERSION</td>
<td align="right">2,100</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_BUILTINS</td>
<td align="right">2,100</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_MODULE</td>
<td align="right">2,100</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_DEREF</td>
<td align="right">2,060</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_LIST</td>
<td align="right">2,000</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_MULTIPLY_INT</td>
<td align="right">200</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNARY_INVERT</td>
<td align="right">180</td>
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
<td align="right">6,980</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">2,520</td>
</tr>
<tr>
<td align="left">BEFORE_WITH</td>
<td align="right">760</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">660</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">560</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">400</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">340</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_GETITEM</td>
<td align="right">200</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">80</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">80</td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right">60</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">60</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">40</td>
</tr>
<tr>
<td align="left">RAISE_VARARGS</td>
<td align="right">40</td>
</tr>
<tr>
<td align="left">STORE_ATTR_WITH_HINT</td>
<td align="right">40</td>
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
<td align="right">240</td>
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
<td align="right">240</td>
</tr>
<tr>
<td align="left">
watched dict modification
<details>
<summary>ⓘ</summary>

A watched dict has been modified
</details>
</td>
<td align="right">320</td>
</tr>
<tr>
<td align="left">
watched globals modification
<details>
<summary>ⓘ</summary>

A watched `globals()` dict has been modified
</details>
</td>
<td align="right">320</td>
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
Stats gathered on: 2024-05-20