# Results vs. 3.13.0b2

- fork: savannahostrowski
- ref: llvm_18
- machine: windows-amd64
- commit hash: 8d9855f
- commit date: 2024-04-26
- overall geometric mean: 1.04x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf1-amd64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 207 ms                                                          | 228 ms: 1.10x slower                                                      |
| chameleon      | 4.80 ms                                                         | 4.77 ms: 1.01x faster                                                     |
| docutils       | 1.63 sec                                                        | 1.72 sec: 1.06x slower                                                    |
| html5lib       | 35.0 ms                                                         | 35.4 ms: 1.01x slower                                                     |
| tornado_http   | 81.8 ms                                                         | 93.0 ms: 1.14x slower                                                     |
| Geometric mean | (ref)                                                           | 1.06x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf1-amd64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|---------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed   | 389 ms                                                          | 396 ms: 1.02x slower                                                      |
| async_tree_none           | 218 ms                                                          | 224 ms: 1.03x slower                                                      |
| async_tree_memoization    | 264 ms                                                          | 272 ms: 1.03x slower                                                      |
| async_tree_io_tg          | 605 ms                                                          | 625 ms: 1.03x slower                                                      |
| async_tree_memoization_tg | 258 ms                                                          | 271 ms: 1.05x slower                                                      |
| async_tree_none_tg        | 202 ms                                                          | 217 ms: 1.07x slower                                                      |
| Geometric mean            | (ref)                                                           | 1.03x slower                                                              |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed_tg, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf1-amd64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| nbody          | 67.6 ms                                                         | 62.4 ms: 1.08x faster                                                     |
| float          | 49.7 ms                                                         | 45.9 ms: 1.08x faster                                                     |
| pidigits       | 150 ms                                                          | 148 ms: 1.01x faster                                                      |
| Geometric mean | (ref)                                                           | 1.06x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf1-amd64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 1.58 ms                                                         | 1.60 ms: 1.01x slower                                                     |
| regex_dna      | 119 ms                                                          | 120 ms: 1.01x slower                                                      |
| regex_compile  | 78.0 ms                                                         | 88.0 ms: 1.13x slower                                                     |
| Geometric mean | (ref)                                                           | 1.03x slower                                                              |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf1-amd64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| tomli_loads          | 1.35 sec                                                        | 1.18 sec: 1.14x faster                                                    |
| xml_etree_iterparse  | 62.3 ms                                                         | 61.6 ms: 1.01x faster                                                     |
| pickle_pure_python   | 175 us                                                          | 173 us: 1.01x faster                                                      |
| json_dumps           | 5.61 ms                                                         | 5.67 ms: 1.01x slower                                                     |
| xml_etree_process    | 36.4 ms                                                         | 36.8 ms: 1.01x slower                                                     |
| unpickle_pure_python | 122 us                                                          | 123 us: 1.01x slower                                                      |
| xml_etree_parse      | 90.9 ms                                                         | 92.3 ms: 1.02x slower                                                     |
| unpickle             | 8.40 us                                                         | 8.56 us: 1.02x slower                                                     |
| xml_etree_generate   | 53.2 ms                                                         | 54.3 ms: 1.02x slower                                                     |
| pickle_dict          | 18.1 us                                                         | 18.7 us: 1.03x slower                                                     |
| pickle               | 7.11 us                                                         | 7.39 us: 1.04x slower                                                     |
| unpickle_list        | 2.62 us                                                         | 2.79 us: 1.07x slower                                                     |
| pickle_list          | 2.90 us                                                         | 3.12 us: 1.07x slower                                                     |
| Geometric mean       | (ref)                                                           | 1.01x slower                                                              |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf1-amd64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup         | 20.3 ms                                                         | 22.4 ms: 1.10x slower                                                     |
| python_startup_no_site | 16.2 ms                                                         | 18.5 ms: 1.14x slower                                                     |
| Geometric mean         | (ref)                                                           | 1.12x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf1-amd64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|-----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako            | 6.36 ms                                                         | 5.34 ms: 1.19x faster                                                     |
| django_template | 21.7 ms                                                         | 22.8 ms: 1.05x slower                                                     |
| genshi_text     | 14.4 ms                                                         | 16.7 ms: 1.16x slower                                                     |
| genshi_xml      | 31.6 ms                                                         | 39.1 ms: 1.24x slower                                                     |
| Geometric mean  | (ref)                                                           | 1.06x slower                                                              |

All benchmarks:
===============

