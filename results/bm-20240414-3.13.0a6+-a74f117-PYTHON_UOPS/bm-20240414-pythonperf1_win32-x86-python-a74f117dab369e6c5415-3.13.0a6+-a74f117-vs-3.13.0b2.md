# Results vs. 3.13.0b2

- fork: python
- ref: a74f117dab369e6c5415
- machine: windows-x86
- commit hash: a74f117
- commit date: 2024-04-14
- overall geometric mean: 1.05x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 233 ms                                                              | 245 ms: 1.05x slower                                                            |
| docutils       | 1.81 sec                                                            | 1.91 sec: 1.06x slower                                                          |
| html5lib       | 45.4 ms                                                             | 44.8 ms: 1.01x faster                                                           |
| tornado_http   | 94.3 ms                                                             | 97.7 ms: 1.04x slower                                                           |
| Geometric mean | (ref)                                                               | 1.02x slower                                                                    |

Benchmark hidden because not significant (1): chameleon

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_none, async_tree_memoization, async_tree_io_tg, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pidigits       | 199 ms                                                              | 197 ms: 1.01x faster                                                            |
| nbody          | 76.9 ms                                                             | 82.9 ms: 1.08x slower                                                           |
| float          | 52.4 ms                                                             | 61.1 ms: 1.17x slower                                                           |
| Geometric mean | (ref)                                                               | 1.08x slower                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_v8       | 15.7 ms                                                             | 16.2 ms: 1.03x slower                                                           |
| regex_dna      | 118 ms                                                              | 123 ms: 1.04x slower                                                            |
| regex_compile  | 99.9 ms                                                             | 125 ms: 1.25x slower                                                            |
| Geometric mean | (ref)                                                               | 1.08x slower                                                                    |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pickle_list          | 3.57 us                                                             | 3.29 us: 1.08x faster                                                           |
| unpickle_list        | 2.93 us                                                             | 2.79 us: 1.05x faster                                                           |
| pickle_dict          | 20.8 us                                                             | 19.9 us: 1.04x faster                                                           |
| pickle               | 8.07 us                                                             | 7.78 us: 1.04x faster                                                           |
| json_dumps           | 6.84 ms                                                             | 6.64 ms: 1.03x faster                                                           |
| json_loads           | 20.5 us                                                             | 20.1 us: 1.02x faster                                                           |
| tomli_loads          | 1.65 sec                                                            | 1.63 sec: 1.01x faster                                                          |
| pickle_pure_python   | 213 us                                                              | 211 us: 1.01x faster                                                            |
| unpickle             | 9.79 us                                                             | 9.84 us: 1.00x slower                                                           |
| xml_etree_process    | 42.1 ms                                                             | 42.8 ms: 1.02x slower                                                           |
| xml_etree_generate   | 59.6 ms                                                             | 61.0 ms: 1.02x slower                                                           |
| xml_etree_parse      | 104 ms                                                              | 108 ms: 1.04x slower                                                            |
| xml_etree_iterparse  | 64.2 ms                                                             | 67.9 ms: 1.06x slower                                                           |
| unpickle_pure_python | 147 us                                                              | 176 us: 1.19x slower                                                            |
| Geometric mean       | (ref)                                                               | 1.00x slower                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 22.2 ms                                                             | 22.6 ms: 1.02x slower                                                           |
| python_startup_no_site | 18.2 ms                                                             | 18.8 ms: 1.03x slower                                                           |
| Geometric mean         | (ref)                                                               | 1.02x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| genshi_text    | 20.1 ms                                                             | 19.6 ms: 1.03x faster                                                           |
| genshi_xml     | 44.3 ms                                                             | 45.0 ms: 1.02x slower                                                           |
| mako           | 6.94 ms                                                             | 7.60 ms: 1.10x slower                                                           |
| Geometric mean | (ref)                                                               | 1.03x slower                                                                    |

All benchmarks:
===============

