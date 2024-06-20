# Results vs. 3.12.0

- fork: brandtbucher
- ref: justin_compact
- machine: windows-x86
- commit hash: e04d5ab
- commit date: 2024-06-19
- overall geometric mean: 1.21x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.14x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240619-pythonperf1_win32-x86-brandtbucher-justin_compact-3.14.0a0-e04d5ab |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 280 ms                                                          | 258 ms: 1.08x faster                                                           |
| docutils       | 1.98 sec                                                        | 1.92 sec: 1.03x faster                                                         |
| tornado_http   | 105 ms                                                          | 97.9 ms: 1.07x faster                                                          |
| Geometric mean | (ref)                                                           | 1.06x faster                                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240619-pythonperf1_win32-x86-brandtbucher-justin_compact-3.14.0a0-e04d5ab |
|----------------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 350 ms                                                          | 266 ms: 1.32x faster                                                           |
| async_tree_none_tg         | 278 ms                                                          | 214 ms: 1.29x faster                                                           |
| async_tree_io              | 693 ms                                                          | 552 ms: 1.26x faster                                                           |
| async_tree_none            | 298 ms                                                          | 238 ms: 1.25x faster                                                           |
| async_tree_memoization     | 364 ms                                                          | 292 ms: 1.25x faster                                                           |
| async_tree_io_tg           | 677 ms                                                          | 544 ms: 1.24x faster                                                           |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 454 ms: 1.20x faster                                                           |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 486 ms: 1.16x faster                                                           |
| Geometric mean             | (ref)                                                           | 1.25x faster                                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240619-pythonperf1_win32-x86-brandtbucher-justin_compact-3.14.0a0-e04d5ab |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| nbody          | 127 ms                                                          | 52.4 ms: 2.42x faster                                                          |
| float          | 76.7 ms                                                         | 42.5 ms: 1.81x faster                                                          |
| pidigits       | 199 ms                                                          | 197 ms: 1.01x faster                                                           |
| Geometric mean | (ref)                                                           | 1.64x faster                                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240619-pythonperf1_win32-x86-brandtbucher-justin_compact-3.14.0a0-e04d5ab |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_compile  | 129 ms                                                          | 94.3 ms: 1.37x faster                                                          |
| regex_dna      | 127 ms                                                          | 118 ms: 1.07x faster                                                           |
| regex_effbot   | 2.04 ms                                                         | 1.99 ms: 1.02x faster                                                          |
| regex_v8       | 15.0 ms                                                         | 15.7 ms: 1.05x slower                                                          |
| Geometric mean | (ref)                                                           | 1.10x faster                                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240619-pythonperf1_win32-x86-brandtbucher-justin_compact-3.14.0a0-e04d5ab |
|----------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| tomli_loads          | 2.20 sec                                                        | 1.46 sec: 1.50x faster                                                         |
| unpickle_pure_python | 210 us                                                          | 147 us: 1.42x faster                                                           |
| pickle_pure_python   | 286 us                                                          | 209 us: 1.37x faster                                                           |
| xml_etree_iterparse  | 77.6 ms                                                         | 62.0 ms: 1.25x faster                                                          |
| xml_etree_generate   | 72.1 ms                                                         | 58.4 ms: 1.24x faster                                                          |
| xml_etree_process    | 53.2 ms                                                         | 43.2 ms: 1.23x faster                                                          |
| xml_etree_parse      | 113 ms                                                          | 104 ms: 1.09x faster                                                           |
| json_dumps           | 7.40 ms                                                         | 6.97 ms: 1.06x faster                                                          |
| unpickle_list        | 2.95 us                                                         | 2.86 us: 1.03x faster                                                          |
| pickle_dict          | 19.9 us                                                         | 20.5 us: 1.03x slower                                                          |
| pickle               | 7.79 us                                                         | 8.14 us: 1.04x slower                                                          |
| json_loads           | 20.4 us                                                         | 21.4 us: 1.05x slower                                                          |
| unpickle             | 9.71 us                                                         | 10.8 us: 1.11x slower                                                          |
| pickle_list          | 3.37 us                                                         | 4.05 us: 1.20x slower                                                          |
| Geometric mean       | (ref)                                                           | 1.11x faster                                                                   |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240619-pythonperf1_win32-x86-brandtbucher-justin_compact-3.14.0a0-e04d5ab |
|------------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup_no_site | 19.1 ms                                                         | 20.7 ms: 1.08x slower                                                          |
| python_startup         | 22.4 ms                                                         | 24.8 ms: 1.11x slower                                                          |
| Geometric mean         | (ref)                                                           | 1.10x slower                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240619-pythonperf1_win32-x86-brandtbucher-justin_compact-3.14.0a0-e04d5ab |
|-----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| mako            | 9.96 ms                                                         | 5.34 ms: 1.87x faster                                                          |
| django_template | 36.9 ms                                                         | 32.8 ms: 1.13x faster                                                          |
| Geometric mean  | (ref)                                                           | 1.45x faster                                                                   |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240619-pythonperf1_win32-x86-brandtbucher-justin_compact-3.14.0a0-e04d5ab |
|----------------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| deepcopy_memo              | 38.4 us                                                         | 15.5 us: 2.48x faster                                                          |
| nbody                      | 127 ms                                                          | 52.4 ms: 2.42x faster                                                          |
| spectral_norm              | 104 ms                                                          | 48.2 ms: 2.15x faster                                                          |
| mako                       | 9.96 ms                                                         | 5.34 ms: 1.87x faster                                                          |
| float                      | 76.7 ms                                                         | 42.5 ms: 1.81x faster                                                          |
| logging_silent             | 101 ns                                                          | 57.3 ns: 1.76x faster                                                          |
| comprehensions             | 19.2 us                                                         | 11.2 us: 1.71x faster                                                          |
| hexiom                     | 6.82 ms                                                         | 4.28 ms: 1.59x faster                                                          |
| scimark_fft                | 271 ms                                                          | 172 ms: 1.57x faster                                                           |
| scimark_sparse_mat_mult    | 3.86 ms                                                         | 2.48 ms: 1.56x faster                                                          |
| fannkuch                   | 354 ms                                                          | 228 ms: 1.55x faster                                                           |
| deepcopy                   | 360 us                                                          | 234 us: 1.54x faster                                                           |
| scimark_monte_carlo        | 66.4 ms                                                         | 43.6 ms: 1.52x faster                                                          |
| pyflate                    | 424 ms                                                          | 279 ms: 1.52x faster                                                           |
| tomli_loads                | 2.20 sec                                                        | 1.46 sec: 1.50x faster                                                         |
| crypto_pyaes               | 69.2 ms                                                         | 48.0 ms: 1.44x faster                                                          |
| unpickle_pure_python       | 210 us                                                          | 147 us: 1.42x faster                                                           |
| generators                 | 38.5 ms                                                         | 27.6 ms: 1.39x faster                                                          |
| pickle_pure_python         | 286 us                                                          | 209 us: 1.37x faster                                                           |
| regex_compile              | 129 ms                                                          | 94.3 ms: 1.37x faster                                                          |
| sqlglot_parse              | 1.25 ms                                                         | 921 us: 1.36x faster                                                           |
| scimark_sor                | 130 ms                                                          | 96.9 ms: 1.34x faster                                                          |
| raytrace                   | 308 ms                                                          | 232 ms: 1.33x faster                                                           |
| logging_simple             | 9.75 us                                                         | 7.39 us: 1.32x faster                                                          |
| async_tree_memoization_tg  | 350 ms                                                          | 266 ms: 1.32x faster                                                           |
| nqueens                    | 93.7 ms                                                         | 71.2 ms: 1.32x faster                                                          |
| deltablue                  | 3.58 ms                                                         | 2.73 ms: 1.31x faster                                                          |
| deepcopy_reduce            | 3.23 us                                                         | 2.47 us: 1.31x faster                                                          |
| async_tree_none_tg         | 278 ms                                                          | 214 ms: 1.29x faster                                                           |
| sqlglot_transpile          | 1.53 ms                                                         | 1.18 ms: 1.29x faster                                                          |
| logging_format             | 10.4 us                                                         | 8.05 us: 1.29x faster                                                          |
| chaos                      | 69.4 ms                                                         | 54.2 ms: 1.28x faster                                                          |
| pprint_pformat             | 1.50 sec                                                        | 1.18 sec: 1.27x faster                                                         |
| pprint_safe_repr           | 721 ms                                                          | 572 ms: 1.26x faster                                                           |
| async_tree_io              | 693 ms                                                          | 552 ms: 1.26x faster                                                           |
| xml_etree_iterparse        | 77.6 ms                                                         | 62.0 ms: 1.25x faster                                                          |
| async_tree_none            | 298 ms                                                          | 238 ms: 1.25x faster                                                           |
| async_tree_memoization     | 364 ms                                                          | 292 ms: 1.25x faster                                                           |
| async_tree_io_tg           | 677 ms                                                          | 544 ms: 1.24x faster                                                           |
| go                         | 137 ms                                                          | 111 ms: 1.24x faster                                                           |
| scimark_lu                 | 93.2 ms                                                         | 75.2 ms: 1.24x faster                                                          |
| xml_etree_generate         | 72.1 ms                                                         | 58.4 ms: 1.24x faster                                                          |
| xml_etree_process          | 53.2 ms                                                         | 43.2 ms: 1.23x faster                                                          |
| richards                   | 41.3 ms                                                         | 33.7 ms: 1.22x faster                                                          |
| richards_super             | 46.5 ms                                                         | 38.2 ms: 1.22x faster                                                          |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 454 ms: 1.20x faster                                                           |
| pycparser                  | 978 ms                                                          | 823 ms: 1.19x faster                                                           |
| coroutines                 | 20.9 ms                                                         | 17.6 ms: 1.19x faster                                                          |
| meteor_contest             | 86.9 ms                                                         | 74.2 ms: 1.17x faster                                                          |
| mdp                        | 1.91 sec                                                        | 1.64 sec: 1.16x faster                                                         |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 486 ms: 1.16x faster                                                           |
| bench_thread_pool          | 1.10 ms                                                         | 964 us: 1.14x faster                                                           |
| django_template            | 36.9 ms                                                         | 32.8 ms: 1.13x faster                                                          |
| sqlglot_optimize           | 48.5 ms                                                         | 43.0 ms: 1.13x faster                                                          |
| sympy_sum                  | 123 ms                                                          | 110 ms: 1.12x faster                                                           |
| pathlib                    | 91.4 ms                                                         | 83.4 ms: 1.10x faster                                                          |
| sympy_str                  | 240 ms                                                          | 219 ms: 1.10x faster                                                           |
| sympy_integrate            | 17.5 ms                                                         | 16.1 ms: 1.09x faster                                                          |
| sqlite_synth               | 2.07 us                                                         | 1.90 us: 1.09x faster                                                          |
| asyncio_tcp                | 662 ms                                                          | 608 ms: 1.09x faster                                                           |
| xml_etree_parse            | 113 ms                                                          | 104 ms: 1.09x faster                                                           |
| 2to3                       | 280 ms                                                          | 258 ms: 1.08x faster                                                           |
| regex_dna                  | 127 ms                                                          | 118 ms: 1.07x faster                                                           |
| tornado_http               | 105 ms                                                          | 97.9 ms: 1.07x faster                                                          |
| json_dumps                 | 7.40 ms                                                         | 6.97 ms: 1.06x faster                                                          |
| async_generators           | 313 ms                                                          | 298 ms: 1.05x faster                                                           |
| asyncio_tcp_ssl            | 17.7 sec                                                        | 16.9 sec: 1.04x faster                                                         |
| docutils                   | 1.98 sec                                                        | 1.92 sec: 1.03x faster                                                         |
| unpickle_list              | 2.95 us                                                         | 2.86 us: 1.03x faster                                                          |
| regex_effbot               | 2.04 ms                                                         | 1.99 ms: 1.02x faster                                                          |
| sympy_expand               | 398 ms                                                          | 391 ms: 1.02x faster                                                           |
| pidigits                   | 199 ms                                                          | 197 ms: 1.01x faster                                                           |
| gc_traversal               | 1.44 ms                                                         | 1.43 ms: 1.01x faster                                                          |
| bench_mp_pool              | 75.4 ms                                                         | 75.9 ms: 1.01x slower                                                          |
| telco                      | 5.51 ms                                                         | 5.66 ms: 1.03x slower                                                          |
| pickle_dict                | 19.9 us                                                         | 20.5 us: 1.03x slower                                                          |
| pickle                     | 7.79 us                                                         | 8.14 us: 1.04x slower                                                          |
| regex_v8                   | 15.0 ms                                                         | 15.7 ms: 1.05x slower                                                          |
| json_loads                 | 20.4 us                                                         | 21.4 us: 1.05x slower                                                          |
| coverage                   | 48.4 ms                                                         | 51.2 ms: 1.06x slower                                                          |
| python_startup_no_site     | 19.1 ms                                                         | 20.7 ms: 1.08x slower                                                          |
| unpickle                   | 9.71 us                                                         | 10.8 us: 1.11x slower                                                          |
| python_startup             | 22.4 ms                                                         | 24.8 ms: 1.11x slower                                                          |
| typing_runtime_protocols   | 126 us                                                          | 146 us: 1.15x slower                                                           |
| create_gc_cycles           | 652 us                                                          | 755 us: 1.16x slower                                                           |
| json                       | 4.15 ms                                                         | 4.84 ms: 1.17x slower                                                          |
| pickle_list                | 3.37 us                                                         | 4.05 us: 1.20x slower                                                          |
| sqlglot_normalize          | 100 ms                                                          | 233 ms: 2.32x slower                                                           |
| Geometric mean             | (ref)                                                           | 1.21x faster                                                                   |
Ignored benchmarks (8) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0.json: aiohttp, chameleon, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240619-3.14.0a0-e04d5ab-JIT/bm-20240619-pythonperf1_win32-x86-brandtbucher-justin_compact-3.14.0a0-e04d5ab.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.17x
- 95% likely to have a speedup of 1.16x
- 99% likely to have a speedup of 1.14x

# Memory
- memory change: unknown