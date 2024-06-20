
# Pystats results

- benchmark: coverage
- fork: python
- ref: caf6064a1bc15ac344afd78b780188e60b9c628e
- commit hash: caf6064
- commit date: 2024-05-18T22:40:51+00:00

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
<td align="right">2,389,635,152</td>
<td align="right">22.4%</td>
<td align="right">22.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">932,487,760</td>
<td align="right">8.8%</td>
<td align="right">31.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">932,319,560</td>
<td align="right">8.8%</td>
<td align="right">40.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">544,028,751</td>
<td align="right">5.1%</td>
<td align="right">45.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">524,690,829</td>
<td align="right">4.9%</td>
<td align="right">50.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">466,337,980</td>
<td align="right">4.4%</td>
<td align="right">54.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">388,587,595</td>
<td align="right">3.6%</td>
<td align="right">58.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">349,643,771</td>
<td align="right">3.3%</td>
<td align="right">61.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">349,633,880</td>
<td align="right">3.3%</td>
<td align="right">64.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">310,886,560</td>
<td align="right">2.9%</td>
<td align="right">67.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">233,287,557</td>
<td align="right">2.2%</td>
<td align="right">69.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">233,128,180</td>
<td align="right">2.2%</td>
<td align="right">71.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">233,080,360</td>
<td align="right">2.2%</td>
<td align="right">74.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">233,080,160</td>
<td align="right">2.2%</td>
<td align="right">76.3%</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">194,245,280</td>
<td align="right">1.8%</td>
<td align="right">78.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">155,485,000</td>
<td align="right">1.5%</td>
<td align="right">79.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">155,452,466</td>
<td align="right">1.5%</td>
<td align="right">81.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">155,425,140</td>
<td align="right">1.5%</td>
<td align="right">82.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">116,651,369</td>
<td align="right">1.1%</td>
<td align="right">83.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">116,573,940</td>
<td align="right">1.1%</td>
<td align="right">84.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">116,539,620</td>
<td align="right">1.1%</td>
<td align="right">85.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">77,867,100</td>
<td align="right">0.7%</td>
<td align="right">86.5%</td>
<td align="right">99.8%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">77,773,775</td>
<td align="right">0.7%</td>
<td align="right">87.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">77,759,480</td>
<td align="right">0.7%</td>
<td align="right">87.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">77,750,346</td>
<td align="right">0.7%</td>
<td align="right">88.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">77,733,940</td>
<td align="right">0.7%</td>
<td align="right">89.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">77,716,540</td>
<td align="right">0.7%</td>
<td align="right">90.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">77,708,500</td>
<td align="right">0.7%</td>
<td align="right">90.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">77,702,660</td>
<td align="right">0.7%</td>
<td align="right">91.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">77,699,500</td>
<td align="right">0.7%</td>
<td align="right">92.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_DICT</td>
<td align="right">77,698,860</td>
<td align="right">0.7%</td>
<td align="right">93.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">77,697,040</td>
<td align="right">0.7%</td>
<td align="right">93.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">DICT_MERGE</td>
<td align="right">77,694,240</td>
<td align="right">0.7%</td>
<td align="right">94.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">77,692,960</td>
<td align="right">0.7%</td>
<td align="right">95.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">58,272,000</td>
<td align="right">0.5%</td>
<td align="right">95.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">38,899,295</td>
<td align="right">0.4%</td>
<td align="right">96.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">38,868,760</td>
<td align="right">0.4%</td>
<td align="right">96.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">38,868,020</td>
<td align="right">0.4%</td>
<td align="right">96.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">38,860,000</td>
<td align="right">0.4%</td>
<td align="right">97.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">38,853,100</td>
<td align="right">0.4%</td>
<td align="right">97.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">38,851,060</td>
<td align="right">0.4%</td>
<td align="right">98.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">38,848,760</td>
<td align="right">0.4%</td>
<td align="right">98.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">38,847,260</td>
<td align="right">0.4%</td>
<td align="right">98.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">INSTRUMENTED_RESUME</td>
<td align="right">38,846,460</td>
<td align="right">0.4%</td>
<td align="right">99.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">UNARY_NEGATIVE</td>
<td align="right">38,846,260</td>
<td align="right">0.4%</td>
<td align="right">99.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">INSTRUMENTED_RETURN_VALUE</td>
<td align="right">38,845,760</td>
<td align="right">0.4%</td>
<td align="right">99.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">19,436,660</td>
<td align="right">0.2%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">177,758</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right">7.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">138,980</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right">3.8%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">71,897</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">58,600</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">54,120</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">33,060</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">28,600</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">27,600</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">24,640</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">21,540</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">21,460</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">19,880</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">19,800</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">19,080</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">18,920</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">18,760</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">18,480</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">16,320</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">16,080</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">14,520</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">14,500</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">14,360</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">13,320</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">11,280</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">11,000</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">11,000</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">9,989</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">8,860</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">8,680</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">8,460</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">7,380</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">7,211</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">6,980</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">6,700</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">6,500</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">6,440</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">5,920</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BUILD_SLICE</td>
<td align="right">5,440</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">5,400</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">5,049</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">4,380</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right">13.7%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">4,320</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CHECK_EXC_MATCH</td>
<td align="right">4,160</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">4,160</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">4,160</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">3,300</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_TUPLE_INT</td>
<td align="right">3,140</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">2,960</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">2,620</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">2,360</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">1,660</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">1,600</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">1,580</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT</td>
<td align="right">1,540</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">1,440</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">1,440</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">1,400</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right">80.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">1,360</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FORMAT_SIMPLE</td>
<td align="right">1,300</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">MAP_ADD</td>
<td align="right">1,280</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">UNPACK_EX</td>
<td align="right">1,280</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">COMPARE_OP_FLOAT</td>
<td align="right">1,140</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">1,040</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">1,000</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BUILD_STRING</td>
<td align="right">980</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">740</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_TYPE_1</td>
<td align="right">740</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">720</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right">16.7%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">660</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">660</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CONVERT_VALUE</td>
<td align="right">560</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">540</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">520</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_ATTR_WITH_HINT</td>
<td align="right">520</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">DELETE_ATTR</td>
<td align="right">480</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">480</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">420</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BEFORE_WITH</td>
<td align="right">360</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_GETITEM</td>
<td align="right">340</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CONTAINS_OP_SET</td>
<td align="right">340</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_STR_INT</td>
<td align="right">320</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right">6.2%</td>
</tr>
<tr>
<td align="left">STORE_GLOBAL</td>
<td align="right">320</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">RAISE_VARARGS</td>
<td align="right">260</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">RERAISE</td>
<td align="right">260</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">INSTRUMENTED_RETURN_CONST</td>
<td align="right">240</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">180</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR</td>
<td align="right">160</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">120</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">120</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">100</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">80</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">INSTRUMENTED_JUMP_BACKWARD</td>
<td align="right">80</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">UNARY_INVERT</td>
<td align="right">60</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">60</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_INT</td>
<td align="right">60</td>
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
<td align="left">FOR_ITER_RANGE</td>
<td align="right">20</td>
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
<td align="right">893,466,220</td>
<td align="right">8.4%</td>
<td align="right">8.4%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE LOAD_FAST</td>
<td align="right">796,390,391</td>
<td align="right">7.5%</td>
<td align="right">15.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST LOAD_CONST</td>
<td align="right">427,338,551</td>
<td align="right">4.0%</td>
<td align="right">19.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST LOAD_ATTR</td>
<td align="right">388,487,520</td>
<td align="right">3.6%</td>
<td align="right">23.5%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL POP_JUMP_IF_FALSE</td>
<td align="right">349,705,580</td>
<td align="right">3.3%</td>
<td align="right">26.8%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE LOAD_FAST</td>
<td align="right">310,771,580</td>
<td align="right">2.9%</td>
<td align="right">29.7%</td>
</tr>
<tr>
<td align="left">LOAD_CONST COMPARE_OP_STR</td>
<td align="right">310,767,851</td>
<td align="right">2.9%</td>
<td align="right">32.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE TO_BOOL_BOOL</td>
<td align="right">310,766,220</td>
<td align="right">2.9%</td>
<td align="right">35.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">233,087,640</td>
<td align="right">2.2%</td>
<td align="right">37.8%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE INTERPRETER_EXIT</td>
<td align="right">233,080,080</td>
<td align="right">2.2%</td>
<td align="right">40.0%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG POP_JUMP_IF_FALSE</td>
<td align="right">233,079,880</td>
<td align="right">2.2%</td>
<td align="right">42.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR LOAD_ATTR_SLOT</td>
<td align="right">194,230,200</td>
<td align="right">1.8%</td>
<td align="right">44.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR EXTENDED_ARG</td>
<td align="right">194,228,440</td>
<td align="right">1.8%</td>
<td align="right">45.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE LOAD_FAST</td>
<td align="right">174,897,220</td>
<td align="right">1.6%</td>
<td align="right">47.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE LOAD_GLOBAL_MODULE</td>
<td align="right">155,388,080</td>
<td align="right">1.5%</td>
<td align="right">48.9%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP POP_JUMP_IF_FALSE</td>
<td align="right">155,384,709</td>
<td align="right">1.5%</td>
<td align="right">50.3%</td>
</tr>
<tr>
<td align="left">RESUME LOAD_GLOBAL_MODULE</td>
<td align="right">155,383,800</td>
<td align="right">1.5%</td>
<td align="right">51.8%</td>
</tr>
<tr>
<td align="left">CACHE RESUME</td>
<td align="right">155,383,560</td>
<td align="right">1.5%</td>
<td align="right">53.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT CONTAINS_OP</td>
<td align="right">155,382,940</td>
<td align="right">1.5%</td>
<td align="right">54.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE RETURN_VALUE</td>
<td align="right">155,382,920</td>
<td align="right">1.5%</td>
<td align="right">56.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST LOAD_FAST</td>
<td align="right">116,608,046</td>
<td align="right">1.1%</td>
<td align="right">57.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT LOAD_FAST</td>
<td align="right">116,576,515</td>
<td align="right">1.1%</td>
<td align="right">58.4%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR POP_JUMP_IF_FALSE</td>
<td align="right">116,568,711</td>
<td align="right">1.1%</td>
<td align="right">59.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE LOAD_FAST</td>
<td align="right">116,543,960</td>
<td align="right">1.1%</td>
<td align="right">60.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">116,540,900</td>
<td align="right">1.1%</td>
<td align="right">61.7%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE LOAD_FAST</td>
<td align="right">116,539,360</td>
<td align="right">1.1%</td>
<td align="right">62.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR LOAD_ATTR</td>
<td align="right">77,812,180</td>
<td align="right">0.7%</td>
<td align="right">63.5%</td>
</tr>
<tr>
<td align="left">PUSH_NULL LOAD_FAST</td>
<td align="right">77,749,820</td>
<td align="right">0.7%</td>
<td align="right">64.2%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE LOAD_GLOBAL_MODULE</td>
<td align="right">77,731,529</td>
<td align="right">0.7%</td>
<td align="right">64.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST RETURN_VALUE</td>
<td align="right">77,708,280</td>
<td align="right">0.7%</td>
<td align="right">65.7%</td>
</tr>
<tr>
<td align="left">NOP LOAD_GLOBAL_MODULE</td>
<td align="right">77,707,300</td>
<td align="right">0.7%</td>
<td align="right">66.4%</td>
</tr>
<tr>
<td align="left">STORE_FAST LOAD_FAST_LOAD_FAST</td>
<td align="right">77,699,880</td>
<td align="right">0.7%</td>
<td align="right">67.1%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK NOP</td>
<td align="right">77,699,520</td>
<td align="right">0.7%</td>
<td align="right">67.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR STORE_FAST</td>
<td align="right">77,698,120</td>
<td align="right">0.7%</td>
<td align="right">68.6%</td>
</tr>
<tr>
<td align="left">LOAD_CONST COMPARE_OP_INT</td>
<td align="right">77,696,280</td>
<td align="right">0.7%</td>
<td align="right">69.3%</td>
</tr>
<tr>
<td align="left">BUILD_MAP LOAD_FAST</td>
<td align="right">77,695,640</td>
<td align="right">0.7%</td>
<td align="right">70.1%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS RESUME_CHECK</td>
<td align="right">77,695,320</td>
<td align="right">0.7%</td>
<td align="right">70.8%</td>
</tr>
<tr>
<td align="left">DICT_MERGE CALL_FUNCTION_EX</td>
<td align="right">77,694,240</td>
<td align="right">0.7%</td>
<td align="right">71.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST DICT_MERGE</td>
<td align="right">77,694,240</td>
<td align="right">0.7%</td>
<td align="right">72.2%</td>
</tr>
<tr>
<td align="left">CACHE COPY_FREE_VARS</td>
<td align="right">77,694,000</td>
<td align="right">0.7%</td>
<td align="right">73.0%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX RETURN_VALUE</td>
<td align="right">77,693,920</td>
<td align="right">0.7%</td>
<td align="right">73.7%</td>
</tr>
<tr>
<td align="left">RESUME LOAD_FAST</td>
<td align="right">77,693,680</td>
<td align="right">0.7%</td>
<td align="right">74.4%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS RESUME</td>
<td align="right">77,693,460</td>
<td align="right">0.7%</td>
<td align="right">75.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST TO_BOOL_BOOL</td>
<td align="right">77,693,360</td>
<td align="right">0.7%</td>
<td align="right">75.9%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O POP_TOP</td>
<td align="right">77,692,840</td>
<td align="right">0.7%</td>
<td align="right">76.6%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR LOAD_FAST</td>
<td align="right">77,692,220</td>
<td align="right">0.7%</td>
<td align="right">77.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">77,692,100</td>
<td align="right">0.7%</td>
<td align="right">78.1%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">77,691,840</td>
<td align="right">0.7%</td>
<td align="right">78.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE LOAD_DEREF</td>
<td align="right">77,691,820</td>
<td align="right">0.7%</td>
<td align="right">79.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST BUILD_MAP</td>
<td align="right">77,691,440</td>
<td align="right">0.7%</td>
<td align="right">80.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE CALL_PY_EXACT_ARGS</td>
<td align="right">77,691,340</td>
<td align="right">0.7%</td>
<td align="right">81.0%</td>
</tr>
<tr>
<td align="left">POP_TOP LOAD_FAST_LOAD_FAST</td>
<td align="right">77,691,300</td>
<td align="right">0.7%</td>
<td align="right">81.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE POP_JUMP_IF_NONE</td>
<td align="right">77,691,280</td>
<td align="right">0.7%</td>
<td align="right">82.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">77,691,220</td>
<td align="right">0.7%</td>
<td align="right">83.2%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF BINARY_SUBSCR_DICT</td>
<td align="right">77,691,200</td>
<td align="right">0.7%</td>
<td align="right">83.9%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_DICT PUSH_NULL</td>
<td align="right">77,691,200</td>
<td align="right">0.7%</td>
<td align="right">84.6%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE BINARY_SUBSCR</td>
<td align="right">77,691,180</td>
<td align="right">0.7%</td>
<td align="right">85.4%</td>
</tr>
<tr>
<td align="left">LOAD_CONST LOAD_FAST</td>
<td align="right">38,868,800</td>
<td align="right">0.4%</td>
<td align="right">85.7%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE LOAD_FAST</td>
<td align="right">38,868,340</td>
<td align="right">0.4%</td>
<td align="right">86.1%</td>
</tr>
<tr>
<td align="left">LOAD_CONST STORE_FAST</td>
<td align="right">38,865,520</td>
<td align="right">0.4%</td>
<td align="right">86.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST BUILD_TUPLE</td>
<td align="right">38,863,460</td>
<td align="right">0.4%</td>
<td align="right">86.8%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE LOAD_CONST</td>
<td align="right">38,855,040</td>
<td align="right">0.4%</td>
<td align="right">87.2%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE LOAD_GLOBAL_MODULE</td>
<td align="right">38,854,599</td>
<td align="right">0.4%</td>
<td align="right">87.6%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE LOAD_CONST</td>
<td align="right">38,852,920</td>
<td align="right">0.4%</td>
<td align="right">87.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST JUMP_FORWARD</td>
<td align="right">38,852,640</td>
<td align="right">0.4%</td>
<td align="right">88.3%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT POP_JUMP_IF_FALSE</td>
<td align="right">38,852,460</td>
<td align="right">0.4%</td>
<td align="right">88.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">38,851,880</td>
<td align="right">0.4%</td>
<td align="right">89.0%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR STORE_FAST</td>
<td align="right">38,850,940</td>
<td align="right">0.4%</td>
<td align="right">89.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE POP_JUMP_IF_FALSE</td>
<td align="right">38,850,240</td>
<td align="right">0.4%</td>
<td align="right">89.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR LOAD_FAST</td>
<td align="right">38,850,080</td>
<td align="right">0.4%</td>
<td align="right">90.1%</td>
</tr>
<tr>
<td align="left">LOAD_CONST BINARY_OP_SUBTRACT_INT</td>
<td align="right">38,849,160</td>
<td align="right">0.4%</td>
<td align="right">90.5%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD LOAD_FAST</td>
<td align="right">38,848,640</td>
<td align="right">0.4%</td>
<td align="right">90.8%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND LOAD_FAST</td>
<td align="right">38,848,280</td>
<td align="right">0.4%</td>
<td align="right">91.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR LOAD_CONST</td>
<td align="right">38,848,220</td>
<td align="right">0.4%</td>
<td align="right">91.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">38,848,060</td>
<td align="right">0.4%</td>
<td align="right">91.9%</td>
</tr>
<tr>
<td align="left">LOAD_CONST BINARY_OP_ADD_INT</td>
<td align="right">38,847,880</td>
<td align="right">0.4%</td>
<td align="right">92.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE TO_BOOL_NONE</td>
<td align="right">38,847,160</td>
<td align="right">0.4%</td>
<td align="right">92.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL POP_JUMP_IF_TRUE</td>
<td align="right">38,847,080</td>
<td align="right">0.4%</td>
<td align="right">93.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE TO_BOOL</td>
<td align="right">38,846,420</td>
<td align="right">0.4%</td>
<td align="right">93.4%</td>
</tr>
<tr>
<td align="left">UNARY_NEGATIVE LOAD_FAST</td>
<td align="right">38,846,260</td>
<td align="right">0.4%</td>
<td align="right">93.8%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR POP_JUMP_IF_TRUE</td>
<td align="right">38,846,120</td>
<td align="right">0.4%</td>
<td align="right">94.1%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_RESUME LOAD_FAST</td>
<td align="right">38,846,000</td>
<td align="right">0.4%</td>
<td align="right">94.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE COMPARE_OP_STR</td>
<td align="right">38,845,940</td>
<td align="right">0.4%</td>
<td align="right">94.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR UNARY_NEGATIVE</td>
<td align="right">38,845,920</td>
<td align="right">0.4%</td>
<td align="right">95.2%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE CALL_LIST_APPEND</td>
<td align="right">38,845,900</td>
<td align="right">0.4%</td>
<td align="right">95.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT BINARY_SUBSCR</td>
<td align="right">38,845,900</td>
<td align="right">0.4%</td>
<td align="right">96.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT STORE_FAST</td>
<td align="right">38,845,900</td>
<td align="right">0.4%</td>
<td align="right">96.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT STORE_FAST</td>
<td align="right">38,845,900</td>
<td align="right">0.4%</td>
<td align="right">96.7%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE POP_JUMP_IF_NONE</td>
<td align="right">38,845,900</td>
<td align="right">0.4%</td>
<td align="right">97.1%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS INSTRUMENTED_RESUME</td>
<td align="right">38,845,840</td>
<td align="right">0.4%</td>
<td align="right">97.4%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE LOAD_FAST</td>
<td align="right">38,845,720</td>
<td align="right">0.4%</td>
<td align="right">97.8%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST UNPACK_SEQUENCE_TUPLE</td>
<td align="right">38,845,680</td>
<td align="right">0.4%</td>
<td align="right">98.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL EXTENDED_ARG</td>
<td align="right">38,845,680</td>
<td align="right">0.4%</td>
<td align="right">98.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT CALL_PY_EXACT_ARGS</td>
<td align="right">38,845,360</td>
<td align="right">0.4%</td>
<td align="right">98.9%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL LOAD_FAST</td>
<td align="right">19,425,740</td>
<td align="right">0.2%</td>
<td align="right">99.1%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE LOAD_GLOBAL</td>
<td align="right">19,424,920</td>
<td align="right">0.2%</td>
<td align="right">99.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST INSTRUMENTED_RETURN_VALUE</td>
<td align="right">19,422,960</td>
<td align="right">0.2%</td>
<td align="right">99.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT INSTRUMENTED_RETURN_VALUE</td>
<td align="right">19,422,700</td>
<td align="right">0.2%</td>
<td align="right">99.6%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_RETURN_VALUE BINARY_OP_ADD_INT</td>
<td align="right">19,422,680</td>
<td align="right">0.2%</td>
<td align="right">99.8%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_RETURN_VALUE LOAD_GLOBAL_MODULE</td>
<td align="right">19,422,680</td>
<td align="right">0.2%</td>
<td align="right">100.0%</td>
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
<td align="right">15,640</td>
<td align="right">82.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">1,480</td>
<td align="right">7.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">960</td>
<td align="right">5.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">940</td>
<td align="right">4.9%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">40</td>
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
<td align="right">7,840</td>
<td align="right">41.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">6,460</td>
<td align="right">33.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,260</td>
<td align="right">6.6%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">960</td>
<td align="right">5.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">800</td>
<td align="right">4.2%</td>
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
<td align="left">RESUME</td>
<td align="right">155,383,560</td>
<td align="right">66.7%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">77,694,000</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">37,260</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">13,320</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">80</td>
<td align="right">0.0%</td>
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
<td align="right">280</td>
<td align="right">77.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">60</td>
<td align="right">16.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
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
<td align="left">POP_TOP</td>
<td align="right">240</td>
<td align="right">66.7%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">120</td>
<td align="right">33.3%</td>
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
<td align="right">80</td>
<td align="right">44.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">60</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">20</td>
<td align="right">11.1%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_STR_INT</td>
<td align="right">20</td>
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
<td align="left">JUMP_BACKWARD</td>
<td align="right">80</td>
<td align="right">44.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">60</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">20</td>
<td align="right">11.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">20</td>
<td align="right">11.1%</td>
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
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">77,691,180</td>
<td align="right">66.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">38,845,900</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">29,300</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BUILD_SLICE</td>
<td align="right">5,440</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">1,680</td>
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
<td align="right">77,692,220</td>
<td align="right">66.6%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">38,850,940</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">29,300</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">460</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">380</td>
<td align="right">0.0%</td>
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
<td align="right">4,080</td>
<td align="right">98.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">80</td>
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
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">4,160</td>
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
<td align="right">660</td>
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
<td align="right">660</td>
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
<td align="left">CONVERT_VALUE</td>
<td align="right">560</td>
<td align="right">43.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">360</td>
<td align="right">27.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">340</td>
<td align="right">26.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">40</td>
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
<td align="left">BUILD_STRING</td>
<td align="right">660</td>
<td align="right">50.8%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">640</td>
<td align="right">49.2%</td>
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
<td align="right">8,920</td>
<td align="right">44.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">6,500</td>
<td align="right">32.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">1,320</td>
<td align="right">6.6%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">1,020</td>
<td align="right">5.1%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">800</td>
<td align="right">4.0%</td>
</tr>
</tbody>
</table>

