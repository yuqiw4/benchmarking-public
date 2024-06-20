# Results vs. 3.12.0

- fork: brandtbucher
- ref: justin_align
- machine: windows-x86
- commit hash: d1a7b3a
- commit date: 2024-03-30
- overall geometric mean: 1.10x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 280 ms                                                          | 254 ms: 1.10x faster                                                          |
| chameleon      | 7.75 ms                                                         | 6.36 ms: 1.22x faster                                                         |
| docutils       | 1.98 sec                                                        | 1.91 sec: 1.04x faster                                                        |
| tornado_http   | 105 ms                                                          | 96.1 ms: 1.09x faster                                                         |
| Geometric mean | (ref)                                                           | 1.11x faster                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none_tg         | 278 ms                                                          | 206 ms: 1.35x faster                                                          |
| async_tree_memoization_tg  | 350 ms                                                          | 262 ms: 1.34x faster                                                          |
| async_tree_none            | 298 ms                                                          | 231 ms: 1.29x faster                                                          |
| async_tree_memoization     | 364 ms                                                          | 284 ms: 1.28x faster                                                          |
| async_tree_io              | 693 ms                                                          | 545 ms: 1.27x faster                                                          |
| async_tree_io_tg           | 677 ms                                                          | 544 ms: 1.24x faster                                                          |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 451 ms: 1.21x faster                                                          |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 474 ms: 1.19x faster                                                          |
| Geometric mean             | (ref)                                                           | 1.27x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| float          | 76.7 ms                                                         | 54.0 ms: 1.42x faster                                                         |
| nbody          | 127 ms                                                          | 96.5 ms: 1.32x faster                                                         |
| pidigits       | 199 ms                                                          | 197 ms: 1.01x faster                                                          |
| Geometric mean | (ref)                                                           | 1.24x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 129 ms                                                          | 113 ms: 1.14x faster                                                          |
| regex_effbot   | 2.04 ms                                                         | 1.90 ms: 1.07x faster                                                         |
| regex_dna      | 127 ms                                                          | 121 ms: 1.05x faster                                                          |
| regex_v8       | 15.0 ms                                                         | 16.3 ms: 1.09x slower                                                         |
| Geometric mean | (ref)                                                           | 1.04x faster                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pickle_pure_python   | 286 us                                                          | 223 us: 1.28x faster                                                          |
| tomli_loads          | 2.20 sec                                                        | 1.74 sec: 1.27x faster                                                        |
| unpickle_pure_python | 210 us                                                          | 171 us: 1.23x faster                                                          |
| xml_etree_process    | 53.2 ms                                                         | 43.8 ms: 1.22x faster                                                         |
| xml_etree_iterparse  | 77.6 ms                                                         | 65.4 ms: 1.19x faster                                                         |
| xml_etree_generate   | 72.1 ms                                                         | 62.0 ms: 1.16x faster                                                         |
| json_dumps           | 7.40 ms                                                         | 6.93 ms: 1.07x faster                                                         |
| xml_etree_parse      | 113 ms                                                          | 107 ms: 1.06x faster                                                          |
| unpickle_list        | 2.95 us                                                         | 2.80 us: 1.05x faster                                                         |
| pickle_list          | 3.37 us                                                         | 3.23 us: 1.04x faster                                                         |
| json_loads           | 20.4 us                                                         | 20.2 us: 1.01x faster                                                         |
| pickle_dict          | 19.9 us                                                         | 19.8 us: 1.00x faster                                                         |
| pickle               | 7.79 us                                                         | 7.90 us: 1.01x slower                                                         |
| unpickle             | 9.71 us                                                         | 10.0 us: 1.03x slower                                                         |
| Geometric mean       | (ref)                                                           | 1.10x faster                                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 22.4 ms                                                         | 24.4 ms: 1.09x slower                                                         |
| python_startup_no_site | 19.1 ms                                                         | 21.8 ms: 1.14x slower                                                         |
| Geometric mean         | (ref)                                                           | 1.12x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|-----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako            | 9.96 ms                                                         | 7.07 ms: 1.41x faster                                                         |
| django_template | 36.9 ms                                                         | 33.6 ms: 1.10x faster                                                         |
| Geometric mean  | (ref)                                                           | 1.24x faster                                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| generators                 | 38.5 ms                                                         | 23.1 ms: 1.66x faster                                                         |
| logging_silent             | 101 ns                                                          | 61.3 ns: 1.65x faster                                                         |
| deepcopy_memo              | 38.4 us                                                         | 26.1 us: 1.47x faster                                                         |
| spectral_norm              | 104 ms                                                          | 72.1 ms: 1.44x faster                                                         |
| float                      | 76.7 ms                                                         | 54.0 ms: 1.42x faster                                                         |
| mako                       | 9.96 ms                                                         | 7.07 ms: 1.41x faster                                                         |
| coroutines                 | 20.9 ms                                                         | 14.9 ms: 1.40x faster                                                         |
| deltablue                  | 3.58 ms                                                         | 2.61 ms: 1.38x faster                                                         |
| unpack_sequence            | 62.5 ns                                                         | 45.7 ns: 1.37x faster                                                         |
| async_tree_none_tg         | 278 ms                                                          | 206 ms: 1.35x faster                                                          |
| typing_runtime_protocols   | 126 us                                                          | 94.1 us: 1.34x faster                                                         |
| async_tree_memoization_tg  | 350 ms                                                          | 262 ms: 1.34x faster                                                          |
| nbody                      | 127 ms                                                          | 96.5 ms: 1.32x faster                                                         |
| scimark_sor                | 130 ms                                                          | 99.9 ms: 1.30x faster                                                         |
| async_tree_none            | 298 ms                                                          | 231 ms: 1.29x faster                                                          |
| deepcopy_reduce            | 3.23 us                                                         | 2.51 us: 1.28x faster                                                         |
| pickle_pure_python         | 286 us                                                          | 223 us: 1.28x faster                                                          |
| async_tree_memoization     | 364 ms                                                          | 284 ms: 1.28x faster                                                          |
| async_tree_io              | 693 ms                                                          | 545 ms: 1.27x faster                                                          |
| tomli_loads                | 2.20 sec                                                        | 1.74 sec: 1.27x faster                                                        |
| comprehensions             | 19.2 us                                                         | 15.4 us: 1.25x faster                                                         |
| sqlglot_parse              | 1.25 ms                                                         | 1.00 ms: 1.24x faster                                                         |
| async_tree_io_tg           | 677 ms                                                          | 544 ms: 1.24x faster                                                          |
| deepcopy                   | 360 us                                                          | 291 us: 1.24x faster                                                          |
| unpickle_pure_python       | 210 us                                                          | 171 us: 1.23x faster                                                          |
| scimark_sparse_mat_mult    | 3.86 ms                                                         | 3.15 ms: 1.23x faster                                                         |
| sqlglot_transpile          | 1.53 ms                                                         | 1.25 ms: 1.22x faster                                                         |
| chameleon                  | 7.75 ms                                                         | 6.36 ms: 1.22x faster                                                         |
| xml_etree_process          | 53.2 ms                                                         | 43.8 ms: 1.22x faster                                                         |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 451 ms: 1.21x faster                                                          |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 474 ms: 1.19x faster                                                          |
| xml_etree_iterparse        | 77.6 ms                                                         | 65.4 ms: 1.19x faster                                                         |
| raytrace                   | 308 ms                                                          | 262 ms: 1.18x faster                                                          |
| xml_etree_generate         | 72.1 ms                                                         | 62.0 ms: 1.16x faster                                                         |
| pyflate                    | 424 ms                                                          | 365 ms: 1.16x faster                                                          |
| chaos                      | 69.4 ms                                                         | 60.7 ms: 1.14x faster                                                         |
| regex_compile              | 129 ms                                                          | 113 ms: 1.14x faster                                                          |
| logging_format             | 10.4 us                                                         | 9.11 us: 1.14x faster                                                         |
| richards                   | 41.3 ms                                                         | 36.2 ms: 1.14x faster                                                         |
| logging_simple             | 9.75 us                                                         | 8.55 us: 1.14x faster                                                         |
| pycparser                  | 978 ms                                                          | 857 ms: 1.14x faster                                                          |
| scimark_fft                | 271 ms                                                          | 238 ms: 1.14x faster                                                          |
| richards_super             | 46.5 ms                                                         | 40.8 ms: 1.14x faster                                                         |
| sympy_sum                  | 123 ms                                                          | 108 ms: 1.14x faster                                                          |
| sympy_str                  | 240 ms                                                          | 213 ms: 1.13x faster                                                          |
| go                         | 137 ms                                                          | 123 ms: 1.12x faster                                                          |
| 2to3                       | 280 ms                                                          | 254 ms: 1.10x faster                                                          |
| mdp                        | 1.91 sec                                                        | 1.74 sec: 1.10x faster                                                        |
| django_template            | 36.9 ms                                                         | 33.6 ms: 1.10x faster                                                         |
| async_generators           | 313 ms                                                          | 286 ms: 1.10x faster                                                          |
| fannkuch                   | 354 ms                                                          | 323 ms: 1.10x faster                                                          |
| sympy_integrate            | 17.5 ms                                                         | 16.0 ms: 1.09x faster                                                         |
| tornado_http               | 105 ms                                                          | 96.1 ms: 1.09x faster                                                         |
| crypto_pyaes               | 69.2 ms                                                         | 63.7 ms: 1.09x faster                                                         |
| hexiom                     | 6.82 ms                                                         | 6.30 ms: 1.08x faster                                                         |
| sqlite_synth               | 2.07 us                                                         | 1.92 us: 1.08x faster                                                         |
| sympy_expand               | 398 ms                                                          | 371 ms: 1.07x faster                                                          |
| scimark_monte_carlo        | 66.4 ms                                                         | 62.0 ms: 1.07x faster                                                         |
| regex_effbot               | 2.04 ms                                                         | 1.90 ms: 1.07x faster                                                         |
| bench_thread_pool          | 1.10 ms                                                         | 1.03 ms: 1.07x faster                                                         |
| json_dumps                 | 7.40 ms                                                         | 6.93 ms: 1.07x faster                                                         |
| sqlglot_optimize           | 48.5 ms                                                         | 45.6 ms: 1.06x faster                                                         |
| xml_etree_parse            | 113 ms                                                          | 107 ms: 1.06x faster                                                          |
| pathlib                    | 91.4 ms                                                         | 86.3 ms: 1.06x faster                                                         |
| meteor_contest             | 86.9 ms                                                         | 82.0 ms: 1.06x faster                                                         |
| asyncio_tcp                | 662 ms                                                          | 627 ms: 1.06x faster                                                          |
| asyncio_tcp_ssl            | 17.7 sec                                                        | 16.7 sec: 1.05x faster                                                        |
| unpickle_list              | 2.95 us                                                         | 2.80 us: 1.05x faster                                                         |
| regex_dna                  | 127 ms                                                          | 121 ms: 1.05x faster                                                          |
| bench_mp_pool              | 75.4 ms                                                         | 72.3 ms: 1.04x faster                                                         |
| pickle_list                | 3.37 us                                                         | 3.23 us: 1.04x faster                                                         |
| docutils                   | 1.98 sec                                                        | 1.91 sec: 1.04x faster                                                        |
| pidigits                   | 199 ms                                                          | 197 ms: 1.01x faster                                                          |
| gc_traversal               | 1.44 ms                                                         | 1.43 ms: 1.01x faster                                                         |
| json_loads                 | 20.4 us                                                         | 20.2 us: 1.01x faster                                                         |
| pprint_pformat             | 1.50 sec                                                        | 1.49 sec: 1.01x faster                                                        |
| pickle_dict                | 19.9 us                                                         | 19.8 us: 1.00x faster                                                         |
| pickle                     | 7.79 us                                                         | 7.90 us: 1.01x slower                                                         |
| scimark_lu                 | 93.2 ms                                                         | 94.8 ms: 1.02x slower                                                         |
| pprint_safe_repr           | 721 ms                                                          | 735 ms: 1.02x slower                                                          |
| unpickle                   | 9.71 us                                                         | 10.0 us: 1.03x slower                                                         |
| regex_v8                   | 15.0 ms                                                         | 16.3 ms: 1.09x slower                                                         |
| python_startup             | 22.4 ms                                                         | 24.4 ms: 1.09x slower                                                         |
| create_gc_cycles           | 652 us                                                          | 738 us: 1.13x slower                                                          |
| python_startup_no_site     | 19.1 ms                                                         | 21.8 ms: 1.14x slower                                                         |
| telco                      | 5.51 ms                                                         | 6.58 ms: 1.19x slower                                                         |
| sqlglot_normalize          | 100 ms                                                          | 241 ms: 2.40x slower                                                          |
| coverage                   | 48.4 ms                                                         | 489 ms: 10.10x slower                                                         |
| Geometric mean             | (ref)                                                           | 1.10x faster                                                                  |

Benchmark hidden because not significant (2): nqueens, json
Ignored benchmarks (6) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (5) of results/bm-20240330-3.13.0a5+-d1a7b3a-JIT/bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-d1a7b3a.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.09x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: unknown