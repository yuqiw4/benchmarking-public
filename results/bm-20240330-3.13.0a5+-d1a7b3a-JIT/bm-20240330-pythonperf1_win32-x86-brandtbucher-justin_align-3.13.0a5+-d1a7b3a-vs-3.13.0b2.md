# Results vs. 3.13.0b2

- fork: brandtbucher
- ref: justin_align
- machine: windows-x86
- commit hash: d1a7b3a
- commit date: 2024-03-30
- overall geometric mean: 1.08x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 233 ms                                                              | 254 ms: 1.09x slower                                                          |
| chameleon      | 5.71 ms                                                             | 6.36 ms: 1.11x slower                                                         |
| docutils       | 1.81 sec                                                            | 1.91 sec: 1.06x slower                                                        |
| tornado_http   | 94.3 ms                                                             | 96.1 ms: 1.02x slower                                                         |
| Geometric mean | (ref)                                                               | 1.05x slower                                                                  |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|---------------------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none           | 228 ms                                                              | 231 ms: 1.01x slower                                                          |
| async_tree_io             | 530 ms                                                              | 545 ms: 1.03x slower                                                          |
| async_tree_io_tg          | 529 ms                                                              | 544 ms: 1.03x slower                                                          |
| async_tree_memoization    | 275 ms                                                              | 284 ms: 1.03x slower                                                          |
| async_tree_memoization_tg | 254 ms                                                              | 262 ms: 1.03x slower                                                          |
| Geometric mean            | (ref)                                                               | 1.02x slower                                                                  |

Benchmark hidden because not significant (3): async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pidigits       | 199 ms                                                              | 197 ms: 1.01x faster                                                          |
| float          | 52.4 ms                                                             | 54.0 ms: 1.03x slower                                                         |
| nbody          | 76.9 ms                                                             | 96.5 ms: 1.25x slower                                                         |
| Geometric mean | (ref)                                                               | 1.09x slower                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_effbot   | 1.88 ms                                                             | 1.90 ms: 1.01x slower                                                         |
| regex_dna      | 118 ms                                                              | 121 ms: 1.03x slower                                                          |
| regex_v8       | 15.7 ms                                                             | 16.3 ms: 1.04x slower                                                         |
| regex_compile  | 99.9 ms                                                             | 113 ms: 1.13x slower                                                          |
| Geometric mean | (ref)                                                               | 1.05x slower                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pickle_list          | 3.57 us                                                             | 3.23 us: 1.10x faster                                                         |
| unpickle_list        | 2.93 us                                                             | 2.80 us: 1.05x faster                                                         |
| pickle_dict          | 20.8 us                                                             | 19.8 us: 1.05x faster                                                         |
| pickle               | 8.07 us                                                             | 7.90 us: 1.02x faster                                                         |
| json_loads           | 20.5 us                                                             | 20.2 us: 1.01x faster                                                         |
| json_dumps           | 6.84 ms                                                             | 6.93 ms: 1.01x slower                                                         |
| xml_etree_iterparse  | 64.2 ms                                                             | 65.4 ms: 1.02x slower                                                         |
| xml_etree_parse      | 104 ms                                                              | 107 ms: 1.02x slower                                                          |
| unpickle             | 9.79 us                                                             | 10.0 us: 1.03x slower                                                         |
| xml_etree_generate   | 59.6 ms                                                             | 62.0 ms: 1.04x slower                                                         |
| xml_etree_process    | 42.1 ms                                                             | 43.8 ms: 1.04x slower                                                         |
| pickle_pure_python   | 213 us                                                              | 223 us: 1.05x slower                                                          |
| tomli_loads          | 1.65 sec                                                            | 1.74 sec: 1.05x slower                                                        |
| unpickle_pure_python | 147 us                                                              | 171 us: 1.16x slower                                                          |
| Geometric mean       | (ref)                                                               | 1.01x slower                                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|------------------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 22.2 ms                                                             | 24.4 ms: 1.10x slower                                                         |
| python_startup_no_site | 18.2 ms                                                             | 21.8 ms: 1.20x slower                                                         |
| Geometric mean         | (ref)                                                               | 1.15x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|-----------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako            | 6.94 ms                                                             | 7.07 ms: 1.02x slower                                                         |
| genshi_text     | 20.1 ms                                                             | 20.7 ms: 1.03x slower                                                         |
| genshi_xml      | 44.3 ms                                                             | 48.8 ms: 1.10x slower                                                         |
| django_template | 30.1 ms                                                             | 33.6 ms: 1.12x slower                                                         |
| Geometric mean  | (ref)                                                               | 1.07x slower                                                                  |

All benchmarks:
===============