<table>
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
<td align="right">12,960</td>
<td align="right">65.2%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">3,000</td>
<td align="right">15.1%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">1,920</td>
<td align="right">9.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">1,200</td>
<td align="right">6.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">440</td>
<td align="right">2.2%</td>
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
<td align="right">233,080,080</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">33,060</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">15,040</td>
<td align="right">0.0%</td>
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
<td align="right">14,520</td>
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
<td align="right">14,280</td>
<td align="right">98.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">160</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">40</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">40</td>
<td align="right">0.3%</td>
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
<td align="left">RESUME_CHECK</td>
<td align="right">77,699,520</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">11,500</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">2,200</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">1,320</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">1,040</td>
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
<td align="right">77,707,300</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">5,340</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">1,420</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">1,400</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">380</td>
<td align="right">0.0%</td>
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
<td align="left">SWAP</td>
<td align="right">3,460</td>
<td align="right">83.2%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">420</td>
<td align="right">10.1%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">260</td>
<td align="right">6.2%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">20</td>
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
<td align="left">RETURN_VALUE</td>
<td align="right">3,460</td>
<td align="right">83.2%</td>
</tr>
<tr>
<td align="left">RERAISE</td>
<td align="right">260</td>
<td align="right">6.2%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">240</td>
<td align="right">5.8%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">180</td>
<td align="right">4.3%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">20</td>
<td align="right">0.5%</td>
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
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">77,692,840</td>
<td align="right">99.9%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">32,420</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">15,171</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CACHE</td>
<td align="right">13,320</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">4,540</td>
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
<td align="right">77,691,300</td>
<td align="right">99.9%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">32,220</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">18,926</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">13,180</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">7,409</td>
<td align="right">0.0%</td>
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
<td align="left">ENTER_EXECUTOR</td>
<td align="right">2,260</td>
<td align="right">54.3%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">820</td>
<td align="right">19.7%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">320</td>
<td align="right">7.7%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_DICT</td>
<td align="right">280</td>
<td align="right">6.7%</td>
</tr>
<tr>
<td align="left">RERAISE</td>
<td align="right">260</td>
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
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">4,000</td>
<td align="right">96.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">160</td>
<td align="right">3.8%</td>
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
<td align="left">BINARY_SUBSCR_DICT</td>
<td align="right">77,691,200</td>
<td align="right">99.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">60,900</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">3,640</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,280</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">1,040</td>
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
<td align="right">77,749,820</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">4,160</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">3,220</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">660</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">660</td>
<td align="right">0.0%</td>
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
<td align="left">COPY_FREE_VARS</td>
<td align="right">12,920</td>
<td align="right">97.0%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">180</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">160</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">60</td>
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
<td align="left">CALL_BUILTIN_O</td>
<td align="right">12,840</td>
<td align="right">96.4%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">200</td>
<td align="right">1.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">160</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">120</td>
<td align="right">0.9%</td>
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
<td align="right">155,382,920</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">77,708,280</td>
<td align="right">25.0%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">77,693,920</td>
<td align="right">25.0%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">33,260</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">11,260</td>
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
<td align="left">INTERPRETER_EXIT</td>
<td align="right">233,080,080</td>
<td align="right">75.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">77,691,840</td>
<td align="right">25.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">40,380</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">22,960</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">11,260</td>
<td align="right">0.0%</td>
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
<td align="right">340</td>
<td align="right">63.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">60</td>
<td align="right">11.1%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">40</td>
<td align="right">7.4%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">20</td>
<td align="right">3.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">20</td>
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
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">260</td>
<td align="right">48.1%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">80</td>
<td align="right">14.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">80</td>
<td align="right">14.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">40</td>
<td align="right">7.4%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">40</td>
<td align="right">7.4%</td>
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
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">38,846,420</td>
<td align="right">99.9%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">10,420</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">5,820</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">1,120</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">1,000</td>
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
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">38,847,080</td>
<td align="right">99.9%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">10,420</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">7,080</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">2,240</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">480</td>
<td align="right">0.0%</td>
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
<td align="right">60</td>
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
<td align="right">60</td>
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
<td align="left">LOAD_ATTR</td>
<td align="right">38,845,920</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">320</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
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
<td align="right">38,846,260</td>
<td align="right">100.0%</td>
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
<td align="left">TO_BOOL_INT</td>
<td align="right">40</td>
<td align="right">66.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
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
<td align="left">COPY</td>
<td align="right">40</td>
<td align="right">66.7%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">20</td>
<td align="right">33.3%</td>
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
<td align="left">BINARY_SLICE</td>
<td align="right">6,460</td>
<td align="right">44.6%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">2,920</td>
<td align="right">20.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,000</td>
<td align="right">13.8%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">840</td>
<td align="right">5.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">580</td>
<td align="right">4.0%</td>
</tr>
</tbody>
</table>

