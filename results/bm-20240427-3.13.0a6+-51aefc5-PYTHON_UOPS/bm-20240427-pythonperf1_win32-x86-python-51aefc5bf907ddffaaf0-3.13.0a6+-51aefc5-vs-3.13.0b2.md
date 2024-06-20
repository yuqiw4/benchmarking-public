# Results vs. 3.13.0b2

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: windows-x86
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.06x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 233 ms                                                              | 250 ms: 1.07x slower                                                            |
| docutils       | 1.81 sec                                                            | 1.95 sec: 1.08x slower                                                          |
| html5lib       | 45.4 ms                                                             | 46.3 ms: 1.02x slower                                                           |
| tornado_http   | 94.3 ms                                                             | 107 ms: 1.14x slower                                                            |
| Geometric mean | (ref)                                                               | 1.06x slower                                                                    |

Benchmark hidden because not significant (1): chameleon

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|---------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_io_tg          | 529 ms                                                              | 537 ms: 1.01x slower                                                            |
| async_tree_memoization_tg | 254 ms                                                              | 260 ms: 1.02x slower                                                            |
| async_tree_cpu_io_mixed   | 471 ms                                                              | 483 ms: 1.02x slower                                                            |
| async_tree_none_tg        | 203 ms                                                              | 210 ms: 1.03x slower                                                            |
| Geometric mean            | (ref)                                                               | 1.02x slower                                                                    |

Benchmark hidden because not significant (4): async_tree_none, async_tree_io, async_tree_memoization, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pidigits       | 199 ms                                                              | 198 ms: 1.00x faster                                                            |
| nbody          | 76.9 ms                                                             | 79.1 ms: 1.03x slower                                                           |
| float          | 52.4 ms                                                             | 57.4 ms: 1.10x slower                                                           |
| Geometric mean | (ref)                                                               | 1.04x slower                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_dna      | 118 ms                                                              | 120 ms: 1.02x slower                                                            |
| regex_effbot   | 1.88 ms                                                             | 1.93 ms: 1.02x slower                                                           |
| regex_v8       | 15.7 ms                                                             | 16.3 ms: 1.03x slower                                                           |
| regex_compile  | 99.9 ms                                                             | 121 ms: 1.21x slower                                                            |
| Geometric mean | (ref)                                                               | 1.07x slower                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pickle_list          | 3.57 us                                                             | 3.32 us: 1.08x faster                                                           |
| pickle               | 8.07 us                                                             | 7.76 us: 1.04x faster                                                           |
| tomli_loads          | 1.65 sec                                                            | 1.60 sec: 1.03x faster                                                          |
| pickle_dict          | 20.8 us                                                             | 20.5 us: 1.01x faster                                                           |
| xml_etree_parse      | 104 ms                                                              | 104 ms: 1.01x faster                                                            |
| json_dumps           | 6.84 ms                                                             | 6.89 ms: 1.01x slower                                                           |
| unpickle             | 9.79 us                                                             | 9.90 us: 1.01x slower                                                           |
| xml_etree_generate   | 59.6 ms                                                             | 60.7 ms: 1.02x slower                                                           |
| xml_etree_process    | 42.1 ms                                                             | 43.2 ms: 1.03x slower                                                           |
| unpickle_list        | 2.93 us                                                             | 3.02 us: 1.03x slower                                                           |
| xml_etree_iterparse  | 64.2 ms                                                             | 67.0 ms: 1.04x slower                                                           |
| pickle_pure_python   | 213 us                                                              | 224 us: 1.05x slower                                                            |
| unpickle_pure_python | 147 us                                                              | 174 us: 1.18x slower                                                            |
| Geometric mean       | (ref)                                                               | 1.01x slower                                                                    |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 22.2 ms                                                             | 22.5 ms: 1.01x slower                                                           |
| python_startup_no_site | 18.2 ms                                                             | 18.8 ms: 1.03x slower                                                           |
| Geometric mean         | (ref)                                                               | 1.02x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| genshi_text     | 20.1 ms                                                             | 20.5 ms: 1.02x slower                                                           |
| django_template | 30.1 ms                                                             | 32.0 ms: 1.07x slower                                                           |
| genshi_xml      | 44.3 ms                                                             | 47.3 ms: 1.07x slower                                                           |
| mako            | 6.94 ms                                                             | 7.76 ms: 1.12x slower                                                           |
| Geometric mean  | (ref)                                                               | 1.07x slower                                                                    |

