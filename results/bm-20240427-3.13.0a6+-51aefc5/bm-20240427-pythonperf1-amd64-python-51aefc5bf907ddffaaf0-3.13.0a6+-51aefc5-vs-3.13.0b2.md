# Results vs. 3.13.0b2

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: windows-amd64
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.04x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 207 ms                                                          | 214 ms: 1.04x slower                                                        |
| docutils       | 1.63 sec                                                        | 1.67 sec: 1.02x slower                                                      |
| html5lib       | 35.0 ms                                                         | 36.5 ms: 1.04x slower                                                       |
| tornado_http   | 81.8 ms                                                         | 92.1 ms: 1.13x slower                                                       |
| Geometric mean | (ref)                                                           | 1.04x slower                                                                |

Benchmark hidden because not significant (1): chameleon

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|---------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed   | 389 ms                                                          | 398 ms: 1.02x slower                                                        |
| async_tree_io             | 588 ms                                                          | 612 ms: 1.04x slower                                                        |
| async_tree_io_tg          | 605 ms                                                          | 631 ms: 1.04x slower                                                        |
| async_tree_memoization    | 264 ms                                                          | 278 ms: 1.05x slower                                                        |
| async_tree_none           | 218 ms                                                          | 231 ms: 1.06x slower                                                        |
| async_tree_memoization_tg | 258 ms                                                          | 274 ms: 1.06x slower                                                        |
| async_tree_none_tg        | 202 ms                                                          | 224 ms: 1.11x slower                                                        |
| Geometric mean            | (ref)                                                           | 1.05x slower                                                                |

Benchmark hidden because not significant (1): async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 150 ms                                                          | 148 ms: 1.01x faster                                                        |
| float          | 49.7 ms                                                         | 51.6 ms: 1.04x slower                                                       |
| nbody          | 67.6 ms                                                         | 70.9 ms: 1.05x slower                                                       |
| Geometric mean | (ref)                                                           | 1.02x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.58 ms                                                         | 1.62 ms: 1.03x slower                                                       |
| regex_compile  | 78.0 ms                                                         | 80.0 ms: 1.03x slower                                                       |
| regex_dna      | 119 ms                                                          | 125 ms: 1.06x slower                                                        |
| Geometric mean | (ref)                                                           | 1.02x slower                                                                |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pickle_pure_python   | 175 us                                                          | 180 us: 1.02x slower                                                        |
| json_dumps           | 5.61 ms                                                         | 5.76 ms: 1.03x slower                                                       |
| xml_etree_iterparse  | 62.3 ms                                                         | 64.3 ms: 1.03x slower                                                       |
| xml_etree_process    | 36.4 ms                                                         | 37.8 ms: 1.04x slower                                                       |
| pickle               | 7.11 us                                                         | 7.37 us: 1.04x slower                                                       |
| xml_etree_generate   | 53.2 ms                                                         | 55.2 ms: 1.04x slower                                                       |
| unpickle_list        | 2.62 us                                                         | 2.77 us: 1.06x slower                                                       |
| tomli_loads          | 1.35 sec                                                        | 1.43 sec: 1.06x slower                                                      |
| unpickle_pure_python | 122 us                                                          | 130 us: 1.06x slower                                                        |
| pickle_dict          | 18.1 us                                                         | 19.8 us: 1.09x slower                                                       |
| Geometric mean       | (ref)                                                           | 1.04x slower                                                                |

