# Results vs. 3.13.0b2

- fork: brandtbucher
- ref: justin_ghccc
- machine: windows-x86
- commit hash: eeeedaf
- commit date: 2024-03-30
- overall geometric mean: 1.01x faster
- HPT reliability: 52.93%
- HPT 99th percentile: 1.00x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 233 ms                                                              | 242 ms: 1.04x slower                                                          |
| chameleon      | 5.71 ms                                                             | 5.89 ms: 1.03x slower                                                         |
| docutils       | 1.81 sec                                                            | 1.84 sec: 1.02x slower                                                        |
| html5lib       | 45.4 ms                                                             | 44.1 ms: 1.03x faster                                                         |
| tornado_http   | 94.3 ms                                                             | 95.7 ms: 1.01x slower                                                         |
| Geometric mean | (ref)                                                               | 1.01x slower                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|-------------------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none         | 228 ms                                                              | 219 ms: 1.04x faster                                                          |
| async_tree_cpu_io_mixed | 471 ms                                                              | 459 ms: 1.03x faster                                                          |
| async_tree_none_tg      | 203 ms                                                              | 198 ms: 1.02x faster                                                          |
| async_tree_io_tg        | 529 ms                                                              | 523 ms: 1.01x faster                                                          |
| Geometric mean          | (ref)                                                               | 1.02x faster                                                                  |

