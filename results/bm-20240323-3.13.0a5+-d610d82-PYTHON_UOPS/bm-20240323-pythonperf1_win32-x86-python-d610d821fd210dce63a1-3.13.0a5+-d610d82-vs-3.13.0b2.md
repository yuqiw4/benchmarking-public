# Results vs. 3.13.0b2

- fork: python
- ref: d610d821fd210dce63a1
- machine: windows-x86
- commit hash: d610d82
- commit date: 2024-03-23
- overall geometric mean: 1.02x slower
- HPT reliability: 99.93%
- HPT 99th percentile: 1.00x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1_win32-x86-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 233 ms                                                              | 241 ms: 1.04x slower                                                            |
| chameleon      | 5.71 ms                                                             | 5.93 ms: 1.04x slower                                                           |
| docutils       | 1.81 sec                                                            | 1.88 sec: 1.03x slower                                                          |
| html5lib       | 45.4 ms                                                             | 47.0 ms: 1.03x slower                                                           |
| tornado_http   | 94.3 ms                                                             | 97.5 ms: 1.03x slower                                                           |
| Geometric mean | (ref)                                                               | 1.04x slower                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1_win32-x86-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_io_tg | 529 ms                                                              | 488 ms: 1.09x faster                                                            |
| async_tree_none  | 228 ms                                                              | 221 ms: 1.03x faster                                                            |
| Geometric mean   | (ref)                                                               | 1.02x faster                                                                    |

Benchmark hidden because not significant (6): async_tree_io, async_tree_memoization, async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1_win32-x86-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| nbody          | 76.9 ms                                                             | 76.4 ms: 1.01x faster                                                           |
| float          | 52.4 ms                                                             | 53.8 ms: 1.03x slower                                                           |
| Geometric mean | (ref)                                                               | 1.01x slower                                                                    |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1_win32-x86-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_v8       | 15.7 ms                                                             | 16.1 ms: 1.02x slower                                                           |
| regex_effbot   | 1.88 ms                                                             | 1.94 ms: 1.03x slower                                                           |
| regex_dna      | 118 ms                                                              | 126 ms: 1.07x slower                                                            |
| regex_compile  | 99.9 ms                                                             | 117 ms: 1.17x slower                                                            |
| Geometric mean | (ref)                                                               | 1.07x slower                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1_win32-x86-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pickle_list          | 3.57 us                                                             | 3.30 us: 1.08x faster                                                           |
| unpickle_list        | 2.93 us                                                             | 2.76 us: 1.06x faster                                                           |
| pickle               | 8.07 us                                                             | 7.73 us: 1.04x faster                                                           |
| pickle_dict          | 20.8 us                                                             | 19.9 us: 1.04x faster                                                           |
| tomli_loads          | 1.65 sec                                                            | 1.59 sec: 1.03x faster                                                          |
| xml_etree_process    | 42.1 ms                                                             | 41.4 ms: 1.02x faster                                                           |
| pickle_pure_python   | 213 us                                                              | 211 us: 1.01x faster                                                            |
| xml_etree_generate   | 59.6 ms                                                             | 59.1 ms: 1.01x faster                                                           |
| json_loads           | 20.5 us                                                             | 20.4 us: 1.01x faster                                                           |
| unpickle             | 9.79 us                                                             | 9.99 us: 1.02x slower                                                           |
| xml_etree_iterparse  | 64.2 ms                                                             | 65.7 ms: 1.02x slower                                                           |
| xml_etree_parse      | 104 ms                                                              | 107 ms: 1.03x slower                                                            |
| unpickle_pure_python | 147 us                                                              | 161 us: 1.10x slower                                                            |
| Geometric mean       | (ref)                                                               | 1.01x faster                                                                    |

Benchmark hidden because not significant (1): json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1_win32-x86-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 22.2 ms                                                             | 22.5 ms: 1.01x slower                                                           |
| python_startup_no_site | 18.2 ms                                                             | 20.2 ms: 1.11x slower                                                           |
| Geometric mean         | (ref)                                                               | 1.06x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1_win32-x86-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|-----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 6.94 ms                                                             | 6.85 ms: 1.01x faster                                                           |
| django_template | 30.1 ms                                                             | 30.3 ms: 1.01x slower                                                           |
| genshi_text     | 20.1 ms                                                             | 20.5 ms: 1.02x slower                                                           |
| genshi_xml      | 44.3 ms                                                             | 46.5 ms: 1.05x slower                                                           |
| Geometric mean  | (ref)                                                               | 1.02x slower                                                                    |

All benchmarks:
===============

