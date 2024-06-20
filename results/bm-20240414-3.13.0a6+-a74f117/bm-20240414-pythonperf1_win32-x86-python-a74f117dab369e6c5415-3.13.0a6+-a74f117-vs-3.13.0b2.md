# Results vs. 3.13.0b2

- fork: python
- ref: a74f117dab369e6c5415
- machine: windows-x86
- commit hash: a74f117
- commit date: 2024-04-14
- overall geometric mean: 1.02x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 233 ms                                                              | 226 ms: 1.03x faster                                                            |
| chameleon      | 5.71 ms                                                             | 5.65 ms: 1.01x faster                                                           |
| docutils       | 1.81 sec                                                            | 1.79 sec: 1.01x faster                                                          |
| html5lib       | 45.4 ms                                                             | 41.7 ms: 1.09x faster                                                           |
| tornado_http   | 94.3 ms                                                             | 92.5 ms: 1.02x faster                                                           |
| Geometric mean | (ref)                                                               | 1.03x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|-------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_memoization  | 275 ms                                                              | 265 ms: 1.04x faster                                                            |
| async_tree_none         | 228 ms                                                              | 222 ms: 1.03x faster                                                            |
| async_tree_io           | 530 ms                                                              | 519 ms: 1.02x faster                                                            |
| async_tree_cpu_io_mixed | 471 ms                                                              | 464 ms: 1.02x faster                                                            |
| async_tree_io_tg        | 529 ms                                                              | 522 ms: 1.01x faster                                                            |
| Geometric mean          | (ref)                                                               | 1.02x faster                                                                    |

Benchmark hidden because not significant (3): async_tree_memoization_tg, async_tree_none_tg, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pidigits       | 199 ms                                                              | 197 ms: 1.01x faster                                                            |
| float          | 52.4 ms                                                             | 53.4 ms: 1.02x slower                                                           |
| nbody          | 76.9 ms                                                             | 78.4 ms: 1.02x slower                                                           |
| Geometric mean | (ref)                                                               | 1.01x slower                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 99.9 ms                                                             | 95.9 ms: 1.04x faster                                                           |
| regex_dna      | 118 ms                                                              | 117 ms: 1.01x faster                                                            |
| regex_v8       | 15.7 ms                                                             | 16.0 ms: 1.02x slower                                                           |
| Geometric mean | (ref)                                                               | 1.01x faster                                                                    |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pickle_list          | 3.57 us                                                             | 3.24 us: 1.10x faster                                                           |
| unpickle_pure_python | 147 us                                                              | 137 us: 1.08x faster                                                            |
| unpickle_list        | 2.93 us                                                             | 2.78 us: 1.05x faster                                                           |
| pickle_pure_python   | 213 us                                                              | 203 us: 1.05x faster                                                            |
| tomli_loads          | 1.65 sec                                                            | 1.58 sec: 1.04x faster                                                          |
| pickle_dict          | 20.8 us                                                             | 19.9 us: 1.04x faster                                                           |
| json_dumps           | 6.84 ms                                                             | 6.60 ms: 1.04x faster                                                           |
| json_loads           | 20.5 us                                                             | 20.1 us: 1.02x faster                                                           |
| pickle               | 8.07 us                                                             | 8.02 us: 1.01x faster                                                           |
| xml_etree_process    | 42.1 ms                                                             | 42.6 ms: 1.01x slower                                                           |
| xml_etree_iterparse  | 64.2 ms                                                             | 65.9 ms: 1.03x slower                                                           |
| unpickle             | 9.79 us                                                             | 10.1 us: 1.03x slower                                                           |
| xml_etree_parse      | 104 ms                                                              | 108 ms: 1.04x slower                                                            |
| xml_etree_generate   | 59.6 ms                                                             | 62.0 ms: 1.04x slower                                                           |
| Geometric mean       | (ref)                                                               | 1.02x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 22.2 ms                                                             | 21.9 ms: 1.02x faster                                                           |
| python_startup_no_site | 18.2 ms                                                             | 18.0 ms: 1.01x faster                                                           |
| Geometric mean         | (ref)                                                               | 1.01x faster                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| genshi_text    | 20.1 ms                                                             | 18.5 ms: 1.09x faster                                                           |
| genshi_xml     | 44.3 ms                                                             | 41.8 ms: 1.06x faster                                                           |
| mako           | 6.94 ms                                                             | 6.74 ms: 1.03x faster                                                           |
| Geometric mean | (ref)                                                               | 1.06x faster                                                                    |