| Benchmark                 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf1-amd64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|---------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| spectral_norm             | 63.7 ms                                                         | 50.4 ms: 1.26x faster                                                     |
| mako                      | 6.36 ms                                                         | 5.34 ms: 1.19x faster                                                     |
| tomli_loads               | 1.35 sec                                                        | 1.18 sec: 1.14x faster                                                    |
| scimark_sparse_mat_mult   | 2.50 ms                                                         | 2.22 ms: 1.13x faster                                                     |
| nbody                     | 67.6 ms                                                         | 62.4 ms: 1.08x faster                                                     |
| float                     | 49.7 ms                                                         | 45.9 ms: 1.08x faster                                                     |
| pprint_safe_repr          | 474 ms                                                          | 440 ms: 1.08x faster                                                      |
| pprint_pformat            | 966 ms                                                          | 905 ms: 1.07x faster                                                      |
| fannkuch                  | 243 ms                                                          | 231 ms: 1.05x faster                                                      |
| pyflate                   | 279 ms                                                          | 268 ms: 1.04x faster                                                      |
| deepcopy_reduce           | 1.99 us                                                         | 1.94 us: 1.03x faster                                                     |
| crypto_pyaes              | 45.5 ms                                                         | 44.3 ms: 1.03x faster                                                     |
| scimark_monte_carlo       | 39.1 ms                                                         | 38.2 ms: 1.03x faster                                                     |
| scimark_fft               | 171 ms                                                          | 167 ms: 1.02x faster                                                      |
| pidigits                  | 150 ms                                                          | 148 ms: 1.01x faster                                                      |
| xml_etree_iterparse       | 62.3 ms                                                         | 61.6 ms: 1.01x faster                                                     |
| pickle_pure_python        | 175 us                                                          | 173 us: 1.01x faster                                                      |
| chameleon                 | 4.80 ms                                                         | 4.77 ms: 1.01x faster                                                     |
| deepcopy_memo             | 22.1 us                                                         | 22.0 us: 1.00x faster                                                     |
| regex_effbot              | 1.58 ms                                                         | 1.60 ms: 1.01x slower                                                     |
| logging_silent            | 52.9 ns                                                         | 53.4 ns: 1.01x slower                                                     |
| json_dumps                | 5.61 ms                                                         | 5.67 ms: 1.01x slower                                                     |
| xml_etree_process         | 36.4 ms                                                         | 36.8 ms: 1.01x slower                                                     |
| telco                     | 4.67 ms                                                         | 4.72 ms: 1.01x slower                                                     |
| regex_dna                 | 119 ms                                                          | 120 ms: 1.01x slower                                                      |
| html5lib                  | 35.0 ms                                                         | 35.4 ms: 1.01x slower                                                     |
| unpickle_pure_python      | 122 us                                                          | 123 us: 1.01x slower                                                      |
| gc_traversal              | 1.55 ms                                                         | 1.58 ms: 1.01x slower                                                     |
| xml_etree_parse           | 90.9 ms                                                         | 92.3 ms: 1.02x slower                                                     |
| richards                  | 26.7 ms                                                         | 27.1 ms: 1.02x slower                                                     |
| sqlite_synth              | 1.60 us                                                         | 1.63 us: 1.02x slower                                                     |
| async_tree_cpu_io_mixed   | 389 ms                                                          | 396 ms: 1.02x slower                                                      |
| logging_format            | 6.22 us                                                         | 6.34 us: 1.02x slower                                                     |
| unpickle                  | 8.40 us                                                         | 8.56 us: 1.02x slower                                                     |
| xml_etree_generate        | 53.2 ms                                                         | 54.3 ms: 1.02x slower                                                     |
| logging_simple            | 5.78 us                                                         | 5.91 us: 1.02x slower                                                     |
| sqlglot_parse             | 748 us                                                          | 770 us: 1.03x slower                                                      |
| deepcopy                  | 220 us                                                          | 226 us: 1.03x slower                                                      |
| async_tree_none           | 218 ms                                                          | 224 ms: 1.03x slower                                                      |
| raytrace                  | 162 ms                                                          | 167 ms: 1.03x slower                                                      |
| async_tree_memoization    | 264 ms                                                          | 272 ms: 1.03x slower                                                      |
| comprehensions            | 10.4 us                                                         | 10.7 us: 1.03x slower                                                     |
| pickle_dict               | 18.1 us                                                         | 18.7 us: 1.03x slower                                                     |
| async_tree_io_tg          | 605 ms                                                          | 625 ms: 1.03x slower                                                      |
| generators                | 19.6 ms                                                         | 20.3 ms: 1.04x slower                                                     |
| pickle                    | 7.11 us                                                         | 7.39 us: 1.04x slower                                                     |
| sqlglot_transpile         | 955 us                                                          | 993 us: 1.04x slower                                                      |
| meteor_contest            | 69.9 ms                                                         | 73.2 ms: 1.05x slower                                                     |
| async_tree_memoization_tg | 258 ms                                                          | 271 ms: 1.05x slower                                                      |
| create_gc_cycles          | 888 us                                                          | 932 us: 1.05x slower                                                      |
| chaos                     | 38.4 ms                                                         | 40.4 ms: 1.05x slower                                                     |
| django_template           | 21.7 ms                                                         | 22.8 ms: 1.05x slower                                                     |
| sqlglot_normalize         | 173 ms                                                          | 183 ms: 1.06x slower                                                      |
| docutils                  | 1.63 sec                                                        | 1.72 sec: 1.06x slower                                                    |
| coverage                  | 42.1 ms                                                         | 44.7 ms: 1.06x slower                                                     |
| sympy_sum                 | 84.4 ms                                                         | 89.8 ms: 1.06x slower                                                     |
| unpickle_list             | 2.62 us                                                         | 2.79 us: 1.07x slower                                                     |
| pathlib                   | 75.9 ms                                                         | 80.9 ms: 1.07x slower                                                     |
| sympy_expand              | 271 ms                                                          | 289 ms: 1.07x slower                                                      |
| sqlglot_optimize          | 32.7 ms                                                         | 35.1 ms: 1.07x slower                                                     |
| async_tree_none_tg        | 202 ms                                                          | 217 ms: 1.07x slower                                                      |
| bench_mp_pool             | 64.8 ms                                                         | 69.5 ms: 1.07x slower                                                     |
| sympy_str                 | 159 ms                                                          | 171 ms: 1.07x slower                                                      |
| pickle_list               | 2.90 us                                                         | 3.12 us: 1.07x slower                                                     |
| async_generators          | 223 ms                                                          | 241 ms: 1.08x slower                                                      |
| dulwich_log               | 38.0 ms                                                         | 41.2 ms: 1.08x slower                                                     |
| aiohttp                   | 889 us                                                          | 963 us: 1.08x slower                                                      |
| pylint                    | 205 ms                                                          | 224 ms: 1.10x slower                                                      |
| mdp                       | 1.31 sec                                                        | 1.44 sec: 1.10x slower                                                    |
| python_startup            | 20.3 ms                                                         | 22.4 ms: 1.10x slower                                                     |
| bench_thread_pool         | 768 us                                                          | 847 us: 1.10x slower                                                      |
| 2to3                      | 207 ms                                                          | 228 ms: 1.10x slower                                                      |
| scimark_sor               | 75.3 ms                                                         | 83.4 ms: 1.11x slower                                                     |
| sympy_integrate           | 12.2 ms                                                         | 13.6 ms: 1.11x slower                                                     |
| typing_runtime_protocols  | 101 us                                                          | 113 us: 1.12x slower                                                      |
| mypy2                     | 418 ms                                                          | 471 ms: 1.13x slower                                                      |
| thrift                    | 8.11 ms                                                         | 9.13 ms: 1.13x slower                                                     |
| regex_compile             | 78.0 ms                                                         | 88.0 ms: 1.13x slower                                                     |
| tornado_http              | 81.8 ms                                                         | 93.0 ms: 1.14x slower                                                     |
| python_startup_no_site    | 16.2 ms                                                         | 18.5 ms: 1.14x slower                                                     |
| nqueens                   | 56.7 ms                                                         | 65.0 ms: 1.15x slower                                                     |
| genshi_text               | 14.4 ms                                                         | 16.7 ms: 1.16x slower                                                     |
| deltablue                 | 1.88 ms                                                         | 2.21 ms: 1.17x slower                                                     |
| go                        | 82.1 ms                                                         | 97.2 ms: 1.18x slower                                                     |
| asyncio_tcp_ssl           | 1.48 sec                                                        | 1.76 sec: 1.19x slower                                                    |
| scimark_lu                | 56.6 ms                                                         | 69.6 ms: 1.23x slower                                                     |
| genshi_xml                | 31.6 ms                                                         | 39.1 ms: 1.24x slower                                                     |
| hexiom                    | 3.72 ms                                                         | 4.70 ms: 1.26x slower                                                     |
| asyncio_tcp               | 471 ms                                                          | 670 ms: 1.42x slower                                                      |
| Geometric mean            | (ref)                                                           | 1.04x slower                                                              |

Benchmark hidden because not significant (8): pycparser, regex_v8, richards_super, coroutines, async_tree_cpu_io_mixed_tg, json_loads, async_tree_io, json
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17.json: flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: unknown