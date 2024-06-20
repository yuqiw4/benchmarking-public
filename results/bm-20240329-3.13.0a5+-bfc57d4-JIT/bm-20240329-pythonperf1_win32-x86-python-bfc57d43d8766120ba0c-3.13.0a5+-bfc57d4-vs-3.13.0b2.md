# Results vs. 3.13.0b2

- fork: python
- ref: bfc57d43d8766120ba0c
- machine: windows-x86
- commit hash: bfc57d4
- commit date: 2024-03-29
- overall geometric mean: 1.09x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 233 ms                                                              | 255 ms: 1.09x slower                                                            |
| chameleon      | 5.71 ms                                                             | 6.13 ms: 1.07x slower                                                           |
| docutils       | 1.81 sec                                                            | 1.95 sec: 1.07x slower                                                          |
| html5lib       | 45.4 ms                                                             | 46.0 ms: 1.01x slower                                                           |
| tornado_http   | 94.3 ms                                                             | 96.4 ms: 1.02x slower                                                           |
| Geometric mean | (ref)                                                               | 1.05x slower                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 471 ms                                                              | 481 ms: 1.02x slower                                                            |
| async_tree_memoization     | 275 ms                                                              | 282 ms: 1.02x slower                                                            |
| async_tree_io              | 530 ms                                                              | 544 ms: 1.03x slower                                                            |
| async_tree_none_tg         | 203 ms                                                              | 209 ms: 1.03x slower                                                            |
| async_tree_io_tg           | 529 ms                                                              | 547 ms: 1.03x slower                                                            |
| async_tree_memoization_tg  | 254 ms                                                              | 265 ms: 1.04x slower                                                            |
| async_tree_cpu_io_mixed_tg | 447 ms                                                              | 468 ms: 1.05x slower                                                            |
| Geometric mean             | (ref)                                                               | 1.03x slower                                                                    |