| Benchmark                | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|--------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols | 136 us                                                              | 94.5 us: 1.43x faster                                                           |
| pickle_list              | 3.57 us                                                             | 3.29 us: 1.08x faster                                                           |
| deepcopy_reduce          | 2.59 us                                                             | 2.41 us: 1.08x faster                                                           |
| coroutines               | 15.5 ms                                                             | 14.5 ms: 1.07x faster                                                           |
| asyncio_tcp              | 662 ms                                                              | 628 ms: 1.05x faster                                                            |
| unpickle_list            | 2.93 us                                                             | 2.79 us: 1.05x faster                                                           |
| pickle_dict              | 20.8 us                                                             | 19.9 us: 1.04x faster                                                           |
| deepcopy                 | 280 us                                                              | 269 us: 1.04x faster                                                            |
| pickle                   | 8.07 us                                                             | 7.78 us: 1.04x faster                                                           |
| richards_super           | 35.5 ms                                                             | 34.4 ms: 1.03x faster                                                           |
| json_dumps               | 6.84 ms                                                             | 6.64 ms: 1.03x faster                                                           |
| create_gc_cycles         | 756 us                                                              | 735 us: 1.03x faster                                                            |
| genshi_text              | 20.1 ms                                                             | 19.6 ms: 1.03x faster                                                           |
| json_loads               | 20.5 us                                                             | 20.1 us: 1.02x faster                                                           |
| richards                 | 31.2 ms                                                             | 30.7 ms: 1.02x faster                                                           |
| html5lib                 | 45.4 ms                                                             | 44.8 ms: 1.01x faster                                                           |
| sqlite_synth             | 1.96 us                                                             | 1.94 us: 1.01x faster                                                           |
| tomli_loads              | 1.65 sec                                                            | 1.63 sec: 1.01x faster                                                          |
| pickle_pure_python       | 213 us                                                              | 211 us: 1.01x faster                                                            |
| pidigits                 | 199 ms                                                              | 197 ms: 1.01x faster                                                            |
| unpickle                 | 9.79 us                                                             | 9.84 us: 1.00x slower                                                           |
| json                     | 4.10 ms                                                             | 4.12 ms: 1.01x slower                                                           |
| sqlglot_transpile        | 1.19 ms                                                             | 1.20 ms: 1.01x slower                                                           |
| python_startup           | 22.2 ms                                                             | 22.6 ms: 1.02x slower                                                           |
| bench_thread_pool        | 985 us                                                              | 1.00 ms: 1.02x slower                                                           |
| xml_etree_process        | 42.1 ms                                                             | 42.8 ms: 1.02x slower                                                           |
| genshi_xml               | 44.3 ms                                                             | 45.0 ms: 1.02x slower                                                           |
| mdp                      | 1.60 sec                                                            | 1.63 sec: 1.02x slower                                                          |
| xml_etree_generate       | 59.6 ms                                                             | 61.0 ms: 1.02x slower                                                           |
| regex_v8                 | 15.7 ms                                                             | 16.2 ms: 1.03x slower                                                           |
| bench_mp_pool            | 69.4 ms                                                             | 71.6 ms: 1.03x slower                                                           |
| logging_format           | 8.13 us                                                             | 8.40 us: 1.03x slower                                                           |
| python_startup_no_site   | 18.2 ms                                                             | 18.8 ms: 1.03x slower                                                           |
| tornado_http             | 94.3 ms                                                             | 97.7 ms: 1.04x slower                                                           |
| logging_simple           | 7.47 us                                                             | 7.75 us: 1.04x slower                                                           |
| xml_etree_parse          | 104 ms                                                              | 108 ms: 1.04x slower                                                            |
| sympy_expand             | 375 ms                                                              | 390 ms: 1.04x slower                                                            |
| regex_dna                | 118 ms                                                              | 123 ms: 1.04x slower                                                            |
| logging_silent           | 57.9 ns                                                             | 60.5 ns: 1.05x slower                                                           |
| pprint_safe_repr         | 607 ms                                                              | 635 ms: 1.05x slower                                                            |
| 2to3                     | 233 ms                                                              | 245 ms: 1.05x slower                                                            |
| telco                    | 6.03 ms                                                             | 6.34 ms: 1.05x slower                                                           |
| pprint_pformat           | 1.24 sec                                                            | 1.31 sec: 1.05x slower                                                          |
| docutils                 | 1.81 sec                                                            | 1.91 sec: 1.06x slower                                                          |
| crypto_pyaes             | 55.8 ms                                                             | 59.0 ms: 1.06x slower                                                           |
| xml_etree_iterparse      | 64.2 ms                                                             | 67.9 ms: 1.06x slower                                                           |
| sympy_str                | 211 ms                                                              | 224 ms: 1.06x slower                                                            |
| pycparser                | 777 ms                                                              | 827 ms: 1.06x slower                                                            |
| meteor_contest           | 74.1 ms                                                             | 79.2 ms: 1.07x slower                                                           |
| sympy_sum                | 105 ms                                                              | 113 ms: 1.07x slower                                                            |
| nbody                    | 76.9 ms                                                             | 82.9 ms: 1.08x slower                                                           |
| generators               | 21.2 ms                                                             | 22.8 ms: 1.08x slower                                                           |
| deepcopy_memo            | 23.5 us                                                             | 25.6 us: 1.09x slower                                                           |
| sympy_integrate          | 14.6 ms                                                             | 16.0 ms: 1.09x slower                                                           |
| sqlglot_optimize         | 39.7 ms                                                             | 43.3 ms: 1.09x slower                                                           |
| sqlglot_normalize        | 206 ms                                                              | 225 ms: 1.09x slower                                                            |
| fannkuch                 | 270 ms                                                              | 295 ms: 1.09x slower                                                            |
| mako                     | 6.94 ms                                                             | 7.60 ms: 1.10x slower                                                           |
| chaos                    | 48.0 ms                                                             | 53.4 ms: 1.11x slower                                                           |
| scimark_fft              | 198 ms                                                              | 223 ms: 1.13x slower                                                            |
| scimark_sparse_mat_mult  | 2.87 ms                                                             | 3.23 ms: 1.13x slower                                                           |
| async_generators         | 266 ms                                                              | 301 ms: 1.13x slower                                                            |
| raytrace                 | 189 ms                                                              | 215 ms: 1.14x slower                                                            |
| nqueens                  | 68.7 ms                                                             | 78.2 ms: 1.14x slower                                                           |
| pyflate                  | 308 ms                                                              | 355 ms: 1.15x slower                                                            |
| thrift                   | 9.73 ms                                                             | 11.3 ms: 1.16x slower                                                           |
| scimark_sor              | 81.0 ms                                                             | 94.4 ms: 1.17x slower                                                           |
| float                    | 52.4 ms                                                             | 61.1 ms: 1.17x slower                                                           |
| go                       | 101 ms                                                              | 120 ms: 1.19x slower                                                            |
| scimark_monte_carlo      | 45.2 ms                                                             | 53.8 ms: 1.19x slower                                                           |
| unpickle_pure_python     | 147 us                                                              | 176 us: 1.19x slower                                                            |
| deltablue                | 2.23 ms                                                             | 2.67 ms: 1.19x slower                                                           |
| comprehensions           | 11.9 us                                                             | 14.5 us: 1.23x slower                                                           |
| regex_compile            | 99.9 ms                                                             | 125 ms: 1.25x slower                                                            |
| spectral_norm            | 68.0 ms                                                             | 86.7 ms: 1.28x slower                                                           |
| hexiom                   | 4.23 ms                                                             | 5.89 ms: 1.39x slower                                                           |
| scimark_lu               | 59.4 ms                                                             | 85.1 ms: 1.43x slower                                                           |
| coverage                 | 307 ms                                                              | 507 ms: 1.65x slower                                                            |
| Geometric mean           | (ref)                                                               | 1.05x slower                                                                    |

Benchmark hidden because not significant (15): async_tree_none, async_tree_memoization, pathlib, chameleon, async_tree_io_tg, gc_traversal, asyncio_tcp_ssl, sqlglot_parse, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg, regex_effbot, pylint, async_tree_none_tg
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17.json: django_template, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: unknown