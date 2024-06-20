# Results vs. 3.13.0b2

- fork: python
- ref: a74f117dab369e6c5415
- machine: windows-x86
- commit hash: a74f117
- commit date: 2024-04-14
- overall geometric mean: 1.07x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 233 ms                                                              | 254 ms: 1.09x slower                                                            |
| chameleon      | 5.71 ms                                                             | 6.22 ms: 1.09x slower                                                           |
| docutils       | 1.81 sec                                                            | 1.91 sec: 1.06x slower                                                          |
| html5lib       | 45.4 ms                                                             | 45.0 ms: 1.01x faster                                                           |
| Geometric mean | (ref)                                                               | 1.04x slower                                                                    |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|---------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_io_tg          | 529 ms                                                              | 538 ms: 1.02x slower                                                            |
| async_tree_none           | 228 ms                                                              | 232 ms: 1.02x slower                                                            |
| async_tree_cpu_io_mixed   | 471 ms                                                              | 481 ms: 1.02x slower                                                            |
| async_tree_memoization    | 275 ms                                                              | 282 ms: 1.02x slower                                                            |
| async_tree_memoization_tg | 254 ms                                                              | 263 ms: 1.03x slower                                                            |
| async_tree_none_tg        | 203 ms                                                              | 211 ms: 1.04x slower                                                            |
| Geometric mean            | (ref)                                                               | 1.02x slower                                                                    |

Benchmark hidden because not significant (2): async_tree_io, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pidigits       | 199 ms                                                              | 197 ms: 1.01x faster                                                            |
| float          | 52.4 ms                                                             | 53.3 ms: 1.02x slower                                                           |
| nbody          | 76.9 ms                                                             | 97.3 ms: 1.27x slower                                                           |
| Geometric mean | (ref)                                                               | 1.08x slower                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_effbot   | 1.88 ms                                                             | 1.91 ms: 1.01x slower                                                           |
| regex_dna      | 118 ms                                                              | 122 ms: 1.04x slower                                                            |
| regex_v8       | 15.7 ms                                                             | 16.4 ms: 1.04x slower                                                           |
| regex_compile  | 99.9 ms                                                             | 110 ms: 1.10x slower                                                            |
| Geometric mean | (ref)                                                               | 1.05x slower                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pickle_list          | 3.57 us                                                             | 3.19 us: 1.12x faster                                                           |
| unpickle_list        | 2.93 us                                                             | 2.83 us: 1.04x faster                                                           |
| json_dumps           | 6.84 ms                                                             | 6.62 ms: 1.03x faster                                                           |
| pickle_dict          | 20.8 us                                                             | 20.1 us: 1.03x faster                                                           |
| json_loads           | 20.5 us                                                             | 20.1 us: 1.02x faster                                                           |
| pickle               | 8.07 us                                                             | 8.01 us: 1.01x faster                                                           |
| tomli_loads          | 1.65 sec                                                            | 1.66 sec: 1.01x slower                                                          |
| unpickle             | 9.79 us                                                             | 10.1 us: 1.03x slower                                                           |
| pickle_pure_python   | 213 us                                                              | 220 us: 1.03x slower                                                            |
| xml_etree_iterparse  | 64.2 ms                                                             | 66.9 ms: 1.04x slower                                                           |
| xml_etree_process    | 42.1 ms                                                             | 44.3 ms: 1.05x slower                                                           |
| xml_etree_generate   | 59.6 ms                                                             | 63.2 ms: 1.06x slower                                                           |
| xml_etree_parse      | 104 ms                                                              | 111 ms: 1.06x slower                                                            |
| unpickle_pure_python | 147 us                                                              | 166 us: 1.12x slower                                                            |
| Geometric mean       | (ref)                                                               | 1.01x slower                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 22.2 ms                                                             | 23.7 ms: 1.07x slower                                                           |
| python_startup_no_site | 18.2 ms                                                             | 20.1 ms: 1.10x slower                                                           |
| Geometric mean         | (ref)                                                               | 1.08x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako           | 6.94 ms                                                             | 7.03 ms: 1.01x slower                                                           |
| genshi_xml     | 44.3 ms                                                             | 48.4 ms: 1.09x slower                                                           |
| genshi_text    | 20.1 ms                                                             | 22.5 ms: 1.12x slower                                                           |
| Geometric mean | (ref)                                                               | 1.07x slower                                                                    |

All benchmarks:
===============

