# Results vs. 3.13.0b2

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: windows-amd64
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.12x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 207 ms                                                          | 232 ms: 1.12x slower                                                        |
| chameleon      | 4.80 ms                                                         | 5.08 ms: 1.06x slower                                                       |
| docutils       | 1.63 sec                                                        | 1.79 sec: 1.10x slower                                                      |
| html5lib       | 35.0 ms                                                         | 38.9 ms: 1.11x slower                                                       |
| tornado_http   | 81.8 ms                                                         | 94.8 ms: 1.16x slower                                                       |
| Geometric mean | (ref)                                                           | 1.11x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|---------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_io             | 588 ms                                                          | 609 ms: 1.04x slower                                                        |
| async_tree_cpu_io_mixed   | 389 ms                                                          | 405 ms: 1.04x slower                                                        |
| async_tree_io_tg          | 605 ms                                                          | 646 ms: 1.07x slower                                                        |
| async_tree_memoization    | 264 ms                                                          | 285 ms: 1.08x slower                                                        |
| async_tree_none           | 218 ms                                                          | 238 ms: 1.09x slower                                                        |
| async_tree_memoization_tg | 258 ms                                                          | 282 ms: 1.09x slower                                                        |
| async_tree_none_tg        | 202 ms                                                          | 227 ms: 1.12x slower                                                        |
| Geometric mean            | (ref)                                                           | 1.07x slower                                                                |

Benchmark hidden because not significant (1): async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 150 ms                                                          | 149 ms: 1.01x faster                                                        |
| float          | 49.7 ms                                                         | 54.5 ms: 1.10x slower                                                       |
| nbody          | 67.6 ms                                                         | 74.3 ms: 1.10x slower                                                       |
| Geometric mean | (ref)                                                           | 1.06x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_dna      | 119 ms                                                          | 118 ms: 1.01x faster                                                        |
| regex_v8       | 15.8 ms                                                         | 20.0 ms: 1.26x slower                                                       |
| regex_compile  | 78.0 ms                                                         | 106 ms: 1.36x slower                                                        |
| Geometric mean | (ref)                                                           | 1.14x slower                                                                |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_parse      | 90.9 ms                                                         | 93.7 ms: 1.03x slower                                                       |
| json_loads           | 14.2 us                                                         | 14.6 us: 1.03x slower                                                       |
| json_dumps           | 5.61 ms                                                         | 5.81 ms: 1.04x slower                                                       |
| pickle               | 7.11 us                                                         | 7.45 us: 1.05x slower                                                       |
| unpickle             | 8.40 us                                                         | 8.83 us: 1.05x slower                                                       |
| tomli_loads          | 1.35 sec                                                        | 1.43 sec: 1.06x slower                                                      |
| pickle_pure_python   | 175 us                                                          | 186 us: 1.06x slower                                                        |
| xml_etree_process    | 36.4 ms                                                         | 38.8 ms: 1.06x slower                                                       |
| xml_etree_generate   | 53.2 ms                                                         | 57.3 ms: 1.08x slower                                                       |
| xml_etree_iterparse  | 62.3 ms                                                         | 67.8 ms: 1.09x slower                                                       |
| unpickle_list        | 2.62 us                                                         | 2.85 us: 1.09x slower                                                       |
| pickle_dict          | 18.1 us                                                         | 20.2 us: 1.12x slower                                                       |
| unpickle_pure_python | 122 us                                                          | 159 us: 1.30x slower                                                        |
| Geometric mean       | (ref)                                                           | 1.07x slower                                                                |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 20.3 ms                                                         | 20.5 ms: 1.01x slower                                                       |
| python_startup_no_site | 16.2 ms                                                         | 16.7 ms: 1.03x slower                                                       |
| Geometric mean         | (ref)                                                           | 1.02x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 6.36 ms                                                         | 6.96 ms: 1.09x slower                                                       |
| django_template | 21.7 ms                                                         | 24.2 ms: 1.12x slower                                                       |
| genshi_xml      | 31.6 ms                                                         | 37.3 ms: 1.18x slower                                                       |
| genshi_text     | 14.4 ms                                                         | 17.8 ms: 1.24x slower                                                       |
| Geometric mean  | (ref)                                                           | 1.16x slower                                                                |

All benchmarks:
===============

