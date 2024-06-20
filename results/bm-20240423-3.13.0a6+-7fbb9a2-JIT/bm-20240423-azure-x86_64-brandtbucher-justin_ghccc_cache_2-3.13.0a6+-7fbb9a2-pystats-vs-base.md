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
<th align="right">Base Count</th>
<th align="right">Head Count</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">550,433,039</td>
<td align="right">321,138,078</td>
<td align="right">-41.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">5,186,295</td>
<td align="right">3,080,595</td>
<td align="right">-40.6%</td>
</tr>
<tr>
<td align="left">BUILD_CONST_KEY_MAP</td>
<td align="right">13,469,287</td>
<td align="right">8,687,678</td>
<td align="right">-35.5%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">1,166,258,044</td>
<td align="right">1,509,145,876</td>
<td align="right">29.4%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_SET</td>
<td align="right">466,184,322</td>
<td align="right">381,556,771</td>
<td align="right">-18.2%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_STR_INT</td>
<td align="right">459,903,418</td>
<td align="right">377,709,751</td>
<td align="right">-17.9%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">123,502,789</td>
<td align="right">105,258,006</td>
<td align="right">-14.8%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">678,537,150</td>
<td align="right">590,916,342</td>
<td align="right">-12.9%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">3,040,657,234</td>
<td align="right">2,664,878,582</td>
<td align="right">-12.4%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">501,289,083</td>
<td align="right">446,604,341</td>
<td align="right">-10.9%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">5,645,421,936</td>
<td align="right">5,206,816,250</td>
<td align="right">-7.8%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">236,409,545</td>
<td align="right">219,823,651</td>
<td align="right">-7.0%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">641,974,206</td>
<td align="right">603,236,723</td>
<td align="right">-6.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">6,316,142,356</td>
<td align="right">5,941,490,002</td>
<td align="right">-5.9%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">316,226,133</td>
<td align="right">300,100,614</td>
<td align="right">-5.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">254,856,360</td>
<td align="right">243,310,330</td>
<td align="right">-4.5%</td>
</tr>
<tr>
<td align="left">UNARY_INVERT</td>
<td align="right">2,613,152</td>
<td align="right">2,495,517</td>
<td align="right">-4.5%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">133,471,642</td>
<td align="right">128,182,305</td>
<td align="right">-4.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">656,854,054</td>
<td align="right">632,391,911</td>
<td align="right">-3.7%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">452,735,866</td>
<td align="right">436,758,106</td>
<td align="right">-3.5%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">6,759,090,080</td>
<td align="right">6,521,475,090</td>
<td align="right">-3.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">376,021,308</td>
<td align="right">388,510,530</td>
<td align="right">3.3%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">197,705,986</td>
<td align="right">192,258,151</td>
<td align="right">-2.8%</td>
</tr>
<tr>
<td align="left">CALL_STR_1</td>
<td align="right">46,760,267</td>
<td align="right">45,676,919</td>
<td align="right">-2.3%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">3,597,582,804</td>
<td align="right">3,514,376,619</td>
<td align="right">-2.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">1,739,099,977</td>
<td align="right">1,772,260,248</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">5,426,305,441</td>
<td align="right">5,323,562,913</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">24,669,720,720</td>
<td align="right">24,235,959,231</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">865,637,459</td>
<td align="right">850,702,734</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_TUPLE_INT</td>
<td align="right">220,935,120</td>
<td align="right">217,635,685</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">2,961,240,750</td>
<td align="right">2,998,952,056</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">403,339,277</td>
<td align="right">398,492,320</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">851,844,308</td>
<td align="right">841,682,871</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">80,654,726</td>
<td align="right">79,778,993</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">DICT_MERGE</td>
<td align="right">47,579,549</td>
<td align="right">47,107,780</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">398,213,035</td>
<td align="right">402,023,564</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">183,461,727</td>
<td align="right">181,798,471</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_FOR_ITER</td>
<td align="right">3,220</td>
<td align="right">3,192</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_GETITEM</td>
<td align="right">65,678,574</td>
<td align="right">65,165,344</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">330,567,077</td>
<td align="right">327,985,974</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">2,310,263,593</td>
<td align="right">2,327,273,519</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">612,171,546</td>
<td align="right">607,704,760</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">542,136,494</td>
<td align="right">538,301,450</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">161,216,761</td>
<td align="right">160,236,445</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">1,228,692,458</td>
<td align="right">1,221,304,817</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">END_FOR</td>
<td align="right">82,846,819</td>
<td align="right">82,367,970</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">116,616,046</td>
<td align="right">115,982,652</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">2,886,121,431</td>
<td align="right">2,901,764,150</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">1,731,158,404</td>
<td align="right">1,721,822,603</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_JUMP_BACKWARD</td>
<td align="right">6,260</td>
<td align="right">6,232</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">122,060,716</td>
<td align="right">121,555,172</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">129,024,989</td>
<td align="right">129,519,332</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">4,304,133,397</td>
<td align="right">4,288,309,863</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">146,565,896</td>
<td align="right">146,047,280</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">BEFORE_WITH</td>
<td align="right">10,119,413</td>
<td align="right">10,086,181</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_POP_JUMP_IF_TRUE</td>
<td align="right">8,740</td>
<td align="right">8,712</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">471,998,475</td>
<td align="right">473,500,691</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">1,233,670,682</td>
<td align="right">1,237,566,434</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">1,356,463,329</td>
<td align="right">1,352,398,758</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">228,162,308</td>
<td align="right">227,488,732</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">178,146,425</td>
<td align="right">177,633,095</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_DICT</td>
<td align="right">579,982,862</td>
<td align="right">578,523,603</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">104,800,981</td>
<td align="right">105,027,961</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">405,464,332</td>
<td align="right">404,594,995</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">28,412,436</td>
<td align="right">28,354,666</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">6,935,563,652</td>
<td align="right">6,921,622,034</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">307,951,525</td>
<td align="right">307,349,716</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">44,959,975</td>
<td align="right">45,037,502</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">11,818,916</td>
<td align="right">11,799,026</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">163,925,072</td>
<td align="right">164,160,703</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">454,036,205</td>
<td align="right">453,391,546</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">4,248,143,537</td>
<td align="right">4,242,237,327</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">567,295,489</td>
<td align="right">568,043,429</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">1,143,054,099</td>
<td align="right">1,141,577,003</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">74,525,334</td>
<td align="right">74,612,839</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">111,119,798</td>
<td align="right">111,238,126</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">134,422,024</td>
<td align="right">134,279,351</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">30,905,104</td>
<td align="right">30,872,316</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">107,690,663</td>
<td align="right">107,796,196</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">2,758,165,625</td>
<td align="right">2,755,462,742</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">126,873,325</td>
<td align="right">126,755,567</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">DICT_UPDATE</td>
<td align="right">72,998</td>
<td align="right">72,932</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">375,716,963</td>
<td align="right">376,048,686</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">122,419,823</td>
<td align="right">122,315,997</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT</td>
<td align="right">460,358,183</td>
<td align="right">459,971,969</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">CALL_PY_WITH_DEFAULTS</td>
<td align="right">221,156,112</td>
<td align="right">220,999,062</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">660,654,950</td>
<td align="right">661,114,167</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">991,540,819</td>
<td align="right">990,875,766</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">1,191,281,210</td>
<td align="right">1,190,487,764</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">507,959,831</td>
<td align="right">507,641,839</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">152,467,851</td>
<td align="right">152,384,785</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">2,063,142,186</td>
<td align="right">2,062,117,685</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">75,777,032</td>
<td align="right">75,804,968</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">321,902,473</td>
<td align="right">321,788,037</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">3,657,328,713</td>
<td align="right">3,656,045,365</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">345,222</td>
<td align="right">345,339</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">421,975,429</td>
<td align="right">422,103,824</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DELETE_FAST</td>
<td align="right">2,229,244</td>
<td align="right">2,228,601</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">226,011,462</td>
<td align="right">225,947,616</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">152,740,479</td>
<td align="right">152,780,667</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_TYPE_1</td>
<td align="right">246,207,495</td>
<td align="right">246,144,029</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">345,808,080</td>
<td align="right">345,896,427</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">667,481,183</td>
<td align="right">667,318,846</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">1,405,869,956</td>
<td align="right">1,406,202,887</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">674,685,591</td>
<td align="right">674,534,186</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">75,851,587</td>
<td align="right">75,834,774</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_FLOAT</td>
<td align="right">87,798,996</td>
<td align="right">87,782,717</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">43,019,818</td>
<td align="right">43,027,426</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">70,415,711</td>
<td align="right">70,406,195</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">CHECK_EXC_MATCH</td>
<td align="right">24,465,838</td>
<td align="right">24,462,534</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">742,762,827</td>
<td align="right">742,859,286</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">24,977,225</td>
<td align="right">24,974,013</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">24,977,371</td>
<td align="right">24,974,166</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">67,110,328</td>
<td align="right">67,101,815</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">95,266,036</td>
<td align="right">95,275,834</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">266,088,891</td>
<td align="right">266,063,314</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">BUILD_STRING</td>
<td align="right">75,723,374</td>
<td align="right">75,730,610</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">84,894,688</td>
<td align="right">84,902,099</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR</td>
<td align="right">23,567</td>
<td align="right">23,569</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">13,104,165</td>
<td align="right">13,103,265</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">275,176,320</td>
<td align="right">275,157,759</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">98,423,965</td>
<td align="right">98,430,170</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_INT</td>
<td align="right">164,920,722</td>
<td align="right">164,930,834</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">540,637</td>
<td align="right">540,607</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">308,474,504</td>
<td align="right">308,490,853</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RAISE_VARARGS</td>
<td align="right">6,185,405</td>
<td align="right">6,185,080</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">1,496,582,699</td>
<td align="right">1,496,660,252</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">349,290,809</td>
<td align="right">349,272,765</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">12,436,390</td>
<td align="right">12,435,761</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">73,750,309</td>
<td align="right">73,753,978</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">FORMAT_SIMPLE</td>
<td align="right">148,908,026</td>
<td align="right">148,915,186</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">505,535,040</td>
<td align="right">505,551,141</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right">2,329,708</td>
<td align="right">2,329,646</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right">210,123,388</td>
<td align="right">210,128,804</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">20,772,670</td>
<td align="right">20,772,933</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_FLOAT</td>
<td align="right">181,060,125</td>
<td align="right">181,058,140</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">254,264,648</td>
<td align="right">254,262,217</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_ATTR</td>
<td align="right">7,751,889</td>
<td align="right">7,751,841</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">UNARY_NEGATIVE</td>
<td align="right">146,012,250</td>
<td align="right">146,011,389</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">156,153,496</td>
<td align="right">156,154,322</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_SLICE</td>
<td align="right">12,601,293</td>
<td align="right">12,601,227</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">SET_ADD</td>
<td align="right">965,677</td>
<td align="right">965,672</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">MAP_ADD</td>
<td align="right">39,905,000</td>
<td align="right">39,905,175</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">28,251,764</td>
<td align="right">28,251,887</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">WITH_EXCEPT_START</td>
<td align="right">233,482</td>
<td align="right">233,481</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">109,895,002</td>
<td align="right">109,894,634</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">202,292,238</td>
<td align="right">202,291,599</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">787,110,595</td>
<td align="right">787,112,723</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BUILD_SLICE</td>
<td align="right">72,099,049</td>
<td align="right">72,098,900</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">GET_YIELD_FROM_ITER</td>
<td align="right">47,328,723</td>
<td align="right">47,328,819</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">173,839,146</td>
<td align="right">173,838,885</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">DELETE_ATTR</td>
<td align="right">6,693,035</td>
<td align="right">6,693,025</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">GET_AWAITABLE</td>
<td align="right">229,793,424</td>
<td align="right">229,793,163</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">RERAISE</td>
<td align="right">3,848,273</td>
<td align="right">3,848,277</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_LIST</td>
<td align="right">12,244,384</td>
<td align="right">12,244,372</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">77,564,182</td>
<td align="right">77,564,253</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">142,935,411</td>
<td align="right">142,935,304</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">556,679,228</td>
<td align="right">556,678,841</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">END_SEND</td>
<td align="right">402,621,479</td>
<td align="right">402,621,218</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">DELETE_SUBSCR</td>
<td align="right">176,488,782</td>
<td align="right">176,488,873</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">94,927,570</td>
<td align="right">94,927,584</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">97,215,632</td>
<td align="right">97,215,646</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CONVERT_VALUE</td>
<td align="right">138,898,276</td>
<td align="right">138,898,256</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_WITH_HINT</td>
<td align="right">64,723,853</td>
<td align="right">64,723,852</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_POP_JUMP_IF_FALSE</td>
<td align="right">38,876,080</td>
<td align="right">38,876,080</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_RESUME</td>
<td align="right">38,855,260</td>
<td align="right">38,855,260</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_RETURN_VALUE</td>
<td align="right">38,851,520</td>
<td align="right">38,851,520</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">14,145,727</td>
<td align="right">14,145,727</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">GET_ANEXT</td>
<td align="right">8,000,960</td>
<td align="right">8,000,960</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">END_ASYNC_FOR</td>
<td align="right">8,000,000</td>
<td align="right">8,000,000</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">GET_AITER</td>
<td align="right">8,000,000</td>
<td align="right">8,000,000</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_GLOBAL</td>
<td align="right">6,944,700</td>
<td align="right">6,944,700</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BEFORE_ASYNC_WITH</td>
<td align="right">3,005,920</td>
<td align="right">3,005,920</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">UNPACK_EX</td>
<td align="right">1,129,822</td>
<td align="right">1,129,822</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">638,582</td>
<td align="right">638,582</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SET_UPDATE</td>
<td align="right">200,488</td>
<td align="right">200,488</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CLEANUP_THROW</td>
<td align="right">152,060</td>
<td align="right">152,060</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_GETATTRIBUTE_OVERRIDDEN</td>
<td align="right">89,680</td>
<td align="right">89,680</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_BUILD_CLASS</td>
<td align="right">30,626</td>
<td align="right">30,626</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_POP_JUMP_IF_NOT_NONE</td>
<td align="right">4,800</td>
<td align="right">4,800</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_LOCALS</td>
<td align="right">2,260</td>
<td align="right">2,260</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FROM_DICT_OR_DEREF</td>
<td align="right">2,240</td>
<td align="right">2,240</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_RETURN_CONST</td>
<td align="right">2,160</td>
<td align="right">2,160</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">FORMAT_WITH_SPEC</td>
<td align="right">1,760</td>
<td align="right">1,760</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SETUP_ANNOTATIONS</td>
<td align="right">1,524</td>
<td align="right">1,524</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DELETE_NAME</td>
<td align="right">1,100</td>
<td align="right">1,100</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_JUMP_FORWARD</td>
<td align="right">1,040</td>
<td align="right">1,040</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_POP_JUMP_IF_NONE</td>
<td align="right">720</td>
<td align="right">720</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_2</td>
<td align="right">80</td>
<td align="right">80</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