Benchmark hidden because not significant (4): json_loads, xml_etree_parse, unpickle, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 20.3 ms                                                         | 21.0 ms: 1.03x slower                                                       |
| python_startup_no_site | 16.2 ms                                                         | 17.3 ms: 1.07x slower                                                       |
| Geometric mean         | (ref)                                                           | 1.05x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_xml      | 31.6 ms                                                         | 33.4 ms: 1.06x slower                                                       |
| django_template | 21.7 ms                                                         | 23.0 ms: 1.06x slower                                                       |
| genshi_text     | 14.4 ms                                                         | 16.0 ms: 1.12x slower                                                       |
| Geometric mean  | (ref)                                                           | 1.06x slower                                                                |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|---------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| spectral_norm             | 63.7 ms                                                         | 61.4 ms: 1.04x faster                                                       |
| pidigits                  | 150 ms                                                          | 148 ms: 1.01x faster                                                        |
| logging_silent            | 52.9 ns                                                         | 53.2 ns: 1.01x slower                                                       |
| sympy_sum                 | 84.4 ms                                                         | 85.5 ms: 1.01x slower                                                       |
| scimark_lu                | 56.6 ms                                                         | 57.4 ms: 1.01x slower                                                       |
| chaos                     | 38.4 ms                                                         | 39.0 ms: 1.02x slower                                                       |
| sqlite_synth              | 1.60 us                                                         | 1.63 us: 1.02x slower                                                       |
| deepcopy_reduce           | 1.99 us                                                         | 2.04 us: 1.02x slower                                                       |
| async_tree_cpu_io_mixed   | 389 ms                                                          | 398 ms: 1.02x slower                                                        |
| scimark_sparse_mat_mult   | 2.50 ms                                                         | 2.56 ms: 1.02x slower                                                       |
| raytrace                  | 162 ms                                                          | 166 ms: 1.02x slower                                                        |
| pickle_pure_python        | 175 us                                                          | 180 us: 1.02x slower                                                        |
| docutils                  | 1.63 sec                                                        | 1.67 sec: 1.02x slower                                                      |
| create_gc_cycles          | 888 us                                                          | 910 us: 1.02x slower                                                        |
| regex_effbot              | 1.58 ms                                                         | 1.62 ms: 1.03x slower                                                       |
| regex_compile             | 78.0 ms                                                         | 80.0 ms: 1.03x slower                                                       |
| coroutines                | 12.8 ms                                                         | 13.1 ms: 1.03x slower                                                       |
| json_dumps                | 5.61 ms                                                         | 5.76 ms: 1.03x slower                                                       |
| pprint_safe_repr          | 474 ms                                                          | 487 ms: 1.03x slower                                                        |
| mypy2                     | 418 ms                                                          | 429 ms: 1.03x slower                                                        |
| pprint_pformat            | 966 ms                                                          | 993 ms: 1.03x slower                                                        |
| sympy_integrate           | 12.2 ms                                                         | 12.6 ms: 1.03x slower                                                       |
| sqlglot_parse             | 748 us                                                          | 771 us: 1.03x slower                                                        |
| sympy_str                 | 159 ms                                                          | 164 ms: 1.03x slower                                                        |
| sympy_expand              | 271 ms                                                          | 279 ms: 1.03x slower                                                        |
| xml_etree_iterparse       | 62.3 ms                                                         | 64.3 ms: 1.03x slower                                                       |
| richards                  | 26.7 ms                                                         | 27.6 ms: 1.03x slower                                                       |
| scimark_sor               | 75.3 ms                                                         | 77.8 ms: 1.03x slower                                                       |
| sqlglot_transpile         | 955 us                                                          | 987 us: 1.03x slower                                                        |
| python_startup            | 20.3 ms                                                         | 21.0 ms: 1.03x slower                                                       |
| deepcopy                  | 220 us                                                          | 227 us: 1.04x slower                                                        |
| xml_etree_process         | 36.4 ms                                                         | 37.8 ms: 1.04x slower                                                       |
| pickle                    | 7.11 us                                                         | 7.37 us: 1.04x slower                                                       |
| fannkuch                  | 243 ms                                                          | 252 ms: 1.04x slower                                                        |
| 2to3                      | 207 ms                                                          | 214 ms: 1.04x slower                                                        |
| xml_etree_generate        | 53.2 ms                                                         | 55.2 ms: 1.04x slower                                                       |
| richards_super            | 30.2 ms                                                         | 31.3 ms: 1.04x slower                                                       |
| float                     | 49.7 ms                                                         | 51.6 ms: 1.04x slower                                                       |
| meteor_contest            | 69.9 ms                                                         | 72.6 ms: 1.04x slower                                                       |
| html5lib                  | 35.0 ms                                                         | 36.5 ms: 1.04x slower                                                       |
| async_tree_io             | 588 ms                                                          | 612 ms: 1.04x slower                                                        |
| async_tree_io_tg          | 605 ms                                                          | 631 ms: 1.04x slower                                                        |
| telco                     | 4.67 ms                                                         | 4.89 ms: 1.05x slower                                                       |
| sqlglot_optimize          | 32.7 ms                                                         | 34.3 ms: 1.05x slower                                                       |
| nbody                     | 67.6 ms                                                         | 70.9 ms: 1.05x slower                                                       |
| logging_format            | 6.22 us                                                         | 6.53 us: 1.05x slower                                                       |
| sqlglot_normalize         | 173 ms                                                          | 181 ms: 1.05x slower                                                        |
| async_tree_memoization    | 264 ms                                                          | 278 ms: 1.05x slower                                                        |
| scimark_monte_carlo       | 39.1 ms                                                         | 41.2 ms: 1.05x slower                                                       |
| regex_dna                 | 119 ms                                                          | 125 ms: 1.06x slower                                                        |
| genshi_xml                | 31.6 ms                                                         | 33.4 ms: 1.06x slower                                                       |
| unpickle_list             | 2.62 us                                                         | 2.77 us: 1.06x slower                                                       |
| hexiom                    | 3.72 ms                                                         | 3.94 ms: 1.06x slower                                                       |
| mdp                       | 1.31 sec                                                        | 1.39 sec: 1.06x slower                                                      |
| async_tree_none           | 218 ms                                                          | 231 ms: 1.06x slower                                                        |
| tomli_loads               | 1.35 sec                                                        | 1.43 sec: 1.06x slower                                                      |
| dulwich_log               | 38.0 ms                                                         | 40.3 ms: 1.06x slower                                                       |
| pyflate                   | 279 ms                                                          | 295 ms: 1.06x slower                                                        |
| scimark_fft               | 171 ms                                                          | 181 ms: 1.06x slower                                                        |
| nqueens                   | 56.7 ms                                                         | 60.1 ms: 1.06x slower                                                       |
| async_tree_memoization_tg | 258 ms                                                          | 274 ms: 1.06x slower                                                        |
| django_template           | 21.7 ms                                                         | 23.0 ms: 1.06x slower                                                       |
| deltablue                 | 1.88 ms                                                         | 2.00 ms: 1.06x slower                                                       |
| unpickle_pure_python      | 122 us                                                          | 130 us: 1.06x slower                                                        |
| go                        | 82.1 ms                                                         | 87.5 ms: 1.07x slower                                                       |
| python_startup_no_site    | 16.2 ms                                                         | 17.3 ms: 1.07x slower                                                       |
| comprehensions            | 10.4 us                                                         | 11.1 us: 1.07x slower                                                       |
| logging_simple            | 5.78 us                                                         | 6.18 us: 1.07x slower                                                       |
| typing_runtime_protocols  | 101 us                                                          | 108 us: 1.07x slower                                                        |
| pathlib                   | 75.9 ms                                                         | 81.3 ms: 1.07x slower                                                       |
| async_generators          | 223 ms                                                          | 239 ms: 1.07x slower                                                        |
| coverage                  | 42.1 ms                                                         | 45.2 ms: 1.07x slower                                                       |
| aiohttp                   | 889 us                                                          | 955 us: 1.07x slower                                                        |
| bench_mp_pool             | 64.8 ms                                                         | 69.7 ms: 1.08x slower                                                       |
| bench_thread_pool         | 768 us                                                          | 836 us: 1.09x slower                                                        |
| pickle_dict               | 18.1 us                                                         | 19.8 us: 1.09x slower                                                       |
| generators                | 19.6 ms                                                         | 21.5 ms: 1.10x slower                                                       |
| async_tree_none_tg        | 202 ms                                                          | 224 ms: 1.11x slower                                                        |
| genshi_text               | 14.4 ms                                                         | 16.0 ms: 1.12x slower                                                       |
| tornado_http              | 81.8 ms                                                         | 92.1 ms: 1.13x slower                                                       |
| asyncio_tcp_ssl           | 1.48 sec                                                        | 1.84 sec: 1.24x slower                                                      |
| asyncio_tcp               | 471 ms                                                          | 664 ms: 1.41x slower                                                        |
| Geometric mean            | (ref)                                                           | 1.04x slower                                                                |

Benchmark hidden because not significant (15): json, regex_v8, deepcopy_memo, thrift, mako, chameleon, json_loads, crypto_pyaes, gc_traversal, xml_etree_parse, unpickle, async_tree_cpu_io_mixed_tg, pickle_list, pycparser, pylint
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17.json: flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: unknown