All benchmarks:
===============

| Benchmark                 | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|---------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pickle_list               | 3.57 us                                                             | 3.32 us: 1.08x faster                                                           |
| telco                     | 6.03 ms                                                             | 5.67 ms: 1.06x faster                                                           |
| pickle                    | 8.07 us                                                             | 7.76 us: 1.04x faster                                                           |
| tomli_loads               | 1.65 sec                                                            | 1.60 sec: 1.03x faster                                                          |
| richards_super            | 35.5 ms                                                             | 34.9 ms: 1.02x faster                                                           |
| pickle_dict               | 20.8 us                                                             | 20.5 us: 1.01x faster                                                           |
| xml_etree_parse           | 104 ms                                                              | 104 ms: 1.01x faster                                                            |
| pidigits                  | 199 ms                                                              | 198 ms: 1.00x faster                                                            |
| json_dumps                | 6.84 ms                                                             | 6.89 ms: 1.01x slower                                                           |
| sqlglot_parse             | 964 us                                                              | 972 us: 1.01x slower                                                            |
| python_startup            | 22.2 ms                                                             | 22.5 ms: 1.01x slower                                                           |
| unpickle                  | 9.79 us                                                             | 9.90 us: 1.01x slower                                                           |
| gc_traversal              | 1.43 ms                                                             | 1.45 ms: 1.01x slower                                                           |
| async_tree_io_tg          | 529 ms                                                              | 537 ms: 1.01x slower                                                            |
| sqlglot_transpile         | 1.19 ms                                                             | 1.21 ms: 1.01x slower                                                           |
| genshi_text               | 20.1 ms                                                             | 20.5 ms: 1.02x slower                                                           |
| coroutines                | 15.5 ms                                                             | 15.8 ms: 1.02x slower                                                           |
| xml_etree_generate        | 59.6 ms                                                             | 60.7 ms: 1.02x slower                                                           |
| html5lib                  | 45.4 ms                                                             | 46.3 ms: 1.02x slower                                                           |
| regex_dna                 | 118 ms                                                              | 120 ms: 1.02x slower                                                            |
| regex_effbot              | 1.88 ms                                                             | 1.93 ms: 1.02x slower                                                           |
| asyncio_tcp_ssl           | 16.9 sec                                                            | 17.3 sec: 1.02x slower                                                          |
| async_tree_memoization_tg | 254 ms                                                              | 260 ms: 1.02x slower                                                            |
| async_tree_cpu_io_mixed   | 471 ms                                                              | 483 ms: 1.02x slower                                                            |
| sqlite_synth              | 1.96 us                                                             | 2.01 us: 1.03x slower                                                           |
| xml_etree_process         | 42.1 ms                                                             | 43.2 ms: 1.03x slower                                                           |
| nbody                     | 76.9 ms                                                             | 79.1 ms: 1.03x slower                                                           |
| python_startup_no_site    | 18.2 ms                                                             | 18.8 ms: 1.03x slower                                                           |
| unpickle_list             | 2.93 us                                                             | 3.02 us: 1.03x slower                                                           |
| crypto_pyaes              | 55.8 ms                                                             | 57.6 ms: 1.03x slower                                                           |
| bench_mp_pool             | 69.4 ms                                                             | 71.7 ms: 1.03x slower                                                           |
| regex_v8                  | 15.7 ms                                                             | 16.3 ms: 1.03x slower                                                           |
| async_tree_none_tg        | 203 ms                                                              | 210 ms: 1.03x slower                                                            |
| bench_thread_pool         | 985 us                                                              | 1.02 ms: 1.04x slower                                                           |
| deepcopy                  | 280 us                                                              | 291 us: 1.04x slower                                                            |
| mdp                       | 1.60 sec                                                            | 1.67 sec: 1.04x slower                                                          |
| logging_format            | 8.13 us                                                             | 8.47 us: 1.04x slower                                                           |
| json                      | 4.10 ms                                                             | 4.27 ms: 1.04x slower                                                           |
| xml_etree_iterparse       | 64.2 ms                                                             | 67.0 ms: 1.04x slower                                                           |
| sympy_expand              | 375 ms                                                              | 393 ms: 1.05x slower                                                            |
| pickle_pure_python        | 213 us                                                              | 224 us: 1.05x slower                                                            |
| logging_silent            | 57.9 ns                                                             | 61.0 ns: 1.05x slower                                                           |
| sympy_str                 | 211 ms                                                              | 223 ms: 1.05x slower                                                            |
| logging_simple            | 7.47 us                                                             | 7.90 us: 1.06x slower                                                           |
| fannkuch                  | 270 ms                                                              | 286 ms: 1.06x slower                                                            |
| meteor_contest            | 74.1 ms                                                             | 78.9 ms: 1.07x slower                                                           |
| django_template           | 30.1 ms                                                             | 32.0 ms: 1.07x slower                                                           |
| sqlglot_normalize         | 206 ms                                                              | 220 ms: 1.07x slower                                                            |
| pathlib                   | 83.9 ms                                                             | 89.7 ms: 1.07x slower                                                           |
| genshi_xml                | 44.3 ms                                                             | 47.3 ms: 1.07x slower                                                           |
| 2to3                      | 233 ms                                                              | 250 ms: 1.07x slower                                                            |
| docutils                  | 1.81 sec                                                            | 1.95 sec: 1.08x slower                                                          |
| sympy_sum                 | 105 ms                                                              | 113 ms: 1.08x slower                                                            |
| sqlglot_optimize          | 39.7 ms                                                             | 43.0 ms: 1.08x slower                                                           |
| scimark_fft               | 198 ms                                                              | 214 ms: 1.08x slower                                                            |
| pycparser                 | 777 ms                                                              | 843 ms: 1.08x slower                                                            |
| pylint                    | 217 ms                                                              | 236 ms: 1.09x slower                                                            |
| typing_runtime_protocols  | 136 us                                                              | 147 us: 1.09x slower                                                            |
| sympy_integrate           | 14.6 ms                                                             | 16.0 ms: 1.09x slower                                                           |
| float                     | 52.4 ms                                                             | 57.4 ms: 1.10x slower                                                           |
| deepcopy_memo             | 23.5 us                                                             | 25.8 us: 1.10x slower                                                           |
| pyflate                   | 308 ms                                                              | 344 ms: 1.12x slower                                                            |
| async_generators          | 266 ms                                                              | 297 ms: 1.12x slower                                                            |
| mako                      | 6.94 ms                                                             | 7.76 ms: 1.12x slower                                                           |
| chaos                     | 48.0 ms                                                             | 53.8 ms: 1.12x slower                                                           |
| generators                | 21.2 ms                                                             | 23.8 ms: 1.12x slower                                                           |
| raytrace                  | 189 ms                                                              | 214 ms: 1.13x slower                                                            |
| tornado_http              | 94.3 ms                                                             | 107 ms: 1.14x slower                                                            |
| scimark_sparse_mat_mult   | 2.87 ms                                                             | 3.26 ms: 1.14x slower                                                           |
| nqueens                   | 68.7 ms                                                             | 78.4 ms: 1.14x slower                                                           |
| scimark_sor               | 81.0 ms                                                             | 93.2 ms: 1.15x slower                                                           |
| scimark_monte_carlo       | 45.2 ms                                                             | 52.4 ms: 1.16x slower                                                           |
| spectral_norm             | 68.0 ms                                                             | 79.5 ms: 1.17x slower                                                           |
| go                        | 101 ms                                                              | 118 ms: 1.17x slower                                                            |
| unpickle_pure_python      | 147 us                                                              | 174 us: 1.18x slower                                                            |
| thrift                    | 9.73 ms                                                             | 11.6 ms: 1.19x slower                                                           |
| comprehensions            | 11.9 us                                                             | 14.1 us: 1.19x slower                                                           |
| deltablue                 | 2.23 ms                                                             | 2.68 ms: 1.20x slower                                                           |
| regex_compile             | 99.9 ms                                                             | 121 ms: 1.21x slower                                                            |
| asyncio_tcp               | 662 ms                                                              | 807 ms: 1.22x slower                                                            |
| hexiom                    | 4.23 ms                                                             | 5.68 ms: 1.34x slower                                                           |
| coverage                  | 307 ms                                                              | 418 ms: 1.36x slower                                                            |
| scimark_lu                | 59.4 ms                                                             | 82.1 ms: 1.38x slower                                                           |
| Geometric mean            | (ref)                                                               | 1.06x slower                                                                    |

Benchmark hidden because not significant (11): create_gc_cycles, chameleon, json_loads, pprint_safe_repr, pprint_pformat, richards, async_tree_none, async_tree_io, deepcopy_reduce, async_tree_memoization, async_tree_cpu_io_mixed_tg
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17.json: flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: unknown