## Pair counts

<details>
<summary> Pair counts for top 100 opcode pairs </summary>


Pairs of specialized operations that deoptimize and are then followed by
the corresponding unspecialized instruction are not counted as pairs.

Not included in comparative output.


</details>

## Predecessor/Successor Pairs

<details>
<summary> Top 5 predecessors and successors of each Tier 1 opcode. </summary>


This does not include the unspecialized instructions that occur after a
specialized instruction deoptimizes.

Not included in comparative output.


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
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
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
<td align="right">641,183,201</td>
<td align="right">8.5%</td>
<td align="right">636,717,444</td>
<td align="right">8.5%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">6,892,421,146</td>
<td align="right">91.5%</td>
<td align="right">6,890,274,708</td>
<td align="right">91.5%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">30,888,252</td>
<td align="right">0.4%</td>
<td align="right">30,888,228</td>
<td align="right">0.4%</td>
<td align="right">-0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Failure</td>
<td align="right">1,240,532</td>
<td align="right">66.1%</td>
<td align="right">1,239,411</td>
<td align="right">66.1%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">636,065</td>
<td align="right">33.9%</td>
<td align="right">636,133</td>
<td align="right">33.9%</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">add different types</td>
<td align="right">78,798</td>
<td align="right">6.4%</td>
<td align="right">77,763</td>
<td align="right">6.3%</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">or</td>
<td align="right">17,751</td>
<td align="right">1.4%</td>
<td align="right">17,645</td>
<td align="right">1.4%</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">and int</td>
<td align="right">41,328</td>
<td align="right">3.3%</td>
<td align="right">41,132</td>
<td align="right">3.3%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">power</td>
<td align="right">5,755</td>
<td align="right">0.5%</td>
<td align="right">5,769</td>
<td align="right">0.5%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">floor divide</td>
<td align="right">33,520</td>
<td align="right">2.7%</td>
<td align="right">33,588</td>
<td align="right">2.7%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">remainder</td>
<td align="right">54,193</td>
<td align="right">4.4%</td>
<td align="right">54,275</td>
<td align="right">4.4%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">and other</td>
<td align="right">2,014</td>
<td align="right">0.2%</td>
<td align="right">2,013</td>
<td align="right">0.2%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">multiply different types</td>
<td align="right">92,355</td>
<td align="right">7.4%</td>
<td align="right">92,396</td>
<td align="right">7.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">true divide float</td>
<td align="right">5,765</td>
<td align="right">0.5%</td>
<td align="right">5,767</td>
<td align="right">0.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">lshift</td>
<td align="right">5,831</td>
<td align="right">0.5%</td>
<td align="right">5,833</td>
<td align="right">0.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">xor</td>
<td align="right">9,885</td>
<td align="right">0.8%</td>
<td align="right">9,887</td>
<td align="right">0.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">rshift</td>
<td align="right">9,999</td>
<td align="right">0.8%</td>
<td align="right">9,997</td>
<td align="right">0.8%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">true divide different types</td>
<td align="right">13,425</td>
<td align="right">1.1%</td>
<td align="right">13,427</td>
<td align="right">1.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">add other</td>
<td align="right">64,791</td>
<td align="right">5.2%</td>
<td align="right">64,797</td>
<td align="right">5.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">subtract different types</td>
<td align="right">783,289</td>
<td align="right">63.1%</td>
<td align="right">783,289</td>
<td align="right">63.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">subtract other</td>
<td align="right">12,554</td>
<td align="right">1.0%</td>
<td align="right">12,554</td>
<td align="right">1.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">multiply other</td>
<td align="right">5,220</td>
<td align="right">0.4%</td>
<td align="right">5,220</td>
<td align="right">0.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">true divide other</td>
<td align="right">3,440</td>
<td align="right">0.3%</td>
<td align="right">3,440</td>
<td align="right">0.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">and different types</td>
<td align="right">619</td>
<td align="right">0.0%</td>
<td align="right">619</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
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
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
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
<td align="right">426,490,626</td>
<td align="right">8.7%</td>
<td align="right">426,618,569</td>
<td align="right">8.7%</td>
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
<td align="right">4,459,272,097</td>
<td align="right">91.3%</td>
<td align="right">4,458,737,433</td>
<td align="right">91.3%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">4,903,271</td>
<td align="right">0.1%</td>
<td align="right">4,902,917</td>
<td align="right">0.1%</td>
<td align="right">-0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Failure</td>
<td align="right">186,205</td>
<td align="right">48.0%</td>
<td align="right">186,293</td>
<td align="right">48.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">201,869</td>
<td align="right">52.0%</td>
<td align="right">201,879</td>
<td align="right">52.0%</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">tuple slice</td>
<td align="right">185</td>
<td align="right">0.1%</td>
<td align="right">187</td>
<td align="right">0.1%</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">57,098</td>
<td align="right">30.7%</td>
<td align="right">57,161</td>
<td align="right">30.7%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">77,383</td>
<td align="right">41.6%</td>
<td align="right">77,409</td>
<td align="right">41.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">buffer int</td>
<td align="right">22,903</td>
<td align="right">12.3%</td>
<td align="right">22,900</td>
<td align="right">12.3%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">array int</td>
<td align="right">16,820</td>
<td align="right">9.0%</td>
<td align="right">16,820</td>
<td align="right">9.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">code complex parameters</td>
<td align="right">5,036</td>
<td align="right">2.7%</td>
<td align="right">5,036</td>
<td align="right">2.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">sequence int</td>
<td align="right">4,300</td>
<td align="right">2.3%</td>
<td align="right">4,300</td>
<td align="right">2.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">list slice</td>
<td align="right">1,400</td>
<td align="right">0.8%</td>
<td align="right">1,400</td>
<td align="right">0.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">buffer slice</td>
<td align="right">980</td>
<td align="right">0.5%</td>
<td align="right">980</td>
<td align="right">0.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">string slice</td>
<td align="right">100</td>
<td align="right">0.1%</td>
<td align="right">100</td>
<td align="right">0.1%</td>
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
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
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
<td align="right">1,442,092,016</td>
<td align="right">10.6%</td>
<td align="right">1,441,365,227</td>
<td align="right">10.6%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">257,249,965</td>
<td align="right">1.9%</td>
<td align="right">257,318,199</td>
<td align="right">1.9%</td>
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
<td align="right">12,209,985,503</td>
<td align="right">89.4%</td>
<td align="right">12,208,717,840</td>
<td align="right">89.4%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">33,100</td>
<td align="right">0.0%</td>
<td align="right">33,100</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Failure</td>
<td align="right">955,540</td>
<td align="right">14.8%</td>
<td align="right">955,784</td>
<td align="right">14.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">5,483,619</td>
<td align="right">85.2%</td>
<td align="right">5,484,952</td>
<td align="right">85.2%</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">bound method</td>
<td align="right">12,101</td>
<td align="right">1.3%</td>
<td align="right">12,222</td>
<td align="right">1.3%</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">method wrapper</td>
<td align="right">8,250</td>
<td align="right">0.9%</td>
<td align="right">8,198</td>
<td align="right">0.9%</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">metaclass</td>
<td align="right">43,249</td>
<td align="right">4.5%</td>
<td align="right">43,475</td>
<td align="right">4.5%</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">class mutable</td>
<td align="right">25,297</td>
<td align="right">2.6%</td>
<td align="right">25,276</td>
<td align="right">2.6%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">operator wrapper</td>
<td align="right">10,180</td>
<td align="right">1.1%</td>
<td align="right">10,172</td>
<td align="right">1.1%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">cfunc varargs keywords</td>
<td align="right">32,294</td>
<td align="right">3.4%</td>
<td align="right">32,274</td>
<td align="right">3.4%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">cfunc noargs</td>
<td align="right">70,272</td>
<td align="right">7.4%</td>
<td align="right">70,306</td>
<td align="right">7.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">67,640</td>
<td align="right">7.1%</td>
<td align="right">67,608</td>
<td align="right">7.1%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">class no vectorcall</td>
<td align="right">78,959</td>
<td align="right">8.3%</td>
<td align="right">78,945</td>
<td align="right">8.3%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">cfunc varargs</td>
<td align="right">14,251</td>
<td align="right">1.5%</td>
<td align="right">14,253</td>
<td align="right">1.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">meth descr varargs keywords</td>
<td align="right">20,875</td>
<td align="right">2.2%</td>
<td align="right">20,874</td>
<td align="right">2.2%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">code complex parameters</td>
<td align="right">185,255</td>
<td align="right">19.4%</td>
<td align="right">185,261</td>
<td align="right">19.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">meth descr method fastcall keywords</td>
<td align="right">207,385</td>
<td align="right">21.7%</td>
<td align="right">207,388</td>
<td align="right">21.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">init not inline values</td>
<td align="right">105,617</td>
<td align="right">11.1%</td>
<td align="right">105,617</td>
<td align="right">11.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">meth descr varargs</td>
<td align="right">16,518</td>
<td align="right">1.7%</td>
<td align="right">16,518</td>
<td align="right">1.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">init not python</td>
<td align="right">16,426</td>
<td align="right">1.7%</td>
<td align="right">16,426</td>
<td align="right">1.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">cmethod</td>
<td align="right">14,100</td>
<td align="right">1.5%</td>
<td align="right">14,100</td>
<td align="right">1.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">wrong number arguments</td>
<td align="right">13,773</td>
<td align="right">1.4%</td>
<td align="right">13,773</td>
<td align="right">1.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">init not simple</td>
<td align="right">12,278</td>
<td align="right">1.3%</td>
<td align="right">12,278</td>
<td align="right">1.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">out of versions</td>
<td align="right">980</td>
<td align="right">0.1%</td>
<td align="right">980</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
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
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">1,913,144</td>
<td align="right">0.0%</td>
<td align="right">1,787,810</td>
<td align="right">0.0%</td>
<td align="right">-6.6%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">154,303,365</td>
<td align="right">3.3%</td>
<td align="right">154,225,213</td>
<td align="right">3.3%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">4,582,870,804</td>
<td align="right">96.7%</td>
<td align="right">4,582,115,520</td>
<td align="right">96.7%</td>
<td align="right">-0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">114,175</td>
<td align="right">32.6%</td>
<td align="right">111,832</td>
<td align="right">32.6%</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">236,083</td>
<td align="right">67.4%</td>
<td align="right">231,432</td>
<td align="right">67.4%</td>
<td align="right">-2.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">different types</td>
<td align="right">55,556</td>
<td align="right">23.5%</td>
<td align="right">51,309</td>
<td align="right">22.2%</td>
<td align="right">-7.6%</td>
</tr>
<tr>
<td align="left">long float</td>
<td align="right">1,568</td>
<td align="right">0.7%</td>
<td align="right">1,605</td>
<td align="right">0.7%</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">big int</td>
<td align="right">64,112</td>
<td align="right">27.2%</td>
<td align="right">63,745</td>
<td align="right">27.5%</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">baseobject</td>
<td align="right">33,802</td>
<td align="right">14.3%</td>
<td align="right">33,702</td>
<td align="right">14.6%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">float long</td>
<td align="right">16,441</td>
<td align="right">7.0%</td>
<td align="right">16,469</td>
<td align="right">7.1%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">14,708</td>
<td align="right">6.2%</td>
<td align="right">14,702</td>
<td align="right">6.4%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">bool</td>
<td align="right">3,821</td>
<td align="right">1.6%</td>
<td align="right">3,820</td>
<td align="right">1.7%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">24,178</td>
<td align="right">10.2%</td>
<td align="right">24,184</td>
<td align="right">10.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">4,234</td>
<td align="right">1.8%</td>
<td align="right">4,233</td>
<td align="right">1.8%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">11,080</td>
<td align="right">4.7%</td>
<td align="right">11,080</td>
<td align="right">4.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">4,240</td>
<td align="right">1.8%</td>
<td align="right">4,240</td>
<td align="right">1.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">2,343</td>
<td align="right">1.0%</td>
<td align="right">2,343</td>
<td align="right">1.0%</td>
<td align="right">0.0%</td>
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
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">2,546,240</td>
<td align="right">0.1%</td>
<td align="right">2,517,260</td>
<td align="right">0.1%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">118,961,662</td>
<td align="right">4.6%</td>
<td align="right">118,301,490</td>
<td align="right">4.6%</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">2,480,728,849</td>
<td align="right">95.4%</td>
<td align="right">2,480,647,318</td>
<td align="right">95.4%</td>
<td align="right">-0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Failure</td>
<td align="right">133,116</td>
<td align="right">66.4%</td>
<td align="right">131,471</td>
<td align="right">66.3%</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">67,508</td>
<td align="right">33.6%</td>
<td align="right">66,951</td>
<td align="right">33.7%</td>
<td align="right">-0.8%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">tuple</td>
<td align="right">47,417</td>
<td align="right">35.6%</td>
<td align="right">45,972</td>
<td align="right">35.0%</td>
<td align="right">-3.0%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">19,781</td>
<td align="right">14.9%</td>
<td align="right">19,622</td>
<td align="right">14.9%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">str</td>
<td align="right">37,064</td>
<td align="right">27.8%</td>
<td align="right">37,024</td>
<td align="right">28.2%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">28,854</td>
<td align="right">21.7%</td>
<td align="right">28,853</td>
<td align="right">21.9%</td>
<td align="right">-0.0%</td>
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
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,218,101,113</td>
<td align="right">84.1%</td>
<td align="right">1,201,504,433</td>
<td align="right">83.8%</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">228,796,722</td>
<td align="right">15.8%</td>
<td align="right">229,262,331</td>
<td align="right">16.0%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">101,954,782</td>
<td align="right">7.0%</td>
<td align="right">101,925,113</td>
<td align="right">7.1%</td>
<td align="right">-0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Failure</td>
<td align="right">193,347</td>
<td align="right">8.9%</td>
<td align="right">192,948</td>
<td align="right">8.8%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">1,989,702</td>
<td align="right">91.1%</td>
<td align="right">1,989,166</td>
<td align="right">91.2%</td>
<td align="right">-0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">dict items</td>
<td align="right">66,364</td>
<td align="right">34.3%</td>
<td align="right">65,875</td>
<td align="right">34.1%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">reversed list</td>
<td align="right">7,985</td>
<td align="right">4.1%</td>
<td align="right">8,025</td>
<td align="right">4.2%</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">26,018</td>
<td align="right">13.5%</td>
<td align="right">26,070</td>
<td align="right">13.5%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">19,930</td>
<td align="right">10.3%</td>
<td align="right">19,928</td>
<td align="right">10.3%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">14,756</td>
<td align="right">7.6%</td>
<td align="right">14,756</td>
<td align="right">7.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">14,699</td>
<td align="right">7.6%</td>
<td align="right">14,699</td>
<td align="right">7.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">zip</td>
<td align="right">14,352</td>
<td align="right">7.4%</td>
<td align="right">14,352</td>
<td align="right">7.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">seq iter</td>
<td align="right">10,300</td>
<td align="right">5.3%</td>
<td align="right">10,300</td>
<td align="right">5.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">itertools</td>
<td align="right">7,471</td>
<td align="right">3.9%</td>
<td align="right">7,471</td>
<td align="right">3.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">dict values</td>
<td align="right">7,070</td>
<td align="right">3.7%</td>
<td align="right">7,070</td>
<td align="right">3.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">ascii string</td>
<td align="right">2,700</td>
<td align="right">1.4%</td>
<td align="right">2,700</td>
<td align="right">1.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">map</td>
<td align="right">740</td>
<td align="right">0.4%</td>
<td align="right">740</td>
<td align="right">0.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">660</td>
<td align="right">0.3%</td>
<td align="right">660</td>
<td align="right">0.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">callable</td>
<td align="right">282</td>
<td align="right">0.1%</td>
<td align="right">282</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">20</td>
<td align="right">0.0%</td>
<td align="right">20</td>
<td align="right">0.0%</td>
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
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">580,417,156</td>
<td align="right">3.6%</td>
<td align="right">618,671,533</td>
<td align="right">3.8%</td>
<td align="right">6.6%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">1,432,504,746</td>
<td align="right">8.8%</td>
<td align="right">1,455,106,703</td>
<td align="right">9.0%</td>
<td align="right">1.6%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">14,774,994,453</td>
<td align="right">91.1%</td>
<td align="right">14,770,276,941</td>
<td align="right">91.0%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">684,794</td>
<td align="right">0.0%</td>
<td align="right">684,709</td>
<td align="right">0.0%</td>
<td align="right">-0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">11,835,254</td>
<td align="right">87.3%</td>
<td align="right">12,556,898</td>
<td align="right">88.0%</td>
<td align="right">6.1%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">1,714,615</td>
<td align="right">12.7%</td>
<td align="right">1,710,666</td>
<td align="right">12.0%</td>
<td align="right">-0.2%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">class method obj</td>
<td align="right">25,853</td>
<td align="right">1.5%</td>
<td align="right">22,433</td>
<td align="right">1.3%</td>
<td align="right">-13.2%</td>
</tr>
<tr>
<td align="left">mutable class</td>
<td align="right">78,189</td>
<td align="right">4.6%</td>
<td align="right">77,928</td>
<td align="right">4.6%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">class attr descriptor</td>
<td align="right">30,200</td>
<td align="right">1.8%</td>
<td align="right">30,260</td>
<td align="right">1.8%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">121,927</td>
<td align="right">7.1%</td>
<td align="right">121,782</td>
<td align="right">7.1%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">non overriding descriptor</td>
<td align="right">13,678</td>
<td align="right">0.8%</td>
<td align="right">13,694</td>
<td align="right">0.8%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">301,593</td>
<td align="right">17.6%</td>
<td align="right">301,446</td>
<td align="right">17.6%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">non string or split</td>
<td align="right">22,235</td>
<td align="right">1.3%</td>
<td align="right">22,230</td>
<td align="right">1.3%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">metaclass attribute</td>
<td align="right">195,255</td>
<td align="right">11.4%</td>
<td align="right">195,214</td>
<td align="right">11.4%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">19,349</td>
<td align="right">1.1%</td>
<td align="right">19,347</td>
<td align="right">1.1%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">shadowed</td>
<td align="right">141,291</td>
<td align="right">8.2%</td>
<td align="right">141,277</td>
<td align="right">8.3%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">719,174</td>
<td align="right">41.9%</td>
<td align="right">719,184</td>
<td align="right">42.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">module attr not found</td>
<td align="right">17,842</td>
<td align="right">1.0%</td>
<td align="right">17,842</td>
<td align="right">1.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">not in keys</td>
<td align="right">16,560</td>
<td align="right">1.0%</td>
<td align="right">16,560</td>
<td align="right">1.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">builtin class method</td>
<td align="right">3,818</td>
<td align="right">0.2%</td>
<td align="right">3,818</td>
<td align="right">0.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">non object slot</td>
<td align="right">3,540</td>
<td align="right">0.2%</td>
<td align="right">3,540</td>
<td align="right">0.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">out of versions</td>
<td align="right">2,331</td>
<td align="right">0.1%</td>
<td align="right">2,331</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">wrong number arguments</td>
<td align="right">1,100</td>
<td align="right">0.1%</td>
<td align="right">1,100</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">not in dict</td>
<td align="right">320</td>
<td align="right">0.0%</td>
<td align="right">320</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">no dict</td>
<td align="right">300</td>
<td align="right">0.0%</td>
<td align="right">300</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">property</td>
<td align="right">60</td>
<td align="right">0.0%</td>
<td align="right">60</td>
<td align="right">0.0%</td>
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
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">6,688,638,711</td>
<td align="right">99.7%</td>
<td align="right">6,229,596,419</td>
<td align="right">99.7%</td>
<td align="right">-6.9%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">456,471</td>
<td align="right">0.0%</td>
<td align="right">457,606</td>
<td align="right">0.0%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">20,561,004</td>
<td align="right">0.3%</td>
<td align="right">20,562,335</td>
<td align="right">0.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">13,103</td>
<td align="right">0.0%</td>
<td align="right">13,103</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">668,137</td>
<td align="right">100.0%</td>
<td align="right">668,204</td>
<td align="right">100.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
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
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">134,720,991</td>
<td align="right">100.0%</td>
<td align="right">134,603,185</td>
<td align="right">100.0%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">11,850</td>
<td align="right">0.0%</td>
<td align="right">11,852</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">11,717</td>
<td align="right">100.0%</td>
<td align="right">11,717</td>
<td align="right">100.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
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
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">787,079,695</td>
<td align="right">81.9%</td>
<td align="right">787,081,823</td>
<td align="right">81.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">173,801,154</td>
<td align="right">18.1%</td>
<td align="right">173,800,880</td>
<td align="right">18.1%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">30,900</td>
<td align="right">0.0%</td>
<td align="right">30,900</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">7,146</td>
<td align="right">10.4%</td>
<td align="right">7,153</td>
<td align="right">10.4%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">61,746</td>
<td align="right">89.6%</td>
<td align="right">61,752</td>
<td align="right">89.6%</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">other</td>
<td align="right">16,126</td>
<td align="right">26.1%</td>
<td align="right">16,132</td>
<td align="right">26.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">async generator send</td>
<td align="right">33,180</td>
<td align="right">53.7%</td>
<td align="right">33,180</td>
<td align="right">53.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">9,980</td>
<td align="right">16.2%</td>
<td align="right">9,980</td>
<td align="right">16.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">2,220</td>
<td align="right">3.6%</td>
<td align="right">2,220</td>
<td align="right">3.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">240</td>
<td align="right">0.4%</td>
<td align="right">240</td>
<td align="right">0.4%</td>
<td align="right">0.0%</td>
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
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">165,642,644</td>
<td align="right">5.5%</td>
<td align="right">167,004,998</td>
<td align="right">5.5%</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">239,784,433</td>
<td align="right">8.0%</td>
<td align="right">241,121,122</td>
<td align="right">8.0%</td>
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
<td align="right">2,765,683,986</td>
<td align="right">91.9%</td>
<td align="right">2,765,514,534</td>
<td align="right">91.9%</td>
<td align="right">-0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">3,274,290</td>
<td align="right">95.7%</td>
<td align="right">3,300,022</td>
<td align="right">95.7%</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">148,103</td>
<td align="right">4.3%</td>
<td align="right">148,107</td>
<td align="right">4.3%</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">not managed dict</td>
<td align="right">28,512</td>
<td align="right">19.3%</td>
<td align="right">28,516</td>
<td align="right">19.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">49,779</td>
<td align="right">33.6%</td>
<td align="right">49,779</td>
<td align="right">33.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">not in dict</td>
<td align="right">15,645</td>
<td align="right">10.6%</td>
<td align="right">15,645</td>
<td align="right">10.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">non string or split</td>
<td align="right">15,520</td>
<td align="right">10.5%</td>
<td align="right">15,520</td>
<td align="right">10.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">overriding descriptor</td>
<td align="right">10,820</td>
<td align="right">7.3%</td>
<td align="right">10,820</td>
<td align="right">7.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">not in keys</td>
<td align="right">7,781</td>
<td align="right">5.3%</td>
<td align="right">7,781</td>
<td align="right">5.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">6,912</td>
<td align="right">4.7%</td>
<td align="right">6,912</td>
<td align="right">4.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">property</td>
<td align="right">5,720</td>
<td align="right">3.9%</td>
<td align="right">5,720</td>
<td align="right">3.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">no dict</td>
<td align="right">5,200</td>
<td align="right">3.5%</td>
<td align="right">5,200</td>
<td align="right">3.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">1,580</td>
<td align="right">1.1%</td>
<td align="right">1,580</td>
<td align="right">1.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">out of versions</td>
<td align="right">594</td>
<td align="right">0.4%</td>
<td align="right">594</td>
<td align="right">0.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">mutable class</td>
<td align="right">40</td>
<td align="right">0.0%</td>
<td align="right">40</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
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
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
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
<td align="right">134,322,168</td>
<td align="right">13.2%</td>
<td align="right">134,179,564</td>
<td align="right">13.1%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">886,308,412</td>
<td align="right">86.8%</td>
<td align="right">886,224,538</td>
<td align="right">86.8%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">2,900</td>
<td align="right">0.0%</td>
<td align="right">2,900</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Failure</td>
<td align="right">84,045</td>
<td align="right">81.8%</td>
<td align="right">83,976</td>
<td align="right">81.8%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">18,711</td>
<td align="right">18.2%</td>
<td align="right">18,711</td>
<td align="right">18.2%</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">py simple</td>
<td align="right">42,838</td>
<td align="right">51.0%</td>
<td align="right">42,780</td>
<td align="right">50.9%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">dict subclass no override</td>
<td align="right">28,299</td>
<td align="right">33.7%</td>
<td align="right">28,288</td>
<td align="right">33.7%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">array int</td>
<td align="right">7,320</td>
<td align="right">8.7%</td>
<td align="right">7,320</td>
<td align="right">8.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">2,108</td>
<td align="right">2.5%</td>
<td align="right">2,108</td>
<td align="right">2.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">2,080</td>
<td align="right">2.5%</td>
<td align="right">2,080</td>
<td align="right">2.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">bytearray int</td>
<td align="right">1,400</td>
<td align="right">1.7%</td>
<td align="right">1,400</td>
<td align="right">1.7%</td>
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
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
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
<td align="right">356,811,992</td>
<td align="right">5.5%</td>
<td align="right">343,763,414</td>
<td align="right">5.3%</td>
<td align="right">-3.7%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">104,885,574</td>
<td align="right">1.6%</td>
<td align="right">103,351,215</td>
<td align="right">1.6%</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">6,096,714,523</td>
<td align="right">94.4%</td>
<td align="right">6,095,049,976</td>
<td align="right">94.6%</td>
<td align="right">-0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">2,263,343</td>
<td align="right">77.2%</td>
<td align="right">2,234,430</td>
<td align="right">77.1%</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">666,599</td>
<td align="right">22.8%</td>
<td align="right">663,701</td>
<td align="right">22.9%</td>
<td align="right">-0.4%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">dict</td>
<td align="right">34,092</td>
<td align="right">5.1%</td>
<td align="right">31,812</td>
<td align="right">4.8%</td>
<td align="right">-6.7%</td>
</tr>
<tr>
<td align="left">mapping</td>
<td align="right">99,490</td>
<td align="right">14.9%</td>
<td align="right">98,783</td>
<td align="right">14.9%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">number</td>
<td align="right">181,624</td>
<td align="right">27.2%</td>
<td align="right">181,705</td>
<td align="right">27.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">18,735</td>
<td align="right">2.8%</td>
<td align="right">18,741</td>
<td align="right">2.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">sequence</td>
<td align="right">18,178</td>
<td align="right">2.7%</td>
<td align="right">18,176</td>
<td align="right">2.7%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">95,470</td>
<td align="right">14.3%</td>
<td align="right">95,480</td>
<td align="right">14.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">174,360</td>
<td align="right">26.2%</td>
<td align="right">174,353</td>
<td align="right">26.3%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">40,670</td>
<td align="right">6.1%</td>
<td align="right">40,671</td>
<td align="right">6.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">float</td>
<td align="right">2,320</td>
<td align="right">0.3%</td>
<td align="right">2,320</td>
<td align="right">0.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">bytearray</td>
<td align="right">1,240</td>
<td align="right">0.2%</td>
<td align="right">1,240</td>
<td align="right">0.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">memory view</td>
<td align="right">420</td>
<td align="right">0.1%</td>
<td align="right">420</td>
<td align="right">0.1%</td>
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
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,562,097,494</td>
<td align="right">100.0%</td>
<td align="right">1,562,554,112</td>
<td align="right">100.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">500,351</td>
<td align="right">0.0%</td>
<td align="right">500,306</td>
<td align="right">0.0%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">3,160</td>
<td align="right">0.0%</td>
<td align="right">3,160</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">39,869</td>
<td align="right">91.8%</td>
<td align="right">39,885</td>
<td align="right">91.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">3,577</td>
<td align="right">8.2%</td>
<td align="right">3,576</td>
<td align="right">8.2%</td>
<td align="right">-0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">sequence</td>
<td align="right">2,516</td>
<td align="right">70.3%</td>
<td align="right">2,515</td>
<td align="right">70.3%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">iterator</td>
<td align="right">681</td>
<td align="right">19.0%</td>
<td align="right">681</td>
<td align="right">19.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">380</td>
<td align="right">10.6%</td>
<td align="right">380</td>
<td align="right">10.6%</td>
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
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
Specialized misses
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that deopt.
</details>
</td>
<td align="right">1,251,080,511</td>
<td align="right">0.9%</td>
<td align="right">1,289,047,659</td>
<td align="right">1.0%</td>
<td align="right">3.0%</td>
</tr>
<tr>
<td align="left">
Specialized hits
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that complete.
</details>
</td>
<td align="right">46,560,072,699</td>
<td align="right">35.3%</td>
<td align="right">45,556,882,787</td>
<td align="right">35.2%</td>
<td align="right">-2.2%</td>
</tr>
<tr>
<td align="left">
Basic
<details>
<summary>ⓘ</summary>

