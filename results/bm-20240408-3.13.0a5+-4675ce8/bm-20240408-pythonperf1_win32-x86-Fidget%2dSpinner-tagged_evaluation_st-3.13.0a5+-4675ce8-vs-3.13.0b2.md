# Results vs. 3.13.0b2

- fork: Fidget-Spinner
- ref: tagged_evaluation_st
- machine: windows-x86
- commit hash: 4675ce8
- commit date: 2024-04-08
- overall geometric mean: 1.02x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.00x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-pythonperf1_win32-x86-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------:|
| 2to3           | 233 ms                                                              | 230 ms: 1.01x faster                                                                      |
| chameleon      | 5.71 ms                                                             | 5.67 ms: 1.01x faster                                                                     |
| docutils       | 1.81 sec                                                            | 1.77 sec: 1.02x faster                                                                    |
| html5lib       | 45.4 ms                                                             | 42.4 ms: 1.07x faster                                                                     |
| tornado_http   | 94.3 ms                                                             | 91.6 ms: 1.03x faster                                                                     |
| Geometric mean | (ref)                                                               | 1.03x faster                                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-pythonperf1_win32-x86-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------:|
| async_tree_none            | 228 ms                                                              | 216 ms: 1.05x faster                                                                      |
| async_tree_memoization     | 275 ms                                                              | 262 ms: 1.05x faster                                                                      |
| async_tree_io              | 530 ms                                                              | 510 ms: 1.04x faster                                                                      |
| async_tree_memoization_tg  | 254 ms                                                              | 244 ms: 1.04x faster                                                                      |
| async_tree_cpu_io_mixed    | 471 ms                                                              | 457 ms: 1.03x faster                                                                      |
| async_tree_io_tg           | 529 ms                                                              | 514 ms: 1.03x faster                                                                      |
| async_tree_cpu_io_mixed_tg | 447 ms                                                              | 439 ms: 1.02x faster                                                                      |
| Geometric mean             | (ref)                                                               | 1.03x faster                                                                              |

