# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: tier1_eval_breaker
- machine: windows-x86
- commit hash: a6d4fd4
- commit date: 2024-04-22
- overall geometric mean: 1.01x faster
- HPT reliability: 81.48%
- HPT 99th percentile: 1.00x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-pythonperf1_win32-x86-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------------------:|
| chameleon      | 5.71 ms                                                             | 5.61 ms: 1.02x faster                                                                   |
| docutils       | 1.81 sec                                                            | 1.80 sec: 1.01x faster                                                                  |
| html5lib       | 45.4 ms                                                             | 42.8 ms: 1.06x faster                                                                   |
| Geometric mean | (ref)                                                               | 1.02x faster                                                                            |

Benchmark hidden because not significant (2): 2to3, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark              | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-pythonperf1_win32-x86-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------------------:|
| async_tree_memoization | 275 ms                                                              | 270 ms: 1.02x faster                                                                    |
| Geometric mean         | (ref)                                                               | 1.00x faster                                                                            |

Benchmark hidden because not significant (7): async_tree_none, async_tree_cpu_io_mixed, async_tree_memoization_tg, async_tree_io_tg, async_tree_io, async_tree_none_tg, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-pythonperf1_win32-x86-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------------------:|
| pidigits       | 199 ms                                                              | 197 ms: 1.01x faster                                                                    |
| nbody          | 76.9 ms                                                             | 76.4 ms: 1.01x faster                                                                   |
| float          | 52.4 ms                                                             | 53.4 ms: 1.02x slower                                                                   |
| Geometric mean | (ref)                                                               | 1.00x slower                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-pythonperf1_win32-x86-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------------------:|
| regex_compile  | 99.9 ms                                                             | 97.4 ms: 1.03x faster                                                                   |
| regex_effbot   | 1.88 ms                                                             | 1.90 ms: 1.01x slower                                                                   |
| regex_dna      | 118 ms                                                              | 121 ms: 1.02x slower                                                                    |
| regex_v8       | 15.7 ms                                                             | 16.1 ms: 1.02x slower                                                                   |
| Geometric mean | (ref)                                                               | 1.01x slower                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-pythonperf1_win32-x86-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------------------:|
| pickle_list          | 3.57 us                                                             | 3.29 us: 1.08x faster                                                                   |
| unpickle_pure_python | 147 us                                                              | 140 us: 1.05x faster                                                                    |
| unpickle_list        | 2.93 us                                                             | 2.86 us: 1.03x faster                                                                   |
| pickle_pure_python   | 213 us                                                              | 209 us: 1.02x faster                                                                    |
| pickle_dict          | 20.8 us                                                             | 20.4 us: 1.02x faster                                                                   |
| tomli_loads          | 1.65 sec                                                            | 1.63 sec: 1.01x faster                                                                  |
| pickle               | 8.07 us                                                             | 7.97 us: 1.01x faster                                                                   |
| xml_etree_generate   | 59.6 ms                                                             | 60.0 ms: 1.01x slower                                                                   |
| xml_etree_process    | 42.1 ms                                                             | 42.3 ms: 1.01x slower                                                                   |
| json_dumps           | 6.84 ms                                                             | 6.92 ms: 1.01x slower                                                                   |
| xml_etree_iterparse  | 64.2 ms                                                             | 65.0 ms: 1.01x slower                                                                   |
| xml_etree_parse      | 104 ms                                                              | 107 ms: 1.02x slower                                                                    |
| Geometric mean       | (ref)                                                               | 1.01x faster                                                                            |

Benchmark hidden because not significant (2): unpickle, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-pythonperf1_win32-x86-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------------------:|
| python_startup | 22.2 ms                                                             | 22.0 ms: 1.01x faster                                                                   |
| Geometric mean | (ref)                                                               | 1.00x faster                                                                            |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-pythonperf1_win32-x86-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|-----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------------------:|
| genshi_text     | 20.1 ms                                                             | 18.8 ms: 1.07x faster                                                                   |
| genshi_xml      | 44.3 ms                                                             | 42.7 ms: 1.04x faster                                                                   |
| django_template | 30.1 ms                                                             | 29.5 ms: 1.02x faster                                                                   |
| mako            | 6.94 ms                                                             | 6.87 ms: 1.01x faster                                                                   |
| Geometric mean  | (ref)                                                               | 1.03x faster                                                                            |