Instructions that are not and cannot be specialized, e.g. `LOAD_FAST`.
</details>
</td>
<td align="right">71,687,576,363</td>
<td align="right">54.4%</td>
<td align="right">70,390,566,426</td>
<td align="right">54.4%</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">
Not specialized
<details>
<summary>ⓘ</summary>

Instructions that could be specialized but aren't, e.g. `LOAD_ATTR`, `BINARY_SLICE`.
</details>
</td>
<td align="right">12,281,934,193</td>
<td align="right">9.3%</td>
<td align="right">12,148,690,252</td>
<td align="right">9.4%</td>
<td align="right">-1.1%</td>
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
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">356,811,992</td>
<td align="right">6.6%</td>
<td align="right">343,763,414</td>
<td align="right">6.4%</td>
<td align="right">-3.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">1,432,504,746</td>
<td align="right">26.7%</td>
<td align="right">1,455,106,703</td>
<td align="right">27.1%</td>
<td align="right">1.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">641,183,201</td>
<td align="right">11.9%</td>
<td align="right">636,717,444</td>
<td align="right">11.8%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">239,784,433</td>
<td align="right">4.5%</td>
<td align="right">241,121,122</td>
<td align="right">4.5%</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">228,796,722</td>
<td align="right">4.3%</td>
<td align="right">229,262,331</td>
<td align="right">4.3%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">134,322,168</td>
<td align="right">2.5%</td>
<td align="right">134,179,564</td>
<td align="right">2.5%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">154,303,365</td>
<td align="right">2.9%</td>
<td align="right">154,225,213</td>
<td align="right">2.9%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">1,442,092,016</td>
<td align="right">26.9%</td>
<td align="right">1,441,365,227</td>
<td align="right">26.8%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">426,490,626</td>
<td align="right">7.9%</td>
<td align="right">426,618,569</td>
<td align="right">7.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">173,801,154</td>
<td align="right">3.2%</td>
<td align="right">173,800,880</td>
<td align="right">3.2%</td>
<td align="right">-0.0%</td>
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
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">164,141,271</td>
<td align="right">13.1%</td>
<td align="right">198,362,605</td>
<td align="right">15.4%</td>
<td align="right">20.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">59,618,554</td>
<td align="right">4.8%</td>
<td align="right">63,655,947</td>
<td align="right">4.9%</td>
<td align="right">6.8%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">70,581,334</td>
<td align="right">5.6%</td>
<td align="right">71,953,891</td>
<td align="right">5.6%</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">49,014,915</td>
<td align="right">3.9%</td>
<td align="right">48,805,732</td>
<td align="right">3.8%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">132,129,170</td>
<td align="right">10.6%</td>
<td align="right">131,856,009</td>
<td align="right">10.2%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">109,410,485</td>
<td align="right">8.7%</td>
<td align="right">109,266,104</td>
<td align="right">8.5%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">50,789,067</td>
<td align="right">4.1%</td>
<td align="right">50,767,243</td>
<td align="right">3.9%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">180,882,797</td>
<td align="right">14.5%</td>
<td align="right">180,831,070</td>
<td align="right">14.0%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">50,923,755</td>
<td align="right">4.1%</td>
<td align="right">50,917,310</td>
<td align="right">3.9%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">95,008,525</td>
<td align="right">7.6%</td>
<td align="right">94,998,317</td>
<td align="right">7.4%</td>
<td align="right">-0.0%</td>
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
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Calls via PyEval_EvalFrame (generator)</td>
<td align="right">866,985,436</td>
<td align="right">9.9%</td>
<td align="right">883,899,734</td>
<td align="right">10.1%</td>
<td align="right">2.0%</td>
</tr>
<tr>
<td align="left">Calls to PyEval_EvalDefault</td>
<td align="right">2,313,930,563</td>
<td align="right">26.3%</td>
<td align="right">2,330,940,504</td>
<td align="right">26.5%</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">2,313,930,563</td>
<td align="right">26.3%</td>
<td align="right">2,330,940,504</td>
<td align="right">26.5%</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">Calls to Python functions inlined</td>
<td align="right">6,475,032,917</td>
<td align="right">73.7%</td>
<td align="right">6,457,082,348</td>
<td align="right">73.5%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (slot)</td>
<td align="right">475,827,169</td>
<td align="right">5.4%</td>
<td align="right">476,338,710</td>
<td align="right">5.4%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (api)</td>
<td align="right">254,446,347</td>
<td align="right">2.9%</td>
<td align="right">254,251,590</td>
<td align="right">2.9%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Frames pushed</td>
<td align="right">6,993,627,668</td>
<td align="right">79.6%</td>
<td align="right">6,992,355,115</td>
<td align="right">79.6%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function vectorcall)</td>
<td align="right">1,441,615,957</td>
<td align="right">16.4%</td>
<td align="right">1,441,711,600</td>
<td align="right">16.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (vector)</td>
<td align="right">1,446,945,127</td>
<td align="right">16.5%</td>
<td align="right">1,447,040,770</td>
<td align="right">16.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function ex)</td>
<td align="right">38,361,731</td>
<td align="right">0.4%</td>
<td align="right">38,363,350</td>
<td align="right">0.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Frame objects created</td>
<td align="right">88,456,284</td>
<td align="right">1.0%</td>
<td align="right">88,452,811</td>
<td align="right">1.0%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (method)</td>
<td align="right">213,137,494</td>
<td align="right">2.4%</td>
<td align="right">213,135,745</td>
<td align="right">2.4%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (legacy)</td>
<td align="right">5,298,544</td>
<td align="right">0.1%</td>
<td align="right">5,298,544</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (build class)</td>
<td align="right">30,626</td>
<td align="right">0.0%</td>
<td align="right">30,626</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
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
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Method cache dunder misses</td>
<td align="right">14,193,772</td>
<td align="right"></td>
<td align="right">12,912,556</td>
<td align="right"></td>
<td align="right">-9.0%</td>
</tr>
<tr>
<td align="left">Increfs</td>
<td align="right">62,304,829,276</td>
<td align="right">51.6%</td>
<td align="right">66,062,451,519</td>
<td align="right">53.4%</td>
<td align="right">6.0%</td>
</tr>
<tr>
<td align="left">Decrefs</td>
<td align="right">64,859,034,870</td>
<td align="right">46.9%</td>
<td align="right">68,623,089,860</td>
<td align="right">48.6%</td>
<td align="right">5.8%</td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">83,721,120</td>
<td align="right"></td>
<td align="right">81,836,582</td>
<td align="right"></td>
<td align="right">-2.3%</td>
</tr>
<tr>
<td align="left">Interpreter increfs</td>
<td align="right">58,547,753,241</td>
<td align="right">48.4%</td>
<td align="right">57,580,920,697</td>
<td align="right">46.6%</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">Interpreter decrefs</td>
<td align="right">73,542,718,910</td>
<td align="right">53.1%</td>
<td align="right">72,568,550,777</td>
<td align="right">51.4%</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">Method cache misses</td>
<td align="right">77,302,688</td>
<td align="right"></td>
<td align="right">76,700,549</td>
<td align="right"></td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">104,938,303</td>
<td align="right">0.6%</td>
<td align="right">105,314,733</td>
<td align="right">0.6%</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">Allocations over 4 kbytes</td>
<td align="right">21,172,386</td>
<td align="right">0.1%</td>
<td align="right">21,200,845</td>
<td align="right">0.1%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">3,560,719,633</td>
<td align="right"></td>
<td align="right">3,562,277,260</td>
<td align="right"></td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Inline values</td>
<td align="right">182,884,235</td>
<td align="right"></td>
<td align="right">182,817,440</td>
<td align="right"></td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Allocations from freelist</td>
<td align="right">6,846,981,444</td>
<td align="right">36.8%</td>
<td align="right">6,845,839,794</td>
<td align="right">36.7%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">6,848,983,550</td>
<td align="right"></td>
<td align="right">6,847,841,900</td>
<td align="right"></td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Method cache hits</td>
<td align="right">3,139,685,849</td>
<td align="right"></td>
<td align="right">3,139,923,848</td>
<td align="right"></td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">11,657,110,838</td>
<td align="right">62.6%</td>
<td align="right">11,656,758,748</td>
<td align="right">62.6%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">11,783,221,527</td>
<td align="right">63.2%</td>
<td align="right">11,783,274,326</td>
<td align="right">63.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">12,115,657,843</td>
<td align="right"></td>
<td align="right">12,115,651,229</td>
<td align="right"></td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Materialize dict (on request)</td>
<td align="right">6,618,746</td>
<td align="right">3.6%</td>
<td align="right">6,618,746</td>
<td align="right">3.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Materialize dict (new key)</td>
<td align="right">116,295</td>
<td align="right">0.1%</td>
<td align="right">116,295</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Materialize dict (too big)</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Materialize dict (str subclass)</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
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
<th align="right">Base Collections</th>
<th align="right">Base Objects collected</th>
<th align="right">Base Object visits</th>
<th align="right">Head Collections</th>
<th align="right">Head Objects collected</th>
<th align="right">Head Object visits</th>
</tr>
</thead>
<tbody>
<tr>
<td align="right">0</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right">0</td>
</tr>
<tr>
<td align="right">1</td>
<td align="right">0</td>
<td align="right">116,241,693</td>
<td align="right">17,082,540,169</td>
<td align="right">0</td>
<td align="right">116,277,361</td>
<td align="right">17,135,485,602</td>
</tr>
<tr>
<td align="right">2</td>
<td align="right">0</td>
<td align="right">10,755,840</td>
<td align="right">6,966,995,410</td>
<td align="right">0</td>
<td align="right">10,755,840</td>
<td align="right">6,968,316,400</td>
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
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
Inner loop found
<details>
<summary>ⓘ</summary>