| Benchmark                 | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|---------------------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols  | 136 us                                                              | 94.1 us: 1.44x faster                                                         |
| pickle_list               | 3.57 us                                                             | 3.23 us: 1.10x faster                                                         |
| asyncio_tcp               | 662 ms                                                              | 627 ms: 1.06x faster                                                          |
| unpickle_list             | 2.93 us                                                             | 2.80 us: 1.05x faster                                                         |
| pickle_dict               | 20.8 us                                                             | 19.8 us: 1.05x faster                                                         |
| coroutines                | 15.5 ms                                                             | 14.9 ms: 1.04x faster                                                         |
| deepcopy_reduce           | 2.59 us                                                             | 2.51 us: 1.03x faster                                                         |
| create_gc_cycles          | 756 us                                                              | 738 us: 1.02x faster                                                          |
| sqlite_synth              | 1.96 us                                                             | 1.92 us: 1.02x faster                                                         |
| pickle                    | 8.07 us                                                             | 7.90 us: 1.02x faster                                                         |
| json_loads                | 20.5 us                                                             | 20.2 us: 1.01x faster                                                         |
| sympy_expand              | 375 ms                                                              | 371 ms: 1.01x faster                                                          |
| pidigits                  | 199 ms                                                              | 197 ms: 1.01x faster                                                          |
| asyncio_tcp_ssl           | 16.9 sec                                                            | 16.7 sec: 1.01x faster                                                        |
| sympy_str                 | 211 ms                                                              | 213 ms: 1.01x slower                                                          |
| regex_effbot              | 1.88 ms                                                             | 1.90 ms: 1.01x slower                                                         |
| json_dumps                | 6.84 ms                                                             | 6.93 ms: 1.01x slower                                                         |
| async_tree_none           | 228 ms                                                              | 231 ms: 1.01x slower                                                          |
| mako                      | 6.94 ms                                                             | 7.07 ms: 1.02x slower                                                         |
| tornado_http              | 94.3 ms                                                             | 96.1 ms: 1.02x slower                                                         |
| xml_etree_iterparse       | 64.2 ms                                                             | 65.4 ms: 1.02x slower                                                         |
| xml_etree_parse           | 104 ms                                                              | 107 ms: 1.02x slower                                                          |
| unpickle                  | 9.79 us                                                             | 10.0 us: 1.03x slower                                                         |
| async_tree_io             | 530 ms                                                              | 545 ms: 1.03x slower                                                          |
| sympy_sum                 | 105 ms                                                              | 108 ms: 1.03x slower                                                          |
| async_tree_io_tg          | 529 ms                                                              | 544 ms: 1.03x slower                                                          |
| pathlib                   | 83.9 ms                                                             | 86.3 ms: 1.03x slower                                                         |
| regex_dna                 | 118 ms                                                              | 121 ms: 1.03x slower                                                          |
| float                     | 52.4 ms                                                             | 54.0 ms: 1.03x slower                                                         |
| genshi_text               | 20.1 ms                                                             | 20.7 ms: 1.03x slower                                                         |
| async_tree_memoization    | 275 ms                                                              | 284 ms: 1.03x slower                                                          |
| async_tree_memoization_tg | 254 ms                                                              | 262 ms: 1.03x slower                                                          |
| json                      | 4.10 ms                                                             | 4.26 ms: 1.04x slower                                                         |
| regex_v8                  | 15.7 ms                                                             | 16.3 ms: 1.04x slower                                                         |
| sqlglot_parse             | 964 us                                                              | 1.00 ms: 1.04x slower                                                         |
| xml_etree_generate        | 59.6 ms                                                             | 62.0 ms: 1.04x slower                                                         |
| xml_etree_process         | 42.1 ms                                                             | 43.8 ms: 1.04x slower                                                         |
| bench_mp_pool             | 69.4 ms                                                             | 72.3 ms: 1.04x slower                                                         |
| deepcopy                  | 280 us                                                              | 291 us: 1.04x slower                                                          |
| bench_thread_pool         | 985 us                                                              | 1.03 ms: 1.05x slower                                                         |
| pickle_pure_python        | 213 us                                                              | 223 us: 1.05x slower                                                          |
| sqlglot_transpile         | 1.19 ms                                                             | 1.25 ms: 1.05x slower                                                         |
| tomli_loads               | 1.65 sec                                                            | 1.74 sec: 1.05x slower                                                        |
| docutils                  | 1.81 sec                                                            | 1.91 sec: 1.06x slower                                                        |
| logging_silent            | 57.9 ns                                                             | 61.3 ns: 1.06x slower                                                         |
| spectral_norm             | 68.0 ms                                                             | 72.1 ms: 1.06x slower                                                         |
| async_generators          | 266 ms                                                              | 286 ms: 1.08x slower                                                          |
| mdp                       | 1.60 sec                                                            | 1.74 sec: 1.08x slower                                                        |
| 2to3                      | 233 ms                                                              | 254 ms: 1.09x slower                                                          |
| telco                     | 6.03 ms                                                             | 6.58 ms: 1.09x slower                                                         |
| generators                | 21.2 ms                                                             | 23.1 ms: 1.09x slower                                                         |
| sympy_integrate           | 14.6 ms                                                             | 16.0 ms: 1.10x slower                                                         |
| scimark_sparse_mat_mult   | 2.87 ms                                                             | 3.15 ms: 1.10x slower                                                         |
| python_startup            | 22.2 ms                                                             | 24.4 ms: 1.10x slower                                                         |
| genshi_xml                | 44.3 ms                                                             | 48.8 ms: 1.10x slower                                                         |
| pycparser                 | 777 ms                                                              | 857 ms: 1.10x slower                                                          |
| meteor_contest            | 74.1 ms                                                             | 82.0 ms: 1.11x slower                                                         |
| deepcopy_memo             | 23.5 us                                                             | 26.1 us: 1.11x slower                                                         |
| chameleon                 | 5.71 ms                                                             | 6.36 ms: 1.11x slower                                                         |
| django_template           | 30.1 ms                                                             | 33.6 ms: 1.12x slower                                                         |
| logging_format            | 8.13 us                                                             | 9.11 us: 1.12x slower                                                         |
| regex_compile             | 99.9 ms                                                             | 113 ms: 1.13x slower                                                          |
| thrift                    | 9.73 ms                                                             | 11.1 ms: 1.14x slower                                                         |
| crypto_pyaes              | 55.8 ms                                                             | 63.7 ms: 1.14x slower                                                         |
| logging_simple            | 7.47 us                                                             | 8.55 us: 1.14x slower                                                         |
| sqlglot_optimize          | 39.7 ms                                                             | 45.6 ms: 1.15x slower                                                         |
| richards_super            | 35.5 ms                                                             | 40.8 ms: 1.15x slower                                                         |
| richards                  | 31.2 ms                                                             | 36.2 ms: 1.16x slower                                                         |
| unpickle_pure_python      | 147 us                                                              | 171 us: 1.16x slower                                                          |
| deltablue                 | 2.23 ms                                                             | 2.61 ms: 1.17x slower                                                         |
| sqlglot_normalize         | 206 ms                                                              | 241 ms: 1.17x slower                                                          |
| pyflate                   | 308 ms                                                              | 365 ms: 1.19x slower                                                          |
| fannkuch                  | 270 ms                                                              | 323 ms: 1.20x slower                                                          |
| python_startup_no_site    | 18.2 ms                                                             | 21.8 ms: 1.20x slower                                                         |
| scimark_fft               | 198 ms                                                              | 238 ms: 1.20x slower                                                          |
| pprint_pformat            | 1.24 sec                                                            | 1.49 sec: 1.20x slower                                                        |
| pprint_safe_repr          | 607 ms                                                              | 735 ms: 1.21x slower                                                          |
| go                        | 101 ms                                                              | 123 ms: 1.22x slower                                                          |
| scimark_sor               | 81.0 ms                                                             | 99.9 ms: 1.23x slower                                                         |
| nbody                     | 76.9 ms                                                             | 96.5 ms: 1.25x slower                                                         |
| chaos                     | 48.0 ms                                                             | 60.7 ms: 1.27x slower                                                         |
| comprehensions            | 11.9 us                                                             | 15.4 us: 1.30x slower                                                         |
| nqueens                   | 68.7 ms                                                             | 93.5 ms: 1.36x slower                                                         |
| scimark_monte_carlo       | 45.2 ms                                                             | 62.0 ms: 1.37x slower                                                         |
| raytrace                  | 189 ms                                                              | 262 ms: 1.39x slower                                                          |
| hexiom                    | 4.23 ms                                                             | 6.30 ms: 1.49x slower                                                         |
| coverage                  | 307 ms                                                              | 489 ms: 1.59x slower                                                          |
| scimark_lu                | 59.4 ms                                                             | 94.8 ms: 1.60x slower                                                         |
| Geometric mean            | (ref)                                                               | 1.08x slower                                                                  |

Benchmark hidden because not significant (6): gc_traversal, html5lib, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_none_tg, pylint
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17.json: flaskblogging
Ignored benchmarks (1) of results/bm-20240330-3.13.0a5+-d1a7b3a-JIT/bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-d1a7b3a.json: unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: unknown