Benchmark hidden because not significant (4): async_tree_memoization, async_tree_io, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| nbody          | 76.9 ms                                                             | 53.7 ms: 1.43x faster                                                         |
| float          | 52.4 ms                                                             | 43.4 ms: 1.21x faster                                                         |
| pidigits       | 199 ms                                                              | 196 ms: 1.01x faster                                                          |
| Geometric mean | (ref)                                                               | 1.20x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 99.9 ms                                                             | 98.7 ms: 1.01x faster                                                         |
| regex_effbot   | 1.88 ms                                                             | 1.91 ms: 1.01x slower                                                         |
| regex_v8       | 15.7 ms                                                             | 16.0 ms: 1.01x slower                                                         |
| Geometric mean | (ref)                                                               | 1.00x slower                                                                  |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| tomli_loads          | 1.65 sec                                                            | 1.45 sec: 1.14x faster                                                        |
| pickle_list          | 3.57 us                                                             | 3.20 us: 1.11x faster                                                         |
| unpickle_pure_python | 147 us                                                              | 139 us: 1.06x faster                                                          |
| pickle               | 8.07 us                                                             | 7.67 us: 1.05x faster                                                         |
| pickle_dict          | 20.8 us                                                             | 19.7 us: 1.05x faster                                                         |
| xml_etree_iterparse  | 64.2 ms                                                             | 62.1 ms: 1.03x faster                                                         |
| xml_etree_generate   | 59.6 ms                                                             | 58.4 ms: 1.02x faster                                                         |
| json_dumps           | 6.84 ms                                                             | 6.72 ms: 1.02x faster                                                         |
| xml_etree_process    | 42.1 ms                                                             | 41.7 ms: 1.01x faster                                                         |
| json_loads           | 20.5 us                                                             | 20.4 us: 1.01x faster                                                         |
| unpickle_list        | 2.93 us                                                             | 2.97 us: 1.01x slower                                                         |
| pickle_pure_python   | 213 us                                                              | 218 us: 1.02x slower                                                          |
| xml_etree_parse      | 104 ms                                                              | 107 ms: 1.02x slower                                                          |
| Geometric mean       | (ref)                                                               | 1.03x faster                                                                  |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|------------------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 22.2 ms                                                             | 24.3 ms: 1.09x slower                                                         |
| python_startup_no_site | 18.2 ms                                                             | 21.8 ms: 1.20x slower                                                         |
| Geometric mean         | (ref)                                                               | 1.14x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|-----------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako            | 6.94 ms                                                             | 5.42 ms: 1.28x faster                                                         |
| genshi_xml      | 44.3 ms                                                             | 45.6 ms: 1.03x slower                                                         |
| django_template | 30.1 ms                                                             | 31.3 ms: 1.04x slower                                                         |
| Geometric mean  | (ref)                                                               | 1.05x faster                                                                  |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|--------------------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols | 136 us                                                              | 90.3 us: 1.50x faster                                                         |
| nbody                    | 76.9 ms                                                             | 53.7 ms: 1.43x faster                                                         |
| spectral_norm            | 68.0 ms                                                             | 50.4 ms: 1.35x faster                                                         |
| mako                     | 6.94 ms                                                             | 5.42 ms: 1.28x faster                                                         |
| fannkuch                 | 270 ms                                                              | 223 ms: 1.21x faster                                                          |
| float                    | 52.4 ms                                                             | 43.4 ms: 1.21x faster                                                         |
| crypto_pyaes             | 55.8 ms                                                             | 47.7 ms: 1.17x faster                                                         |
| scimark_fft              | 198 ms                                                              | 171 ms: 1.16x faster                                                          |
| tomli_loads              | 1.65 sec                                                            | 1.45 sec: 1.14x faster                                                        |
| scimark_monte_carlo      | 45.2 ms                                                             | 39.8 ms: 1.13x faster                                                         |
| scimark_sparse_mat_mult  | 2.87 ms                                                             | 2.54 ms: 1.13x faster                                                         |
| pickle_list              | 3.57 us                                                             | 3.20 us: 1.11x faster                                                         |
| pyflate                  | 308 ms                                                              | 280 ms: 1.10x faster                                                          |
| pprint_pformat           | 1.24 sec                                                            | 1.16 sec: 1.07x faster                                                        |
| asyncio_tcp              | 662 ms                                                              | 619 ms: 1.07x faster                                                          |
| pprint_safe_repr         | 607 ms                                                              | 569 ms: 1.07x faster                                                          |
| unpickle_pure_python     | 147 us                                                              | 139 us: 1.06x faster                                                          |
| comprehensions           | 11.9 us                                                             | 11.2 us: 1.06x faster                                                         |
| coroutines               | 15.5 ms                                                             | 14.7 ms: 1.05x faster                                                         |
| pickle                   | 8.07 us                                                             | 7.67 us: 1.05x faster                                                         |
| pickle_dict              | 20.8 us                                                             | 19.7 us: 1.05x faster                                                         |
| sqlite_synth             | 1.96 us                                                             | 1.87 us: 1.05x faster                                                         |
| sqlglot_parse            | 964 us                                                              | 923 us: 1.04x faster                                                          |
| sympy_expand             | 375 ms                                                              | 359 ms: 1.04x faster                                                          |
| async_tree_none          | 228 ms                                                              | 219 ms: 1.04x faster                                                          |
| sympy_str                | 211 ms                                                              | 203 ms: 1.04x faster                                                          |
| xml_etree_iterparse      | 64.2 ms                                                             | 62.1 ms: 1.03x faster                                                         |
| html5lib                 | 45.4 ms                                                             | 44.1 ms: 1.03x faster                                                         |
| create_gc_cycles         | 756 us                                                              | 734 us: 1.03x faster                                                          |
| telco                    | 6.03 ms                                                             | 5.87 ms: 1.03x faster                                                         |
| async_tree_cpu_io_mixed  | 471 ms                                                              | 459 ms: 1.03x faster                                                          |
| async_tree_none_tg       | 203 ms                                                              | 198 ms: 1.02x faster                                                          |
| xml_etree_generate       | 59.6 ms                                                             | 58.4 ms: 1.02x faster                                                         |
| sqlglot_transpile        | 1.19 ms                                                             | 1.17 ms: 1.02x faster                                                         |
| deepcopy_reduce          | 2.59 us                                                             | 2.54 us: 1.02x faster                                                         |
| json_dumps               | 6.84 ms                                                             | 6.72 ms: 1.02x faster                                                         |
| regex_compile            | 99.9 ms                                                             | 98.7 ms: 1.01x faster                                                         |
| pidigits                 | 199 ms                                                              | 196 ms: 1.01x faster                                                          |
| async_tree_io_tg         | 529 ms                                                              | 523 ms: 1.01x faster                                                          |
| xml_etree_process        | 42.1 ms                                                             | 41.7 ms: 1.01x faster                                                         |
| sympy_sum                | 105 ms                                                              | 104 ms: 1.01x faster                                                          |
| json_loads               | 20.5 us                                                             | 20.4 us: 1.01x faster                                                         |
| asyncio_tcp_ssl          | 16.9 sec                                                            | 16.8 sec: 1.01x faster                                                        |
| meteor_contest           | 74.1 ms                                                             | 73.8 ms: 1.00x faster                                                         |
| regex_effbot             | 1.88 ms                                                             | 1.91 ms: 1.01x slower                                                         |
| mdp                      | 1.60 sec                                                            | 1.62 sec: 1.01x slower                                                        |
| unpickle_list            | 2.93 us                                                             | 2.97 us: 1.01x slower                                                         |
| regex_v8                 | 15.7 ms                                                             | 16.0 ms: 1.01x slower                                                         |
| gc_traversal             | 1.43 ms                                                             | 1.45 ms: 1.01x slower                                                         |
| tornado_http             | 94.3 ms                                                             | 95.7 ms: 1.01x slower                                                         |
| docutils                 | 1.81 sec                                                            | 1.84 sec: 1.02x slower                                                        |
| pickle_pure_python       | 213 us                                                              | 218 us: 1.02x slower                                                          |
| xml_etree_parse          | 104 ms                                                              | 107 ms: 1.02x slower                                                          |
| pathlib                  | 83.9 ms                                                             | 85.8 ms: 1.02x slower                                                         |
| sympy_integrate          | 14.6 ms                                                             | 15.0 ms: 1.03x slower                                                         |
| logging_silent           | 57.9 ns                                                             | 59.4 ns: 1.03x slower                                                         |
| pycparser                | 777 ms                                                              | 799 ms: 1.03x slower                                                          |
| genshi_xml               | 44.3 ms                                                             | 45.6 ms: 1.03x slower                                                         |
| chameleon                | 5.71 ms                                                             | 5.89 ms: 1.03x slower                                                         |
| deepcopy                 | 280 us                                                              | 288 us: 1.03x slower                                                          |
| bench_mp_pool            | 69.4 ms                                                             | 71.7 ms: 1.03x slower                                                         |
| 2to3                     | 233 ms                                                              | 242 ms: 1.04x slower                                                          |
| logging_format           | 8.13 us                                                             | 8.43 us: 1.04x slower                                                         |
| django_template          | 30.1 ms                                                             | 31.3 ms: 1.04x slower                                                         |
| deepcopy_memo            | 23.5 us                                                             | 24.5 us: 1.04x slower                                                         |
| sqlglot_normalize        | 206 ms                                                              | 215 ms: 1.04x slower                                                          |
| nqueens                  | 68.7 ms                                                             | 71.7 ms: 1.04x slower                                                         |
| logging_simple           | 7.47 us                                                             | 7.81 us: 1.05x slower                                                         |
| sqlglot_optimize         | 39.7 ms                                                             | 41.6 ms: 1.05x slower                                                         |
| scimark_sor              | 81.0 ms                                                             | 85.6 ms: 1.06x slower                                                         |
| json                     | 4.10 ms                                                             | 4.37 ms: 1.06x slower                                                         |
| async_generators         | 266 ms                                                              | 283 ms: 1.07x slower                                                          |
| deltablue                | 2.23 ms                                                             | 2.38 ms: 1.07x slower                                                         |
| richards_super           | 35.5 ms                                                             | 37.8 ms: 1.07x slower                                                         |
| go                       | 101 ms                                                              | 110 ms: 1.09x slower                                                          |
| richards                 | 31.2 ms                                                             | 34.0 ms: 1.09x slower                                                         |
| hexiom                   | 4.23 ms                                                             | 4.61 ms: 1.09x slower                                                         |
| python_startup           | 22.2 ms                                                             | 24.3 ms: 1.09x slower                                                         |
| thrift                   | 9.73 ms                                                             | 10.6 ms: 1.09x slower                                                         |
| generators               | 21.2 ms                                                             | 23.1 ms: 1.09x slower                                                         |
| chaos                    | 48.0 ms                                                             | 53.1 ms: 1.11x slower                                                         |
| raytrace                 | 189 ms                                                              | 220 ms: 1.16x slower                                                          |
| python_startup_no_site   | 18.2 ms                                                             | 21.8 ms: 1.20x slower                                                         |
| scimark_lu               | 59.4 ms                                                             | 75.2 ms: 1.27x slower                                                         |
| coverage                 | 307 ms                                                              | 486 ms: 1.58x slower                                                          |
| Geometric mean           | (ref)                                                               | 1.01x faster                                                                  |

Benchmark hidden because not significant (9): async_tree_memoization, async_tree_io, pylint, async_tree_memoization_tg, genshi_text, regex_dna, unpickle, bench_thread_pool, async_tree_cpu_io_mixed_tg
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17.json: flaskblogging
Ignored benchmarks (1) of results/bm-20240330-3.13.0a5+-eeeedaf-JIT/bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf.json: unpack_sequence

# HPT report

- Reliability score: 52.93% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: unknown