A trace is truncated because it has an inner loop
</details>
</td>
<td align="right">16,411</td>
<td align="right">2.5%</td>
<td align="right">22,338</td>
<td align="right">3.0%</td>
<td align="right">36.1%</td>
</tr>
<tr>
<td align="left">
Trace stack underflow
<details>
<summary>ⓘ</summary>

A potential trace is abandoned because it pops more frames than it pushes.
</details>
</td>
<td align="right">132,425</td>
<td align="right">20.0%</td>
<td align="right">167,263</td>
<td align="right">22.2%</td>
<td align="right">26.3%</td>
</tr>
<tr>
<td align="left">
Trace too short
<details>
<summary>ⓘ</summary>

A potential trace is abandoced because it it too short.
</details>
</td>
<td align="right">554,172</td>
<td align="right">83.6%</td>
<td align="right">645,210</td>
<td align="right">85.5%</td>
<td align="right">16.4%</td>
</tr>
<tr>
<td align="left">
Optimization attempts
<details>
<summary>ⓘ</summary>

The number of times a potential trace is identified.  Specifically, this occurs in the JUMP BACKWARD instruction when the counter reaches a threshold.
</details>
</td>
<td align="right">662,888</td>
<td align="right"></td>
<td align="right">754,242</td>
<td align="right"></td>
<td align="right">13.8%</td>
</tr>
<tr>
<td align="left">
Trace stack overflow
<details>
<summary>ⓘ</summary>

A trace is truncated because it would require more than 5 stack frames.
</details>
</td>
<td align="right">612</td>
<td align="right">0.1%</td>
<td align="right">570</td>
<td align="right">0.1%</td>
<td align="right">-6.9%</td>
</tr>
<tr>
<td align="left">
Traces executed
<details>
<summary>ⓘ</summary>

The number of traces that were executed
</details>
</td>
<td align="right">6,395,232,580</td>
<td align="right"></td>
<td align="right">6,762,643,554</td>
<td align="right"></td>
<td align="right">5.7%</td>
</tr>
<tr>
<td align="left">
Recursive call
<details>
<summary>ⓘ</summary>

A trace is truncated because it has a recursive call.
</details>
</td>
<td align="right">1,531</td>
<td align="right">0.2%</td>
<td align="right">1,449</td>
<td align="right">0.2%</td>
<td align="right">-5.4%</td>
</tr>
<tr>
<td align="left">
Low confidence
<details>
<summary>ⓘ</summary>

A trace is abandoned because the likelihood of the jump to top being taken is too low.
</details>
</td>
<td align="right">6,786</td>
<td align="right">1.0%</td>
<td align="right">6,947</td>
<td align="right">0.9%</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">
Uops executed
<details>
<summary>ⓘ</summary>

The total number of uops (micro-operations) that were executed
</details>
</td>
<td align="right">175,791,588,391</td>
<td align="right">2,748.8%</td>
<td align="right">179,876,759,381</td>
<td align="right">2,659.9%</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">
Executors invalidated
<details>
<summary>ⓘ</summary>

The number of executors that were invalidated due to watched dictionary changes.
</details>
</td>
<td align="right">5,460</td>
<td align="right">5.0%</td>
<td align="right">5,400</td>
<td align="right">5.0%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">
Traces created
<details>
<summary>ⓘ</summary>

The number of traces that were successfully created.
</details>
</td>
<td align="right">108,716</td>
<td align="right">16.4%</td>
<td align="right">109,032</td>
<td align="right">14.5%</td>
<td align="right">0.3%</td>
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
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left"></th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
Optimizer successes
<details>
<summary>ⓘ</summary>

The number of traces that were successfully optimized.
</details>
</td>
<td align="right">106,556</td>
<td align="right">98.0%</td>
<td align="right">106,872</td>
<td align="right">98.0%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">
Optimizer attempts
<details>
<summary>ⓘ</summary>

The number of times the trace optimizer (_Py_uop_analyze_and_optimize) was run.
</details>
</td>
<td align="right">108,716</td>
<td align="right"></td>
<td align="right">109,032</td>
<td align="right"></td>
<td align="right">0.3%</td>
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
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
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
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">
Remove globals incorrect keys
<details>
<summary>ⓘ</summary>