| Benchmark                 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|---------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_dna                 | 119 ms                                                          | 118 ms: 1.01x faster                                                        |
| pidigits                  | 150 ms                                                          | 149 ms: 1.01x faster                                                        |
| python_startup            | 20.3 ms                                                         | 20.5 ms: 1.01x slower                                                       |
| coverage                  | 42.1 ms                                                         | 42.8 ms: 1.02x slower                                                       |
| gc_traversal              | 1.55 ms                                                         | 1.58 ms: 1.02x slower                                                       |
| richards_super            | 30.2 ms                                                         | 30.7 ms: 1.02x slower                                                       |
| richards                  | 26.7 ms                                                         | 27.3 ms: 1.02x slower                                                       |
| deepcopy_reduce           | 1.99 us                                                         | 2.04 us: 1.02x slower                                                       |
| coroutines                | 12.8 ms                                                         | 13.1 ms: 1.02x slower                                                       |
| python_startup_no_site    | 16.2 ms                                                         | 16.7 ms: 1.03x slower                                                       |
| sqlite_synth              | 1.60 us                                                         | 1.64 us: 1.03x slower                                                       |
| xml_etree_parse           | 90.9 ms                                                         | 93.7 ms: 1.03x slower                                                       |
| json_loads                | 14.2 us                                                         | 14.6 us: 1.03x slower                                                       |
| json_dumps                | 5.61 ms                                                         | 5.81 ms: 1.04x slower                                                       |
| async_tree_io             | 588 ms                                                          | 609 ms: 1.04x slower                                                        |
| async_tree_cpu_io_mixed   | 389 ms                                                          | 405 ms: 1.04x slower                                                        |
| bench_mp_pool             | 64.8 ms                                                         | 67.7 ms: 1.05x slower                                                       |
| create_gc_cycles          | 888 us                                                          | 929 us: 1.05x slower                                                        |
| pickle                    | 7.11 us                                                         | 7.45 us: 1.05x slower                                                       |
| unpickle                  | 8.40 us                                                         | 8.83 us: 1.05x slower                                                       |
| deepcopy                  | 220 us                                                          | 231 us: 1.05x slower                                                        |
| logging_format            | 6.22 us                                                         | 6.56 us: 1.05x slower                                                       |
| tomli_loads               | 1.35 sec                                                        | 1.43 sec: 1.06x slower                                                      |
| chameleon                 | 4.80 ms                                                         | 5.08 ms: 1.06x slower                                                       |
| pickle_pure_python        | 175 us                                                          | 186 us: 1.06x slower                                                        |
| telco                     | 4.67 ms                                                         | 4.95 ms: 1.06x slower                                                       |
| xml_etree_process         | 36.4 ms                                                         | 38.8 ms: 1.06x slower                                                       |
| async_tree_io_tg          | 605 ms                                                          | 646 ms: 1.07x slower                                                        |
| logging_simple            | 5.78 us                                                         | 6.20 us: 1.07x slower                                                       |
| deepcopy_memo             | 22.1 us                                                         | 23.8 us: 1.08x slower                                                       |
| xml_etree_generate        | 53.2 ms                                                         | 57.3 ms: 1.08x slower                                                       |
| async_tree_memoization    | 264 ms                                                          | 285 ms: 1.08x slower                                                        |
| pathlib                   | 75.9 ms                                                         | 82.3 ms: 1.08x slower                                                       |
| xml_etree_iterparse       | 62.3 ms                                                         | 67.8 ms: 1.09x slower                                                       |
| unpickle_list             | 2.62 us                                                         | 2.85 us: 1.09x slower                                                       |
| async_tree_none           | 218 ms                                                          | 238 ms: 1.09x slower                                                        |
| meteor_contest            | 69.9 ms                                                         | 76.3 ms: 1.09x slower                                                       |
| raytrace                  | 162 ms                                                          | 177 ms: 1.09x slower                                                        |
| logging_silent            | 52.9 ns                                                         | 57.8 ns: 1.09x slower                                                       |
| async_tree_memoization_tg | 258 ms                                                          | 282 ms: 1.09x slower                                                        |
| mako                      | 6.36 ms                                                         | 6.96 ms: 1.09x slower                                                       |
| float                     | 49.7 ms                                                         | 54.5 ms: 1.10x slower                                                       |
| crypto_pyaes              | 45.5 ms                                                         | 50.0 ms: 1.10x slower                                                       |
| nbody                     | 67.6 ms                                                         | 74.3 ms: 1.10x slower                                                       |
| docutils                  | 1.63 sec                                                        | 1.79 sec: 1.10x slower                                                      |
| fannkuch                  | 243 ms                                                          | 268 ms: 1.10x slower                                                        |
| pprint_safe_repr          | 474 ms                                                          | 523 ms: 1.10x slower                                                        |
| aiohttp                   | 889 us                                                          | 986 us: 1.11x slower                                                        |
| pylint                    | 205 ms                                                          | 227 ms: 1.11x slower                                                        |
| sqlglot_transpile         | 955 us                                                          | 1.06 ms: 1.11x slower                                                       |
| pprint_pformat            | 966 ms                                                          | 1.07 sec: 1.11x slower                                                      |
| html5lib                  | 35.0 ms                                                         | 38.9 ms: 1.11x slower                                                       |
| pickle_dict               | 18.1 us                                                         | 20.2 us: 1.12x slower                                                       |
| django_template           | 21.7 ms                                                         | 24.2 ms: 1.12x slower                                                       |
| 2to3                      | 207 ms                                                          | 232 ms: 1.12x slower                                                        |
| async_generators          | 223 ms                                                          | 251 ms: 1.12x slower                                                        |
| async_tree_none_tg        | 202 ms                                                          | 227 ms: 1.12x slower                                                        |
| sqlglot_normalize         | 173 ms                                                          | 195 ms: 1.13x slower                                                        |
| bench_thread_pool         | 768 us                                                          | 869 us: 1.13x slower                                                        |
| sympy_sum                 | 84.4 ms                                                         | 95.6 ms: 1.13x slower                                                       |
| sympy_integrate           | 12.2 ms                                                         | 14.0 ms: 1.15x slower                                                       |
| sympy_expand              | 271 ms                                                          | 311 ms: 1.15x slower                                                        |
| typing_runtime_protocols  | 101 us                                                          | 116 us: 1.15x slower                                                        |
| mdp                       | 1.31 sec                                                        | 1.51 sec: 1.15x slower                                                      |
| mypy2                     | 418 ms                                                          | 480 ms: 1.15x slower                                                        |
| chaos                     | 38.4 ms                                                         | 44.1 ms: 1.15x slower                                                       |
| sqlglot_optimize          | 32.7 ms                                                         | 37.7 ms: 1.15x slower                                                       |
| tornado_http              | 81.8 ms                                                         | 94.8 ms: 1.16x slower                                                       |
| pyflate                   | 279 ms                                                          | 324 ms: 1.16x slower                                                        |
| generators                | 19.6 ms                                                         | 22.7 ms: 1.16x slower                                                       |
| sympy_str                 | 159 ms                                                          | 185 ms: 1.17x slower                                                        |
| sqlglot_parse             | 748 us                                                          | 874 us: 1.17x slower                                                        |
| asyncio_tcp_ssl           | 1.48 sec                                                        | 1.73 sec: 1.17x slower                                                      |
| spectral_norm             | 63.7 ms                                                         | 74.6 ms: 1.17x slower                                                       |
| dulwich_log               | 38.0 ms                                                         | 44.9 ms: 1.18x slower                                                       |
| genshi_xml                | 31.6 ms                                                         | 37.3 ms: 1.18x slower                                                       |
| scimark_fft               | 171 ms                                                          | 202 ms: 1.18x slower                                                        |
| scimark_sparse_mat_mult   | 2.50 ms                                                         | 3.02 ms: 1.21x slower                                                       |
| scimark_sor               | 75.3 ms                                                         | 92.9 ms: 1.23x slower                                                       |
| genshi_text               | 14.4 ms                                                         | 17.8 ms: 1.24x slower                                                       |
| thrift                    | 8.11 ms                                                         | 10.1 ms: 1.24x slower                                                       |
| scimark_monte_carlo       | 39.1 ms                                                         | 48.7 ms: 1.25x slower                                                       |
| go                        | 82.1 ms                                                         | 102 ms: 1.25x slower                                                        |
| nqueens                   | 56.7 ms                                                         | 70.7 ms: 1.25x slower                                                       |
| regex_v8                  | 15.8 ms                                                         | 20.0 ms: 1.26x slower                                                       |
| comprehensions            | 10.4 us                                                         | 13.3 us: 1.28x slower                                                       |
| unpickle_pure_python      | 122 us                                                          | 159 us: 1.30x slower                                                        |
| deltablue                 | 1.88 ms                                                         | 2.52 ms: 1.34x slower                                                       |
| regex_compile             | 78.0 ms                                                         | 106 ms: 1.36x slower                                                        |
| hexiom                    | 3.72 ms                                                         | 5.29 ms: 1.42x slower                                                       |
| scimark_lu                | 56.6 ms                                                         | 80.8 ms: 1.43x slower                                                       |
| asyncio_tcp               | 471 ms                                                          | 676 ms: 1.44x slower                                                        |
| Geometric mean            | (ref)                                                           | 1.12x slower                                                                |

Benchmark hidden because not significant (5): json, regex_effbot, pycparser, pickle_list, async_tree_cpu_io_mixed_tg
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17.json: flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.10x
- 99% likely to have a slowdown of 1.09x

# Memory
- memory change: unknown