<table>
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
<td align="right">8,700</td>
<td align="right">60.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">1,400</td>
<td align="right">9.7%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">1,300</td>
<td align="right">9.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">840</td>
<td align="right">5.8%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">540</td>
<td align="right">3.7%</td>
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
<td align="left">LOAD_FAST</td>
<td align="right">2,900</td>
<td align="right">34.3%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">2,100</td>
<td align="right">24.8%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">1,120</td>
<td align="right">13.2%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">560</td>
<td align="right">6.6%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">400</td>
<td align="right">4.7%</td>
</tr>
</tbody>
</table>

<table>
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
<td align="right">4,280</td>
<td align="right">50.6%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">2,380</td>
<td align="right">28.1%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">1,200</td>
<td align="right">14.2%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">240</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">240</td>
<td align="right">2.8%</td>
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
<td align="left">LOAD_FAST</td>
<td align="right">77,691,440</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">4,860</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">2,800</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">1,280</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
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
<td align="left">LOAD_FAST</td>
<td align="right">77,695,640</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">5,500</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">1,280</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">80</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_GLOBAL</td>
<td align="right">80</td>
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
<td align="right">5,440</td>
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
<td align="right">5,440</td>
<td align="right">100.0%</td>
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
<td align="right">660</td>
<td align="right">67.3%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">320</td>
<td align="right">32.7%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">340</td>
<td align="right">34.7%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">320</td>
<td align="right">32.7%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">160</td>
<td align="right">16.3%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">160</td>
<td align="right">16.3%</td>
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
<td align="right">38,863,460</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">4,040</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">380</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">320</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">280</td>
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
<td align="left">CALL_LIST_APPEND</td>
<td align="right">38,845,900</td>
<td align="right">99.9%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">13,320</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">3,720</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">2,340</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,300</td>
<td align="right">0.0%</td>
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
<td align="right">4,640</td>
<td align="right">28.9%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">3,820</td>
<td align="right">23.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">1,900</td>
<td align="right">11.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">720</td>
<td align="right">4.5%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">660</td>
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
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">3,020</td>
<td align="right">18.8%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">1,800</td>
<td align="right">11.2%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">1,720</td>
<td align="right">10.7%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">1,080</td>
<td align="right">6.7%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">840</td>
<td align="right">5.2%</td>
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
<td align="right">77,694,240</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,360</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">1,280</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">80</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">MAP_ADD</td>
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
<td align="left">RETURN_VALUE</td>
<td align="right">77,693,920</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">1,280</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">1,240</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">160</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">120</td>
<td align="right">0.0%</td>
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
<td align="left">LIST_EXTEND</td>
<td align="right">1,440</td>
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
<td align="left">UNPACK_EX</td>
<td align="right">1,280</td>
<td align="right">88.9%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">80</td>
<td align="right">5.6%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">80</td>
<td align="right">5.6%</td>
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
<td align="right">4,380</td>
<td align="right">81.1%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">920</td>
<td align="right">17.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">100</td>
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
<td align="left">RETURN_VALUE</td>
<td align="right">1,600</td>
<td align="right">29.6%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">1,560</td>
<td align="right">28.9%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">1,340</td>
<td align="right">24.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">480</td>
<td align="right">8.9%</td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">320</td>
<td align="right">5.9%</td>
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
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">3,880</td>
<td align="right">65.5%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">960</td>
<td align="right">16.2%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">280</td>
<td align="right">4.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">200</td>
<td align="right">3.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">140</td>
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
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">4,880</td>
<td align="right">82.4%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">300</td>
<td align="right">5.1%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">280</td>
<td align="right">4.7%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">220</td>
<td align="right">3.7%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">160</td>
<td align="right">2.7%</td>
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
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">155,382,940</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">38,500</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">1,040</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">749</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">660</td>
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
<td align="right">155,384,709</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">38,500</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">1,040</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">651</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">160</td>
<td align="right">0.0%</td>
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
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">480</td>
<td align="right">85.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">80</td>
<td align="right">14.3%</td>
</tr>
</tbody>
</table>

<table>
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
<td align="right">560</td>
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
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">7,600</td>
<td align="right">38.4%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">4,660</td>
<td align="right">23.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">3,920</td>
<td align="right">19.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">980</td>
<td align="right">4.9%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">960</td>
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
<td align="left">TO_BOOL_STR</td>
<td align="right">13,660</td>
<td align="right">69.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">3,860</td>
<td align="right">19.5%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">1,000</td>
<td align="right">5.1%</td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">260</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">240</td>
<td align="right">1.2%</td>
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
<td align="right">77,694,000</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">13,720</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">400</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">300</td>
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
<td align="right">77,695,320</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">12,920</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">260</td>
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
<td align="right">480</td>
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
<td align="right">320</td>
<td align="right">66.7%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">160</td>
<td align="right">33.3%</td>
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
<td align="right">77,694,240</td>
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
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">77,694,240</td>
<td align="right">100.0%</td>
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
<td align="right">32,220</td>
<td align="right">44.8%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">10,700</td>
<td align="right">14.9%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">6,940</td>
<td align="right">9.7%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">6,900</td>
<td align="right">9.6%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">5,900</td>
<td align="right">8.2%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">18,640</td>
<td align="right">25.9%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">15,171</td>
<td align="right">21.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">9,530</td>
<td align="right">13.3%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">6,420</td>
<td align="right">8.9%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">5,900</td>
<td align="right">8.2%</td>
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
<td align="right">194,228,440</td>
<td align="right">83.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">38,845,680</td>
<td align="right">16.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">5,680</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">320</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
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
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">233,079,880</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">320</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">80</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">80</td>
<td align="right">0.0%</td>
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
<td align="left">JUMP_BACKWARD</td>
<td align="right">3,340</td>
<td align="right">51.4%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">1,920</td>
<td align="right">29.5%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">600</td>
<td align="right">9.2%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">440</td>
<td align="right">6.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">120</td>
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
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">2,129</td>
<td align="right">32.8%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">2,111</td>
<td align="right">32.5%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">600</td>
<td align="right">9.2%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">440</td>
<td align="right">6.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">311</td>
<td align="right">4.8%</td>
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
<td align="right">1,600</td>
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
<td align="right">1,600</td>
<td align="right">100.0%</td>
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
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">1,060</td>
<td align="right">63.9%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">320</td>
<td align="right">19.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">240</td>
<td align="right">14.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">40</td>
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
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">1,400</td>
<td align="right">84.3%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">100</td>
<td align="right">6.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">80</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">80</td>
<td align="right">4.8%</td>
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
<td align="right">2,960</td>
<td align="right">26.9%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">2,220</td>
<td align="right">20.2%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">1,760</td>
<td align="right">16.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">1,240</td>
<td align="right">11.3%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">1,120</td>
<td align="right">10.2%</td>
</tr>
</tbody>
</table>

<table>
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
<td align="right">4,140</td>
<td align="right">37.6%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">3,340</td>
<td align="right">30.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,220</td>
<td align="right">11.1%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">520</td>
<td align="right">4.7%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">404</td>
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
<td align="left">STORE_FAST</td>
<td align="right">38,852,640</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">4,780</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">1,380</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">520</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">320</td>
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
<td align="right">38,848,640</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">5,100</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">3,520</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">2,200</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">320</td>
<td align="right">0.0%</td>
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
<td align="right">3,980</td>
<td align="right">92.1%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">340</td>
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
<td align="left">ENTER_EXECUTOR</td>
<td align="right">3,200</td>
<td align="right">74.1%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">1,120</td>
<td align="right">25.9%</td>
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
<td align="left">LOAD_FAST</td>
<td align="right">1,360</td>
<td align="right">94.4%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">80</td>
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
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">1,440</td>
<td align="right">100.0%</td>
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
<td align="right">388,487,520</td>
<td align="right">83.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">77,812,180</td>
<td align="right">16.7%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">31,460</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">1,920</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">1,660</td>
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
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">194,230,200</td>
<td align="right">41.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">77,812,180</td>
<td align="right">16.7%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">77,698,120</td>
<td align="right">16.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">38,850,080</td>
<td align="right">8.3%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">38,848,220</td>
<td align="right">8.3%</td>
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
<td align="right">427,338,551</td>
<td align="right">78.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">38,855,040</td>
<td align="right">7.1%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">38,852,920</td>
<td align="right">7.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">38,848,220</td>
<td align="right">7.1%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">34,180</td>
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
<td align="left">COMPARE_OP_STR</td>
<td align="right">310,767,851</td>
<td align="right">57.1%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">77,696,280</td>
<td align="right">14.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">38,868,800</td>
<td align="right">7.1%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">38,865,520</td>
<td align="right">7.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">38,849,160</td>
<td align="right">7.1%</td>
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
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">77,691,820</td>
<td align="right">99.9%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">18,060</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">13,300</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">3,600</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">2,960</td>
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
<td align="left">BINARY_SUBSCR_DICT</td>
<td align="right">77,691,200</td>
<td align="right">99.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">19,120</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">5,940</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">5,900</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">3,580</td>
<td align="right">0.0%</td>
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
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">796,390,391</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">310,771,580</td>
<td align="right">13.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">174,897,220</td>
<td align="right">7.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">116,608,046</td>
<td align="right">4.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">116,576,515</td>
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
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">893,466,220</td>
<td align="right">37.4%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">427,338,551</td>
<td align="right">17.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">388,487,520</td>
<td align="right">16.3%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">233,087,640</td>
<td align="right">9.8%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">77,708,280</td>
<td align="right">3.3%</td>
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
<td align="right">1,200</td>
<td align="right">88.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">160</td>
<td align="right">11.8%</td>
</tr>
</tbody>
</table>