Benchmark hidden because not significant (1): async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-pythonperf1_win32-x86-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------:|
| nbody          | 76.9 ms                                                             | 75.1 ms: 1.02x faster                                                                     |
| pidigits       | 199 ms                                                              | 196 ms: 1.01x faster                                                                      |
| float          | 52.4 ms                                                             | 52.7 ms: 1.01x slower                                                                     |
| Geometric mean | (ref)                                                               | 1.01x faster                                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-pythonperf1_win32-x86-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------:|
| regex_compile  | 99.9 ms                                                             | 96.3 ms: 1.04x faster                                                                     |
| regex_dna      | 118 ms                                                              | 117 ms: 1.01x faster                                                                      |
| regex_v8       | 15.7 ms                                                             | 16.1 ms: 1.02x slower                                                                     |
| Geometric mean | (ref)                                                               | 1.01x faster                                                                              |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-pythonperf1_win32-x86-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------:|
| pickle_list          | 3.57 us                                                             | 3.21 us: 1.11x faster                                                                     |
| json_dumps           | 6.84 ms                                                             | 6.55 ms: 1.04x faster                                                                     |
| tomli_loads          | 1.65 sec                                                            | 1.59 sec: 1.04x faster                                                                    |
| pickle_pure_python   | 213 us                                                              | 206 us: 1.03x faster                                                                      |
| pickle_dict          | 20.8 us                                                             | 20.1 us: 1.03x faster                                                                     |
| pickle               | 8.07 us                                                             | 7.88 us: 1.02x faster                                                                     |
| json_loads           | 20.5 us                                                             | 20.1 us: 1.02x faster                                                                     |
| unpickle_pure_python | 147 us                                                              | 145 us: 1.02x faster                                                                      |
| unpickle             | 9.79 us                                                             | 9.87 us: 1.01x slower                                                                     |
| xml_etree_generate   | 59.6 ms                                                             | 60.1 ms: 1.01x slower                                                                     |
| xml_etree_iterparse  | 64.2 ms                                                             | 65.1 ms: 1.01x slower                                                                     |
| xml_etree_parse      | 104 ms                                                              | 106 ms: 1.02x slower                                                                      |
| xml_etree_process    | 42.1 ms                                                             | 42.9 ms: 1.02x slower                                                                     |
| unpickle_list        | 2.93 us                                                             | 3.00 us: 1.02x slower                                                                     |
| Geometric mean       | (ref)                                                               | 1.02x faster                                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-pythonperf1_win32-x86-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|------------------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------:|
| python_startup_no_site | 18.2 ms                                                             | 19.8 ms: 1.09x slower                                                                     |
| Geometric mean         | (ref)                                                               | 1.04x slower                                                                              |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-pythonperf1_win32-x86-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------:|
| mako           | 6.94 ms                                                             | 6.76 ms: 1.03x faster                                                                     |
| genshi_text    | 20.1 ms                                                             | 19.7 ms: 1.02x faster                                                                     |
| genshi_xml     | 44.3 ms                                                             | 43.9 ms: 1.01x faster                                                                     |
| Geometric mean | (ref)                                                               | 1.02x faster                                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-pythonperf1_win32-x86-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 136 us                                                              | 92.8 us: 1.46x faster                                                                     |
| pickle_list                | 3.57 us                                                             | 3.21 us: 1.11x faster                                                                     |
| sqlglot_parse              | 964 us                                                              | 878 us: 1.10x faster                                                                      |
| pprint_pformat             | 1.24 sec                                                            | 1.14 sec: 1.09x faster                                                                    |
| pprint_safe_repr           | 607 ms                                                              | 558 ms: 1.09x faster                                                                      |
| coroutines                 | 15.5 ms                                                             | 14.2 ms: 1.09x faster                                                                     |
| sqlglot_transpile          | 1.19 ms                                                             | 1.10 ms: 1.08x faster                                                                     |
| sympy_expand               | 375 ms                                                              | 349 ms: 1.08x faster                                                                      |
| html5lib                   | 45.4 ms                                                             | 42.4 ms: 1.07x faster                                                                     |
| deepcopy_reduce            | 2.59 us                                                             | 2.43 us: 1.07x faster                                                                     |
| pylint                     | 217 ms                                                              | 204 ms: 1.06x faster                                                                      |
| richards_super             | 35.5 ms                                                             | 33.6 ms: 1.06x faster                                                                     |
| sympy_str                  | 211 ms                                                              | 200 ms: 1.06x faster                                                                      |
| richards                   | 31.2 ms                                                             | 29.7 ms: 1.05x faster                                                                     |
| async_tree_none            | 228 ms                                                              | 216 ms: 1.05x faster                                                                      |
| async_tree_memoization     | 275 ms                                                              | 262 ms: 1.05x faster                                                                      |
| json_dumps                 | 6.84 ms                                                             | 6.55 ms: 1.04x faster                                                                     |
| sympy_sum                  | 105 ms                                                              | 101 ms: 1.04x faster                                                                      |
| deltablue                  | 2.23 ms                                                             | 2.14 ms: 1.04x faster                                                                     |
| go                         | 101 ms                                                              | 96.6 ms: 1.04x faster                                                                     |
| async_tree_io              | 530 ms                                                              | 510 ms: 1.04x faster                                                                      |
| tomli_loads                | 1.65 sec                                                            | 1.59 sec: 1.04x faster                                                                    |
| async_tree_memoization_tg  | 254 ms                                                              | 244 ms: 1.04x faster                                                                      |
| regex_compile              | 99.9 ms                                                             | 96.3 ms: 1.04x faster                                                                     |
| sympy_integrate            | 14.6 ms                                                             | 14.2 ms: 1.04x faster                                                                     |
| crypto_pyaes               | 55.8 ms                                                             | 53.9 ms: 1.03x faster                                                                     |
| pickle_pure_python         | 213 us                                                              | 206 us: 1.03x faster                                                                      |
| pickle_dict                | 20.8 us                                                             | 20.1 us: 1.03x faster                                                                     |
| sqlite_synth               | 1.96 us                                                             | 1.90 us: 1.03x faster                                                                     |
| deepcopy_memo              | 23.5 us                                                             | 22.8 us: 1.03x faster                                                                     |
| async_tree_cpu_io_mixed    | 471 ms                                                              | 457 ms: 1.03x faster                                                                      |
| create_gc_cycles           | 756 us                                                              | 733 us: 1.03x faster                                                                      |
| async_tree_io_tg           | 529 ms                                                              | 514 ms: 1.03x faster                                                                      |
| deepcopy                   | 280 us                                                              | 272 us: 1.03x faster                                                                      |
| tornado_http               | 94.3 ms                                                             | 91.6 ms: 1.03x faster                                                                     |
| mako                       | 6.94 ms                                                             | 6.76 ms: 1.03x faster                                                                     |
| scimark_sor                | 81.0 ms                                                             | 79.0 ms: 1.03x faster                                                                     |
| chaos                      | 48.0 ms                                                             | 46.8 ms: 1.02x faster                                                                     |
| pickle                     | 8.07 us                                                             | 7.88 us: 1.02x faster                                                                     |
| nbody                      | 76.9 ms                                                             | 75.1 ms: 1.02x faster                                                                     |
| docutils                   | 1.81 sec                                                            | 1.77 sec: 1.02x faster                                                                    |
| bench_mp_pool              | 69.4 ms                                                             | 68.0 ms: 1.02x faster                                                                     |
| json_loads                 | 20.5 us                                                             | 20.1 us: 1.02x faster                                                                     |
| genshi_text                | 20.1 ms                                                             | 19.7 ms: 1.02x faster                                                                     |
| async_tree_cpu_io_mixed_tg | 447 ms                                                              | 439 ms: 1.02x faster                                                                      |
| unpickle_pure_python       | 147 us                                                              | 145 us: 1.02x faster                                                                      |
| json                       | 4.10 ms                                                             | 4.04 ms: 1.02x faster                                                                     |
| 2to3                       | 233 ms                                                              | 230 ms: 1.01x faster                                                                      |
| pycparser                  | 777 ms                                                              | 767 ms: 1.01x faster                                                                      |
| pidigits                   | 199 ms                                                              | 196 ms: 1.01x faster                                                                      |
| pyflate                    | 308 ms                                                              | 304 ms: 1.01x faster                                                                      |
| regex_dna                  | 118 ms                                                              | 117 ms: 1.01x faster                                                                      |
| genshi_xml                 | 44.3 ms                                                             | 43.9 ms: 1.01x faster                                                                     |
| chameleon                  | 5.71 ms                                                             | 5.67 ms: 1.01x faster                                                                     |
| logging_silent             | 57.9 ns                                                             | 57.5 ns: 1.01x faster                                                                     |
| asyncio_tcp_ssl            | 16.9 sec                                                            | 16.8 sec: 1.01x faster                                                                    |
| telco                      | 6.03 ms                                                             | 6.00 ms: 1.00x faster                                                                     |
| comprehensions             | 11.9 us                                                             | 11.8 us: 1.00x faster                                                                     |
| hexiom                     | 4.23 ms                                                             | 4.22 ms: 1.00x faster                                                                     |
| float                      | 52.4 ms                                                             | 52.7 ms: 1.01x slower                                                                     |
| scimark_monte_carlo        | 45.2 ms                                                             | 45.5 ms: 1.01x slower                                                                     |
| scimark_lu                 | 59.4 ms                                                             | 59.7 ms: 1.01x slower                                                                     |
| unpickle                   | 9.79 us                                                             | 9.87 us: 1.01x slower                                                                     |
| xml_etree_generate         | 59.6 ms                                                             | 60.1 ms: 1.01x slower                                                                     |
| logging_simple             | 7.47 us                                                             | 7.54 us: 1.01x slower                                                                     |
| mdp                        | 1.60 sec                                                            | 1.62 sec: 1.01x slower                                                                    |
| spectral_norm              | 68.0 ms                                                             | 68.7 ms: 1.01x slower                                                                     |
| xml_etree_iterparse        | 64.2 ms                                                             | 65.1 ms: 1.01x slower                                                                     |
| fannkuch                   | 270 ms                                                              | 275 ms: 1.02x slower                                                                      |
| xml_etree_parse            | 104 ms                                                              | 106 ms: 1.02x slower                                                                      |
| xml_etree_process          | 42.1 ms                                                             | 42.9 ms: 1.02x slower                                                                     |
| meteor_contest             | 74.1 ms                                                             | 75.5 ms: 1.02x slower                                                                     |
| regex_v8                   | 15.7 ms                                                             | 16.1 ms: 1.02x slower                                                                     |
| pathlib                    | 83.9 ms                                                             | 85.6 ms: 1.02x slower                                                                     |
| unpickle_list              | 2.93 us                                                             | 3.00 us: 1.02x slower                                                                     |
| scimark_fft                | 198 ms                                                              | 204 ms: 1.03x slower                                                                      |
| nqueens                    | 68.7 ms                                                             | 70.9 ms: 1.03x slower                                                                     |
| async_generators           | 266 ms                                                              | 278 ms: 1.05x slower                                                                      |
| scimark_sparse_mat_mult    | 2.87 ms                                                             | 3.03 ms: 1.06x slower                                                                     |
| generators                 | 21.2 ms                                                             | 22.5 ms: 1.06x slower                                                                     |
| python_startup_no_site     | 18.2 ms                                                             | 19.8 ms: 1.09x slower                                                                     |
| coverage                   | 307 ms                                                              | 507 ms: 1.65x slower                                                                      |
| Geometric mean             | (ref)                                                               | 1.02x faster                                                                              |

Benchmark hidden because not significant (11): async_tree_none_tg, asyncio_tcp, gc_traversal, bench_thread_pool, raytrace, regex_effbot, sqlglot_optimize, logging_format, python_startup, sqlglot_normalize, thrift
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17.json: django_template, flaskblogging

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: unknown