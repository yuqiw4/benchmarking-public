# Results vs. 3.12.0

- fork: python
- ref: 05e0b67a43c5c1778dc2
- machine: windows-x86
- commit hash: 05e0b67
- commit date: 2024-03-29
- overall geometric mean: 1.10x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 280 ms                                                          | 257 ms: 1.09x faster                                                            |
| chameleon      | 7.75 ms                                                         | 6.17 ms: 1.26x faster                                                           |
| docutils       | 1.98 sec                                                        | 1.93 sec: 1.03x faster                                                          |
| tornado_http   | 105 ms                                                          | 96.1 ms: 1.09x faster                                                           |
| Geometric mean | (ref)                                                           | 1.11x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none_tg         | 278 ms                                                          | 207 ms: 1.34x faster                                                            |
| async_tree_memoization_tg  | 350 ms                                                          | 264 ms: 1.33x faster                                                            |
| async_tree_none            | 298 ms                                                          | 232 ms: 1.28x faster                                                            |
| async_tree_memoization     | 364 ms                                                          | 286 ms: 1.27x faster                                                            |
| async_tree_io              | 693 ms                                                          | 547 ms: 1.27x faster                                                            |
| async_tree_io_tg           | 677 ms                                                          | 549 ms: 1.23x faster                                                            |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 451 ms: 1.21x faster                                                            |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 472 ms: 1.19x faster                                                            |
| Geometric mean             | (ref)                                                           | 1.27x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| float          | 76.7 ms                                                         | 53.6 ms: 1.43x faster                                                           |
| nbody          | 127 ms                                                          | 95.8 ms: 1.33x faster                                                           |
| Geometric mean | (ref)                                                           | 1.24x faster                                                                    |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 129 ms                                                          | 114 ms: 1.13x faster                                                            |
| regex_dna      | 127 ms                                                          | 120 ms: 1.06x faster                                                            |
| regex_effbot   | 2.04 ms                                                         | 1.92 ms: 1.06x faster                                                           |
| regex_v8       | 15.0 ms                                                         | 16.2 ms: 1.08x slower                                                           |
| Geometric mean | (ref)                                                           | 1.04x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pickle_pure_python   | 286 us                                                          | 220 us: 1.30x faster                                                            |
| tomli_loads          | 2.20 sec                                                        | 1.73 sec: 1.27x faster                                                          |
| xml_etree_process    | 53.2 ms                                                         | 43.7 ms: 1.22x faster                                                           |
| xml_etree_iterparse  | 77.6 ms                                                         | 65.4 ms: 1.19x faster                                                           |
| unpickle_pure_python | 210 us                                                          | 180 us: 1.17x faster                                                            |
| xml_etree_generate   | 72.1 ms                                                         | 62.4 ms: 1.16x faster                                                           |
| json_dumps           | 7.40 ms                                                         | 6.93 ms: 1.07x faster                                                           |
| xml_etree_parse      | 113 ms                                                          | 107 ms: 1.06x faster                                                            |
| pickle_list          | 3.37 us                                                         | 3.25 us: 1.04x faster                                                           |
| unpickle_list        | 2.95 us                                                         | 2.85 us: 1.03x faster                                                           |
| json_loads           | 20.4 us                                                         | 19.9 us: 1.02x faster                                                           |
| pickle_dict          | 19.9 us                                                         | 19.9 us: 1.00x faster                                                           |
| pickle               | 7.79 us                                                         | 7.98 us: 1.02x slower                                                           |
| unpickle             | 9.71 us                                                         | 10.0 us: 1.03x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.10x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 22.4 ms                                                         | 24.3 ms: 1.09x slower                                                           |
| python_startup_no_site | 19.1 ms                                                         | 21.9 ms: 1.15x slower                                                           |
| Geometric mean         | (ref)                                                           | 1.12x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|-----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 9.96 ms                                                         | 7.10 ms: 1.40x faster                                                           |
| django_template | 36.9 ms                                                         | 33.4 ms: 1.10x faster                                                           |
| Geometric mean  | (ref)                                                           | 1.24x faster                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| logging_silent             | 101 ns                                                          | 60.3 ns: 1.67x faster                                                           |
| generators                 | 38.5 ms                                                         | 23.1 ms: 1.66x faster                                                           |
| deepcopy_memo              | 38.4 us                                                         | 26.3 us: 1.46x faster                                                           |
| spectral_norm              | 104 ms                                                          | 71.2 ms: 1.46x faster                                                           |
| float                      | 76.7 ms                                                         | 53.6 ms: 1.43x faster                                                           |
| coroutines                 | 20.9 ms                                                         | 14.7 ms: 1.42x faster                                                           |
| mako                       | 9.96 ms                                                         | 7.10 ms: 1.40x faster                                                           |
| deltablue                  | 3.58 ms                                                         | 2.62 ms: 1.37x faster                                                           |
| async_tree_none_tg         | 278 ms                                                          | 207 ms: 1.34x faster                                                            |
| unpack_sequence            | 62.5 ns                                                         | 46.6 ns: 1.34x faster                                                           |
| async_tree_memoization_tg  | 350 ms                                                          | 264 ms: 1.33x faster                                                            |
| nbody                      | 127 ms                                                          | 95.8 ms: 1.33x faster                                                           |
| typing_runtime_protocols   | 126 us                                                          | 96.5 us: 1.31x faster                                                           |
| pickle_pure_python         | 286 us                                                          | 220 us: 1.30x faster                                                            |
| scimark_sor                | 130 ms                                                          | 100.0 ms: 1.30x faster                                                          |
| async_tree_none            | 298 ms                                                          | 232 ms: 1.28x faster                                                            |
| async_tree_memoization     | 364 ms                                                          | 286 ms: 1.27x faster                                                            |
| tomli_loads                | 2.20 sec                                                        | 1.73 sec: 1.27x faster                                                          |
| async_tree_io              | 693 ms                                                          | 547 ms: 1.27x faster                                                            |
| chameleon                  | 7.75 ms                                                         | 6.17 ms: 1.26x faster                                                           |
| sqlglot_parse              | 1.25 ms                                                         | 1.01 ms: 1.24x faster                                                           |
| async_tree_io_tg           | 677 ms                                                          | 549 ms: 1.23x faster                                                            |
| comprehensions             | 19.2 us                                                         | 15.6 us: 1.23x faster                                                           |
| deepcopy_reduce            | 3.23 us                                                         | 2.64 us: 1.22x faster                                                           |
| xml_etree_process          | 53.2 ms                                                         | 43.7 ms: 1.22x faster                                                           |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 451 ms: 1.21x faster                                                            |
| sqlglot_transpile          | 1.53 ms                                                         | 1.26 ms: 1.21x faster                                                           |
| scimark_sparse_mat_mult    | 3.86 ms                                                         | 3.19 ms: 1.21x faster                                                           |
| deepcopy                   | 360 us                                                          | 300 us: 1.20x faster                                                            |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 472 ms: 1.19x faster                                                            |
| xml_etree_iterparse        | 77.6 ms                                                         | 65.4 ms: 1.19x faster                                                           |
| logging_simple             | 9.75 us                                                         | 8.24 us: 1.18x faster                                                           |
| logging_format             | 10.4 us                                                         | 8.81 us: 1.18x faster                                                           |
| unpickle_pure_python       | 210 us                                                          | 180 us: 1.17x faster                                                            |
| richards                   | 41.3 ms                                                         | 35.6 ms: 1.16x faster                                                           |
| xml_etree_generate         | 72.1 ms                                                         | 62.4 ms: 1.16x faster                                                           |
| richards_super             | 46.5 ms                                                         | 40.2 ms: 1.16x faster                                                           |
| pyflate                    | 424 ms                                                          | 370 ms: 1.15x faster                                                            |
| scimark_fft                | 271 ms                                                          | 237 ms: 1.14x faster                                                            |
| regex_compile              | 129 ms                                                          | 114 ms: 1.13x faster                                                            |
| raytrace                   | 308 ms                                                          | 273 ms: 1.13x faster                                                            |
| pycparser                  | 978 ms                                                          | 872 ms: 1.12x faster                                                            |
| crypto_pyaes               | 69.2 ms                                                         | 61.8 ms: 1.12x faster                                                           |
| sympy_sum                  | 123 ms                                                          | 110 ms: 1.12x faster                                                            |
| go                         | 137 ms                                                          | 123 ms: 1.12x faster                                                            |
| fannkuch                   | 354 ms                                                          | 319 ms: 1.11x faster                                                            |
| django_template            | 36.9 ms                                                         | 33.4 ms: 1.10x faster                                                           |
| sympy_str                  | 240 ms                                                          | 218 ms: 1.10x faster                                                            |
| chaos                      | 69.4 ms                                                         | 63.1 ms: 1.10x faster                                                           |
| async_generators           | 313 ms                                                          | 285 ms: 1.10x faster                                                            |
| asyncio_tcp                | 662 ms                                                          | 604 ms: 1.10x faster                                                            |
| tornado_http               | 105 ms                                                          | 96.1 ms: 1.09x faster                                                           |
| bench_thread_pool          | 1.10 ms                                                         | 1.01 ms: 1.09x faster                                                           |
| 2to3                       | 280 ms                                                          | 257 ms: 1.09x faster                                                            |
| hexiom                     | 6.82 ms                                                         | 6.28 ms: 1.09x faster                                                           |
| scimark_monte_carlo        | 66.4 ms                                                         | 61.5 ms: 1.08x faster                                                           |
| mdp                        | 1.91 sec                                                        | 1.78 sec: 1.07x faster                                                          |
| sympy_integrate            | 17.5 ms                                                         | 16.4 ms: 1.07x faster                                                           |
| json_dumps                 | 7.40 ms                                                         | 6.93 ms: 1.07x faster                                                           |
| sqlite_synth               | 2.07 us                                                         | 1.94 us: 1.07x faster                                                           |
| pathlib                    | 91.4 ms                                                         | 86.3 ms: 1.06x faster                                                           |
| regex_dna                  | 127 ms                                                          | 120 ms: 1.06x faster                                                            |
| regex_effbot               | 2.04 ms                                                         | 1.92 ms: 1.06x faster                                                           |
| xml_etree_parse            | 113 ms                                                          | 107 ms: 1.06x faster                                                            |
| asyncio_tcp_ssl            | 17.7 sec                                                        | 16.9 sec: 1.05x faster                                                          |
| bench_mp_pool              | 75.4 ms                                                         | 72.2 ms: 1.04x faster                                                           |
| sympy_expand               | 398 ms                                                          | 381 ms: 1.04x faster                                                            |
| sqlglot_optimize           | 48.5 ms                                                         | 46.5 ms: 1.04x faster                                                           |
| pickle_list                | 3.37 us                                                         | 3.25 us: 1.04x faster                                                           |
| meteor_contest             | 86.9 ms                                                         | 83.9 ms: 1.04x faster                                                           |
| unpickle_list              | 2.95 us                                                         | 2.85 us: 1.03x faster                                                           |
| docutils                   | 1.98 sec                                                        | 1.93 sec: 1.03x faster                                                          |
| json_loads                 | 20.4 us                                                         | 19.9 us: 1.02x faster                                                           |
| nqueens                    | 93.7 ms                                                         | 92.1 ms: 1.02x faster                                                           |
| pickle_dict                | 19.9 us                                                         | 19.9 us: 1.00x faster                                                           |
| pprint_pformat             | 1.50 sec                                                        | 1.51 sec: 1.01x slower                                                          |
| pickle                     | 7.79 us                                                         | 7.98 us: 1.02x slower                                                           |
| pprint_safe_repr           | 721 ms                                                          | 742 ms: 1.03x slower                                                            |
| unpickle                   | 9.71 us                                                         | 10.0 us: 1.03x slower                                                           |
| json                       | 4.15 ms                                                         | 4.45 ms: 1.07x slower                                                           |
| regex_v8                   | 15.0 ms                                                         | 16.2 ms: 1.08x slower                                                           |
| python_startup             | 22.4 ms                                                         | 24.3 ms: 1.09x slower                                                           |
| create_gc_cycles           | 652 us                                                          | 737 us: 1.13x slower                                                            |
| python_startup_no_site     | 19.1 ms                                                         | 21.9 ms: 1.15x slower                                                           |
| telco                      | 5.51 ms                                                         | 6.50 ms: 1.18x slower                                                           |
| sqlglot_normalize          | 100 ms                                                          | 241 ms: 2.40x slower                                                            |
| coverage                   | 48.4 ms                                                         | 487 ms: 10.06x slower                                                           |
| Geometric mean             | (ref)                                                           | 1.10x faster                                                                    |

Benchmark hidden because not significant (3): gc_traversal, scimark_lu, pidigits
Ignored benchmarks (6) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (5) of results/bm-20240329-3.13.0a5+-05e0b67-JIT/bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: unknown