<table>
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
<td align="right">1,200</td>
<td align="right">88.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">160</td>
<td align="right">11.8%</td>
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
<td align="right">120</td>
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
<td align="left">TO_BOOL_LIST</td>
<td align="right">80</td>
<td align="right">66.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">40</td>
<td align="right">33.3%</td>
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
<td align="left">STORE_FAST</td>
<td align="right">77,699,880</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">77,691,300</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">34,100</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">12,960</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">11,300</td>
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
<td align="right">116,540,900</td>
<td align="right">75.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">38,848,060</td>
<td align="right">25.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">28,460</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">12,960</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">10,160</td>
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
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">19,424,920</td>
<td align="right">99.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">1,640</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,440</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">1,240</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">1,040</td>
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
<td align="right">19,425,740</td>
<td align="right">99.9%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">4,520</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">1,920</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">1,800</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">580</td>
<td align="right">0.0%</td>
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
<td align="right">160</td>
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
<td align="right">80</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">40</td>
<td align="right">25.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">20</td>
<td align="right">12.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">20</td>
<td align="right">12.5%</td>
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
<td align="right">6,560</td>
<td align="right">94.0%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">240</td>
<td align="right">3.4%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">100</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">CACHE</td>
<td align="right">80</td>
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
<td align="right">6,660</td>
<td align="right">95.4%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">240</td>
<td align="right">3.4%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">80</td>
<td align="right">1.1%</td>
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
<td align="left">LOAD_FAST</td>
<td align="right">1,120</td>
<td align="right">87.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">80</td>
<td align="right">6.2%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">80</td>
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
<td align="left">LOAD_CONST</td>
<td align="right">1,200</td>
<td align="right">93.8%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">80</td>
<td align="right">6.2%</td>
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
<td align="right">349,705,580</td>
<td align="right">37.5%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">233,079,880</td>
<td align="right">25.0%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">155,384,709</td>
<td align="right">16.7%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">116,568,711</td>
<td align="right">12.5%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">38,852,460</td>
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
<td align="right">796,390,391</td>
<td align="right">85.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">77,731,529</td>
<td align="right">8.3%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">38,855,040</td>
<td align="right">4.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">19,424,920</td>
<td align="right">2.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">34,100</td>
<td align="right">0.0%</td>
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
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">77,691,280</td>
<td align="right">66.7%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">38,845,900</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,400</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
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
<td align="left">LOAD_FAST</td>
<td align="right">116,539,360</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">140</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">80</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">20</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">20</td>
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
<td align="right">13,840</td>
<td align="right">84.8%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_TUPLE_INT</td>
<td align="right">1,260</td>
<td align="right">7.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">720</td>
<td align="right">4.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">220</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">180</td>
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
<td align="left">LOAD_FAST</td>
<td align="right">9,400</td>
<td align="right">57.6%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">4,200</td>
<td align="right">25.7%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">1,320</td>
<td align="right">8.1%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">380</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">340</td>
<td align="right">2.1%</td>
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
<td align="left">TO_BOOL</td>
<td align="right">38,847,080</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">38,846,120</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">36,335</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">14,420</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">2,160</td>
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
<td align="right">38,868,340</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">38,854,599</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">7,600</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">5,620</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">4,440</td>
<td align="right">0.0%</td>
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
<td align="left">LOAD_CONST</td>
<td align="right">260</td>
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
<td align="left">COPY</td>
<td align="right">260</td>
<td align="right">100.0%</td>
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
<td align="left">POP_EXCEPT</td>
<td align="right">260</td>
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
<td align="left">PUSH_EXC_INFO</td>
<td align="right">260</td>
<td align="right">100.0%</td>
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
<td align="right">18,926</td>
<td align="right">66.2%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">4,700</td>
<td align="right">16.4%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">1,340</td>
<td align="right">4.7%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">1,005</td>
<td align="right">3.5%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">820</td>
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
<td align="left">INTERPRETER_EXIT</td>
<td align="right">15,040</td>
<td align="right">52.6%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">4,540</td>
<td align="right">15.9%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">4,140</td>
<td align="right">14.5%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">3,380</td>
<td align="right">11.8%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">660</td>
<td align="right">2.3%</td>
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
<td align="right">14,280</td>
<td align="right">99.4%</td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">80</td>
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
<td align="left">LOAD_FAST</td>
<td align="right">6,460</td>
<td align="right">45.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">6,420</td>
<td align="right">44.7%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">1,360</td>
<td align="right">9.5%</td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">80</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">40</td>
<td align="right">0.3%</td>
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
<td align="right">12,940</td>
<td align="right">60.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">5,440</td>
<td align="right">25.3%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">2,160</td>
<td align="right">10.0%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">880</td>
<td align="right">4.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">40</td>
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
<td align="left">LOAD_FAST</td>
<td align="right">4,900</td>
<td align="right">22.7%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">4,820</td>
<td align="right">22.4%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">4,360</td>
<td align="right">20.2%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">2,160</td>
<td align="right">10.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">1,560</td>
<td align="right">7.2%</td>
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
<td align="left">RETURN_VALUE</td>
<td align="right">6,460</td>
<td align="right">96.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">120</td>
<td align="right">1.8%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">120</td>
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
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">6,420</td>
<td align="right">95.8%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">240</td>
<td align="right">3.6%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">40</td>
<td align="right">0.6%</td>
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
<td align="left">LOAD_ATTR</td>
<td align="right">77,698,120</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">38,865,520</td>
<td align="right">16.7%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">38,850,940</td>
<td align="right">16.7%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">38,845,900</td>
<td align="right">16.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">38,845,900</td>
<td align="right">16.7%</td>
</tr>
</tbody>
</table>

<table>
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
<td align="right">116,608,046</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">77,699,880</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">38,852,640</td>
<td align="right">16.7%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">36,051</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">33,240</td>
<td align="right">0.0%</td>
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
<td align="right">960</td>
<td align="right">92.3%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">60</td>
<td align="right">5.8%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">20</td>
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
<td align="left">PUSH_NULL</td>
<td align="right">1,040</td>
<td align="right">100.0%</td>
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
<td align="right">5,029</td>
<td align="right">50.3%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">1,520</td>
<td align="right">15.2%</td>
</tr>
<tr>
<td align="left">UNPACK_EX</td>
<td align="right">1,280</td>
<td align="right">12.8%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">1,200</td>
<td align="right">12.0%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">560</td>
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
<td align="right">4,480</td>
<td align="right">44.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">1,340</td>
<td align="right">13.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">1,240</td>
<td align="right">12.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">1,229</td>
<td align="right">12.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">1,200</td>
<td align="right">12.0%</td>
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
<td align="left">LOAD_FAST</td>
<td align="right">160</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">80</td>
<td align="right">25.0%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">80</td>
<td align="right">25.0%</td>
</tr>
</tbody>
</table>

<table>
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
<td align="right">160</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">80</td>
<td align="right">25.0%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_RETURN_CONST</td>
<td align="right">80</td>
<td align="right">25.0%</td>
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
<td align="left">LOAD_FAST</td>
<td align="right">3,540</td>
<td align="right">48.0%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">1,200</td>
<td align="right">16.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">1,200</td>
<td align="right">16.3%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">800</td>
<td align="right">10.8%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">260</td>
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
<td align="left">POP_EXCEPT</td>
<td align="right">3,460</td>
<td align="right">46.9%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">1,120</td>
<td align="right">15.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">1,120</td>
<td align="right">15.2%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">760</td>
<td align="right">10.3%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">440</td>
<td align="right">6.0%</td>
</tr>
</tbody>
</table>


</details>

### UNPACK_EX

<details>
<summary> Successors and predecessors for UNPACK_EX </summary>

<table>
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
<td align="right">1,280</td>
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
<td align="right">1,280</td>
<td align="right">100.0%</td>
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
<td align="right">200</td>
<td align="right">38.5%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">160</td>
<td align="right">30.8%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">40</td>
<td align="right">7.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">40</td>
<td align="right">7.7%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">40</td>
<td align="right">7.7%</td>
</tr>
</tbody>
</table>

<table>
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
<td align="right">220</td>
<td align="right">42.3%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">180</td>
<td align="right">34.6%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">80</td>
<td align="right">15.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">40</td>
<td align="right">7.7%</td>
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
<td align="right">18,640</td>
<td align="right">56.4%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">13,260</td>
<td align="right">40.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">380</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">BUILD_STRING</td>
<td align="right">340</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">240</td>
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
<td align="left">INTERPRETER_EXIT</td>
<td align="right">33,060</td>
<td align="right">100.0%</td>
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
<td align="right">155,383,560</td>
<td align="right">66.7%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">77,693,460</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">1,720</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_RESUME</td>
<td align="right">320</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
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
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">155,383,800</td>
<td align="right">66.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">77,693,680</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">1,240</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">400</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_RESUME</td>
<td align="right">360</td>
<td align="right">0.0%</td>
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
<td align="right">38,847,880</td>
<td align="right">66.7%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_RETURN_VALUE</td>
<td align="right">19,422,680</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">1,280</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">140</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_INT</td>
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
<td align="left">BINARY_SUBSCR</td>
<td align="right">38,845,900</td>
<td align="right">66.7%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_RETURN_VALUE</td>
<td align="right">19,422,700</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">1,780</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">1,480</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">100</td>
<td align="right">0.0%</td>
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
<td align="right">10,160</td>
<td align="right">54.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">8,520</td>
<td align="right">45.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">40</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">40</td>
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
<td align="right">10,660</td>
<td align="right">56.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">7,960</td>
<td align="right">42.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">80</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">40</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">20</td>
<td align="right">0.1%</td>
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
<td align="left">LOAD_CONST</td>
<td align="right">40</td>
<td align="right">66.7%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_TUPLE_INT</td>
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
<td align="left">LOAD_CONST</td>
<td align="right">20</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">20</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">20</td>
<td align="right">33.3%</td>
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
<td align="left">RETURN_VALUE</td>
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
<td align="right">38,849,160</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,540</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">1,400</td>
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
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">38,845,360</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">3,800</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,540</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">1,240</td>
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
<td align="left">LOAD_DEREF</td>
<td align="right">77,691,200</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">5,840</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">720</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">520</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">260</td>
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
<td align="left">PUSH_NULL</td>
<td align="right">77,691,200</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">2,280</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">1,720</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">1,220</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">1,160</td>
<td align="right">0.0%</td>
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
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">260</td>
<td align="right">76.5%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">80</td>
<td align="right">23.5%</td>
</tr>
</tbody>
</table>

<table>
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
<td align="right">340</td>
<td align="right">100.0%</td>
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
<td align="right">1,320</td>
<td align="right">85.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">200</td>
<td align="right">13.0%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">20</td>
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
<td align="left">STORE_FAST</td>
<td align="right">1,260</td>
<td align="right">84.0%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">200</td>
<td align="right">13.3%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">40</td>
<td align="right">2.7%</td>
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
<td align="left">CALL_LEN</td>
<td align="right">200</td>
<td align="right">62.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">100</td>
<td align="right">31.2%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">20</td>
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
<td align="right">200</td>
<td align="right">62.5%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">60</td>
<td align="right">18.8%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">20</td>
<td align="right">6.2%</td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">20</td>
<td align="right">6.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">20</td>
<td align="right">6.2%</td>
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
<td align="right">3,080</td>
<td align="right">98.1%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">60</td>
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
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">1,260</td>
<td align="right">40.1%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">1,140</td>
<td align="right">36.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">540</td>
<td align="right">17.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">80</td>
<td align="right">2.5%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">60</td>
<td align="right">1.9%</td>
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
<td align="left">CALL</td>
<td align="right">200</td>
<td align="right">30.3%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">160</td>
<td align="right">24.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">140</td>
<td align="right">21.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">60</td>
<td align="right">9.1%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">40</td>
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
<td align="left">RESUME_CHECK</td>
<td align="right">660</td>
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
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">280</td>
<td align="right">38.9%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">180</td>
<td align="right">25.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">100</td>
<td align="right">13.9%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">40</td>
<td align="right">5.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">40</td>
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
<td align="left">RESUME</td>
<td align="right">300</td>
<td align="right">41.7%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">300</td>
<td align="right">41.7%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">120</td>
<td align="right">16.7%</td>
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
<td align="right">1,280</td>
<td align="right">48.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">440</td>
<td align="right">16.8%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">320</td>
<td align="right">12.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">240</td>
<td align="right">9.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">200</td>
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
<td align="left">LOAD_FAST</td>
<td align="right">900</td>
<td align="right">34.4%</td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">820</td>
<td align="right">31.3%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">280</td>
<td align="right">10.7%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">240</td>
<td align="right">9.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">180</td>
<td align="right">6.9%</td>
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
<td align="right">12,720</td>
<td align="right">67.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">3,180</td>
<td align="right">16.8%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">1,800</td>
<td align="right">9.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">640</td>
<td align="right">3.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">440</td>
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
<td align="left">TO_BOOL_BOOL</td>
<td align="right">8,220</td>
<td align="right">43.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">4,380</td>
<td align="right">23.2%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">1,840</td>
<td align="right">9.7%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">1,420</td>
<td align="right">7.5%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">1,040</td>
<td align="right">5.5%</td>
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
<td align="right">51,260</td>
<td align="right">94.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">1,240</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">1,240</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">240</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">80</td>
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
<td align="right">36,280</td>
<td align="right">67.0%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">7,600</td>
<td align="right">14.0%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">5,300</td>
<td align="right">9.8%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">3,620</td>
<td align="right">6.7%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">1,240</td>
<td align="right">2.3%</td>
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
<td align="right">12,840</td>
<td align="right">52.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">10,160</td>
<td align="right">41.2%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">1,040</td>
<td align="right">4.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">120</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">100</td>
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
<td align="left">TO_BOOL_BOOL</td>
<td align="right">24,040</td>
<td align="right">97.6%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">540</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">60</td>
<td align="right">0.2%</td>
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
<td align="left">LOAD_ATTR</td>
<td align="right">29,320</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">27,660</td>
<td align="right">47.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">980</td>
<td align="right">1.7%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">360</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">280</td>
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
<td align="left">RETURN_VALUE</td>
<td align="right">33,260</td>
<td align="right">56.8%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">25,100</td>
<td align="right">42.8%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">220</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">20</td>
<td align="right">0.0%</td>
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
<td align="right">6,060</td>
<td align="right">94.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">180</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">160</td>
<td align="right">2.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">40</td>
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
<td align="left">LOAD_CONST</td>
<td align="right">2,400</td>
<td align="right">37.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,320</td>
<td align="right">20.5%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">1,260</td>
<td align="right">19.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">560</td>
<td align="right">8.7%</td>
</tr>
<tr>
<td align="left">UNARY_NEGATIVE</td>
<td align="right">320</td>
<td align="right">5.0%</td>
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
<td align="left">BUILD_TUPLE</td>
<td align="right">38,845,900</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">1,240</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">900</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">520</td>
<td align="right">0.0%</td>
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
<td align="left">LOAD_FAST</td>
<td align="right">38,848,280</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">320</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">100</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_RETURN_CONST</td>
<td align="right">60</td>
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
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">38,851,880</td>
<td align="right">99.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">27,135</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">18,060</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_DICT</td>
<td align="right">1,220</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">740</td>
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
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">38,845,680</td>
<td align="right">99.9%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">22,995</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">13,260</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">8,060</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">3,880</td>
<td align="right">0.0%</td>
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
<td align="left">LOAD_FAST</td>
<td align="right">5,320</td>
<td align="right">73.8%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">1,051</td>
<td align="right">14.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">680</td>
<td align="right">9.4%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">120</td>
<td align="right">1.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">40</td>
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
<td align="left">LOAD_CONST</td>
<td align="right">5,340</td>
<td align="right">74.1%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">960</td>
<td align="right">13.3%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">631</td>
<td align="right">8.8%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">160</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">120</td>
<td align="right">1.7%</td>
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
<td align="right">2,220</td>
<td align="right">94.1%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">140</td>
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
<td align="left">STORE_FAST</td>
<td align="right">1,560</td>
<td align="right">66.1%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">800</td>
<td align="right">33.9%</td>
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
<td align="right">77,691,220</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_DICT</td>
<td align="right">500</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">460</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">440</td>
<td align="right">0.0%</td>
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
<td align="left">POP_TOP</td>
<td align="right">77,692,840</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">60</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">40</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">20</td>
<td align="right">0.0%</td>
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
<td align="left">BUILD_TUPLE</td>
<td align="right">3,720</td>
<td align="right">42.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,460</td>
<td align="right">16.8%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">1,200</td>
<td align="right">13.8%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">660</td>
<td align="right">7.6%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">600</td>
<td align="right">6.9%</td>
</tr>
</tbody>
</table>

