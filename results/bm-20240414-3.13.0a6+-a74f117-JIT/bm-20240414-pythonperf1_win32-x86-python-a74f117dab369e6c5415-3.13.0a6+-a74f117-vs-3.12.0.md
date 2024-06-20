# Results vs. 3.12.0

- fork: python
- ref: a74f117dab369e6c5415
- machine: windows-x86
- commit hash: a74f117
- commit date: 2024-04-14
- overall geometric mean: 1.11x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 280 ms                                                          | 254 ms: 1.10x faster                                                            |
| chameleon      | 7.75 ms                                                         | 6.22 ms: 1.25x faster                                                           |
| docutils       | 1.98 sec                                                        | 1.91 sec: 1.04x faster                                                          |
| tornado_http   | 105 ms                                                          | 94.2 ms: 1.11x faster                                                           |
| Geometric mean | (ref)                                                           | 1.12x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 350 ms                                                          | 263 ms: 1.33x faster                                                            |
| async_tree_none_tg         | 278 ms                                                          | 211 ms: 1.31x faster                                                            |
| async_tree_io              | 693 ms                                                          | 537 ms: 1.29x faster                                                            |
| async_tree_memoization     | 364 ms                                                          | 282 ms: 1.29x faster                                                            |
| async_tree_none            | 298 ms                                                          | 232 ms: 1.28x faster                                                            |
| async_tree_io_tg           | 677 ms                                                          | 538 ms: 1.26x faster                                                            |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 453 ms: 1.20x faster                                                            |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 481 ms: 1.17x faster                                                            |
| Geometric mean             | (ref)                                                           | 1.27x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| float          | 76.7 ms                                                         | 53.3 ms: 1.44x faster                                                           |
| nbody          | 127 ms                                                          | 97.3 ms: 1.30x faster                                                           |
| pidigits       | 199 ms                                                          | 197 ms: 1.01x faster                                                            |
| Geometric mean | (ref)                                                           | 1.24x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 129 ms                                                          | 110 ms: 1.17x faster                                                            |
| regex_effbot   | 2.04 ms                                                         | 1.91 ms: 1.07x faster                                                           |
| regex_dna      | 127 ms                                                          | 122 ms: 1.04x faster                                                            |
| regex_v8       | 15.0 ms                                                         | 16.4 ms: 1.09x slower                                                           |
| Geometric mean | (ref)                                                           | 1.05x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| tomli_loads          | 2.20 sec                                                        | 1.66 sec: 1.32x faster                                                          |
| pickle_pure_python   | 286 us                                                          | 220 us: 1.30x faster                                                            |
| unpickle_pure_python | 210 us                                                          | 166 us: 1.27x faster                                                            |
| xml_etree_process    | 53.2 ms                                                         | 44.3 ms: 1.20x faster                                                           |
| xml_etree_iterparse  | 77.6 ms                                                         | 66.9 ms: 1.16x faster                                                           |
| xml_etree_generate   | 72.1 ms                                                         | 63.2 ms: 1.14x faster                                                           |
| json_dumps           | 7.40 ms                                                         | 6.62 ms: 1.12x faster                                                           |
| pickle_list          | 3.37 us                                                         | 3.19 us: 1.06x faster                                                           |
| unpickle_list        | 2.95 us                                                         | 2.83 us: 1.04x faster                                                           |
| xml_etree_parse      | 113 ms                                                          | 111 ms: 1.02x faster                                                            |
| json_loads           | 20.4 us                                                         | 20.1 us: 1.01x faster                                                           |
| pickle_dict          | 19.9 us                                                         | 20.1 us: 1.01x slower                                                           |
| pickle               | 7.79 us                                                         | 8.01 us: 1.03x slower                                                           |
| unpickle             | 9.71 us                                                         | 10.1 us: 1.04x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.11x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 19.1 ms                                                         | 20.1 ms: 1.05x slower                                                           |
| python_startup         | 22.4 ms                                                         | 23.7 ms: 1.06x slower                                                           |
| Geometric mean         | (ref)                                                           | 1.06x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|-----------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako      | 9.96 ms                                                         | 7.03 ms: 1.42x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| generators                 | 38.5 ms                                                         | 22.1 ms: 1.74x faster                                                           |
| logging_silent             | 101 ns                                                          | 60.3 ns: 1.67x faster                                                           |
| deepcopy_memo              | 38.4 us                                                         | 25.5 us: 1.51x faster                                                           |
| spectral_norm              | 104 ms                                                          | 70.0 ms: 1.48x faster                                                           |
| float                      | 76.7 ms                                                         | 53.3 ms: 1.44x faster                                                           |
| mako                       | 9.96 ms                                                         | 7.03 ms: 1.42x faster                                                           |
| coroutines                 | 20.9 ms                                                         | 14.9 ms: 1.40x faster                                                           |
| raytrace                   | 308 ms                                                          | 221 ms: 1.39x faster                                                            |
| scimark_sor                | 130 ms                                                          | 93.7 ms: 1.39x faster                                                           |
| typing_runtime_protocols   | 126 us                                                          | 93.8 us: 1.35x faster                                                           |
| deltablue                  | 3.58 ms                                                         | 2.68 ms: 1.34x faster                                                           |
| async_tree_memoization_tg  | 350 ms                                                          | 263 ms: 1.33x faster                                                            |
| tomli_loads                | 2.20 sec                                                        | 1.66 sec: 1.32x faster                                                          |
| async_tree_none_tg         | 278 ms                                                          | 211 ms: 1.31x faster                                                            |
| nbody                      | 127 ms                                                          | 97.3 ms: 1.30x faster                                                           |
| pickle_pure_python         | 286 us                                                          | 220 us: 1.30x faster                                                            |
| async_tree_io              | 693 ms                                                          | 537 ms: 1.29x faster                                                            |
| async_tree_memoization     | 364 ms                                                          | 282 ms: 1.29x faster                                                            |
| async_tree_none            | 298 ms                                                          | 232 ms: 1.28x faster                                                            |
| unpickle_pure_python       | 210 us                                                          | 166 us: 1.27x faster                                                            |
| sqlglot_parse              | 1.25 ms                                                         | 990 us: 1.26x faster                                                            |
| async_tree_io_tg           | 677 ms                                                          | 538 ms: 1.26x faster                                                            |
| comprehensions             | 19.2 us                                                         | 15.3 us: 1.26x faster                                                           |
| chameleon                  | 7.75 ms                                                         | 6.22 ms: 1.25x faster                                                           |
| sqlglot_transpile          | 1.53 ms                                                         | 1.24 ms: 1.23x faster                                                           |
| richards                   | 41.3 ms                                                         | 33.8 ms: 1.22x faster                                                           |
| logging_simple             | 9.75 us                                                         | 7.98 us: 1.22x faster                                                           |
| richards_super             | 46.5 ms                                                         | 38.3 ms: 1.21x faster                                                           |
| logging_format             | 10.4 us                                                         | 8.58 us: 1.21x faster                                                           |
| chaos                      | 69.4 ms                                                         | 57.3 ms: 1.21x faster                                                           |
| scimark_sparse_mat_mult    | 3.86 ms                                                         | 3.20 ms: 1.21x faster                                                           |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 453 ms: 1.20x faster                                                            |
| xml_etree_process          | 53.2 ms                                                         | 44.3 ms: 1.20x faster                                                           |
| deepcopy_reduce            | 3.23 us                                                         | 2.71 us: 1.19x faster                                                           |
| deepcopy                   | 360 us                                                          | 305 us: 1.18x faster                                                            |
| pyflate                    | 424 ms                                                          | 361 ms: 1.17x faster                                                            |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 481 ms: 1.17x faster                                                            |
| regex_compile              | 129 ms                                                          | 110 ms: 1.17x faster                                                            |
| xml_etree_iterparse        | 77.6 ms                                                         | 66.9 ms: 1.16x faster                                                           |
| scimark_fft                | 271 ms                                                          | 236 ms: 1.15x faster                                                            |
| go                         | 137 ms                                                          | 120 ms: 1.14x faster                                                            |
| xml_etree_generate         | 72.1 ms                                                         | 63.2 ms: 1.14x faster                                                           |
| hexiom                     | 6.82 ms                                                         | 5.98 ms: 1.14x faster                                                           |
| pycparser                  | 978 ms                                                          | 859 ms: 1.14x faster                                                            |
| sympy_sum                  | 123 ms                                                          | 109 ms: 1.13x faster                                                            |
| scimark_monte_carlo        | 66.4 ms                                                         | 59.4 ms: 1.12x faster                                                           |
| json_dumps                 | 7.40 ms                                                         | 6.62 ms: 1.12x faster                                                           |
| tornado_http               | 105 ms                                                          | 94.2 ms: 1.11x faster                                                           |
| sympy_str                  | 240 ms                                                          | 215 ms: 1.11x faster                                                            |
| bench_thread_pool          | 1.10 ms                                                         | 991 us: 1.11x faster                                                            |
| fannkuch                   | 354 ms                                                          | 319 ms: 1.11x faster                                                            |
| scimark_lu                 | 93.2 ms                                                         | 84.2 ms: 1.11x faster                                                           |
| 2to3                       | 280 ms                                                          | 254 ms: 1.10x faster                                                            |
| pathlib                    | 91.4 ms                                                         | 83.1 ms: 1.10x faster                                                           |
| mdp                        | 1.91 sec                                                        | 1.74 sec: 1.10x faster                                                          |
| crypto_pyaes               | 69.2 ms                                                         | 63.5 ms: 1.09x faster                                                           |
| sympy_integrate            | 17.5 ms                                                         | 16.1 ms: 1.09x faster                                                           |
| sqlglot_optimize           | 48.5 ms                                                         | 44.9 ms: 1.08x faster                                                           |
| async_generators           | 313 ms                                                          | 291 ms: 1.08x faster                                                            |
| sympy_expand               | 398 ms                                                          | 371 ms: 1.07x faster                                                            |
| regex_effbot               | 2.04 ms                                                         | 1.91 ms: 1.07x faster                                                           |
| asyncio_tcp                | 662 ms                                                          | 626 ms: 1.06x faster                                                            |
| pickle_list                | 3.37 us                                                         | 3.19 us: 1.06x faster                                                           |
| sqlite_synth               | 2.07 us                                                         | 1.97 us: 1.05x faster                                                           |
| bench_mp_pool              | 75.4 ms                                                         | 71.8 ms: 1.05x faster                                                           |
| asyncio_tcp_ssl            | 17.7 sec                                                        | 16.8 sec: 1.05x faster                                                          |
| unpickle_list              | 2.95 us                                                         | 2.83 us: 1.04x faster                                                           |
| meteor_contest             | 86.9 ms                                                         | 83.5 ms: 1.04x faster                                                           |
| regex_dna                  | 127 ms                                                          | 122 ms: 1.04x faster                                                            |
| docutils                   | 1.98 sec                                                        | 1.91 sec: 1.04x faster                                                          |
| nqueens                    | 93.7 ms                                                         | 90.8 ms: 1.03x faster                                                           |
| xml_etree_parse            | 113 ms                                                          | 111 ms: 1.02x faster                                                            |
| pidigits                   | 199 ms                                                          | 197 ms: 1.01x faster                                                            |
| json_loads                 | 20.4 us                                                         | 20.1 us: 1.01x faster                                                           |
| gc_traversal               | 1.44 ms                                                         | 1.42 ms: 1.01x faster                                                           |
| json                       | 4.15 ms                                                         | 4.13 ms: 1.01x faster                                                           |
| pprint_pformat             | 1.50 sec                                                        | 1.51 sec: 1.01x slower                                                          |
| pickle_dict                | 19.9 us                                                         | 20.1 us: 1.01x slower                                                           |
| pprint_safe_repr           | 721 ms                                                          | 736 ms: 1.02x slower                                                            |
| pickle                     | 7.79 us                                                         | 8.01 us: 1.03x slower                                                           |
| unpickle                   | 9.71 us                                                         | 10.1 us: 1.04x slower                                                           |
| python_startup_no_site     | 19.1 ms                                                         | 20.1 ms: 1.05x slower                                                           |
| python_startup             | 22.4 ms                                                         | 23.7 ms: 1.06x slower                                                           |
| regex_v8                   | 15.0 ms                                                         | 16.4 ms: 1.09x slower                                                           |
| create_gc_cycles           | 652 us                                                          | 733 us: 1.12x slower                                                            |
| telco                      | 5.51 ms                                                         | 6.42 ms: 1.16x slower                                                           |
| sqlglot_normalize          | 100 ms                                                          | 228 ms: 2.28x slower                                                            |
| coverage                   | 48.4 ms                                                         | 504 ms: 10.40x slower                                                           |
| Geometric mean             | (ref)                                                           | 1.11x faster                                                                    |
Ignored benchmarks (8) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0.json: aiohttp, dask, django_template, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240414-3.13.0a6+-a74f117-JIT/bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.11x
- 95% likely to have a speedup of 1.10x
- 99% likely to have a speedup of 1.09x

# Memory
- memory change: unknown