The keys in the globals dictionary aren't what was expected
</details>
</td>
<td align="right">2,120</td>
<td align="right">2.0%</td>
<td align="right">2,120</td>
<td align="right">1.9%</td>
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
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left"><= 1</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 2</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 4</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 8</td>
<td align="right">2,791</td>
<td align="right">2.6%</td>
<td align="right">2,811</td>
<td align="right">2.6%</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">16,962</td>
<td align="right">15.6%</td>
<td align="right">16,603</td>
<td align="right">15.2%</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">41,857</td>
<td align="right">38.5%</td>
<td align="right">41,918</td>
<td align="right">38.4%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">26,655</td>
<td align="right">24.5%</td>
<td align="right">27,000</td>
<td align="right">24.8%</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">14,974</td>
<td align="right">13.8%</td>
<td align="right">15,207</td>
<td align="right">13.9%</td>
<td align="right">1.6%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">4,612</td>
<td align="right">4.2%</td>
<td align="right">4,669</td>
<td align="right">4.3%</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">865</td>
<td align="right">0.8%</td>
<td align="right">824</td>
<td align="right">0.8%</td>
<td align="right">-4.7%</td>
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
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left"><= 1</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 2</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 4</td>
<td align="right">618</td>
<td align="right">0.6%</td>
<td align="right">659</td>
<td align="right">0.6%</td>
<td align="right">6.6%</td>
</tr>
<tr>
<td align="left"><= 8</td>
<td align="right">8,960</td>
<td align="right">8.2%</td>
<td align="right">8,904</td>
<td align="right">8.2%</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">34,300</td>
<td align="right">31.6%</td>
<td align="right">34,007</td>
<td align="right">31.2%</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">35,108</td>
<td align="right">32.3%</td>
<td align="right">35,487</td>
<td align="right">32.5%</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">18,118</td>
<td align="right">16.7%</td>
<td align="right">18,249</td>
<td align="right">16.7%</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">7,366</td>
<td align="right">6.8%</td>
<td align="right">7,519</td>
<td align="right">6.9%</td>
<td align="right">2.1%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">1,866</td>
<td align="right">1.7%</td>
<td align="right">1,827</td>
<td align="right">1.7%</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">220</td>
<td align="right">0.2%</td>
<td align="right">220</td>
<td align="right">0.2%</td>
<td align="right">0.0%</td>
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
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left"><= 1</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
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
<th align="right">Base Count</th>
<th align="right">Head Count</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">_COLD_EXIT</td>
<td align="right">1,652,294,669</td>
<td align="right">1,976,218,554</td>
<td align="right">19.6%</td>
</tr>
<tr>
<td align="left">_SET_IP</td>
<td align="right">16,396,888,331</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY</td>
<td align="right">9,852,808,453</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW</td>
<td align="right">8,897,364,400</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_1</td>
<td align="right">6,199,412,128</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST</td>
<td align="right">5,487,472,436</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION</td>
<td align="right">5,382,628,215</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_0</td>
<td align="right">5,332,634,541</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_IS_FALSE_POP</td>
<td align="right">5,319,125,332</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_START_EXECUTOR</td>
<td align="right">4,742,937,911</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_SIDE_EXIT</td>
<td align="right">3,636,940,722</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_7</td>
<td align="right">3,378,592,992</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_3</td>
<td align="right">3,099,156,745</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST</td>
<td align="right">2,972,986,395</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_EXIT_TRACE</td>
<td align="right">2,752,610,436</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_2</td>
<td align="right">2,705,781,448</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_IS_TRUE_POP</td>
<td align="right">2,570,205,940</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_INT</td>
<td align="right">2,490,229,321</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_NOS_INT</td>
<td align="right">2,422,583,537</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_PERIODIC</td>
<td align="right">2,130,184,426</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_JUMP_TO_TOP</td>
<td align="right">2,101,948,126</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_5</td>
<td align="right">2,052,255,482</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_4</td>
<td align="right">1,969,647,324</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL_BOOL</td>
<td align="right">1,937,398,378</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_MANAGED_OBJECT_HAS_VALUES</td>
<td align="right">1,901,882,196</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE_0</td>
<td align="right">1,895,406,680</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_1</td>
<td align="right">1,849,560,485</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COMPARE_OP_STR</td>
<td align="right">1,825,069,721</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_WITH_NULL</td>
<td align="right">1,655,540,053</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_EXACT_ARGS</td>
<td align="right">1,590,663,494</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_PUSH_FRAME</td>
<td align="right">1,527,393,871</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_SAVE_RETURN_OFFSET</td>
<td align="right">1,527,393,871</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_ITER_CHECK_LIST</td>
<td align="right">1,511,297,457</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_LIST</td>
<td align="right">1,495,257,536</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_SET</td>
<td align="right">1,478,815,993</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_RESUME_CHECK</td>
<td align="right">1,308,273,275</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION</td>
<td align="right">1,278,029,400</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COPY</td>
<td align="right">1,252,536,209</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_6</td>
<td align="right">1,244,746,853</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR</td>
<td align="right">1,241,214,528</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE</td>
<td align="right">1,240,296,969</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_STR_INT</td>
<td align="right">1,215,783,045</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_ITER_NEXT_LIST</td>
<td align="right">1,208,490,713</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_7</td>
<td align="right">1,202,451,480</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_SWAP</td>
<td align="right">1,130,196,140</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right">1,124,307,820</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_DEOPT</td>
<td align="right">1,105,511,315</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR</td>
<td align="right">1,097,188,280</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_LIST_INT</td>
<td align="right">1,056,089,981</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_DORV_VALUES_INST_ATTR_FROM_DICT</td>
<td align="right">1,046,300,334</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY_AND_SET_IP</td>
<td align="right">1,034,961,602</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_KEYS_VERSION</td>
<td align="right">1,003,176,745</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_UNICODE</td>
<td align="right">965,856,684</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COMPARE_OP_INT</td>
<td align="right">944,345,849</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">910,407,971</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_FLOAT</td>
<td align="right">867,639,925</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE_OPERAND</td>
<td align="right">867,004,415</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP</td>
<td align="right">855,512,245</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">830,550,898</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST</td>
<td align="right">790,131,313</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_ITER_CHECK_RANGE</td>
<td align="right">783,998,710</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_RANGE</td>
<td align="right">782,640,950</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_ITER_NEXT_RANGE</td>
<td align="right">734,429,611</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_PUSH_NULL</td>
<td align="right">730,312,106</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_SLOT_0</td>
<td align="right">705,209,204</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_2</td>
<td align="right">705,122,963</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_POP_TOP</td>
<td align="right">699,471,567</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_4</td>
<td align="right">656,354,557</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_5</td>
<td align="right">647,135,893</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_NOS_FLOAT</td>
<td align="right">628,576,603</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_3</td>
<td align="right">625,179,909</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">619,344,929</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_O</td>
<td align="right">615,543,693</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_FLOAT</td>
<td align="right">571,783,760</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_POP_FRAME</td>
<td align="right">553,454,391</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_ITER_CHECK_TUPLE</td>
<td align="right">543,391,472</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_BOTH_INT</td>
<td align="right">533,797,265</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_1</td>
<td align="right">526,234,164</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_LIST_INT</td>
<td align="right">478,864,182</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_TUPLE</td>
<td align="right">466,136,313</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_4</td>
<td align="right">448,283,584</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_DEREF</td>
<td align="right">447,194,674</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBTRACT_INT</td>
<td align="right">442,144,160</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_6</td>
<td align="right">417,856,371</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_FOR_ITER_TIER_TWO</td>
<td align="right">413,832,834</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">382,602,700</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_0</td>
<td align="right">381,808,084</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BUILD_TUPLE</td>
<td align="right">374,116,777</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW_WITH_NULL</td>
<td align="right">364,624,665</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_DICT</td>
<td align="right">360,160,209</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_IS_OP</td>
<td align="right">337,693,979</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR</td>
<td align="right">317,348,611</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_ITER_NEXT_TUPLE</td>
<td align="right">311,557,909</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_ISINSTANCE</td>
<td align="right">310,093,220</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_DICT</td>
<td align="right">258,326,692</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BUILD_LIST</td>
<td align="right">245,606,347</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GET_ITER</td>
<td align="right">244,699,152</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL</td>
<td align="right">239,468,610</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_TYPE_1</td>
<td align="right">237,538,981</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">225,953,442</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_TOS_INT</td>
<td align="right">209,265,829</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_0</td>
<td align="right">204,628,651</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_LEN</td>
<td align="right">196,781,641</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL_INT</td>
<td align="right">196,541,464</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TUPLE</td>
<td align="right">190,910,408</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL</td>
<td align="right">188,829,178</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">184,988,470</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_MULTIPLY_INT</td>
<td align="right">184,971,232</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LIST_APPEND</td>
<td align="right">182,702,735</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL_NONE</td>
<td align="right">173,061,638</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE</td>
<td align="right">164,092,258</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">153,701,567</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_SLICE</td>
<td align="right">149,868,340</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_IS_NOT_NONE_POP</td>
<td align="right">148,487,880</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_SUBSCR_TUPLE_INT</td>
<td align="right">147,485,036</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_DICT</td>
<td align="right">143,859,481</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BUILD_SLICE</td>
<td align="right">139,781,460</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GET_ANEXT</td>
<td align="right">125,514,720</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_ATTR_SLOT</td>
<td align="right">124,257,735</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_SLICE</td>
<td align="right">119,837,390</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CONTAINS_OP</td>
<td align="right">107,488,858</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_2</td>
<td align="right">104,795,235</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_DORV_NO_DICT</td>
<td align="right">104,016,004</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">102,708,244</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_WITH_HINT</td>
<td align="right">97,383,791</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_METHOD_LAZY_DICT</td>
<td align="right">97,310,314</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">97,310,314</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_WITH_HINT</td>
<td align="right">97,272,930</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LIST_EXTEND</td>
<td align="right">96,951,712</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_INTRINSIC_1</td>
<td align="right">96,027,912</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COMPARE_OP</td>
<td align="right">93,380,106</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">88,597,947</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_LIST</td>
<td align="right">77,567,840</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">76,424,995</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">76,371,555</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COMPARE_OP_FLOAT</td>
<td align="right">70,082,948</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_STR_1</td>
<td align="right">66,199,794</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNARY_NOT</td>
<td align="right">62,209,893</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_MAKE_FUNCTION</td>
<td align="right">60,637,298</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL_LIST</td>
<td align="right">59,313,852</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_TOS_FLOAT</td>
<td align="right">58,173,820</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_CLASS</td>
<td align="right">57,440,054</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_3</td>
<td align="right">56,651,034</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_ATTR</td>
<td align="right">51,270,753</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_GLOBALS_VERSION</td>
<td align="right">50,855,144</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COPY_FREE_VARS</td>
<td align="right">49,393,962</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_SET_FUNCTION_ATTRIBUTE</td>
<td align="right">47,055,705</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_MODULE</td>
<td align="right">44,267,468</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_IS_NONE_POP</td>
<td align="right">41,801,073</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_REPLACE_WITH_TRUE</td>
<td align="right">32,282,763</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNARY_NEGATIVE</td>
<td align="right">25,045,775</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_CLASS</td>
<td align="right">25,021,813</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL_STR</td>
<td align="right">24,373,137</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_UNICODE</td>
<td align="right">23,610,903</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_CLASS_0</td>
<td align="right">23,413,597</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">22,175,188</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">21,933,044</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">21,767,640</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_MAP_ADD</td>
<td align="right">20,605,296</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_AND_CLEAR</td>
<td align="right">15,847,393</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNARY_INVERT</td>
<td align="right">12,534,740</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BUILD_MAP</td>
<td align="right">9,901,998</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS</td>
<td align="right">9,621,770</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_DICT_MERGE</td>
<td align="right">7,203,149</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_BUILTINS</td>
<td align="right">6,587,676</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_MODULE</td>
<td align="right">6,479,705</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_MODULE</td>
<td align="right">6,479,705</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE_1</td>
<td align="right">6,364,796</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_MAKE_CELL</td>
<td align="right">5,631,931</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_DEREF</td>
<td align="right">2,930,205</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE</td>
<td align="right">1,554,881</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_SET_ADD</td>
<td align="right">1,449,309</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_DELETE_SUBSCR</td>
<td align="right">1,428,140</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_FORMAT_SIMPLE</td>
<td align="right">1,407,265</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_GLOBAL</td>
<td align="right">1,260,560</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_POP_TOP_LOAD_CONST_INLINE_BORROW</td>
<td align="right">1,239,857</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CONVERT_VALUE</td>
<td align="right">790,640</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BUILD_STRING</td>
<td align="right">595,780</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_TUPLE_1</td>
<td align="right">572,540</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_NAME</td>
<td align="right">545,860</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_ERROR_POP_N</td>
<td align="right">485,874</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_CHECK</td>
<td align="right">253,629</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GET_YIELD_FROM_ITER</td>
<td align="right">179,880</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_SUPER_ATTR_METHOD</td>
<td align="right">95,777</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BUILD_CONST_KEY_MAP</td>
<td align="right">79,650</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_BUILTINS_VERSION</td>
<td align="right">38,636</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_CLASS_1</td>
<td align="right">3,840</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNPACK_EX</td>
<td align="right">104</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__CHECK_VALIDITY</td>
<td align="right"></td>
<td align="right">7,822,354,774</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__SET_IP</td>
<td align="right"></td>
<td align="right">7,656,135,748</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__LOAD_CONST_INLINE_BORROW</td>
<td align="right"></td>
<td align="right">7,099,270,424</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__SET_IP</td>
<td align="right"></td>
<td align="right">5,549,899,560</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__GUARD_IS_FALSE_POP</td>
<td align="right"></td>
<td align="right">5,044,541,831</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__START_EXECUTOR</td>
<td align="right"></td>
<td align="right">4,786,425,000</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__LOAD_FAST_0</td>
<td align="right"></td>
<td align="right">3,843,342,580</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__GUARD_TYPE_VERSION</td>
<td align="right"></td>
<td align="right">3,725,528,571</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__SET_IP</td>
<td align="right"></td>
<td align="right">3,706,817,365</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__LOAD_FAST_1</td>
<td align="right"></td>
<td align="right">3,089,903,223</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__LOAD_FAST_7</td>
<td align="right"></td>
<td align="right">2,995,242,050</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__CHECK_PERIODIC</td>
<td align="right"></td>
<td align="right">2,380,559,908</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__GUARD_IS_TRUE_POP</td>
<td align="right"></td>
<td align="right">2,335,704,839</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__LOAD_FAST_1</td>
<td align="right"></td>
<td align="right">2,286,815,180</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__GUARD_NOS_INT</td>
<td align="right"></td>
<td align="right">2,241,419,787</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__LOAD_FAST</td>
<td align="right"></td>
<td align="right">2,211,488,303</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__JUMP_TO_TOP</td>
<td align="right"></td>
<td align="right">2,096,977,574</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__SIDE_EXIT</td>
<td align="right"></td>
<td align="right">2,084,505,113</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__LOAD_FAST</td>
<td align="right"></td>
<td align="right">2,076,415,956</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__COMPARE_OP_STR</td>
<td align="right"></td>
<td align="right">1,826,636,935</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__BINARY_OP_ADD_INT</td>
<td align="right"></td>
<td align="right">1,807,131,590</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__CHECK_VALIDITY</td>
<td align="right"></td>
<td align="right">1,775,699,364</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__EXIT_TRACE</td>
<td align="right"></td>
<td align="right">1,765,120,740</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__LOAD_CONST_INLINE_WITH_NULL</td>
<td align="right"></td>
<td align="right">1,688,490,491</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__LOAD_FAST_2</td>
<td align="right"></td>
<td align="right">1,663,455,737</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__SIDE_EXIT</td>
<td align="right"></td>
<td align="right">1,651,127,548</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__CHECK_MANAGED_OBJECT_HAS_VALUES</td>
<td align="right"></td>
<td align="right">1,518,164,191</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__PUSH_FRAME</td>
<td align="right"></td>
<td align="right">1,516,469,021</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__SAVE_RETURN_OFFSET</td>
<td align="right"></td>
<td align="right">1,516,469,021</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__LOAD_ATTR_INSTANCE_VALUE_0</td>
<td align="right"></td>
<td align="right">1,511,821,596</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__STORE_FAST</td>
<td align="right"></td>
<td align="right">1,500,363,384</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__CONTAINS_OP_SET</td>
<td align="right"></td>
<td align="right">1,491,673,658</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__GUARD_NOT_EXHAUSTED_LIST</td>
<td align="right"></td>
<td align="right">1,490,646,788</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__LOAD_FAST_3</td>
<td align="right"></td>
<td align="right">1,489,100,918</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__LOAD_CONST_INLINE_BORROW</td>
<td align="right"></td>
<td align="right">1,469,688,690</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__ITER_CHECK_LIST</td>
<td align="right"></td>
<td align="right">1,415,668,111</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__GUARD_TYPE_VERSION</td>
<td align="right"></td>
<td align="right">1,385,178,144</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__TO_BOOL_BOOL</td>
<td align="right"></td>
<td align="right">1,352,273,416</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__LOAD_FAST_0</td>
<td align="right"></td>
<td align="right">1,333,734,172</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__RESUME_CHECK</td>
<td align="right"></td>
<td align="right">1,321,258,135</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__STORE_FAST_1</td>
<td align="right"></td>
<td align="right">1,296,655,811</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__BINARY_SUBSCR_STR_INT</td>
<td align="right"></td>
<td align="right">1,289,457,372</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__ITER_NEXT_LIST</td>
<td align="right"></td>
<td align="right">1,204,117,663</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__LOAD_FAST</td>
<td align="right"></td>
<td align="right">1,157,407,536</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__SWAP</td>
<td align="right"></td>
<td align="right">1,097,293,213</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__LOAD_FAST_5</td>
<td align="right"></td>
<td align="right">1,092,840,303</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__LOAD_FAST_1</td>
<td align="right"></td>
<td align="right">1,064,688,311</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__STORE_FAST_7</td>
<td align="right"></td>
<td align="right">1,060,166,112</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__LOAD_FAST_4</td>
<td align="right"></td>
<td align="right">1,017,087,573</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__GUARD_BOTH_UNICODE</td>
<td align="right"></td>
<td align="right">930,638,679</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__LOAD_FAST_3</td>
<td align="right"></td>
<td align="right">893,060,314</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__CHECK_STACK_SPACE_OPERAND</td>
<td align="right"></td>
<td align="right">869,331,679</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__LOAD_CONST_INLINE</td>
<td align="right"></td>
<td align="right">840,437,047</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__LOAD_FAST_6</td>
<td align="right"></td>
<td align="right">830,153,784</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__LOAD_FAST_5</td>
<td align="right"></td>
<td align="right">824,887,562</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__LOAD_FAST_2</td>
<td align="right"></td>
<td align="right">815,046,468</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__LOAD_CONST_INLINE_BORROW</td>
<td align="right"></td>
<td align="right">814,928,833</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__EXIT_TRACE</td>
<td align="right"></td>
<td align="right">809,758,534</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__GUARD_NOT_EXHAUSTED_RANGE</td>
<td align="right"></td>
<td align="right">782,388,459</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__STORE_FAST</td>
<td align="right"></td>
<td align="right">765,472,612</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__COPY</td>
<td align="right"></td>
<td align="right">764,202,452</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__STORE_FAST</td>
<td align="right"></td>
<td align="right">762,447,725</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__LOAD_FAST_4</td>
<td align="right"></td>
<td align="right">759,850,323</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__ITER_CHECK_RANGE</td>
<td align="right"></td>
<td align="right">757,201,153</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__LOAD_FAST_3</td>
<td align="right"></td>
<td align="right">734,312,852</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__ITER_NEXT_RANGE</td>
<td align="right"></td>
<td align="right">734,272,053</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__CHECK_FUNCTION</td>
<td align="right"></td>
<td align="right">689,875,838</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right"></td>
<td align="right">687,256,830</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__BINARY_SUBSCR_LIST_INT</td>
<td align="right"></td>
<td align="right">655,798,602</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__CHECK_VALIDITY</td>
<td align="right"></td>
<td align="right">654,410,846</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__CALL_BUILTIN_FAST</td>
<td align="right"></td>
<td align="right">647,938,723</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right"></td>
<td align="right">631,963,040</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__CHECK_VALIDITY_AND_SET_IP</td>
<td align="right"></td>
<td align="right">627,794,225</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__BINARY_SUBSCR</td>
<td align="right"></td>
<td align="right">627,608,463</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__GUARD_DORV_VALUES_INST_ATTR_FROM_DICT</td>
<td align="right"></td>
<td align="right">605,102,295</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right"></td>
<td align="right">601,436,973</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__GUARD_KEYS_VERSION</td>
<td align="right"></td>
<td align="right">586,165,348</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__CHECK_FUNCTION_EXACT_ARGS</td>
<td align="right"></td>
<td align="right">571,827,860</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right"></td>
<td align="right">564,626,700</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__STORE_FAST_1</td>
<td align="right"></td>
<td align="right">549,459,205</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__CHECK_FUNCTION</td>
<td align="right"></td>
<td align="right">548,526,506</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__TO_BOOL_BOOL</td>
<td align="right"></td>
<td align="right">537,779,457</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__LOAD_ATTR</td>
<td align="right"></td>
<td align="right">535,039,264</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__CALL_BUILTIN_O</td>
<td align="right"></td>
<td align="right">532,260,433</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__CHECK_FUNCTION_EXACT_ARGS</td>
<td align="right"></td>
<td align="right">529,361,717</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__COMPARE_OP_INT</td>
<td align="right"></td>
<td align="right">519,858,134</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__DEOPT</td>
<td align="right"></td>
<td align="right">514,249,102</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__INIT_CALL_PY_EXACT_ARGS_1</td>
<td align="right"></td>
<td align="right">509,919,694</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__LOAD_ATTR_SLOT_0</td>
<td align="right"></td>
<td align="right">506,027,311</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__ITER_CHECK_TUPLE</td>
<td align="right"></td>
<td align="right">492,627,740</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__BINARY_SUBSCR</td>
<td align="right"></td>
<td align="right">481,043,433</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__CHECK_FUNCTION_EXACT_ARGS</td>
<td align="right"></td>
<td align="right">478,614,026</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__POP_TOP</td>
<td align="right"></td>
<td align="right">467,319,741</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__POP_FRAME</td>
<td align="right"></td>
<td align="right">467,104,812</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__GUARD_NOT_EXHAUSTED_TUPLE</td>
<td align="right"></td>
<td align="right">465,772,563</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__INIT_CALL_PY_EXACT_ARGS_4</td>
<td align="right"></td>
<td align="right">448,796,267</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__STORE_FAST_2</td>
<td align="right"></td>
<td align="right">436,726,971</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__BINARY_OP</td>
<td align="right"></td>
<td align="right">428,098,492</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__PUSH_NULL</td>
<td align="right"></td>
<td align="right">425,362,103</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__GUARD_DORV_VALUES_INST_ATTR_FROM_DICT</td>
<td align="right"></td>
<td align="right">422,900,116</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__GUARD_KEYS_VERSION</td>
<td align="right"></td>
<td align="right">422,425,819</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__FOR_ITER_TIER_TWO</td>
<td align="right"></td>
<td align="right">418,387,708</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__STORE_SUBSCR_LIST_INT</td>
<td align="right"></td>
<td align="right">418,188,822</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__GUARD_NOS_FLOAT</td>
<td align="right"></td>
<td align="right">417,330,900</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__BINARY_OP_ADD_INT</td>
<td align="right"></td>
<td align="right">413,446,059</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__GUARD_BOTH_FLOAT</td>
<td align="right"></td>
<td align="right">411,855,600</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__BINARY_SUBSCR_LIST_INT</td>
<td align="right"></td>
<td align="right">399,332,538</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__COMPARE_OP_INT</td>
<td align="right"></td>
<td align="right">394,269,905</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__CHECK_MANAGED_OBJECT_HAS_VALUES</td>
<td align="right"></td>
<td align="right">388,678,706</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__LOAD_ATTR_INSTANCE_VALUE_0</td>
<td align="right"></td>
<td align="right">388,545,785</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__COPY</td>
<td align="right"></td>
<td align="right">384,329,060</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__GUARD_IS_FALSE_POP</td>
<td align="right"></td>
<td align="right">383,891,447</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__INIT_CALL_PY_EXACT_ARGS_0</td>
<td align="right"></td>
<td align="right">383,140,845</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__STORE_FAST_6</td>
<td align="right"></td>
<td align="right">376,668,582</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right"></td>
<td align="right">372,876,520</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__CALL_BUILTIN_FAST</td>
<td align="right"></td>
<td align="right">370,619,617</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__GUARD_BOTH_FLOAT</td>
<td align="right"></td>
<td align="right">369,633,041</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__STORE_FAST_5</td>
<td align="right"></td>
<td align="right">362,503,545</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__LOAD_FAST_5</td>
<td align="right"></td>
<td align="right">359,433,049</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__BINARY_OP_ADD_INT</td>
<td align="right"></td>
<td align="right">357,269,842</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__STORE_FAST_4</td>
<td align="right"></td>
<td align="right">352,080,769</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right"></td>
<td align="right">347,279,065</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__LOAD_ATTR</td>
<td align="right"></td>
<td align="right">346,411,191</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__BUILD_TUPLE</td>
<td align="right"></td>
<td align="right">341,521,286</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__BINARY_OP</td>
<td align="right"></td>
<td align="right">323,649,144</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__STORE_FAST_3</td>
<td align="right"></td>
<td align="right">321,000,726</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__BINARY_OP_ADD_FLOAT</td>
<td align="right"></td>
<td align="right">313,402,260</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__ITER_NEXT_TUPLE</td>
<td align="right"></td>
<td align="right">311,238,899</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__CALL_ISINSTANCE</td>
<td align="right"></td>
<td align="right">310,754,420</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__CHECK_VALIDITY_AND_SET_IP</td>
<td align="right"></td>
<td align="right">307,781,798</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__IS_OP</td>
<td align="right"></td>
<td align="right">298,959,200</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__LOAD_FAST_2</td>
<td align="right"></td>
<td align="right">296,779,846</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__LOAD_FAST_6</td>
<td align="right"></td>
<td align="right">287,923,921</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__BINARY_OP_SUBTRACT_INT</td>
<td align="right"></td>
<td align="right">281,679,715</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__STORE_SUBSCR</td>
<td align="right"></td>
<td align="right">275,101,757</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__LOAD_DEREF</td>
<td align="right"></td>
<td align="right">272,746,111</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__LOAD_FAST_0</td>
<td align="right"></td>
<td align="right">272,121,055</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__SIDE_EXIT</td>
<td align="right"></td>
<td align="right">271,420,071</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__GUARD_NOS_INT</td>
<td align="right"></td>
<td align="right">268,785,805</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__LOAD_CONST_INLINE_BORROW_WITH_NULL</td>
<td align="right"></td>
<td align="right">268,635,751</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__DEOPT</td>
<td align="right"></td>
<td align="right">262,498,747</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__GUARD_TYPE_VERSION</td>
<td align="right"></td>
<td align="right">261,872,426</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__STORE_FAST_4</td>
<td align="right"></td>
<td align="right">259,137,290</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__LOAD_CONST_INLINE</td>
<td align="right"></td>
<td align="right">248,737,238</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__STORE_FAST_5</td>
<td align="right"></td>
<td align="right">241,678,875</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__CALL_TYPE_1</td>
<td align="right"></td>
<td align="right">237,456,999</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__LOAD_CONST_INLINE</td>
<td align="right"></td>
<td align="right">230,031,556</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__POP_TOP</td>
<td align="right"></td>
<td align="right">228,014,316</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__STORE_FAST_2</td>
<td align="right"></td>
<td align="right">224,370,509</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__LOAD_GLOBAL</td>
<td align="right"></td>
<td align="right">217,690,370</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__STORE_FAST_3</td>
<td align="right"></td>
<td align="right">217,055,721</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__GUARD_NOS_FLOAT</td>
<td align="right"></td>
<td align="right">211,245,706</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__LOAD_FAST_7</td>
<td align="right"></td>
<td align="right">204,992,811</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__LOAD_ATTR_SLOT_0</td>
<td align="right"></td>
<td align="right">203,353,945</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__GUARD_IS_TRUE_POP</td>
<td align="right"></td>
<td align="right">203,335,049</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right"></td>
<td align="right">202,171,311</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__LOAD_FAST_4</td>
<td align="right"></td>
<td align="right">201,191,304</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__CONTAINS_OP_DICT</td>
<td align="right"></td>
<td align="right">198,997,989</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__GUARD_BOTH_INT</td>
<td align="right"></td>
<td align="right">197,880,047</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__BUILD_LIST</td>
<td align="right"></td>
<td align="right">197,294,980</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right"></td>
<td align="right">195,700,240</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__TO_BOOL_INT</td>
<td align="right"></td>
<td align="right">195,111,683</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__LOAD_CONST_INLINE_WITH_NULL</td>
<td align="right"></td>
<td align="right">194,685,385</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__PUSH_NULL</td>
<td align="right"></td>
<td align="right">192,261,906</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__LOAD_ATTR</td>
<td align="right"></td>
<td align="right">192,001,056</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__CALL_LEN</td>
<td align="right"></td>
<td align="right">185,613,045</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right"></td>
<td align="right">184,970,894</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__BINARY_OP_ADD_FLOAT</td>
<td align="right"></td>
<td align="right">178,903,140</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__LIST_APPEND</td>
<td align="right"></td>
<td align="right">176,981,709</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__LOAD_FAST_7</td>
<td align="right"></td>
<td align="right">176,855,620</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__GUARD_BOTH_INT</td>
<td align="right"></td>
<td align="right">174,816,493</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__LOAD_DEREF</td>
<td align="right"></td>
<td align="right">170,947,331</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__GUARD_BOTH_INT</td>
<td align="right"></td>
<td align="right">157,824,572</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__BINARY_SUBSCR_DICT</td>
<td align="right"></td>
<td align="right">149,905,787</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__STORE_FAST_0</td>
<td align="right"></td>
<td align="right">149,679,244</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right"></td>
<td align="right">147,391,642</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__BINARY_OP_MULTIPLY_INT</td>
<td align="right"></td>
<td align="right">146,673,160</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__TO_BOOL</td>
<td align="right"></td>
<td align="right">145,080,796</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right"></td>
<td align="right">144,465,979</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__GET_ITER</td>
<td align="right"></td>
<td align="right">144,028,921</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__STORE_SUBSCR_DICT</td>
<td align="right"></td>
<td align="right">143,207,405</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__BINARY_OP_SUBTRACT_INT</td>
<td align="right"></td>
<td align="right">141,737,918</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__CHECK_STACK_SPACE</td>
<td align="right"></td>
<td align="right">140,091,171</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__BUILD_SLICE</td>
<td align="right"></td>
<td align="right">139,780,100</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__EXIT_TRACE</td>
<td align="right"></td>
<td align="right">138,601,737</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__STORE_SLICE</td>
<td align="right"></td>
<td align="right">138,542,280</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__BINARY_SUBSCR</td>
<td align="right"></td>
<td align="right">133,311,721</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__LOAD_FAST_6</td>
<td align="right"></td>
<td align="right">126,218,387</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__GET_ANEXT</td>
<td align="right"></td>
<td align="right">125,514,720</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right"></td>
<td align="right">125,403,660</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__GUARD_IS_NOT_NONE_POP</td>
<td align="right"></td>
<td align="right">120,764,497</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__PUSH_NULL</td>
<td align="right"></td>
<td align="right">119,951,434</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right"></td>
<td align="right">119,462,920</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__TO_BOOL_NONE</td>
<td align="right"></td>
<td align="right">116,249,682</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__STORE_ATTR_SLOT</td>
<td align="right"></td>
<td align="right">111,162,973</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__BINARY_OP</td>
<td align="right"></td>
<td align="right">109,845,974</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__TO_BOOL</td>
<td align="right"></td>
<td align="right">107,406,640</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__GUARD_TOS_INT</td>
<td align="right"></td>
<td align="right">105,576,707</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__BINARY_SUBSCR_TUPLE_INT</td>
<td align="right"></td>
<td align="right">105,072,974</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__UNPACK_SEQUENCE_TUPLE</td>
<td align="right"></td>
<td align="right">103,995,360</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__INIT_CALL_PY_EXACT_ARGS_2</td>
<td align="right"></td>
<td align="right">103,487,281</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__COPY</td>
<td align="right"></td>
<td align="right">103,053,055</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__POP_FRAME</td>
<td align="right"></td>
<td align="right">101,908,653</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__CHECK_VALIDITY_AND_SET_IP</td>
<td align="right"></td>
<td align="right">100,532,258</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__CONTAINS_OP_DICT</td>
<td align="right"></td>
<td align="right">99,465,275</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__BINARY_SUBSCR_DICT</td>
<td align="right"></td>
<td align="right">97,832,702</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__BINARY_SLICE</td>
<td align="right"></td>
<td align="right">97,248,371</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__STORE_FAST_3</td>
<td align="right"></td>
<td align="right">96,122,560</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__CALL_INTRINSIC_1</td>
<td align="right"></td>
<td align="right">96,027,595</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__LIST_EXTEND</td>
<td align="right"></td>
<td align="right">95,931,675</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__STORE_FAST_6</td>
<td align="right"></td>
<td align="right">91,651,138</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__ITER_CHECK_LIST</td>
<td align="right"></td>
<td align="right">91,186,793</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__STORE_FAST_1</td>
<td align="right"></td>
<td align="right">88,092,722</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__GUARD_BOTH_FLOAT</td>
<td align="right"></td>
<td align="right">86,145,700</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__IS_OP</td>
<td align="right"></td>
<td align="right">85,713,480</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__STORE_FAST_7</td>
<td align="right"></td>
<td align="right">82,996,059</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__INIT_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right"></td>
<td align="right">81,811,216</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__CHECK_FUNCTION</td>
<td align="right"></td>
<td align="right">80,801,744</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__BINARY_OP_ADD_FLOAT</td>
<td align="right"></td>
<td align="right">79,478,200</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__UNPACK_SEQUENCE_LIST</td>
<td align="right"></td>
<td align="right">77,263,200</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__GET_ITER</td>
<td align="right"></td>
<td align="right">77,063,652</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__CHECK_ATTR_METHOD_LAZY_DICT</td>
<td align="right"></td>
<td align="right">75,868,906</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right"></td>
<td align="right">75,868,906</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__LOAD_CONST_INLINE_BORROW_WITH_NULL</td>
<td align="right"></td>
<td align="right">75,200,651</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right"></td>
<td align="right">73,768,240</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__UNPACK_SEQUENCE_TUPLE</td>
<td align="right"></td>
<td align="right">72,035,609</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__CONTAINS_OP_SET</td>
<td align="right"></td>
<td align="right">71,044,251</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__CALL_BUILTIN_O</td>
<td align="right"></td>
<td align="right">69,521,789</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__GUARD_TOS_INT</td>
<td align="right"></td>
<td align="right">69,513,636</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__CALL_STR_1</td>
<td align="right"></td>
<td align="right">64,091,234</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__CHECK_ATTR_WITH_HINT</td>
<td align="right"></td>
<td align="right">63,822,915</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__COMPARE_OP_FLOAT</td>
<td align="right"></td>
<td align="right">63,795,141</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__LOAD_ATTR_WITH_HINT</td>
<td align="right"></td>
<td align="right">63,712,174</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__GUARD_DORV_NO_DICT</td>
<td align="right"></td>
<td align="right">62,316,084</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__CONTAINS_OP_DICT</td>
<td align="right"></td>
<td align="right">62,125,960</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right"></td>
<td align="right">61,498,800</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__STORE_FAST_6</td>
<td align="right"></td>
<td align="right">61,428,206</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__UNARY_NOT</td>
<td align="right"></td>
<td align="right">61,361,666</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__INIT_CALL_PY_EXACT_ARGS_3</td>
<td align="right"></td>
<td align="right">61,345,104</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__STORE_ATTR_INSTANCE_VALUE</td>
<td align="right"></td>
<td align="right">61,128,884</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__STORE_SUBSCR_LIST_INT</td>
<td align="right"></td>
<td align="right">60,554,740</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__CHECK_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right"></td>
<td align="right">59,407,419</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__STORE_FAST_7</td>
<td align="right"></td>
<td align="right">59,182,258</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__BUILD_TUPLE</td>
<td align="right"></td>
<td align="right">53,739,908</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__CONTAINS_OP</td>
<td align="right"></td>
<td align="right">53,201,201</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__CONTAINS_OP</td>
<td align="right"></td>
<td align="right">52,187,932</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__ITER_CHECK_TUPLE</td>
<td align="right"></td>
<td align="right">50,406,539</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__COPY_FREE_VARS</td>
<td align="right"></td>
<td align="right">49,404,263</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__STORE_FAST_2</td>
<td align="right"></td>
<td align="right">49,295,323</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__MAKE_FUNCTION</td>
<td align="right"></td>
<td align="right">48,974,528</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__CALL_BUILTIN_CLASS</td>
<td align="right"></td>
<td align="right">48,937,354</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__STORE_FAST_4</td>
<td align="right"></td>
<td align="right">48,269,765</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__BUILD_LIST</td>
<td align="right"></td>
<td align="right">47,922,037</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__GUARD_TOS_FLOAT</td>
<td align="right"></td>
<td align="right">47,674,800</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__STORE_ATTR</td>
<td align="right"></td>
<td align="right">47,142,588</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__SET_FUNCTION_ATTRIBUTE</td>
<td align="right"></td>
<td align="right">47,055,140</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__BINARY_SUBSCR_TUPLE_INT</td>
<td align="right"></td>
<td align="right">45,710,962</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__STORE_FAST_5</td>
<td align="right"></td>
<td align="right">45,060,330</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__GUARD_DORV_NO_DICT</td>
<td align="right"></td>
<td align="right">44,257,813</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__STORE_ATTR_INSTANCE_VALUE</td>
<td align="right"></td>
<td align="right">44,257,813</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__COMPARE_OP</td>
<td align="right"></td>
<td align="right">42,724,722</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__STORE_SUBSCR</td>
<td align="right"></td>
<td align="right">42,389,660</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__TO_BOOL_LIST</td>
<td align="right"></td>
<td align="right">42,143,147</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__GUARD_IS_NONE_POP</td>
<td align="right"></td>
<td align="right">39,618,424</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__CALL_BUILTIN_O</td>
<td align="right"></td>
<td align="right">38,236,405</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__GUARD_GLOBALS_VERSION</td>
<td align="right"></td>
<td align="right">34,938,904</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__STORE_FAST_0</td>
<td align="right"></td>
<td align="right">34,466,820</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__GUARD_TOS_INT</td>
<td align="right"></td>
<td align="right">34,149,240</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__COMPARE_OP</td>
<td align="right"></td>
<td align="right">32,514,625</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__GUARD_BOTH_UNICODE</td>
<td align="right"></td>
<td align="right">32,260,435</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__REPLACE_WITH_TRUE</td>
<td align="right"></td>
<td align="right">31,859,576</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__TO_BOOL_NONE</td>
<td align="right"></td>
<td align="right">31,640,004</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__UNPACK_SEQUENCE_TUPLE</td>
<td align="right"></td>
<td align="right">31,004,320</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__LOAD_GLOBAL_MODULE</td>
<td align="right"></td>
<td align="right">28,413,652</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__BINARY_OP_MULTIPLY_INT</td>
<td align="right"></td>
<td align="right">26,655,886</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__ITER_CHECK_RANGE</td>
<td align="right"></td>
<td align="right">26,545,066</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__COMPARE_OP_INT</td>
<td align="right"></td>
<td align="right">26,271,788</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__TO_BOOL_NONE</td>
<td align="right"></td>
<td align="right">25,023,740</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__UNARY_NEGATIVE</td>
<td align="right"></td>
<td align="right">24,696,463</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__LOAD_ATTR_CLASS_0</td>
<td align="right"></td>
<td align="right">24,341,691</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__BINARY_OP_ADD_UNICODE</td>
<td align="right"></td>
<td align="right">23,582,967</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__BINARY_SLICE</td>
<td align="right"></td>
<td align="right">23,230,102</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__GET_ITER</td>
<td align="right"></td>
<td align="right">23,032,494</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right"></td>
<td align="right">21,565,202</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__CHECK_ATTR_METHOD_LAZY_DICT</td>
<td align="right"></td>
<td align="right">21,441,580</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right"></td>
<td align="right">21,441,580</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__LOAD_ATTR_WITH_HINT</td>
<td align="right"></td>
<td align="right">21,148,020</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__CHECK_ATTR_WITH_HINT</td>
<td align="right"></td>
<td align="right">21,148,020</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__STORE_FAST_0</td>
<td align="right"></td>
<td align="right">20,459,717</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__BINARY_OP_SUBTRACT_INT</td>
<td align="right"></td>
<td align="right">19,590,790</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__SWAP</td>
<td align="right"></td>
<td align="right">19,284,704</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__TO_BOOL_STR</td>
<td align="right"></td>
<td align="right">19,110,829</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__COMPARE_OP</td>
<td align="right"></td>
<td align="right">18,962,228</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right"></td>
<td align="right">18,824,427</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__LOAD_CONST_INLINE_BORROW_WITH_NULL</td>
<td align="right"></td>
<td align="right">18,261,888</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__CALL_METHOD_DESCRIPTOR_O</td>
<td align="right"></td>
<td align="right">17,866,257</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__BUILD_TUPLE</td>
<td align="right"></td>
<td align="right">17,537,352</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right"></td>
<td align="right">17,313,299</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__TO_BOOL_LIST</td>
<td align="right"></td>
<td align="right">17,299,193</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__GUARD_IS_NOT_NONE_POP</td>
<td align="right"></td>
<td align="right">17,040,606</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right"></td>
<td align="right">16,851,627</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__GUARD_GLOBALS_VERSION</td>
<td align="right"></td>
<td align="right">15,762,872</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__LOAD_GLOBAL_MODULE</td>
<td align="right"></td>
<td align="right">15,748,536</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__GUARD_IS_NOT_NONE_POP</td>
<td align="right"></td>
<td align="right">15,630,871</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__CHECK_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right"></td>
<td align="right">15,393,897</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__LOAD_FAST_AND_CLEAR</td>
<td align="right"></td>
<td align="right">14,883,112</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__CHECK_ATTR_CLASS</td>
<td align="right"></td>
<td align="right">14,552,573</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__MAP_ADD</td>
<td align="right"></td>
<td align="right">13,105,924</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__STORE_ATTR_SLOT</td>
<td align="right"></td>
<td align="right">13,008,755</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__BUILD_MAP</td>
<td align="right"></td>
<td align="right">12,801,989</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__UNARY_INVERT</td>
<td align="right"></td>
<td align="right">12,534,740</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__LOAD_CONST_INLINE_WITH_NULL</td>
<td align="right"></td>
<td align="right">12,164,047</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__BINARY_SUBSCR_DICT</td>
<td align="right"></td>
<td align="right">12,045,384</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__FOR_ITER_TIER_TWO</td>
<td align="right"></td>
<td align="right">12,003,576</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__SWAP</td>
<td align="right"></td>
<td align="right">11,980,090</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right"></td>
<td align="right">11,866,677</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__MAKE_FUNCTION</td>
<td align="right"></td>
<td align="right">11,671,376</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__BINARY_OP_MULTIPLY_INT</td>
<td align="right"></td>
<td align="right">11,632,200</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__CHECK_ATTR_CLASS</td>
<td align="right"></td>
<td align="right">11,330,720</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__STORE_SLICE</td>
<td align="right"></td>
<td align="right">11,326,060</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__GUARD_IS_FALSE_POP</td>
<td align="right"></td>
<td align="right">10,463,758</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__CALL_LEN</td>
<td align="right"></td>
<td align="right">9,990,815</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right"></td>
<td align="right">9,900,994</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__INIT_CALL_PY_EXACT_ARGS</td>
<td align="right"></td>
<td align="right">9,779,830</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__TO_BOOL_BOOL</td>
<td align="right"></td>
<td align="right">9,001,720</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__CALL_ISINSTANCE</td>
<td align="right"></td>
<td align="right">8,824,689</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right"></td>
<td align="right">8,722,098</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__GUARD_TOS_FLOAT</td>
<td align="right"></td>
<td align="right">8,103,420</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__IS_OP</td>
<td align="right"></td>
<td align="right">7,790,473</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__DICT_MERGE</td>
<td align="right"></td>
<td align="right">7,675,863</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__CHECK_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right"></td>
<td align="right">7,080,940</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__LOAD_GLOBAL_BUILTINS</td>
<td align="right"></td>
<td align="right">6,525,252</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__BINARY_SUBSCR_STR_INT</td>
<td align="right"></td>
<td align="right">6,489,560</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__COMPARE_OP_FLOAT</td>
<td align="right"></td>
<td align="right">6,276,540</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__LOAD_ATTR_MODULE</td>
<td align="right"></td>
<td align="right">6,263,976</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__LOAD_ATTR_INSTANCE_VALUE_1</td>
<td align="right"></td>
<td align="right">6,242,275</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__CHECK_ATTR_MODULE</td>
<td align="right"></td>
<td align="right">5,923,670</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__GUARD_IS_TRUE_POP</td>
<td align="right"></td>
<td align="right">5,851,586</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__CALL_BUILTIN_CLASS</td>
<td align="right"></td>
<td align="right">5,851,008</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__TO_BOOL_STR</td>
<td align="right"></td>
<td align="right">5,585,579</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__MAKE_CELL</td>
<td align="right"></td>
<td align="right">5,401,057</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__JUMP_TO_TOP</td>
<td align="right"></td>
<td align="right">5,152,450</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__POP_TOP</td>
<td align="right"></td>
<td align="right">4,950,550</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__BUILD_CONST_KEY_MAP</td>
<td align="right"></td>
<td align="right">4,860,160</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__LOAD_ATTR_SLOT_1</td>
<td align="right"></td>
<td align="right">4,781,440</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right"></td>
<td align="right">4,619,730</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__MAP_ADD</td>
<td align="right"></td>
<td align="right">4,581,340</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__GUARD_NOT_EXHAUSTED_LIST</td>
<td align="right"></td>
<td align="right">4,544,972</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__ITER_CHECK_LIST</td>
<td align="right"></td>
<td align="right">4,544,972</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__ITER_NEXT_LIST</td>
<td align="right"></td>
<td align="right">4,356,702</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__LIST_APPEND</td>
<td align="right"></td>
<td align="right">4,324,773</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__GUARD_BOTH_UNICODE</td>
<td align="right"></td>
<td align="right">4,227,353</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__LOAD_DEREF</td>
<td align="right"></td>
<td align="right">3,773,374</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__CALL_STR_1</td>
<td align="right"></td>
<td align="right">3,190,720</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__MAP_ADD</td>
<td align="right"></td>
<td align="right">2,917,640</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__STORE_DEREF</td>
<td align="right"></td>
<td align="right">2,912,949</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__CONTAINS_OP</td>
<td align="right"></td>
<td align="right">2,777,126</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__GUARD_TOS_FLOAT</td>
<td align="right"></td>
<td align="right">2,396,000</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right"></td>
<td align="right">2,341,890</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__CALL_BUILTIN_CLASS</td>
<td align="right"></td>
<td align="right">2,315,703</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__DEOPT</td>
<td align="right"></td>
<td align="right">2,138,275</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__BINARY_SUBSCR_STR_INT</td>
<td align="right"></td>
<td align="right">2,033,340</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__BUILD_MAP</td>
<td align="right"></td>
<td align="right">1,950,845</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__CALL_LEN</td>
<td align="right"></td>
<td align="right">1,763,960</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__STORE_ATTR</td>
<td align="right"></td>
<td align="right">1,488,145</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__DELETE_SUBSCR</td>
<td align="right"></td>
<td align="right">1,426,174</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right"></td>
<td align="right">1,425,250</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__SET_ADD</td>
<td align="right"></td>
<td align="right">1,368,270</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__LIST_APPEND</td>
<td align="right"></td>
<td align="right">1,342,434</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__BINARY_SUBSCR_LIST_INT</td>
<td align="right"></td>
<td align="right">1,325,880</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__STORE_ATTR</td>
<td align="right"></td>
<td align="right">1,293,200</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__STORE_GLOBAL</td>
<td align="right"></td>
<td align="right">1,260,560</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__GUARD_IS_NONE_POP</td>
<td align="right"></td>
<td align="right">1,247,286</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__POP_TOP_LOAD_CONST_INLINE_BORROW</td>
<td align="right"></td>
<td align="right">1,042,857</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__UNPACK_SEQUENCE</td>
<td align="right"></td>
<td align="right">1,036,857</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__LIST_EXTEND</td>
<td align="right"></td>
<td align="right">1,013,000</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__TO_BOOL_INT</td>
<td align="right"></td>
<td align="right">961,496</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__TO_BOOL</td>
<td align="right"></td>
<td align="right">931,480</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__FORMAT_SIMPLE</td>
<td align="right"></td>
<td align="right">927,388</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__LOAD_FAST_AND_CLEAR</td>
<td align="right"></td>
<td align="right">923,654</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__UNARY_NOT</td>
<td align="right"></td>
<td align="right">889,400</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__GUARD_IS_NONE_POP</td>
<td align="right"></td>
<td align="right">880,366</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__CALL_BUILTIN_FAST</td>
<td align="right"></td>
<td align="right">783,180</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__CONVERT_VALUE</td>
<td align="right"></td>
<td align="right">723,600</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__CONTAINS_OP_SET</td>
<td align="right"></td>
<td align="right">699,439</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__TO_BOOL_INT</td>
<td align="right"></td>
<td align="right">595,900</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__CALL_ISINSTANCE</td>
<td align="right"></td>
<td align="right">587,452</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__BUILD_STRING</td>
<td align="right"></td>
<td align="right">550,556</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__CALL_TUPLE_1</td>
<td align="right"></td>
<td align="right">540,720</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__UNPACK_SEQUENCE</td>
<td align="right"></td>
<td align="right">518,010</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__CALL_METHOD_DESCRIPTOR_O</td>
<td align="right"></td>
<td align="right">490,492</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__REPLACE_WITH_TRUE</td>
<td align="right"></td>
<td align="right">482,987</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__FORMAT_SIMPLE</td>
<td align="right"></td>
<td align="right">463,492</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right"></td>
<td align="right">436,217</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__ERROR_POP_N</td>
<td align="right"></td>
<td align="right">407,136</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__STORE_SUBSCR_DICT</td>
<td align="right"></td>
<td align="right">402,140</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__BUILD_MAP</td>
<td align="right"></td>
<td align="right">373,693</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__BUILD_LIST</td>
<td align="right"></td>
<td align="right">352,701</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__TO_BOOL_LIST</td>
<td align="right"></td>
<td align="right">343,762</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__CHECK_ATTR_MODULE</td>
<td align="right"></td>
<td align="right">340,306</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__UNPACK_SEQUENCE_LIST</td>
<td align="right"></td>
<td align="right">302,800</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__STORE_NAME</td>
<td align="right"></td>
<td align="right">277,040</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__STORE_NAME</td>
<td align="right"></td>
<td align="right">268,820</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__STORE_SUBSCR_DICT</td>
<td align="right"></td>
<td align="right">251,420</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__LOAD_FAST_CHECK</td>
<td align="right"></td>
<td align="right">249,051</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__CHECK_ATTR_MODULE</td>
<td align="right"></td>
<td align="right">206,960</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__LOAD_ATTR_MODULE</td>
<td align="right"></td>
<td align="right">206,960</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__POP_TOP_LOAD_CONST_INLINE_BORROW</td>
<td align="right"></td>
<td align="right">197,020</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__COMPARE_OP_STR</td>
<td align="right"></td>
<td align="right">185,600</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__UNARY_NEGATIVE</td>
<td align="right"></td>
<td align="right">180,900</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__GET_YIELD_FROM_ITER</td>
<td align="right"></td>
<td align="right">179,880</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__UNARY_NEGATIVE</td>
<td align="right"></td>
<td align="right">169,205</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__LOAD_ATTR_INSTANCE_VALUE_1</td>
<td align="right"></td>
<td align="right">122,521</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__TO_BOOL_STR</td>
<td align="right"></td>
<td align="right">122,024</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__GUARD_NOT_EXHAUSTED_TUPLE</td>
<td align="right"></td>
<td align="right">98,260</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__ITER_CHECK_TUPLE</td>
<td align="right"></td>
<td align="right">98,260</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__ITER_NEXT_TUPLE</td>
<td align="right"></td>
<td align="right">98,260</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__GUARD_GLOBALS_VERSION</td>
<td align="right"></td>
<td align="right">97,048</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__LOAD_SUPER_ATTR_METHOD</td>
<td align="right"></td>
<td align="right">95,777</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__ERROR_POP_N</td>
<td align="right"></td>
<td align="right">77,488</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__CHECK_ATTR_CLASS</td>
<td align="right"></td>
<td align="right">76,070</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__SET_ADD</td>
<td align="right"></td>
<td align="right">67,839</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__CONVERT_VALUE</td>
<td align="right"></td>
<td align="right">49,520</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__LOAD_GLOBAL_MODULE</td>
<td align="right"></td>
<td align="right">49,120</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__LOAD_GLOBAL_BUILTINS</td>
<td align="right"></td>
<td align="right">47,928</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__BUILD_STRING</td>
<td align="right"></td>
<td align="right">37,844</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__BINARY_SLICE</td>
<td align="right"></td>
<td align="right">32,160</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__CALL_TUPLE_1</td>
<td align="right"></td>
<td align="right">31,820</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__GUARD_BUILTINS_VERSION</td>
<td align="right"></td>
<td align="right">30,932</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__LOAD_ATTR_CLASS_0</td>
<td align="right"></td>
<td align="right">18,606</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__CONVERT_VALUE</td>
<td align="right"></td>
<td align="right">17,520</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__LOAD_GLOBAL_BUILTINS</td>
<td align="right"></td>
<td align="right">14,336</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__SET_ADD</td>
<td align="right"></td>
<td align="right">13,205</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__COMPARE_OP_FLOAT</td>
<td align="right"></td>
<td align="right">11,186</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__FORMAT_SIMPLE</td>
<td align="right"></td>
<td align="right">9,005</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__SET_FUNCTION_ATTRIBUTE</td>
<td align="right"></td>
<td align="right">7,704</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__LOAD_FAST_CHECK</td>
<td align="right"></td>
<td align="right">7,600</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__FOR_ITER_TIER_TWO</td>
<td align="right"></td>
<td align="right">7,040</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__LIST_EXTEND</td>
<td align="right"></td>
<td align="right">6,720</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__STORE_DEREF</td>
<td align="right"></td>
<td align="right">6,699</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__GUARD_BUILTINS_VERSION</td>
<td align="right"></td>
<td align="right">5,136</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__LOAD_ATTR_CLASS_1</td>
<td align="right"></td>
<td align="right">3,840</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__GUARD_BUILTINS_VERSION</td>
<td align="right"></td>
<td align="right">2,568</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__DELETE_SUBSCR</td>
<td align="right"></td>
<td align="right">1,966</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__UNPACK_SEQUENCE_LIST</td>
<td align="right"></td>
<td align="right">1,840</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__ERROR_POP_N</td>
<td align="right"></td>
<td align="right">1,520</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__BUILD_SLICE</td>
<td align="right"></td>
<td align="right">1,360</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R1__BUILD_CONST_KEY_MAP</td>
<td align="right"></td>
<td align="right">1,290</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R0__DICT_MERGE</td>
<td align="right"></td>
<td align="right">240</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">__R2__UNPACK_EX</td>
<td align="right"></td>
<td align="right">104</td>
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