<table>
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
<td align="right">3,920</td>
<td align="right">45.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">1,920</td>
<td align="right">22.1%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">1,040</td>
<td align="right">12.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">960</td>
<td align="right">11.1%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">340</td>
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
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">77,691,340</td>
<td align="right">66.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">38,845,360</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">72,989</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">12,960</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">9,220</td>
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
<td align="left">RESUME</td>
<td align="right">77,693,460</td>
<td align="right">66.6%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_RESUME</td>
<td align="right">38,845,840</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">87,629</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">13,720</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">6,560</td>
<td align="right">0.0%</td>
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
<td align="left">LOAD_FAST</td>
<td align="right">10,000</td>
<td align="right">90.9%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">360</td>
<td align="right">3.3%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">340</td>
<td align="right">3.1%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">120</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">80</td>
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
<td align="left">RESUME_CHECK</td>
<td align="right">10,580</td>
<td align="right">96.2%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">400</td>
<td align="right">3.6%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">20</td>
<td align="right">0.2%</td>
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
<td align="right">220</td>
<td align="right">29.7%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">200</td>
<td align="right">27.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">200</td>
<td align="right">27.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">80</td>
<td align="right">10.8%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
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
<td align="left">LOAD_CONST</td>
<td align="right">220</td>
<td align="right">29.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">220</td>
<td align="right">29.7%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">200</td>
<td align="right">27.0%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">60</td>
<td align="right">8.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">20</td>
<td align="right">2.7%</td>
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
<td align="left">LOAD_FAST</td>
<td align="right">740</td>
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
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">740</td>
<td align="right">100.0%</td>
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
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">1,120</td>
<td align="right">98.2%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">20</td>
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
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">1,140</td>
<td align="right">100.0%</td>
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
<td align="right">77,696,280</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">1,260</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">1,120</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">560</td>
<td align="right">0.0%</td>
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
<td align="right">38,852,460</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">38,845,900</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">1,140</td>
<td align="right">0.0%</td>
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
<td align="left">LOAD_CONST</td>
<td align="right">310,767,851</td>
<td align="right">88.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">38,845,940</td>
<td align="right">11.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">28,460</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">540</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
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
<td align="left">EXTENDED_ARG</td>
<td align="right">194,228,440</td>
<td align="right">55.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">116,568,711</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">38,846,120</td>
<td align="right">11.1%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">500</td>
<td align="right">0.0%</td>
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
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">5,900</td>
<td align="right">52.3%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">4,640</td>
<td align="right">41.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">460</td>
<td align="right">4.1%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">160</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
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
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">11,280</td>
<td align="right">100.0%</td>
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
<td align="left">LOAD_FAST</td>
<td align="right">160</td>
<td align="right">47.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">100</td>
<td align="right">29.4%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">80</td>
<td align="right">23.5%</td>
</tr>
</tbody>
</table>

<table>
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
<td align="right">320</td>
<td align="right">94.1%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">20</td>
<td align="right">5.9%</td>
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
<td align="left">LOAD_FAST</td>
<td align="right">13,040</td>
<td align="right">60.8%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">4,140</td>
<td align="right">19.3%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">3,000</td>
<td align="right">14.0%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">760</td>
<td align="right">3.5%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">440</td>
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
<td align="left">STORE_FAST</td>
<td align="right">17,695</td>
<td align="right">82.5%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">1,005</td>
<td align="right">4.7%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">960</td>
<td align="right">4.5%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">420</td>
<td align="right">2.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">420</td>
<td align="right">2.0%</td>
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
<td align="right">20</td>
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
<td align="right">20</td>
<td align="right">100.0%</td>
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
<td align="left">JUMP_BACKWARD</td>
<td align="right">520</td>
<td align="right">52.0%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">440</td>
<td align="right">44.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">40</td>
<td align="right">4.0%</td>
</tr>
</tbody>
</table>

<table>
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
<td align="right">740</td>
<td align="right">74.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">100</td>
<td align="right">10.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">80</td>
<td align="right">8.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">40</td>
<td align="right">4.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">40</td>
<td align="right">4.0%</td>
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
<td align="left">LOAD_ATTR</td>
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
<td align="left">LOAD_CONST</td>
<td align="right">60</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">40</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">20</td>
<td align="right">16.7%</td>
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
<td align="right">893,466,220</td>
<td align="right">95.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">38,848,060</td>
<td align="right">4.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">3,540</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">1,160</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">580</td>
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
<td align="right">310,766,220</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">155,382,920</td>
<td align="right">16.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">116,543,960</td>
<td align="right">12.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">77,692,100</td>
<td align="right">8.3%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">77,691,340</td>
<td align="right">8.3%</td>
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
<td align="right">80</td>
<td align="right">80.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">20</td>
<td align="right">20.0%</td>
</tr>
</tbody>
</table>

<table>
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
<td align="right">100</td>
<td align="right">100.0%</td>
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
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">77,692,100</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">77,691,840</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">40,546</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">19,120</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">4,120</td>
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
<td align="right">116,576,515</td>
<td align="right">75.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">38,851,880</td>
<td align="right">25.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">16,991</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">2,960</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">2,220</td>
<td align="right">0.0%</td>
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
<td align="right">1,780</td>
<td align="right">40.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">1,520</td>
<td align="right">34.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">920</td>
<td align="right">21.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">120</td>
<td align="right">2.7%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">20</td>
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
<td align="left">LOAD_FAST</td>
<td align="right">1,300</td>
<td align="right">29.7%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">1,040</td>
<td align="right">23.7%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">1,000</td>
<td align="right">22.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">600</td>
<td align="right">13.7%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">400</td>
<td align="right">9.1%</td>
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
<td align="right">117,549</td>
<td align="right">66.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">43,229</td>
<td align="right">24.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">14,220</td>
<td align="right">8.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">2,320</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">280</td>
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
<td align="left">PUSH_NULL</td>
<td align="right">60,900</td>
<td align="right">34.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">43,229</td>
<td align="right">24.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">15,120</td>
<td align="right">8.5%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">13,829</td>
<td align="right">7.8%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">9,180</td>
<td align="right">5.2%</td>
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
<td align="right">1,280</td>
<td align="right">81.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">260</td>
<td align="right">16.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">40</td>
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
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">1,000</td>
<td align="right">63.3%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">180</td>
<td align="right">11.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">160</td>
<td align="right">10.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">100</td>
<td align="right">6.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">80</td>
<td align="right">5.1%</td>
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
<td align="right">240</td>
<td align="right">57.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">80</td>
<td align="right">19.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">60</td>
<td align="right">14.3%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">40</td>
<td align="right">9.5%</td>
</tr>
</tbody>
</table>

<table>
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
<td align="right">360</td>
<td align="right">85.7%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">60</td>
<td align="right">14.3%</td>
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
<td align="left">LOAD_ATTR</td>
<td align="right">194,230,200</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">12,840</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
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
<td align="left">CONTAINS_OP</td>
<td align="right">155,382,940</td>
<td align="right">80.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">38,845,900</td>
<td align="right">20.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">10,160</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">2,540</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,360</td>
<td align="right">0.0%</td>
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
<td align="right">1,920</td>
<td align="right">58.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">700</td>
<td align="right">21.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">640</td>
<td align="right">19.4%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">40</td>
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
<td align="left">LOAD_FAST</td>
<td align="right">580</td>
<td align="right">17.6%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">400</td>
<td align="right">12.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">360</td>
<td align="right">10.9%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">280</td>
<td align="right">8.5%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">220</td>
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
<td align="left">RESUME_CHECK</td>
<td align="right">41,240</td>
<td align="right">29.7%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">33,240</td>
<td align="right">23.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">30,600</td>
<td align="right">22.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">14,480</td>
<td align="right">10.4%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">4,440</td>
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
<td align="left">LOAD_FAST</td>
<td align="right">96,480</td>
<td align="right">69.4%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">27,660</td>
<td align="right">19.9%</td>
</tr>
<tr>
<td align="left">CHECK_EXC_MATCH</td>
<td align="right">4,080</td>
<td align="right">2.9%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">2,960</td>
<td align="right">2.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">2,400</td>
<td align="right">1.7%</td>
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
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">155,388,080</td>
<td align="right">29.6%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">155,383,800</td>
<td align="right">29.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">77,731,529</td>
<td align="right">14.8%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">77,707,300</td>
<td align="right">14.8%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">38,854,599</td>
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
<td align="left">LOAD_FAST</td>
<td align="right">174,897,220</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">155,388,080</td>
<td align="right">29.6%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">77,691,820</td>
<td align="right">14.8%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">77,691,180</td>
<td align="right">14.8%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">38,845,900</td>
<td align="right">7.4%</td>
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
<td align="right">2,880</td>
<td align="right">97.3%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR</td>
<td align="right">80</td>
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
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">2,520</td>
<td align="right">85.1%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">220</td>
<td align="right">7.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">220</td>
<td align="right">7.4%</td>
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
<td align="left">COPY_FREE_VARS</td>
<td align="right">77,695,320</td>
<td align="right">99.8%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">87,629</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">CACHE</td>
<td align="right">37,260</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">13,180</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">10,580</td>
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
<td align="right">77,699,520</td>
<td align="right">99.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">52,260</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">41,240</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">32,420</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">28,960</td>
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
<td align="right">233,087,640</td>
<td align="right">66.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">116,540,900</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">4,360</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">880</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
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
<td align="right">310,771,580</td>
<td align="right">88.9%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">38,852,920</td>
<td align="right">11.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">2,240</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">2,100</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">1,340</td>
<td align="right">0.0%</td>
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
<td align="left">LOAD_FAST</td>
<td align="right">360</td>
<td align="right">69.2%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">120</td>
<td align="right">23.1%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">40</td>
<td align="right">7.7%</td>
</tr>
</tbody>
</table>

<table>
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
<td align="right">240</td>
<td align="right">46.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">200</td>
<td align="right">38.5%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">60</td>
<td align="right">11.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">20</td>
<td align="right">3.8%</td>
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
<td align="right">9,800</td>
<td align="right">53.0%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">3,860</td>
<td align="right">20.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">3,060</td>
<td align="right">16.6%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">1,040</td>
<td align="right">5.6%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">460</td>
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
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">8,560</td>
<td align="right">46.3%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">6,900</td>
<td align="right">37.3%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">1,760</td>
<td align="right">9.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">660</td>
<td align="right">3.6%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">300</td>
<td align="right">1.6%</td>
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
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">60</td>
<td align="right">75.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">20</td>
<td align="right">25.0%</td>
</tr>
</tbody>
</table>

<table>
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
<td align="right">40</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">40</td>
<td align="right">50.0%</td>
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
<td align="left">ENTER_EXECUTOR</td>
<td align="right">1,040</td>
<td align="right">74.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">120</td>
<td align="right">8.6%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">80</td>
<td align="right">5.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">60</td>
<td align="right">4.3%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">40</td>
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
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">1,220</td>
<td align="right">87.1%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">160</td>
<td align="right">11.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">20</td>
<td align="right">1.4%</td>
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
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">310,766,220</td>
<td align="right">80.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">77,693,360</td>
<td align="right">20.0%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">40,380</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">25,100</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">24,040</td>
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
<td align="right">349,705,580</td>
<td align="right">90.0%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">38,845,680</td>
<td align="right">10.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">36,335</td>
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
<td align="left">BINARY_OP</td>
<td align="right">380</td>
<td align="right">79.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">100</td>
<td align="right">20.8%</td>
</tr>
</tbody>
</table>

<table>
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
<td align="right">360</td>
<td align="right">75.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">80</td>
<td align="right">16.7%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">40</td>
<td align="right">8.3%</td>
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
<td align="right">7,740</td>
<td align="right">87.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">360</td>
<td align="right">4.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">280</td>
<td align="right">3.2%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">200</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">160</td>
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
<td align="left">EXTENDED_ARG</td>
<td align="right">5,680</td>
<td align="right">64.1%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">2,160</td>
<td align="right">24.4%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">1,000</td>
<td align="right">11.3%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">20</td>
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
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">38,847,160</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,100</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">940</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">480</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">COPY</td>
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
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">38,850,240</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">800</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">20</td>
<td align="right">0.0%</td>
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
<td align="left">COPY</td>
<td align="right">13,660</td>
<td align="right">49.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">8,560</td>
<td align="right">31.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">4,380</td>
<td align="right">15.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">440</td>
<td align="right">1.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">280</td>
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
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">14,420</td>
<td align="right">52.2%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">13,180</td>
<td align="right">47.8%</td>
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
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">38,845,680</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,180</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">280</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">80</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
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
<td align="right">38,845,720</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">1,520</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">20</td>
<td align="right">0.0%</td>
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
<td align="right">2,129</td>
<td align="right">42.2%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">1,740</td>
<td align="right">34.5%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">540</td>
<td align="right">10.7%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">420</td>
<td align="right">8.3%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">180</td>
<td align="right">3.6%</td>
</tr>
</tbody>
</table>