Benchmark hidden because not significant (1): async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pidigits       | 199 ms                                                              | 198 ms: 1.00x faster                                                            |
| float          | 52.4 ms                                                             | 53.3 ms: 1.02x slower                                                           |
| nbody          | 76.9 ms                                                             | 98.8 ms: 1.29x slower                                                           |
| Geometric mean | (ref)                                                               | 1.09x slower                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_effbot   | 1.88 ms                                                             | 1.93 ms: 1.02x slower                                                           |
| regex_v8       | 15.7 ms                                                             | 16.2 ms: 1.03x slower                                                           |
| regex_dna      | 118 ms                                                              | 125 ms: 1.06x slower                                                            |
| regex_compile  | 99.9 ms                                                             | 113 ms: 1.14x slower                                                            |
| Geometric mean | (ref)                                                               | 1.06x slower                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pickle_list          | 3.57 us                                                             | 3.25 us: 1.10x faster                                                           |
| unpickle_list        | 2.93 us                                                             | 2.80 us: 1.05x faster                                                           |
| pickle_dict          | 20.8 us                                                             | 19.9 us: 1.05x faster                                                           |
| json_loads           | 20.5 us                                                             | 20.3 us: 1.01x faster                                                           |
| json_dumps           | 6.84 ms                                                             | 6.78 ms: 1.01x faster                                                           |
| unpickle             | 9.79 us                                                             | 9.88 us: 1.01x slower                                                           |
| pickle               | 8.07 us                                                             | 8.18 us: 1.01x slower                                                           |
| xml_etree_iterparse  | 64.2 ms                                                             | 65.4 ms: 1.02x slower                                                           |
| xml_etree_process    | 42.1 ms                                                             | 43.4 ms: 1.03x slower                                                           |
| xml_etree_generate   | 59.6 ms                                                             | 61.7 ms: 1.04x slower                                                           |
| xml_etree_parse      | 104 ms                                                              | 108 ms: 1.04x slower                                                            |
| tomli_loads          | 1.65 sec                                                            | 1.72 sec: 1.04x slower                                                          |
| pickle_pure_python   | 213 us                                                              | 227 us: 1.07x slower                                                            |
| unpickle_pure_python | 147 us                                                              | 171 us: 1.16x slower                                                            |
| Geometric mean       | (ref)                                                               | 1.01x slower                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 22.2 ms                                                             | 24.4 ms: 1.10x slower                                                           |
| python_startup_no_site | 18.2 ms                                                             | 21.9 ms: 1.20x slower                                                           |
| Geometric mean         | (ref)                                                               | 1.15x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 6.94 ms                                                             | 7.24 ms: 1.04x slower                                                           |
| genshi_xml      | 44.3 ms                                                             | 47.7 ms: 1.08x slower                                                           |
| django_template | 30.1 ms                                                             | 33.2 ms: 1.10x slower                                                           |
| Geometric mean  | (ref)                                                               | 1.06x slower                                                                    |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 136 us                                                              | 98.2 us: 1.38x faster                                                           |
| pickle_list                | 3.57 us                                                             | 3.25 us: 1.10x faster                                                           |
| coroutines                 | 15.5 ms                                                             | 14.8 ms: 1.05x faster                                                           |
| asyncio_tcp                | 662 ms                                                              | 632 ms: 1.05x faster                                                            |
| unpickle_list              | 2.93 us                                                             | 2.80 us: 1.05x faster                                                           |
| pickle_dict                | 20.8 us                                                             | 19.9 us: 1.05x faster                                                           |
| create_gc_cycles           | 756 us                                                              | 740 us: 1.02x faster                                                            |
| json_loads                 | 20.5 us                                                             | 20.3 us: 1.01x faster                                                           |
| json_dumps                 | 6.84 ms                                                             | 6.78 ms: 1.01x faster                                                           |
| gc_traversal               | 1.43 ms                                                             | 1.42 ms: 1.01x faster                                                           |
| sqlite_synth               | 1.96 us                                                             | 1.95 us: 1.01x faster                                                           |
| pidigits                   | 199 ms                                                              | 198 ms: 1.00x faster                                                            |
| sympy_expand               | 375 ms                                                              | 378 ms: 1.01x slower                                                            |
| unpickle                   | 9.79 us                                                             | 9.88 us: 1.01x slower                                                           |
| html5lib                   | 45.4 ms                                                             | 46.0 ms: 1.01x slower                                                           |
| pickle                     | 8.07 us                                                             | 8.18 us: 1.01x slower                                                           |
| deepcopy_reduce            | 2.59 us                                                             | 2.63 us: 1.02x slower                                                           |
| float                      | 52.4 ms                                                             | 53.3 ms: 1.02x slower                                                           |
| xml_etree_iterparse        | 64.2 ms                                                             | 65.4 ms: 1.02x slower                                                           |
| async_tree_cpu_io_mixed    | 471 ms                                                              | 481 ms: 1.02x slower                                                            |
| tornado_http               | 94.3 ms                                                             | 96.4 ms: 1.02x slower                                                           |
| async_tree_memoization     | 275 ms                                                              | 282 ms: 1.02x slower                                                            |
| regex_effbot               | 1.88 ms                                                             | 1.93 ms: 1.02x slower                                                           |
| pathlib                    | 83.9 ms                                                             | 86.0 ms: 1.03x slower                                                           |
| pylint                     | 217 ms                                                              | 223 ms: 1.03x slower                                                            |
| async_tree_io              | 530 ms                                                              | 544 ms: 1.03x slower                                                            |
| sympy_str                  | 211 ms                                                              | 217 ms: 1.03x slower                                                            |
| bench_thread_pool          | 985 us                                                              | 1.01 ms: 1.03x slower                                                           |
| regex_v8                   | 15.7 ms                                                             | 16.2 ms: 1.03x slower                                                           |
| xml_etree_process          | 42.1 ms                                                             | 43.4 ms: 1.03x slower                                                           |
| async_tree_none_tg         | 203 ms                                                              | 209 ms: 1.03x slower                                                            |
| async_tree_io_tg           | 529 ms                                                              | 547 ms: 1.03x slower                                                            |
| sqlglot_parse              | 964 us                                                              | 996 us: 1.03x slower                                                            |
| xml_etree_generate         | 59.6 ms                                                             | 61.7 ms: 1.04x slower                                                           |
| xml_etree_parse            | 104 ms                                                              | 108 ms: 1.04x slower                                                            |
| sympy_sum                  | 105 ms                                                              | 109 ms: 1.04x slower                                                            |
| tomli_loads                | 1.65 sec                                                            | 1.72 sec: 1.04x slower                                                          |
| async_tree_memoization_tg  | 254 ms                                                              | 265 ms: 1.04x slower                                                            |
| bench_mp_pool              | 69.4 ms                                                             | 72.3 ms: 1.04x slower                                                           |
| mako                       | 6.94 ms                                                             | 7.24 ms: 1.04x slower                                                           |
| async_tree_cpu_io_mixed_tg | 447 ms                                                              | 468 ms: 1.05x slower                                                            |
| logging_silent             | 57.9 ns                                                             | 60.7 ns: 1.05x slower                                                           |
| telco                      | 6.03 ms                                                             | 6.33 ms: 1.05x slower                                                           |
| spectral_norm              | 68.0 ms                                                             | 71.3 ms: 1.05x slower                                                           |
| deepcopy                   | 280 us                                                              | 295 us: 1.06x slower                                                            |
| regex_dna                  | 118 ms                                                              | 125 ms: 1.06x slower                                                            |
| sqlglot_transpile          | 1.19 ms                                                             | 1.26 ms: 1.06x slower                                                           |
| pickle_pure_python         | 213 us                                                              | 227 us: 1.07x slower                                                            |
| chameleon                  | 5.71 ms                                                             | 6.13 ms: 1.07x slower                                                           |
| docutils                   | 1.81 sec                                                            | 1.95 sec: 1.07x slower                                                          |
| genshi_xml                 | 44.3 ms                                                             | 47.7 ms: 1.08x slower                                                           |
| generators                 | 21.2 ms                                                             | 23.0 ms: 1.09x slower                                                           |
| 2to3                       | 233 ms                                                              | 255 ms: 1.09x slower                                                            |
| meteor_contest             | 74.1 ms                                                             | 81.2 ms: 1.10x slower                                                           |
| python_startup             | 22.2 ms                                                             | 24.4 ms: 1.10x slower                                                           |
| json                       | 4.10 ms                                                             | 4.50 ms: 1.10x slower                                                           |
| django_template            | 30.1 ms                                                             | 33.2 ms: 1.10x slower                                                           |
| mdp                        | 1.60 sec                                                            | 1.78 sec: 1.11x slower                                                          |
| scimark_sparse_mat_mult    | 2.87 ms                                                             | 3.18 ms: 1.11x slower                                                           |
| sympy_integrate            | 14.6 ms                                                             | 16.3 ms: 1.11x slower                                                           |
| crypto_pyaes               | 55.8 ms                                                             | 62.0 ms: 1.11x slower                                                           |
| async_generators           | 266 ms                                                              | 295 ms: 1.11x slower                                                            |
| logging_format             | 8.13 us                                                             | 9.05 us: 1.11x slower                                                           |
| pycparser                  | 777 ms                                                              | 871 ms: 1.12x slower                                                            |
| deepcopy_memo              | 23.5 us                                                             | 26.5 us: 1.13x slower                                                           |
| thrift                     | 9.73 ms                                                             | 11.0 ms: 1.13x slower                                                           |
| regex_compile              | 99.9 ms                                                             | 113 ms: 1.14x slower                                                            |
| logging_simple             | 7.47 us                                                             | 8.50 us: 1.14x slower                                                           |
| richards_super             | 35.5 ms                                                             | 40.6 ms: 1.15x slower                                                           |
| sqlglot_normalize          | 206 ms                                                              | 238 ms: 1.16x slower                                                            |
| richards                   | 31.2 ms                                                             | 36.1 ms: 1.16x slower                                                           |
| unpickle_pure_python       | 147 us                                                              | 171 us: 1.16x slower                                                            |
| fannkuch                   | 270 ms                                                              | 313 ms: 1.16x slower                                                            |
| deltablue                  | 2.23 ms                                                             | 2.59 ms: 1.16x slower                                                           |
| sqlglot_optimize           | 39.7 ms                                                             | 46.3 ms: 1.16x slower                                                           |
| pyflate                    | 308 ms                                                              | 369 ms: 1.20x slower                                                            |
| pprint_pformat             | 1.24 sec                                                            | 1.49 sec: 1.20x slower                                                          |
| python_startup_no_site     | 18.2 ms                                                             | 21.9 ms: 1.20x slower                                                           |
| go                         | 101 ms                                                              | 122 ms: 1.21x slower                                                            |
| pprint_safe_repr           | 607 ms                                                              | 741 ms: 1.22x slower                                                            |
| scimark_sor                | 81.0 ms                                                             | 99.1 ms: 1.22x slower                                                           |
| scimark_fft                | 198 ms                                                              | 247 ms: 1.25x slower                                                            |
| nbody                      | 76.9 ms                                                             | 98.8 ms: 1.29x slower                                                           |
| chaos                      | 48.0 ms                                                             | 61.8 ms: 1.29x slower                                                           |
| comprehensions             | 11.9 us                                                             | 15.3 us: 1.29x slower                                                           |
| nqueens                    | 68.7 ms                                                             | 93.0 ms: 1.35x slower                                                           |
| raytrace                   | 189 ms                                                              | 260 ms: 1.38x slower                                                            |
| scimark_monte_carlo        | 45.2 ms                                                             | 62.4 ms: 1.38x slower                                                           |
| hexiom                     | 4.23 ms                                                             | 6.24 ms: 1.48x slower                                                           |
| coverage                   | 307 ms                                                              | 482 ms: 1.57x slower                                                            |
| scimark_lu                 | 59.4 ms                                                             | 96.7 ms: 1.63x slower                                                           |
| Geometric mean             | (ref)                                                               | 1.09x slower                                                                    |

Benchmark hidden because not significant (3): asyncio_tcp_ssl, genshi_text, async_tree_none
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17.json: flaskblogging
Ignored benchmarks (1) of results/bm-20240329-3.13.0a5+-bfc57d4-JIT/bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json: unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: unknown