Not included in comparative output.


</details>

### Unsupported opcodes

<details>
<summary> unsupported opcodes </summary>

<table>
<thead>
<tr>
<th align="left">Opcode</th>
<th align="right">Base Count</th>
<th align="right">Head Count</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">2,800</td>
<td align="right">31,400</td>
<td align="right">1,021.4%</td>
</tr>
<tr>
<td align="left">CALL_PY_WITH_DEFAULTS</td>
<td align="right">9,180</td>
<td align="right">5,806</td>
<td align="right">-36.8%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">1,360</td>
<td align="right">1,700</td>
<td align="right">25.0%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">34,271</td>
<td align="right">27,344</td>
<td align="right">-20.2%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">127,520</td>
<td align="right">146,203</td>
<td align="right">14.7%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">119,753</td>
<td align="right">135,055</td>
<td align="right">12.8%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_WITH_HINT</td>
<td align="right">180</td>
<td align="right">160</td>
<td align="right">-11.1%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_GETITEM</td>
<td align="right">2,540</td>
<td align="right">2,740</td>
<td align="right">7.9%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">266</td>
<td align="right">286</td>
<td align="right">7.5%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">26,201</td>
<td align="right">24,690</td>
<td align="right">-5.8%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">1,424</td>
<td align="right">1,484</td>
<td align="right">4.2%</td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right">226</td>
<td align="right">220</td>
<td align="right">-2.7%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">40,947</td>
<td align="right">40,507</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">6,691</td>
<td align="right">6,629</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">5,987</td>
<td align="right">6,007</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">56,483</td>
<td align="right">56,483</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">31,240</td>
<td align="right">31,240</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">603</td>
<td align="right">603</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BEFORE_WITH</td>
<td align="right">240</td>
<td align="right">240</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">60</td>
<td align="right">60</td>
<td align="right">0.0%</td>
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
<th align="right">Base Count</th>
<th align="right">Head Count</th>
<th align="right">Change</th>
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
<td align="right">0</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">
set bases
<details>
<summary>ⓘ</summary>

Setting the bases of a class, `cls.__bases__ = ...`
</details>
</td>
<td align="right">281</td>
<td align="right">281</td>
<td align="right">0.0%</td>
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
<td align="right">0</td>
<td align="right"></td>
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
<td align="right">0</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">
func modification
<details>
<summary>ⓘ</summary>

Modifying a function, e.g. `func.__defaults__ = ...`, etc.
</details>
</td>
<td align="right">461</td>
<td align="right">461</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">
watched dict modification
<details>
<summary>ⓘ</summary>

A watched dict has been modified
</details>
</td>
<td align="right">1,120</td>
<td align="right">1,120</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">
watched globals modification
<details>
<summary>ⓘ</summary>

A watched `globals()` dict has been modified
</details>
</td>
<td align="right">1,120</td>
<td align="right">1,120</td>
<td align="right">0.0%</td>
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
<th align="right">Base Count</th>
<th align="right">Head Count</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Number of data files</td>
<td align="right">2,000</td>
<td align="right">2,000</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

---
Stats gathered on: 2024-04-24