<table>
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
<td align="right">5,029</td>
<td align="right">99.6%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">20</td>
<td align="right">0.4%</td>
</tr>
</tbody>
</table>


</details>

### INSTRUMENTED_RESUME

<details>
<summary> Successors and predecessors for INSTRUMENTED_RESUME </summary>

<table>
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
<td align="right">38,845,840</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">360</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">140</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">60</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_RESUME</td>
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
<td align="right">38,846,000</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">320</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">80</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_RESUME</td>
<td align="right">60</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### INSTRUMENTED_RETURN_VALUE

<details>
<summary> Successors and predecessors for INSTRUMENTED_RETURN_VALUE </summary>

<table>
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
<td align="right">19,422,960</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">19,422,700</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">60</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">20</td>
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
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">19,422,680</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">19,422,680</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">240</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">80</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">40</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### INSTRUMENTED_RETURN_CONST

<details>
<summary> Successors and predecessors for INSTRUMENTED_RETURN_CONST </summary>

<table>
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
<td align="right">100</td>
<td align="right">41.7%</td>
</tr>
<tr>
<td align="left">STORE_GLOBAL</td>
<td align="right">80</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">60</td>
<td align="right">25.0%</td>
</tr>
</tbody>
</table>

<table>
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
<td align="right">240</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### INSTRUMENTED_JUMP_BACKWARD

<details>
<summary> Successors and predecessors for INSTRUMENTED_JUMP_BACKWARD </summary>

<table>
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
<td align="left">FOR_ITER</td>
<td align="right">80</td>
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
<td align="right">13,320</td>
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
<td align="right">97,144,160</td>
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
<td align="right">380</td>
<td align="right">32.2%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">800</td>
<td align="right">67.8%</td>
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
<td align="right">280</td>
<td align="right">35.0%</td>
</tr>
<tr>
<td align="left">floor divide</td>
<td align="right">200</td>
<td align="right">25.0%</td>
</tr>
<tr>
<td align="left">add different types</td>
<td align="right">100</td>
<td align="right">12.5%</td>
</tr>
<tr>
<td align="left">multiply different types</td>
<td align="right">80</td>
<td align="right">10.0%</td>
</tr>
<tr>
<td align="left">remainder</td>
<td align="right">60</td>
<td align="right">7.5%</td>
</tr>
<tr>
<td align="left">subtract other</td>
<td align="right">40</td>
<td align="right">5.0%</td>
</tr>
<tr>
<td align="left">and other</td>
<td align="right">20</td>
<td align="right">2.5%</td>
</tr>
<tr>
<td align="left">or</td>
<td align="right">20</td>
<td align="right">2.5%</td>
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
<td align="right">116,544,440</td>
<td align="right">60.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">77,704,140</td>
<td align="right">40.0%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">60</td>
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
<td align="right">260</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">29,300</td>
<td align="right">99.1%</td>
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
<td align="left">code complex parameters</td>
<td align="right">19,160</td>
<td align="right">65.4%</td>
</tr>
<tr>
<td align="left">buffer int</td>
<td align="right">9,860</td>
<td align="right">33.7%</td>
</tr>
<tr>
<td align="left">list slice</td>
<td align="right">180</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">100</td>
<td align="right">0.3%</td>
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
<td align="right">8,840</td>
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
<td align="right">272,270,535</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">300</td>
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
<td align="right">7,440</td>
<td align="right">98.7%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">100</td>
<td align="right">1.3%</td>
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
<td align="right">100</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">init not python</td>
<td align="right">40</td>
<td align="right">40.0%</td>
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
<td align="right">5,400</td>
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
<td align="right">427,344,111</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">300</td>
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
<td align="right">540</td>
<td align="right">65.9%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">280</td>
<td align="right">34.1%</td>
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
<td align="left">different types</td>
<td align="right">160</td>
<td align="right">57.1%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">60</td>
<td align="right">21.4%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">40</td>
<td align="right">14.3%</td>
</tr>
<tr>
<td align="left">big int</td>
<td align="right">20</td>
<td align="right">7.1%</td>
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
<td align="right">155,386,400</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">11,620</td>
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
<td align="right">240</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">38,500</td>
<td align="right">99.4%</td>
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
<td align="left">str</td>
<td align="right">38,140</td>
<td align="right">99.1%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">180</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">100</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">80</td>
<td align="right">0.2%</td>
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
<td align="right">5,420</td>
<td align="right">18.7%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">22,480</td>
<td align="right">77.6%</td>
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
<td align="right">480</td>
<td align="right">44.4%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">600</td>
<td align="right">55.6%</td>
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
<td align="right">320</td>
<td align="right">53.3%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">180</td>
<td align="right">30.0%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">80</td>
<td align="right">13.3%</td>
</tr>
<tr>
<td align="left">dict values</td>
<td align="right">20</td>
<td align="right">3.3%</td>
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
<td align="right">466,223,400</td>
<td align="right">26.7%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,282,191,644</td>
<td align="right">73.3%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">13,320</td>
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
<td align="right">9,580</td>
<td align="right">7.5%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">118,320</td>
<td align="right">92.5%</td>
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
<td align="right">106,720</td>
<td align="right">90.2%</td>
</tr>
<tr>
<td align="left">non object slot</td>
<td align="right">9,780</td>
<td align="right">8.3%</td>
</tr>
<tr>
<td align="left">module attr not found</td>
<td align="right">1,000</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">440</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">shadowed</td>
<td align="right">120</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">non string or split</td>
<td align="right">100</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">class method obj</td>
<td align="right">60</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">60</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">metaclass attribute</td>
<td align="right">40</td>
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
<td align="right">19,435,640</td>
<td align="right">3.6%</td>
</tr>
<tr>
<td align="left">
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">260</td>
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
<td align="right">524,824,369</td>
<td align="right">96.4%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">5,440</td>
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
<td align="right">6,460</td>
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
<td align="right">80</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">2,960</td>
<td align="right">94.9%</td>
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
<td align="right">80</td>
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
<td align="right">14,900</td>
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
<td align="right">349,634,400</td>
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
<td align="right">4,480</td>
<td align="right">67.5%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">2,160</td>
<td align="right">32.5%</td>
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
<td align="left">not in dict</td>
<td align="right">1,700</td>
<td align="right">78.7%</td>
</tr>
<tr>
<td align="left">no dict</td>
<td align="right">200</td>
<td align="right">9.3%</td>
</tr>
<tr>
<td align="left">not in keys</td>
<td align="right">100</td>
<td align="right">4.6%</td>
</tr>
<tr>
<td align="left">non object slot</td>
<td align="right">80</td>
<td align="right">3.7%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">40</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">40</td>
<td align="right">1.9%</td>
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
<td align="right">280</td>
<td align="right">1.5%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">18,560</td>
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
<td align="right">38,857,100</td>
<td align="right">8.3%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">427,473,755</td>
<td align="right">91.7%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">2,960</td>
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
<td align="right">3,460</td>
<td align="right">24.9%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">10,420</td>
<td align="right">75.1%</td>
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
<td align="right">9,740</td>
<td align="right">93.5%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">320</td>
<td align="right">3.1%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">220</td>
<td align="right">2.1%</td>
</tr>
<tr>
<td align="left">dict</td>
<td align="right">80</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">60</td>
<td align="right">0.6%</td>
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
<td align="right">260</td>
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
<td align="right">38,852,309</td>
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
<td align="right">5,148,975,561</td>
<td align="right">48.4%</td>
</tr>
<tr>
<td align="left">
Not specialized
<details>
<summary>ⓘ</summary>

Instructions that could be specialized but aren't, e.g. `LOAD_ATTR`, `BINARY_SLICE`.
</details>
</td>
<td align="right">1,923,520,626</td>
<td align="right">18.1%</td>
</tr>
<tr>
<td align="left">
Specialized hits
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that complete.
</details>
</td>
<td align="right">3,497,677,303</td>
<td align="right">32.8%</td>
</tr>
<tr>
<td align="left">
Specialized misses
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that deopt.
</details>
</td>
<td align="right">77,726,500</td>
<td align="right">0.7%</td>
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
<td align="right">466,223,400</td>
<td align="right">58.5%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">155,386,400</td>
<td align="right">19.5%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">116,544,440</td>
<td align="right">14.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">38,857,100</td>
<td align="right">4.9%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">19,435,640</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">14,900</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">13,320</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">8,840</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">5,420</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">5,400</td>
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
<td align="left">RESUME</td>
<td align="right">77,704,120</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">77,704,120</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">12,720</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">5,220</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">1,280</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">1,120</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">600</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">520</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">300</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">220</td>
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
<td align="right">233,128,220</td>
<td align="right">66.6%</td>
</tr>
<tr>
<td align="left">Calls to Python functions inlined</td>
<td align="right">116,681,260</td>
<td align="right">33.4%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">233,128,220</td>
<td align="right">66.6%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (vector)</td>
<td align="right">233,082,360</td>
<td align="right">66.6%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (generator)</td>
<td align="right">45,860</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (legacy)</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function vectorcall)</td>
<td align="right">233,082,360</td>
<td align="right">66.6%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (build class)</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (slot)</td>
<td align="right">77,691,460</td>
<td align="right">22.2%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function ex)</td>
<td align="right">480</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (api)</td>
<td align="right">1,880</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (method)</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Frame objects created</td>
<td align="right">38,851,320</td>
<td align="right">11.1%</td>
</tr>
<tr>
<td align="left">Frames pushed</td>
<td align="right">349,764,280</td>
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
<td align="right">272,351,220</td>
<td align="right">77.4%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">272,352,340</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">79,610,160</td>
<td align="right">22.6%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">79,598,960</td>
<td align="right">22.6%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">6,360</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Allocations over 4 kbytes</td>
<td align="right">4,840</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">79,623,798</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Inline values</td>
<td align="right">3,040</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Interpreter increfs</td>
<td align="right">4,101,750,215</td>
<td align="right">75.3%</td>
</tr>
<tr>
<td align="left">Interpreter decrefs</td>
<td align="right">4,665,792,120</td>
<td align="right">80.5%</td>
</tr>
<tr>
<td align="left">Increfs</td>
<td align="right">1,342,387,025</td>
<td align="right">24.7%</td>
</tr>
<tr>
<td align="left">Decrefs</td>
<td align="right">1,130,156,035</td>
<td align="right">19.5%</td>
</tr>
<tr>
<td align="left">Materialize dict (on request)</td>
<td align="right">240</td>
<td align="right">7.9%</td>
</tr>
<tr>
<td align="left">Materialize dict (new key)</td>
<td align="right">400</td>
<td align="right">13.2%</td>
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
<td align="right">466,374,783</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Method cache misses</td>
<td align="right">10,337</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">9,684</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">77,820,476</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Method cache dunder misses</td>
<td align="right">1,744</td>
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
<td align="right">8,320</td>
<td align="right">575,800</td>
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
<td align="right">1,820</td>
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
<td align="right">1,600</td>
<td align="right">87.9%</td>
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
<td align="right">480</td>
<td align="right">26.4%</td>
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
<td align="right">220</td>
<td align="right">12.1%</td>
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
<td align="right">3.3%</td>
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
<td align="right">40</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">
Executors invalidated
<details>
<summary>ⓘ</summary>

The number of executors that were invalidated due to watched dictionary changes.
</details>
</td>
<td align="right">2,960</td>
<td align="right">185.0%</td>
</tr>
<tr>
<td align="left">
Traces executed
<details>
<summary>ⓘ</summary>