All benchmarks:
===============

| Benchmark                | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-pythonperf1_win32-x86-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|--------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------------------:|
| typing_runtime_protocols | 136 us                                                              | 90.7 us: 1.49x faster                                                                   |
| sqlglot_parse            | 964 us                                                              | 878 us: 1.10x faster                                                                    |
| deepcopy_reduce          | 2.59 us                                                             | 2.36 us: 1.10x faster                                                                   |
| pprint_safe_repr         | 607 ms                                                              | 558 ms: 1.09x faster                                                                    |
| pickle_list              | 3.57 us                                                             | 3.29 us: 1.08x faster                                                                   |
| pprint_pformat           | 1.24 sec                                                            | 1.15 sec: 1.08x faster                                                                  |
| sqlglot_transpile        | 1.19 ms                                                             | 1.10 ms: 1.08x faster                                                                   |
| genshi_text              | 20.1 ms                                                             | 18.8 ms: 1.07x faster                                                                   |
| html5lib                 | 45.4 ms                                                             | 42.8 ms: 1.06x faster                                                                   |
| deepcopy                 | 280 us                                                              | 264 us: 1.06x faster                                                                    |
| coroutines               | 15.5 ms                                                             | 14.7 ms: 1.05x faster                                                                   |
| unpickle_pure_python     | 147 us                                                              | 140 us: 1.05x faster                                                                    |
| sympy_expand             | 375 ms                                                              | 359 ms: 1.04x faster                                                                    |
| richards_super           | 35.5 ms                                                             | 34.2 ms: 1.04x faster                                                                   |
| genshi_xml               | 44.3 ms                                                             | 42.7 ms: 1.04x faster                                                                   |
| create_gc_cycles         | 756 us                                                              | 732 us: 1.03x faster                                                                    |
| richards                 | 31.2 ms                                                             | 30.3 ms: 1.03x faster                                                                   |
| sympy_str                | 211 ms                                                              | 205 ms: 1.03x faster                                                                    |
| deepcopy_memo            | 23.5 us                                                             | 22.9 us: 1.03x faster                                                                   |
| regex_compile            | 99.9 ms                                                             | 97.4 ms: 1.03x faster                                                                   |
| unpickle_list            | 2.93 us                                                             | 2.86 us: 1.03x faster                                                                   |
| go                       | 101 ms                                                              | 98.3 ms: 1.02x faster                                                                   |
| telco                    | 6.03 ms                                                             | 5.90 ms: 1.02x faster                                                                   |
| bench_mp_pool            | 69.4 ms                                                             | 68.1 ms: 1.02x faster                                                                   |
| pickle_pure_python       | 213 us                                                              | 209 us: 1.02x faster                                                                    |
| chameleon                | 5.71 ms                                                             | 5.61 ms: 1.02x faster                                                                   |
| django_template          | 30.1 ms                                                             | 29.5 ms: 1.02x faster                                                                   |
| async_tree_memoization   | 275 ms                                                              | 270 ms: 1.02x faster                                                                    |
| logging_format           | 8.13 us                                                             | 8.01 us: 1.02x faster                                                                   |
| pickle_dict              | 20.8 us                                                             | 20.4 us: 1.02x faster                                                                   |
| comprehensions           | 11.9 us                                                             | 11.7 us: 1.02x faster                                                                   |
| sqlglot_normalize        | 206 ms                                                              | 203 ms: 1.02x faster                                                                    |
| deltablue                | 2.23 ms                                                             | 2.20 ms: 1.02x faster                                                                   |
| tomli_loads              | 1.65 sec                                                            | 1.63 sec: 1.01x faster                                                                  |
| pickle                   | 8.07 us                                                             | 7.97 us: 1.01x faster                                                                   |
| sympy_integrate          | 14.6 ms                                                             | 14.5 ms: 1.01x faster                                                                   |
| mako                     | 6.94 ms                                                             | 6.87 ms: 1.01x faster                                                                   |
| gc_traversal             | 1.43 ms                                                             | 1.42 ms: 1.01x faster                                                                   |
| docutils                 | 1.81 sec                                                            | 1.80 sec: 1.01x faster                                                                  |
| python_startup           | 22.2 ms                                                             | 22.0 ms: 1.01x faster                                                                   |
| pidigits                 | 199 ms                                                              | 197 ms: 1.01x faster                                                                    |
| nbody                    | 76.9 ms                                                             | 76.4 ms: 1.01x faster                                                                   |
| sympy_sum                | 105 ms                                                              | 104 ms: 1.01x faster                                                                    |
| sqlglot_optimize         | 39.7 ms                                                             | 39.5 ms: 1.01x faster                                                                   |
| sqlite_synth             | 1.96 us                                                             | 1.97 us: 1.00x slower                                                                   |
| json                     | 4.10 ms                                                             | 4.12 ms: 1.01x slower                                                                   |
| xml_etree_generate       | 59.6 ms                                                             | 60.0 ms: 1.01x slower                                                                   |
| xml_etree_process        | 42.1 ms                                                             | 42.3 ms: 1.01x slower                                                                   |
| regex_effbot             | 1.88 ms                                                             | 1.90 ms: 1.01x slower                                                                   |
| pathlib                  | 83.9 ms                                                             | 84.8 ms: 1.01x slower                                                                   |
| json_dumps               | 6.84 ms                                                             | 6.92 ms: 1.01x slower                                                                   |
| crypto_pyaes             | 55.8 ms                                                             | 56.5 ms: 1.01x slower                                                                   |
| xml_etree_iterparse      | 64.2 ms                                                             | 65.0 ms: 1.01x slower                                                                   |
| meteor_contest           | 74.1 ms                                                             | 75.2 ms: 1.01x slower                                                                   |
| thrift                   | 9.73 ms                                                             | 9.88 ms: 1.02x slower                                                                   |
| float                    | 52.4 ms                                                             | 53.4 ms: 1.02x slower                                                                   |
| hexiom                   | 4.23 ms                                                             | 4.32 ms: 1.02x slower                                                                   |
| mdp                      | 1.60 sec                                                            | 1.64 sec: 1.02x slower                                                                  |
| regex_dna                | 118 ms                                                              | 121 ms: 1.02x slower                                                                    |
| chaos                    | 48.0 ms                                                             | 49.1 ms: 1.02x slower                                                                   |
| pyflate                  | 308 ms                                                              | 316 ms: 1.02x slower                                                                    |
| xml_etree_parse          | 104 ms                                                              | 107 ms: 1.02x slower                                                                    |
| regex_v8                 | 15.7 ms                                                             | 16.1 ms: 1.02x slower                                                                   |
| nqueens                  | 68.7 ms                                                             | 70.6 ms: 1.03x slower                                                                   |
| logging_silent           | 57.9 ns                                                             | 59.8 ns: 1.03x slower                                                                   |
| fannkuch                 | 270 ms                                                              | 279 ms: 1.03x slower                                                                    |
| scimark_monte_carlo      | 45.2 ms                                                             | 46.7 ms: 1.03x slower                                                                   |
| scimark_lu               | 59.4 ms                                                             | 61.4 ms: 1.03x slower                                                                   |
| spectral_norm            | 68.0 ms                                                             | 71.0 ms: 1.04x slower                                                                   |
| async_generators         | 266 ms                                                              | 280 ms: 1.05x slower                                                                    |
| scimark_fft              | 198 ms                                                              | 212 ms: 1.07x slower                                                                    |
| scimark_sparse_mat_mult  | 2.87 ms                                                             | 3.11 ms: 1.08x slower                                                                   |
| generators               | 21.2 ms                                                             | 23.0 ms: 1.09x slower                                                                   |
| coverage                 | 307 ms                                                              | 506 ms: 1.65x slower                                                                    |
| Geometric mean           | (ref)                                                               | 1.01x faster                                                                            |

Benchmark hidden because not significant (20): async_tree_none, bench_thread_pool, pycparser, async_tree_cpu_io_mixed, async_tree_memoization_tg, asyncio_tcp, async_tree_io_tg, tornado_http, async_tree_io, 2to3, asyncio_tcp_ssl, scimark_sor, raytrace, logging_simple, unpickle, json_loads, python_startup_no_site, pylint, async_tree_none_tg, async_tree_cpu_io_mixed_tg
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17.json: flaskblogging

# HPT report

- Reliability score: 81.48% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: unknown