| Benchmark                | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1_win32-x86-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|--------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols | 136 us                                                              | 89.5 us: 1.51x faster                                                           |
| create_gc_cycles         | 756 us                                                              | 652 us: 1.16x faster                                                            |
| async_tree_io_tg         | 529 ms                                                              | 488 ms: 1.09x faster                                                            |
| pickle_list              | 3.57 us                                                             | 3.30 us: 1.08x faster                                                           |
| richards_super           | 35.5 ms                                                             | 32.8 ms: 1.08x faster                                                           |
| asyncio_tcp              | 662 ms                                                              | 617 ms: 1.07x faster                                                            |
| richards                 | 31.2 ms                                                             | 29.2 ms: 1.07x faster                                                           |
| unpickle_list            | 2.93 us                                                             | 2.76 us: 1.06x faster                                                           |
| deepcopy_reduce          | 2.59 us                                                             | 2.44 us: 1.06x faster                                                           |
| pprint_safe_repr         | 607 ms                                                              | 574 ms: 1.06x faster                                                            |
| coroutines               | 15.5 ms                                                             | 14.7 ms: 1.05x faster                                                           |
| pprint_pformat           | 1.24 sec                                                            | 1.18 sec: 1.05x faster                                                          |
| pickle                   | 8.07 us                                                             | 7.73 us: 1.04x faster                                                           |
| pickle_dict              | 20.8 us                                                             | 19.9 us: 1.04x faster                                                           |
| gc_traversal             | 1.43 ms                                                             | 1.38 ms: 1.04x faster                                                           |
| crypto_pyaes             | 55.8 ms                                                             | 54.0 ms: 1.03x faster                                                           |
| fannkuch                 | 270 ms                                                              | 261 ms: 1.03x faster                                                            |
| tomli_loads              | 1.65 sec                                                            | 1.59 sec: 1.03x faster                                                          |
| async_tree_none          | 228 ms                                                              | 221 ms: 1.03x faster                                                            |
| sqlglot_parse            | 964 us                                                              | 942 us: 1.02x faster                                                            |
| xml_etree_process        | 42.1 ms                                                             | 41.4 ms: 1.02x faster                                                           |
| deepcopy                 | 280 us                                                              | 275 us: 1.02x faster                                                            |
| sqlite_synth             | 1.96 us                                                             | 1.93 us: 1.01x faster                                                           |
| mako                     | 6.94 ms                                                             | 6.85 ms: 1.01x faster                                                           |
| pickle_pure_python       | 213 us                                                              | 211 us: 1.01x faster                                                            |
| xml_etree_generate       | 59.6 ms                                                             | 59.1 ms: 1.01x faster                                                           |
| json_loads               | 20.5 us                                                             | 20.4 us: 1.01x faster                                                           |
| nbody                    | 76.9 ms                                                             | 76.4 ms: 1.01x faster                                                           |
| mdp                      | 1.60 sec                                                            | 1.61 sec: 1.00x slower                                                          |
| sympy_expand             | 375 ms                                                              | 377 ms: 1.00x slower                                                            |
| sqlglot_transpile        | 1.19 ms                                                             | 1.20 ms: 1.01x slower                                                           |
| django_template          | 30.1 ms                                                             | 30.3 ms: 1.01x slower                                                           |
| sympy_str                | 211 ms                                                              | 213 ms: 1.01x slower                                                            |
| python_startup           | 22.2 ms                                                             | 22.5 ms: 1.01x slower                                                           |
| json                     | 4.10 ms                                                             | 4.17 ms: 1.02x slower                                                           |
| genshi_text              | 20.1 ms                                                             | 20.5 ms: 1.02x slower                                                           |
| async_generators         | 266 ms                                                              | 270 ms: 1.02x slower                                                            |
| unpickle                 | 9.79 us                                                             | 9.99 us: 1.02x slower                                                           |
| xml_etree_iterparse      | 64.2 ms                                                             | 65.7 ms: 1.02x slower                                                           |
| regex_v8                 | 15.7 ms                                                             | 16.1 ms: 1.02x slower                                                           |
| pathlib                  | 83.9 ms                                                             | 86.0 ms: 1.03x slower                                                           |
| sympy_sum                | 105 ms                                                              | 108 ms: 1.03x slower                                                            |
| xml_etree_parse          | 104 ms                                                              | 107 ms: 1.03x slower                                                            |
| float                    | 52.4 ms                                                             | 53.8 ms: 1.03x slower                                                           |
| regex_effbot             | 1.88 ms                                                             | 1.94 ms: 1.03x slower                                                           |
| deltablue                | 2.23 ms                                                             | 2.30 ms: 1.03x slower                                                           |
| meteor_contest           | 74.1 ms                                                             | 76.5 ms: 1.03x slower                                                           |
| html5lib                 | 45.4 ms                                                             | 47.0 ms: 1.03x slower                                                           |
| tornado_http             | 94.3 ms                                                             | 97.5 ms: 1.03x slower                                                           |
| docutils                 | 1.81 sec                                                            | 1.88 sec: 1.03x slower                                                          |
| 2to3                     | 233 ms                                                              | 241 ms: 1.04x slower                                                            |
| deepcopy_memo            | 23.5 us                                                             | 24.4 us: 1.04x slower                                                           |
| scimark_fft              | 198 ms                                                              | 205 ms: 1.04x slower                                                            |
| chameleon                | 5.71 ms                                                             | 5.93 ms: 1.04x slower                                                           |
| bench_thread_pool        | 985 us                                                              | 1.02 ms: 1.04x slower                                                           |
| sympy_integrate          | 14.6 ms                                                             | 15.2 ms: 1.04x slower                                                           |
| logging_format           | 8.13 us                                                             | 8.47 us: 1.04x slower                                                           |
| sqlglot_normalize        | 206 ms                                                              | 215 ms: 1.04x slower                                                            |
| scimark_sparse_mat_mult  | 2.87 ms                                                             | 3.01 ms: 1.05x slower                                                           |
| pylint                   | 217 ms                                                              | 228 ms: 1.05x slower                                                            |
| logging_silent           | 57.9 ns                                                             | 60.8 ns: 1.05x slower                                                           |
| genshi_xml               | 44.3 ms                                                             | 46.5 ms: 1.05x slower                                                           |
| logging_simple           | 7.47 us                                                             | 7.88 us: 1.06x slower                                                           |
| sqlglot_optimize         | 39.7 ms                                                             | 42.0 ms: 1.06x slower                                                           |
| scimark_monte_carlo      | 45.2 ms                                                             | 47.9 ms: 1.06x slower                                                           |
| spectral_norm            | 68.0 ms                                                             | 72.3 ms: 1.06x slower                                                           |
| regex_dna                | 118 ms                                                              | 126 ms: 1.07x slower                                                            |
| pyflate                  | 308 ms                                                              | 329 ms: 1.07x slower                                                            |
| pycparser                | 777 ms                                                              | 838 ms: 1.08x slower                                                            |
| chaos                    | 48.0 ms                                                             | 51.9 ms: 1.08x slower                                                           |
| generators               | 21.2 ms                                                             | 23.0 ms: 1.09x slower                                                           |
| comprehensions           | 11.9 us                                                             | 12.9 us: 1.09x slower                                                           |
| unpickle_pure_python     | 147 us                                                              | 161 us: 1.10x slower                                                            |
| python_startup_no_site   | 18.2 ms                                                             | 20.2 ms: 1.11x slower                                                           |
| nqueens                  | 68.7 ms                                                             | 76.0 ms: 1.11x slower                                                           |
| go                       | 101 ms                                                              | 113 ms: 1.12x slower                                                            |
| scimark_sor              | 81.0 ms                                                             | 91.6 ms: 1.13x slower                                                           |
| thrift                   | 9.73 ms                                                             | 11.0 ms: 1.13x slower                                                           |
| raytrace                 | 189 ms                                                              | 217 ms: 1.15x slower                                                            |
| regex_compile            | 99.9 ms                                                             | 117 ms: 1.17x slower                                                            |
| hexiom                   | 4.23 ms                                                             | 5.25 ms: 1.24x slower                                                           |
| scimark_lu               | 59.4 ms                                                             | 79.6 ms: 1.34x slower                                                           |
| coverage                 | 307 ms                                                              | 469 ms: 1.53x slower                                                            |
| Geometric mean           | (ref)                                                               | 1.02x slower                                                                    |

Benchmark hidden because not significant (11): async_tree_io, async_tree_memoization, async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_memoization_tg, asyncio_tcp_ssl, pidigits, telco, bench_mp_pool, json_dumps, async_tree_cpu_io_mixed_tg
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17.json: flaskblogging
Ignored benchmarks (1) of results/bm-20240323-3.13.0a5+-d610d82-PYTHON_UOPS/bm-20240323-pythonperf1_win32-x86-python-d610d821fd210dce63a1-3.13.0a5+-d610d82.json: unpack_sequence

# HPT report

- Reliability score: 99.93% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: unknown