The number of traces that were executed
</details>
</td>
<td align="right">161,063</td>
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
<td align="right">10,821,770</td>
<td align="right">6,719.0%</td>
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
<td align="right">1,600</td>
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
<td align="right">1,600</td>
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
<td align="right">20</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">60</td>
<td align="right">3.8%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">900</td>
<td align="right">56.2%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">500</td>
<td align="right">31.2%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">120</td>
<td align="right">7.5%</td>
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
<td align="right">20</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">180</td>
<td align="right">11.2%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">1,300</td>
<td align="right">81.2%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">100</td>
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
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left"><= 4</td>
<td align="right">880</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left"><= 8</td>
<td align="right">20,527</td>
<td align="right">12.7%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">6,680</td>
<td align="right">4.1%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">50,167</td>
<td align="right">31.1%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">5,151</td>
<td align="right">3.2%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">581</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">40</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">1,640</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left"><= 1,024</td>
<td align="right">2,520</td>
<td align="right">1.6%</td>
</tr>
<tr>
<td align="left"><= 2,048</td>
<td align="right">60</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left"><= 4,096</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left"><= 8,192</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left"><= 16,384</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left"><= 32,768</td>
<td align="right">320</td>
<td align="right">0.2%</td>
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
<td align="right">1,225,296</td>
<td align="right">11.3%</td>
<td align="right">11.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY</td>
<td align="right">1,210,305</td>
<td align="right">11.2%</td>
<td align="right">22.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_3</td>
<td align="right">725,929</td>
<td align="right">6.7%</td>
<td align="right">29.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_IS_FALSE_POP</td>
<td align="right">508,703</td>
<td align="right">4.7%</td>
<td align="right">33.9%</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">_TIER2_RESUME_CHECK</td>
<td align="right">463,500</td>
<td align="right">4.3%</td>
<td align="right">38.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_2</td>
<td align="right">437,963</td>
<td align="right">4.0%</td>
<td align="right">42.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_4</td>
<td align="right">379,231</td>
<td align="right">3.5%</td>
<td align="right">45.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_JUMP_TO_TOP</td>
<td align="right">376,423</td>
<td align="right">3.5%</td>
<td align="right">49.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_0</td>
<td align="right">365,820</td>
<td align="right">3.4%</td>
<td align="right">52.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_3</td>
<td align="right">359,340</td>
<td align="right">3.3%</td>
<td align="right">55.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST</td>
<td align="right">357,300</td>
<td align="right">3.3%</td>
<td align="right">59.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_FOR_ITER_TIER_TWO</td>
<td align="right">337,620</td>
<td align="right">3.1%</td>
<td align="right">62.4%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_4</td>
<td align="right">335,411</td>
<td align="right">3.1%</td>
<td align="right">65.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">335,311</td>
<td align="right">3.1%</td>
<td align="right">68.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CONTAINS_OP</td>
<td align="right">330,840</td>
<td align="right">3.1%</td>
<td align="right">71.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_DICT</td>
<td align="right">329,000</td>
<td align="right">3.0%</td>
<td align="right">74.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_PERIODIC</td>
<td align="right">181,574</td>
<td align="right">1.7%</td>
<td align="right">76.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_UNICODE</td>
<td align="right">171,329</td>
<td align="right">1.6%</td>
<td align="right">77.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION</td>
<td align="right">165,954</td>
<td align="right">1.5%</td>
<td align="right">79.4%</td>
<td align="right">3.3%</td>
</tr>
<tr>
<td align="left">_STORE_FAST</td>
<td align="right">135,720</td>
<td align="right">1.3%</td>
<td align="right">80.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COMPARE_OP_STR</td>
<td align="right">128,949</td>
<td align="right">1.2%</td>
<td align="right">81.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_6</td>
<td align="right">109,020</td>
<td align="right">1.0%</td>
<td align="right">82.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_IS_TRUE_POP</td>
<td align="right">106,151</td>
<td align="right">1.0%</td>
<td align="right">83.9%</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">_START_EXECUTOR</td>
<td align="right">95,577</td>
<td align="right">0.9%</td>
<td align="right">84.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">94,514</td>
<td align="right">0.9%</td>
<td align="right">85.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE</td>
<td align="right">94,471</td>
<td align="right">0.9%</td>
<td align="right">86.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_PUSH_NULL</td>
<td align="right">88,480</td>
<td align="right">0.8%</td>
<td align="right">87.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_EXIT_TRACE</td>
<td align="right">85,186</td>
<td align="right">0.8%</td>
<td align="right">88.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_7</td>
<td align="right">83,400</td>
<td align="right">0.8%</td>
<td align="right">88.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_UNICODE</td>
<td align="right">81,340</td>
<td align="right">0.8%</td>
<td align="right">89.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">70,685</td>
<td align="right">0.7%</td>
<td align="right">90.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COLD_EXIT</td>
<td align="right">65,486</td>
<td align="right">0.6%</td>
<td align="right">90.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_ITER_CHECK_LIST</td>
<td align="right">61,220</td>
<td align="right">0.6%</td>
<td align="right">91.5%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_LIST</td>
<td align="right">61,180</td>
<td align="right">0.6%</td>
<td align="right">92.0%</td>
<td align="right">23.4%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_LIST</td>
<td align="right">56,660</td>
<td align="right">0.5%</td>
<td align="right">92.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION</td>
<td align="right">56,620</td>
<td align="right">0.5%</td>
<td align="right">93.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_IS_NOT_NONE_POP</td>
<td align="right">52,400</td>
<td align="right">0.5%</td>
<td align="right">93.6%</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_STR</td>
<td align="right">51,900</td>
<td align="right">0.5%</td>
<td align="right">94.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_ITER_NEXT_LIST</td>
<td align="right">46,845</td>
<td align="right">0.4%</td>
<td align="right">94.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL_BOOL</td>
<td align="right">42,345</td>
<td align="right">0.4%</td>
<td align="right">94.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_O</td>
<td align="right">41,860</td>
<td align="right">0.4%</td>
<td align="right">95.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">41,620</td>
<td align="right">0.4%</td>
<td align="right">95.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_SLOT_0</td>
<td align="right">41,500</td>
<td align="right">0.4%</td>
<td align="right">96.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_7</td>
<td align="right">41,020</td>
<td align="right">0.4%</td>
<td align="right">96.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_2</td>
<td align="right">28,674</td>
<td align="right">0.3%</td>
<td align="right">96.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_1</td>
<td align="right">27,585</td>
<td align="right">0.3%</td>
<td align="right">96.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_NON_PY_GENERAL</td>
<td align="right">23,240</td>
<td align="right">0.2%</td>
<td align="right">97.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_IS_NOT_PY_CALLABLE</td>
<td align="right">23,240</td>
<td align="right">0.2%</td>
<td align="right">97.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_DORV_VALUES_INST_ATTR_FROM_DICT</td>
<td align="right">22,900</td>
<td align="right">0.2%</td>
<td align="right">97.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_KEYS_VERSION</td>
<td align="right">22,900</td>
<td align="right">0.2%</td>
<td align="right">97.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">22,880</td>
<td align="right">0.2%</td>
<td align="right">98.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_1</td>
<td align="right">19,040</td>
<td align="right">0.2%</td>
<td align="right">98.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_DEREF</td>
<td align="right">18,000</td>
<td align="right">0.2%</td>
<td align="right">98.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL_NONE</td>
<td align="right">17,000</td>
<td align="right">0.2%</td>
<td align="right">98.5%</td>
<td align="right">4.7%</td>
</tr>
<tr>
<td align="left">_POP_TOP</td>
<td align="right">16,780</td>
<td align="right">0.2%</td>
<td align="right">98.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_WITH_NULL</td>
<td align="right">15,391</td>
<td align="right">0.1%</td>
<td align="right">98.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_EXACT_ARGS</td>
<td align="right">11,611</td>
<td align="right">0.1%</td>
<td align="right">98.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_PUSH_FRAME</td>
<td align="right">11,611</td>
<td align="right">0.1%</td>
<td align="right">99.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_SAVE_RETURN_OFFSET</td>
<td align="right">11,611</td>
<td align="right">0.1%</td>
<td align="right">99.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_1</td>
<td align="right">10,651</td>
<td align="right">0.1%</td>
<td align="right">99.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY_AND_SET_IP</td>
<td align="right">7,549</td>
<td align="right">0.1%</td>
<td align="right">99.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR</td>
<td align="right">7,160</td>
<td align="right">0.1%</td>
<td align="right">99.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE</td>
<td align="right">7,011</td>
<td align="right">0.1%</td>
<td align="right">99.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_DYNAMIC_EXIT</td>
<td align="right">7,011</td>
<td align="right">0.1%</td>
<td align="right">99.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW</td>
<td align="right">6,978</td>
<td align="right">0.1%</td>
<td align="right">99.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_ISINSTANCE</td>
<td align="right">6,240</td>
<td align="right">0.1%</td>
<td align="right">99.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_RESUME_CHECK</td>
<td align="right">4,600</td>
<td align="right">0.0%</td>
<td align="right">99.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE_OPERAND</td>
<td align="right">4,580</td>
<td align="right">0.0%</td>
<td align="right">99.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW_WITH_NULL</td>
<td align="right">4,580</td>
<td align="right">0.0%</td>
<td align="right">99.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_CLASS</td>
<td align="right">4,560</td>
<td align="right">0.0%</td>
<td align="right">99.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL</td>
<td align="right">4,320</td>
<td align="right">0.0%</td>
<td align="right">99.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR</td>
<td align="right">2,520</td>
<td align="right">0.0%</td>
<td align="right">99.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LIST_APPEND</td>
<td align="right">2,320</td>
<td align="right">0.0%</td>
<td align="right">99.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_POP_FRAME</td>
<td align="right">2,300</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_ERROR_POP_N</td>
<td align="right">2,280</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST</td>
<td align="right">1,400</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_DEOPT</td>
<td align="right">1,100</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_MANAGED_OBJECT_HAS_VALUES</td>
<td align="right">1,060</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE_0</td>
<td align="right">1,060</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BUILD_TUPLE</td>
<td align="right">940</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_2</td>
<td align="right">880</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP</td>
<td align="right">820</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_IS_NONE_POP</td>
<td align="right">740</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_TUPLE</td>
<td align="right">640</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right">34.4%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_TUPLE</td>
<td align="right">640</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_5</td>
<td align="right">560</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_5</td>
<td align="right">440</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_DICT</td>
<td align="right">420</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">420</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_ITER_NEXT_TUPLE</td>
<td align="right">420</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_REPLACE_WITH_TRUE</td>
<td align="right">360</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_IS_OP</td>
<td align="right">160</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_LEN</td>
<td align="right">160</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_DORV_NO_DICT</td>
<td align="right">100</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">100</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COPY</td>
<td align="right">80</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_STR_INT</td>
<td align="right">80</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBTRACT_INT</td>
<td align="right">80</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_INT</td>
<td align="right">80</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">69</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_RANGE</td>
<td align="right">60</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right">66.7%</td>
</tr>
<tr>
<td align="left">_FORMAT_SIMPLE</td>
<td align="right">60</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNARY_NEGATIVE</td>
<td align="right">60</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BUILD_LIST</td>
<td align="right">60</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BUILD_STRING</td>
<td align="right">60</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_SET</td>
<td align="right">60</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_ITER_CHECK_RANGE</td>
<td align="right">60</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GET_ITER</td>
<td align="right">40</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_DICT</td>
<td align="right">40</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_NOS_INT</td>
<td align="right">40</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_0</td>
<td align="right">40</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BUILD_SLICE</td>
<td align="right">20</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_TUPLE_INT</td>
<td align="right">20</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL_INT</td>
<td align="right">20</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TUPLE</td>
<td align="right">20</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_INT</td>
<td align="right">20</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">20</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COMPARE_OP_INT</td>
<td align="right">20</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">20</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_3</td>
<td align="right">20</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_4</td>
<td align="right">20</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_ITER_NEXT_RANGE</td>
<td align="right">20</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">20</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL</td>
<td align="right">20</td>
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
<td align="left">_JUMP_TO_TOP _TIER2_RESUME_CHECK</td>
<td align="right">376,423</td>
<td align="right">3.5%</td>
<td align="right">3.5%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_2 _SET_IP</td>
<td align="right">356,845</td>
<td align="right">3.3%</td>
<td align="right">6.8%</td>
</tr>
<tr>
<td align="left">_SET_IP _FOR_ITER_TIER_TWO</td>
<td align="right">337,620</td>
<td align="right">3.1%</td>
<td align="right">9.9%</td>
</tr>
<tr>
<td align="left">_TIER2_RESUME_CHECK _SET_IP</td>
<td align="right">337,520</td>
<td align="right">3.1%</td>
<td align="right">13.0%</td>
</tr>
<tr>
<td align="left">_FOR_ITER_TIER_TWO _CHECK_VALIDITY</td>
<td align="right">336,520</td>
<td align="right">3.1%</td>
<td align="right">16.1%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY _UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">335,311</td>
<td align="right">3.1%</td>
<td align="right">19.2%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TWO_TUPLE _STORE_FAST_3</td>
<td align="right">334,471</td>
<td align="right">3.1%</td>
<td align="right">22.3%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_3 _STORE_FAST_4</td>
<td align="right">334,471</td>
<td align="right">3.1%</td>
<td align="right">25.4%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY _GUARD_IS_FALSE_POP</td>
<td align="right">333,169</td>
<td align="right">3.1%</td>
<td align="right">28.5%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP _CHECK_VALIDITY</td>
<td align="right">330,840</td>
<td align="right">3.1%</td>
<td align="right">31.5%</td>
</tr>
<tr>
<td align="left">_SET_IP _CONTAINS_OP</td>
<td align="right">330,771</td>
<td align="right">3.1%</td>
<td align="right">34.6%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_DICT _CHECK_VALIDITY</td>
<td align="right">329,000</td>
<td align="right">3.0%</td>
<td align="right">37.6%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY _JUMP_TO_TOP</td>
<td align="right">329,000</td>
<td align="right">3.0%</td>
<td align="right">40.7%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_3 _SET_IP</td>
<td align="right">328,900</td>
<td align="right">3.0%</td>
<td align="right">43.7%</td>
</tr>
<tr>
<td align="left">_SET_IP _STORE_SUBSCR_DICT</td>
<td align="right">328,640</td>
<td align="right">3.0%</td>
<td align="right">46.8%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_FALSE_POP _LOAD_FAST_4</td>
<td align="right">328,640</td>
<td align="right">3.0%</td>
<td align="right">49.8%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_0 _LOAD_FAST_3</td>
<td align="right">328,640</td>
<td align="right">3.0%</td>
<td align="right">52.8%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_3 _LOAD_FAST_2</td>
<td align="right">328,640</td>
<td align="right">3.0%</td>
<td align="right">55.9%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_4 _LOAD_FAST_0</td>
<td align="right">328,640</td>
<td align="right">3.0%</td>
<td align="right">58.9%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_4 _LOAD_FAST_3</td>
<td align="right">328,640</td>
<td align="right">3.0%</td>
<td align="right">61.9%</td>
</tr>
<tr>
<td align="left">_CHECK_PERIODIC _CHECK_VALIDITY</td>
<td align="right">180,785</td>
<td align="right">1.7%</td>
<td align="right">63.6%</td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_UNICODE _COMPARE_OP_STR</td>
<td align="right">128,909</td>
<td align="right">1.2%</td>
<td align="right">64.8%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_STR _GUARD_IS_FALSE_POP</td>
<td align="right">121,429</td>
<td align="right">1.1%</td>
<td align="right">65.9%</td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION _LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">94,514</td>
<td align="right">0.9%</td>
<td align="right">66.8%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY _STORE_FAST</td>
<td align="right">93,820</td>
<td align="right">0.9%</td>
<td align="right">67.7%</td>
</tr>
<tr>
<td align="left">_START_EXECUTOR _TIER2_RESUME_CHECK</td>
<td align="right">87,077</td>
<td align="right">0.8%</td>
<td align="right">68.5%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_FALSE_POP _LOAD_FAST</td>
<td align="right">84,680</td>
<td align="right">0.8%</td>
<td align="right">69.2%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE _PUSH_NULL</td>
<td align="right">83,920</td>
<td align="right">0.8%</td>
<td align="right">70.0%</td>
</tr>
<tr>
<td align="left">_PUSH_NULL _LOAD_FAST</td>
<td align="right">83,000</td>
<td align="right">0.8%</td>
<td align="right">70.8%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_FALSE_POP _LOAD_FAST_7</td>
<td align="right">80,820</td>
<td align="right">0.7%</td>
<td align="right">71.5%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_2 _GUARD_BOTH_UNICODE</td>
<td align="right">80,800</td>
<td align="right">0.7%</td>
<td align="right">72.3%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_7 _LOAD_FAST_2</td>
<td align="right">80,800</td>
<td align="right">0.7%</td>
<td align="right">73.0%</td>
</tr>
<tr>
<td align="left">_SET_IP _CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">70,685</td>
<td align="right">0.7%</td>
<td align="right">73.7%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST _CHECK_PERIODIC</td>
<td align="right">70,685</td>
<td align="right">0.7%</td>
<td align="right">74.3%</td>
</tr>
<tr>
<td align="left">_TIER2_RESUME_CHECK _ITER_CHECK_LIST</td>
<td align="right">61,200</td>
<td align="right">0.6%</td>
<td align="right">74.9%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_LIST _GUARD_NOT_EXHAUSTED_LIST</td>
<td align="right">61,180</td>
<td align="right">0.6%</td>
<td align="right">75.5%</td>
</tr>
<tr>
<td align="left">_TIER2_RESUME_CHECK _LOAD_FAST_6</td>
<td align="right">56,840</td>
<td align="right">0.5%</td>
<td align="right">76.0%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_LIST _GUARD_IS_TRUE_POP</td>
<td align="right">56,660</td>
<td align="right">0.5%</td>
<td align="right">76.5%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_6 _TO_BOOL_LIST</td>
<td align="right">56,660</td>
<td align="right">0.5%</td>
<td align="right">77.0%</td>
</tr>
<tr>
<td align="left">_STORE_FAST _LOAD_FAST</td>
<td align="right">52,500</td>
<td align="right">0.5%</td>
<td align="right">77.5%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST _GUARD_IS_NOT_NONE_POP</td>
<td align="right">52,400</td>
<td align="right">0.5%</td>
<td align="right">78.0%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_6 _GUARD_TYPE_VERSION</td>
<td align="right">52,320</td>
<td align="right">0.5%</td>
<td align="right">78.5%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_NO_DICT _SET_IP</td>
<td align="right">52,300</td>
<td align="right">0.5%</td>
<td align="right">79.0%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_TRUE_POP _LOAD_FAST_6</td>
<td align="right">52,120</td>
<td align="right">0.5%</td>
<td align="right">79.5%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NOT_NONE_POP _LOAD_FAST</td>
<td align="right">51,880</td>
<td align="right">0.5%</td>
<td align="right">79.9%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST _TO_BOOL_STR</td>
<td align="right">51,820</td>
<td align="right">0.5%</td>
<td align="right">80.4%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_LIST _ITER_NEXT_LIST</td>
<td align="right">46,845</td>
<td align="right">0.4%</td>
<td align="right">80.8%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_3 _GUARD_BOTH_UNICODE</td>
<td align="right">44,340</td>
<td align="right">0.4%</td>
<td align="right">81.3%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_STR _GUARD_IS_TRUE_POP</td>
<td align="right">43,500</td>
<td align="right">0.4%</td>
<td align="right">81.7%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_TRUE_POP _LOAD_FAST</td>
<td align="right">43,420</td>
<td align="right">0.4%</td>
<td align="right">82.1%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST _LOAD_FAST_3</td>
<td align="right">43,420</td>
<td align="right">0.4%</td>
<td align="right">82.5%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST _LOAD_FAST_4</td>
<td align="right">43,420</td>
<td align="right">0.4%</td>
<td align="right">82.9%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_4 _GUARD_BOTH_UNICODE</td>
<td align="right">43,420</td>
<td align="right">0.4%</td>
<td align="right">83.3%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION _LOAD_CONST_INLINE</td>
<td align="right">42,620</td>
<td align="right">0.4%</td>
<td align="right">83.7%</td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_UNICODE _BINARY_OP_ADD_UNICODE</td>
<td align="right">42,420</td>
<td align="right">0.4%</td>
<td align="right">84.1%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY _TO_BOOL_BOOL</td>
<td align="right">42,345</td>
<td align="right">0.4%</td>
<td align="right">84.4%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_BOOL _GUARD_IS_FALSE_POP</td>
<td align="right">41,865</td>
<td align="right">0.4%</td>
<td align="right">84.8%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_O _CHECK_PERIODIC</td>
<td align="right">41,860</td>
<td align="right">0.4%</td>
<td align="right">85.2%</td>
</tr>
<tr>
<td align="left">_SET_IP _CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">41,620</td>
<td align="right">0.4%</td>
<td align="right">85.6%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST_WITH_KEYWORDS _CHECK_PERIODIC</td>
<td align="right">41,620</td>
<td align="right">0.4%</td>
<td align="right">86.0%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST _SET_IP</td>
<td align="right">41,560</td>
<td align="right">0.4%</td>
<td align="right">86.4%</td>
</tr>
<tr>
<td align="left">_SET_IP _CALL_BUILTIN_O</td>
<td align="right">41,500</td>
<td align="right">0.4%</td>
<td align="right">86.8%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_UNICODE _STORE_FAST</td>
<td align="right">41,500</td>
<td align="right">0.4%</td>
<td align="right">87.1%</td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION _LOAD_ATTR_SLOT_0</td>
<td align="right">41,500</td>
<td align="right">0.4%</td>
<td align="right">87.5%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_SLOT_0 _SET_IP</td>
<td align="right">41,500</td>
<td align="right">0.4%</td>
<td align="right">87.9%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST _GUARD_TYPE_VERSION</td>
<td align="right">41,500</td>
<td align="right">0.4%</td>
<td align="right">88.3%</td>
</tr>
<tr>
<td align="left">_STORE_FAST _CHECK_FUNCTION</td>
<td align="right">41,500</td>
<td align="right">0.4%</td>
<td align="right">88.7%</td>
</tr>
<tr>
<td align="left">_STORE_FAST _LOAD_CONST_INLINE</td>
<td align="right">41,500</td>
<td align="right">0.4%</td>
<td align="right">89.1%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST _STORE_FAST_7</td>
<td align="right">41,020</td>
<td align="right">0.4%</td>
<td align="right">89.4%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_UNICODE _LOAD_FAST</td>
<td align="right">38,920</td>
<td align="right">0.4%</td>
<td align="right">89.8%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST _BINARY_OP_ADD_UNICODE</td>
<td align="right">38,920</td>
<td align="right">0.4%</td>
<td align="right">90.2%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_7 _JUMP_TO_TOP</td>
<td align="right">38,440</td>
<td align="right">0.4%</td>
<td align="right">90.5%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_LIST _STORE_FAST_2</td>
<td align="right">27,845</td>
<td align="right">0.3%</td>
<td align="right">90.8%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY _EXIT_TRACE</td>
<td align="right">25,060</td>
<td align="right">0.2%</td>
<td align="right">91.0%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_0 _GUARD_TYPE_VERSION</td>
<td align="right">24,580</td>
<td align="right">0.2%</td>
<td align="right">91.2%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY _STORE_FAST_3</td>
<td align="right">24,060</td>
<td align="right">0.2%</td>
<td align="right">91.4%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_3 _LOAD_FAST_3</td>
<td align="right">23,620</td>
<td align="right">0.2%</td>
<td align="right">91.7%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_NO_DICT _LOAD_FAST_2</td>
<td align="right">23,245</td>
<td align="right">0.2%</td>
<td align="right">91.9%</td>
</tr>
<tr>
<td align="left">_SET_IP _CHECK_IS_NOT_PY_CALLABLE</td>
<td align="right">23,240</td>
<td align="right">0.2%</td>
<td align="right">92.1%</td>
</tr>
<tr>
<td align="left">_CALL_NON_PY_GENERAL _CHECK_PERIODIC</td>
<td align="right">23,240</td>
<td align="right">0.2%</td>
<td align="right">92.3%</td>
</tr>
<tr>
<td align="left">_CHECK_IS_NOT_PY_CALLABLE _CALL_NON_PY_GENERAL</td>
<td align="right">23,240</td>
<td align="right">0.2%</td>
<td align="right">92.5%</td>
</tr>
<tr>
<td align="left">_GUARD_DORV_VALUES_INST_ATTR_FROM_DICT _GUARD_KEYS_VERSION</td>
<td align="right">22,900</td>
<td align="right">0.2%</td>
<td align="right">92.7%</td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION _GUARD_DORV_VALUES_INST_ATTR_FROM_DICT</td>
<td align="right">22,900</td>
<td align="right">0.2%</td>
<td align="right">92.9%</td>
</tr>
<tr>
<td align="left">_GUARD_KEYS_VERSION _LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">22,880</td>
<td align="right">0.2%</td>
<td align="right">93.2%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES _GUARD_TYPE_VERSION</td>
<td align="right">22,880</td>
<td align="right">0.2%</td>
<td align="right">93.4%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_2 _LOAD_FAST_0</td>
<td align="right">22,880</td>
<td align="right">0.2%</td>
<td align="right">93.6%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_LIST _STORE_FAST_1</td>
<td align="right">19,000</td>
<td align="right">0.2%</td>
<td align="right">93.8%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_1 _SET_IP</td>
<td align="right">18,960</td>
<td align="right">0.2%</td>
<td align="right">93.9%</td>
</tr>
<tr>
<td align="left">_LOAD_DEREF _CHECK_VALIDITY</td>
<td align="right">18,000</td>
<td align="right">0.2%</td>
<td align="right">94.1%</td>
</tr>
<tr>
<td align="left">_SET_IP _LOAD_DEREF</td>
<td align="right">18,000</td>
<td align="right">0.2%</td>
<td align="right">94.3%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY _GUARD_TYPE_VERSION</td>
<td align="right">18,000</td>
<td align="right">0.2%</td>
<td align="right">94.4%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_NO_DICT _LOAD_FAST_1</td>
<td align="right">18,000</td>
<td align="right">0.2%</td>
<td align="right">94.6%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_1 _SET_IP</td>
<td align="right">18,000</td>
<td align="right">0.2%</td>
<td align="right">94.8%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_3 _TO_BOOL_NONE</td>
<td align="right">17,000</td>
<td align="right">0.2%</td>
<td align="right">94.9%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_NONE _POP_TOP</td>
<td align="right">16,200</td>
<td align="right">0.1%</td>
<td align="right">95.1%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_LIST _EXIT_TRACE</td>
<td align="right">14,335</td>
<td align="right">0.1%</td>
<td align="right">95.2%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_FALSE_POP _EXIT_TRACE</td>
<td align="right">14,111</td>
<td align="right">0.1%</td>
<td align="right">95.3%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION _LOAD_CONST_INLINE_WITH_NULL</td>
<td align="right">11,880</td>
<td align="right">0.1%</td>
<td align="right">95.4%</td>
</tr>
<tr>
<td align="left">_SAVE_RETURN_OFFSET _PUSH_FRAME</td>
<td align="right">11,611</td>
<td align="right">0.1%</td>
<td align="right">95.6%</td>
</tr>
<tr>
<td align="left">_SET_IP _CHECK_FUNCTION_EXACT_ARGS</td>
<td align="right">11,591</td>
<td align="right">0.1%</td>
<td align="right">95.7%</td>
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
<td align="left">CALL_KW</td>
<td align="right">120</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">60</td>
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
<td align="right">40</td>
</tr>
<tr>
<td align="left">
watched globals modification
<details>
<summary>ⓘ</summary>

A watched `globals()` dict has been modified
</details>
</td>
<td align="right">40</td>
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
Stats gathered on: 2024-05-19