All benchmarks:
===============

| Benchmark                | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|--------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols | 136 us                                                              | 93.0 us: 1.46x faster                                                           |
| sqlglot_parse            | 964 us                                                              | 862 us: 1.12x faster                                                            |
| pickle_list              | 3.57 us                                                             | 3.24 us: 1.10x faster                                                           |
| sqlglot_transpile        | 1.19 ms                                                             | 1.09 ms: 1.09x faster                                                           |
| pprint_pformat           | 1.24 sec                                                            | 1.14 sec: 1.09x faster                                                          |
| html5lib                 | 45.4 ms                                                             | 41.7 ms: 1.09x faster                                                           |
| pprint_safe_repr         | 607 ms                                                              | 558 ms: 1.09x faster                                                            |
| genshi_text              | 20.1 ms                                                             | 18.5 ms: 1.09x faster                                                           |
| coroutines               | 15.5 ms                                                             | 14.3 ms: 1.09x faster                                                           |
| richards_super           | 35.5 ms                                                             | 32.8 ms: 1.08x faster                                                           |
| unpickle_pure_python     | 147 us                                                              | 137 us: 1.08x faster                                                            |
| richards                 | 31.2 ms                                                             | 29.0 ms: 1.08x faster                                                           |
| sympy_expand             | 375 ms                                                              | 349 ms: 1.07x faster                                                            |
| sympy_str                | 211 ms                                                              | 199 ms: 1.06x faster                                                            |
| chaos                    | 48.0 ms                                                             | 45.3 ms: 1.06x faster                                                           |
| genshi_xml               | 44.3 ms                                                             | 41.8 ms: 1.06x faster                                                           |
| deltablue                | 2.23 ms                                                             | 2.12 ms: 1.06x faster                                                           |
| unpickle_list            | 2.93 us                                                             | 2.78 us: 1.05x faster                                                           |
| pylint                   | 217 ms                                                              | 206 ms: 1.05x faster                                                            |
| raytrace                 | 189 ms                                                              | 180 ms: 1.05x faster                                                            |
| pickle_pure_python       | 213 us                                                              | 203 us: 1.05x faster                                                            |
| create_gc_cycles         | 756 us                                                              | 723 us: 1.05x faster                                                            |
| deepcopy_reduce          | 2.59 us                                                             | 2.48 us: 1.05x faster                                                           |
| tomli_loads              | 1.65 sec                                                            | 1.58 sec: 1.04x faster                                                          |
| go                       | 101 ms                                                              | 96.6 ms: 1.04x faster                                                           |
| regex_compile            | 99.9 ms                                                             | 95.9 ms: 1.04x faster                                                           |
| pickle_dict              | 20.8 us                                                             | 19.9 us: 1.04x faster                                                           |
| scimark_sor              | 81.0 ms                                                             | 77.9 ms: 1.04x faster                                                           |
| async_tree_memoization   | 275 ms                                                              | 265 ms: 1.04x faster                                                            |
| deepcopy                 | 280 us                                                              | 269 us: 1.04x faster                                                            |
| sympy_sum                | 105 ms                                                              | 101 ms: 1.04x faster                                                            |
| json_dumps               | 6.84 ms                                                             | 6.60 ms: 1.04x faster                                                           |
| deepcopy_memo            | 23.5 us                                                             | 22.7 us: 1.04x faster                                                           |
| asyncio_tcp              | 662 ms                                                              | 639 ms: 1.04x faster                                                            |
| sqlglot_optimize         | 39.7 ms                                                             | 38.4 ms: 1.04x faster                                                           |
| sympy_integrate          | 14.6 ms                                                             | 14.2 ms: 1.03x faster                                                           |
| 2to3                     | 233 ms                                                              | 226 ms: 1.03x faster                                                            |
| sqlglot_normalize        | 206 ms                                                              | 200 ms: 1.03x faster                                                            |
| mako                     | 6.94 ms                                                             | 6.74 ms: 1.03x faster                                                           |
| async_tree_none          | 228 ms                                                              | 222 ms: 1.03x faster                                                            |
| sqlite_synth             | 1.96 us                                                             | 1.91 us: 1.02x faster                                                           |
| pycparser                | 777 ms                                                              | 760 ms: 1.02x faster                                                            |
| json_loads               | 20.5 us                                                             | 20.1 us: 1.02x faster                                                           |
| async_tree_io            | 530 ms                                                              | 519 ms: 1.02x faster                                                            |
| bench_mp_pool            | 69.4 ms                                                             | 67.9 ms: 1.02x faster                                                           |
| tornado_http             | 94.3 ms                                                             | 92.5 ms: 1.02x faster                                                           |
| mdp                      | 1.60 sec                                                            | 1.57 sec: 1.02x faster                                                          |
| telco                    | 6.03 ms                                                             | 5.93 ms: 1.02x faster                                                           |
| python_startup           | 22.2 ms                                                             | 21.9 ms: 1.02x faster                                                           |
| async_tree_cpu_io_mixed  | 471 ms                                                              | 464 ms: 1.02x faster                                                            |
| async_tree_io_tg         | 529 ms                                                              | 522 ms: 1.01x faster                                                            |
| fannkuch                 | 270 ms                                                              | 266 ms: 1.01x faster                                                            |
| json                     | 4.10 ms                                                             | 4.04 ms: 1.01x faster                                                           |
| crypto_pyaes             | 55.8 ms                                                             | 55.1 ms: 1.01x faster                                                           |
| logging_format           | 8.13 us                                                             | 8.04 us: 1.01x faster                                                           |
| chameleon                | 5.71 ms                                                             | 5.65 ms: 1.01x faster                                                           |
| regex_dna                | 118 ms                                                              | 117 ms: 1.01x faster                                                            |
| python_startup_no_site   | 18.2 ms                                                             | 18.0 ms: 1.01x faster                                                           |
| docutils                 | 1.81 sec                                                            | 1.79 sec: 1.01x faster                                                          |
| comprehensions           | 11.9 us                                                             | 11.7 us: 1.01x faster                                                           |
| hexiom                   | 4.23 ms                                                             | 4.19 ms: 1.01x faster                                                           |
| pidigits                 | 199 ms                                                              | 197 ms: 1.01x faster                                                            |
| gc_traversal             | 1.43 ms                                                             | 1.42 ms: 1.01x faster                                                           |
| pickle                   | 8.07 us                                                             | 8.02 us: 1.01x faster                                                           |
| pathlib                  | 83.9 ms                                                             | 83.4 ms: 1.01x faster                                                           |
| spectral_norm            | 68.0 ms                                                             | 68.5 ms: 1.01x slower                                                           |
| nqueens                  | 68.7 ms                                                             | 69.3 ms: 1.01x slower                                                           |
| xml_etree_process        | 42.1 ms                                                             | 42.6 ms: 1.01x slower                                                           |
| regex_v8                 | 15.7 ms                                                             | 16.0 ms: 1.02x slower                                                           |
| scimark_monte_carlo      | 45.2 ms                                                             | 46.0 ms: 1.02x slower                                                           |
| float                    | 52.4 ms                                                             | 53.4 ms: 1.02x slower                                                           |
| nbody                    | 76.9 ms                                                             | 78.4 ms: 1.02x slower                                                           |
| xml_etree_iterparse      | 64.2 ms                                                             | 65.9 ms: 1.03x slower                                                           |
| unpickle                 | 9.79 us                                                             | 10.1 us: 1.03x slower                                                           |
| meteor_contest           | 74.1 ms                                                             | 76.7 ms: 1.03x slower                                                           |
| xml_etree_parse          | 104 ms                                                              | 108 ms: 1.04x slower                                                            |
| xml_etree_generate       | 59.6 ms                                                             | 62.0 ms: 1.04x slower                                                           |
| scimark_lu               | 59.4 ms                                                             | 61.9 ms: 1.04x slower                                                           |
| generators               | 21.2 ms                                                             | 22.2 ms: 1.05x slower                                                           |
| scimark_fft              | 198 ms                                                              | 211 ms: 1.07x slower                                                            |
| logging_silent           | 57.9 ns                                                             | 61.7 ns: 1.07x slower                                                           |
| scimark_sparse_mat_mult  | 2.87 ms                                                             | 3.07 ms: 1.07x slower                                                           |
| async_generators         | 266 ms                                                              | 287 ms: 1.08x slower                                                            |
| coverage                 | 307 ms                                                              | 503 ms: 1.64x slower                                                            |
| Geometric mean           | (ref)                                                               | 1.02x faster                                                                    |

Benchmark hidden because not significant (9): async_tree_memoization_tg, asyncio_tcp_ssl, regex_effbot, thrift, bench_thread_pool, logging_simple, async_tree_none_tg, async_tree_cpu_io_mixed_tg, pyflate
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17.json: django_template, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: unknown