| Benchmark                 | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|---------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols  | 136 us                                                              | 93.8 us: 1.45x faster                                                           |
| pickle_list               | 3.57 us                                                             | 3.19 us: 1.12x faster                                                           |
| asyncio_tcp               | 662 ms                                                              | 626 ms: 1.06x faster                                                            |
| coroutines                | 15.5 ms                                                             | 14.9 ms: 1.04x faster                                                           |
| unpickle_list             | 2.93 us                                                             | 2.83 us: 1.04x faster                                                           |
| json_dumps                | 6.84 ms                                                             | 6.62 ms: 1.03x faster                                                           |
| pickle_dict               | 20.8 us                                                             | 20.1 us: 1.03x faster                                                           |
| create_gc_cycles          | 756 us                                                              | 733 us: 1.03x faster                                                            |
| json_loads                | 20.5 us                                                             | 20.1 us: 1.02x faster                                                           |
| sympy_expand              | 375 ms                                                              | 371 ms: 1.01x faster                                                            |
| pathlib                   | 83.9 ms                                                             | 83.1 ms: 1.01x faster                                                           |
| html5lib                  | 45.4 ms                                                             | 45.0 ms: 1.01x faster                                                           |
| pidigits                  | 199 ms                                                              | 197 ms: 1.01x faster                                                            |
| pickle                    | 8.07 us                                                             | 8.01 us: 1.01x faster                                                           |
| json                      | 4.10 ms                                                             | 4.13 ms: 1.01x slower                                                           |
| tomli_loads               | 1.65 sec                                                            | 1.66 sec: 1.01x slower                                                          |
| mako                      | 6.94 ms                                                             | 7.03 ms: 1.01x slower                                                           |
| regex_effbot              | 1.88 ms                                                             | 1.91 ms: 1.01x slower                                                           |
| async_tree_io_tg          | 529 ms                                                              | 538 ms: 1.02x slower                                                            |
| float                     | 52.4 ms                                                             | 53.3 ms: 1.02x slower                                                           |
| async_tree_none           | 228 ms                                                              | 232 ms: 1.02x slower                                                            |
| sympy_str                 | 211 ms                                                              | 215 ms: 1.02x slower                                                            |
| async_tree_cpu_io_mixed   | 471 ms                                                              | 481 ms: 1.02x slower                                                            |
| async_tree_memoization    | 275 ms                                                              | 282 ms: 1.02x slower                                                            |
| sqlglot_parse             | 964 us                                                              | 990 us: 1.03x slower                                                            |
| spectral_norm             | 68.0 ms                                                             | 70.0 ms: 1.03x slower                                                           |
| unpickle                  | 9.79 us                                                             | 10.1 us: 1.03x slower                                                           |
| bench_mp_pool             | 69.4 ms                                                             | 71.8 ms: 1.03x slower                                                           |
| async_tree_memoization_tg | 254 ms                                                              | 263 ms: 1.03x slower                                                            |
| pickle_pure_python        | 213 us                                                              | 220 us: 1.03x slower                                                            |
| sympy_sum                 | 105 ms                                                              | 109 ms: 1.04x slower                                                            |
| regex_dna                 | 118 ms                                                              | 122 ms: 1.04x slower                                                            |
| regex_v8                  | 15.7 ms                                                             | 16.4 ms: 1.04x slower                                                           |
| async_tree_none_tg        | 203 ms                                                              | 211 ms: 1.04x slower                                                            |
| xml_etree_iterparse       | 64.2 ms                                                             | 66.9 ms: 1.04x slower                                                           |
| logging_silent            | 57.9 ns                                                             | 60.3 ns: 1.04x slower                                                           |
| generators                | 21.2 ms                                                             | 22.1 ms: 1.04x slower                                                           |
| sqlglot_transpile         | 1.19 ms                                                             | 1.24 ms: 1.04x slower                                                           |
| deepcopy_reduce           | 2.59 us                                                             | 2.71 us: 1.05x slower                                                           |
| xml_etree_process         | 42.1 ms                                                             | 44.3 ms: 1.05x slower                                                           |
| logging_format            | 8.13 us                                                             | 8.58 us: 1.05x slower                                                           |
| docutils                  | 1.81 sec                                                            | 1.91 sec: 1.06x slower                                                          |
| xml_etree_generate        | 59.6 ms                                                             | 63.2 ms: 1.06x slower                                                           |
| xml_etree_parse           | 104 ms                                                              | 111 ms: 1.06x slower                                                            |
| telco                     | 6.03 ms                                                             | 6.42 ms: 1.06x slower                                                           |
| python_startup            | 22.2 ms                                                             | 23.7 ms: 1.07x slower                                                           |
| logging_simple            | 7.47 us                                                             | 7.98 us: 1.07x slower                                                           |
| richards_super            | 35.5 ms                                                             | 38.3 ms: 1.08x slower                                                           |
| richards                  | 31.2 ms                                                             | 33.8 ms: 1.08x slower                                                           |
| deepcopy_memo             | 23.5 us                                                             | 25.5 us: 1.08x slower                                                           |
| mdp                       | 1.60 sec                                                            | 1.74 sec: 1.08x slower                                                          |
| chameleon                 | 5.71 ms                                                             | 6.22 ms: 1.09x slower                                                           |
| 2to3                      | 233 ms                                                              | 254 ms: 1.09x slower                                                            |
| deepcopy                  | 280 us                                                              | 305 us: 1.09x slower                                                            |
| thrift                    | 9.73 ms                                                             | 10.6 ms: 1.09x slower                                                           |
| genshi_xml                | 44.3 ms                                                             | 48.4 ms: 1.09x slower                                                           |
| async_generators          | 266 ms                                                              | 291 ms: 1.09x slower                                                            |
| sympy_integrate           | 14.6 ms                                                             | 16.1 ms: 1.10x slower                                                           |
| python_startup_no_site    | 18.2 ms                                                             | 20.1 ms: 1.10x slower                                                           |
| regex_compile             | 99.9 ms                                                             | 110 ms: 1.10x slower                                                            |
| pycparser                 | 777 ms                                                              | 859 ms: 1.11x slower                                                            |
| sqlglot_normalize         | 206 ms                                                              | 228 ms: 1.11x slower                                                            |
| scimark_sparse_mat_mult   | 2.87 ms                                                             | 3.20 ms: 1.11x slower                                                           |
| genshi_text               | 20.1 ms                                                             | 22.5 ms: 1.12x slower                                                           |
| unpickle_pure_python      | 147 us                                                              | 166 us: 1.12x slower                                                            |
| meteor_contest            | 74.1 ms                                                             | 83.5 ms: 1.13x slower                                                           |
| sqlglot_optimize          | 39.7 ms                                                             | 44.9 ms: 1.13x slower                                                           |
| crypto_pyaes              | 55.8 ms                                                             | 63.5 ms: 1.14x slower                                                           |
| scimark_sor               | 81.0 ms                                                             | 93.7 ms: 1.16x slower                                                           |
| raytrace                  | 189 ms                                                              | 221 ms: 1.17x slower                                                            |
| pyflate                   | 308 ms                                                              | 361 ms: 1.17x slower                                                            |
| fannkuch                  | 270 ms                                                              | 319 ms: 1.18x slower                                                            |
| scimark_fft               | 198 ms                                                              | 236 ms: 1.19x slower                                                            |
| go                        | 101 ms                                                              | 120 ms: 1.19x slower                                                            |
| chaos                     | 48.0 ms                                                             | 57.3 ms: 1.20x slower                                                           |
| deltablue                 | 2.23 ms                                                             | 2.68 ms: 1.20x slower                                                           |
| pprint_safe_repr          | 607 ms                                                              | 736 ms: 1.21x slower                                                            |
| pprint_pformat            | 1.24 sec                                                            | 1.51 sec: 1.22x slower                                                          |
| nbody                     | 76.9 ms                                                             | 97.3 ms: 1.27x slower                                                           |
| comprehensions            | 11.9 us                                                             | 15.3 us: 1.29x slower                                                           |
| scimark_monte_carlo       | 45.2 ms                                                             | 59.4 ms: 1.32x slower                                                           |
| nqueens                   | 68.7 ms                                                             | 90.8 ms: 1.32x slower                                                           |
| hexiom                    | 4.23 ms                                                             | 5.98 ms: 1.41x slower                                                           |
| scimark_lu                | 59.4 ms                                                             | 84.2 ms: 1.42x slower                                                           |
| coverage                  | 307 ms                                                              | 504 ms: 1.64x slower                                                            |
| Geometric mean            | (ref)                                                               | 1.07x slower                                                                    |

Benchmark hidden because not significant (8): gc_traversal, asyncio_tcp_ssl, tornado_http, sqlite_synth, bench_thread_pool, async_tree_io, async_tree_cpu_io_mixed_tg, pylint
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17.json: django_template, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.04x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: unknown