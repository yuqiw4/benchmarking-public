# Results vs. 3.13.0b2

- fork: brandtbucher
- ref: justin_align
- machine: windows-x86
- commit hash: 790b1f8
- commit date: 2024-03-30
- overall geometric mean: 1.08x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 233 ms                                                              | 252 ms: 1.08x slower                                                          |
| chameleon      | 5.71 ms                                                             | 6.20 ms: 1.09x slower                                                         |
| docutils       | 1.81 sec                                                            | 1.93 sec: 1.07x slower                                                        |
| tornado_http   | 94.3 ms                                                             | 96.9 ms: 1.03x slower                                                         |
| Geometric mean | (ref)                                                               | 1.05x slower                                                                  |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|---------------------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none           | 228 ms                                                              | 234 ms: 1.03x slower                                                          |
| async_tree_none_tg        | 203 ms                                                              | 209 ms: 1.03x slower                                                          |
| async_tree_io             | 530 ms                                                              | 548 ms: 1.03x slower                                                          |
| async_tree_io_tg          | 529 ms                                                              | 547 ms: 1.03x slower                                                          |
| async_tree_memoization    | 275 ms                                                              | 285 ms: 1.03x slower                                                          |
| async_tree_memoization_tg | 254 ms                                                              | 264 ms: 1.04x slower                                                          |
| Geometric mean            | (ref)                                                               | 1.03x slower                                                                  |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pidigits       | 199 ms                                                              | 202 ms: 1.02x slower                                                          |
| float          | 52.4 ms                                                             | 53.6 ms: 1.02x slower                                                         |
| nbody          | 76.9 ms                                                             | 92.1 ms: 1.20x slower                                                         |
| Geometric mean | (ref)                                                               | 1.08x slower                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_dna      | 118 ms                                                              | 119 ms: 1.01x slower                                                          |
| regex_effbot   | 1.88 ms                                                             | 1.92 ms: 1.02x slower                                                         |
| regex_v8       | 15.7 ms                                                             | 16.2 ms: 1.03x slower                                                         |
| regex_compile  | 99.9 ms                                                             | 115 ms: 1.15x slower                                                          |
| Geometric mean | (ref)                                                               | 1.05x slower                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pickle_list          | 3.57 us                                                             | 3.18 us: 1.12x faster                                                         |
| pickle_dict          | 20.8 us                                                             | 19.6 us: 1.06x faster                                                         |
| json_dumps           | 6.84 ms                                                             | 6.70 ms: 1.02x faster                                                         |
| json_loads           | 20.5 us                                                             | 20.1 us: 1.02x faster                                                         |
| unpickle_list        | 2.93 us                                                             | 2.90 us: 1.01x faster                                                         |
| pickle               | 8.07 us                                                             | 8.04 us: 1.00x faster                                                         |
| xml_etree_iterparse  | 64.2 ms                                                             | 64.8 ms: 1.01x slower                                                         |
| xml_etree_process    | 42.1 ms                                                             | 42.6 ms: 1.01x slower                                                         |
| tomli_loads          | 1.65 sec                                                            | 1.67 sec: 1.01x slower                                                        |
| xml_etree_generate   | 59.6 ms                                                             | 60.8 ms: 1.02x slower                                                         |
| xml_etree_parse      | 104 ms                                                              | 108 ms: 1.03x slower                                                          |
| pickle_pure_python   | 213 us                                                              | 221 us: 1.04x slower                                                          |
| unpickle_pure_python | 147 us                                                              | 166 us: 1.13x slower                                                          |
| Geometric mean       | (ref)                                                               | 1.00x slower                                                                  |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|------------------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 22.2 ms                                                             | 24.2 ms: 1.09x slower                                                         |
| python_startup_no_site | 18.2 ms                                                             | 21.8 ms: 1.20x slower                                                         |
| Geometric mean         | (ref)                                                               | 1.14x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|-----------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako            | 6.94 ms                                                             | 7.05 ms: 1.02x slower                                                         |
| genshi_text     | 20.1 ms                                                             | 20.8 ms: 1.03x slower                                                         |
| genshi_xml      | 44.3 ms                                                             | 47.0 ms: 1.06x slower                                                         |
| django_template | 30.1 ms                                                             | 33.0 ms: 1.10x slower                                                         |
| Geometric mean  | (ref)                                                               | 1.05x slower                                                                  |

All benchmarks:
===============

| Benchmark                 | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|---------------------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols  | 136 us                                                              | 95.3 us: 1.42x faster                                                         |
| pickle_list               | 3.57 us                                                             | 3.18 us: 1.12x faster                                                         |
| asyncio_tcp               | 662 ms                                                              | 623 ms: 1.06x faster                                                          |
| pickle_dict               | 20.8 us                                                             | 19.6 us: 1.06x faster                                                         |
| coroutines                | 15.5 ms                                                             | 14.9 ms: 1.04x faster                                                         |
| create_gc_cycles          | 756 us                                                              | 738 us: 1.02x faster                                                          |
| sqlite_synth              | 1.96 us                                                             | 1.92 us: 1.02x faster                                                         |
| json_dumps                | 6.84 ms                                                             | 6.70 ms: 1.02x faster                                                         |
| json_loads                | 20.5 us                                                             | 20.1 us: 1.02x faster                                                         |
| unpickle_list             | 2.93 us                                                             | 2.90 us: 1.01x faster                                                         |
| asyncio_tcp_ssl           | 16.9 sec                                                            | 16.8 sec: 1.01x faster                                                        |
| pickle                    | 8.07 us                                                             | 8.04 us: 1.00x faster                                                         |
| sympy_expand              | 375 ms                                                              | 377 ms: 1.01x slower                                                          |
| gc_traversal              | 1.43 ms                                                             | 1.44 ms: 1.01x slower                                                         |
| xml_etree_iterparse       | 64.2 ms                                                             | 64.8 ms: 1.01x slower                                                         |
| xml_etree_process         | 42.1 ms                                                             | 42.6 ms: 1.01x slower                                                         |
| regex_dna                 | 118 ms                                                              | 119 ms: 1.01x slower                                                          |
| deepcopy_reduce           | 2.59 us                                                             | 2.62 us: 1.01x slower                                                         |
| tomli_loads               | 1.65 sec                                                            | 1.67 sec: 1.01x slower                                                        |
| mako                      | 6.94 ms                                                             | 7.05 ms: 1.02x slower                                                         |
| regex_effbot              | 1.88 ms                                                             | 1.92 ms: 1.02x slower                                                         |
| pidigits                  | 199 ms                                                              | 202 ms: 1.02x slower                                                          |
| xml_etree_generate        | 59.6 ms                                                             | 60.8 ms: 1.02x slower                                                         |
| sqlglot_parse             | 964 us                                                              | 983 us: 1.02x slower                                                          |
| bench_thread_pool         | 985 us                                                              | 1.01 ms: 1.02x slower                                                         |
| json                      | 4.10 ms                                                             | 4.19 ms: 1.02x slower                                                         |
| pylint                    | 217 ms                                                              | 222 ms: 1.02x slower                                                          |
| float                     | 52.4 ms                                                             | 53.6 ms: 1.02x slower                                                         |
| sympy_str                 | 211 ms                                                              | 216 ms: 1.03x slower                                                          |
| tornado_http              | 94.3 ms                                                             | 96.9 ms: 1.03x slower                                                         |
| async_tree_none           | 228 ms                                                              | 234 ms: 1.03x slower                                                          |
| async_tree_none_tg        | 203 ms                                                              | 209 ms: 1.03x slower                                                          |
| xml_etree_parse           | 104 ms                                                              | 108 ms: 1.03x slower                                                          |
| regex_v8                  | 15.7 ms                                                             | 16.2 ms: 1.03x slower                                                         |
| async_tree_io             | 530 ms                                                              | 548 ms: 1.03x slower                                                          |
| async_tree_io_tg          | 529 ms                                                              | 547 ms: 1.03x slower                                                          |
| async_tree_memoization    | 275 ms                                                              | 285 ms: 1.03x slower                                                          |
| pathlib                   | 83.9 ms                                                             | 86.7 ms: 1.03x slower                                                         |
| genshi_text               | 20.1 ms                                                             | 20.8 ms: 1.03x slower                                                         |
| spectral_norm             | 68.0 ms                                                             | 70.4 ms: 1.04x slower                                                         |
| sympy_sum                 | 105 ms                                                              | 109 ms: 1.04x slower                                                          |
| sqlglot_transpile         | 1.19 ms                                                             | 1.24 ms: 1.04x slower                                                         |
| pickle_pure_python        | 213 us                                                              | 221 us: 1.04x slower                                                          |
| bench_mp_pool             | 69.4 ms                                                             | 72.1 ms: 1.04x slower                                                         |
| async_tree_memoization_tg | 254 ms                                                              | 264 ms: 1.04x slower                                                          |
| logging_silent            | 57.9 ns                                                             | 60.7 ns: 1.05x slower                                                         |
| deepcopy                  | 280 us                                                              | 294 us: 1.05x slower                                                          |
| genshi_xml                | 44.3 ms                                                             | 47.0 ms: 1.06x slower                                                         |
| telco                     | 6.03 ms                                                             | 6.41 ms: 1.06x slower                                                         |
| docutils                  | 1.81 sec                                                            | 1.93 sec: 1.07x slower                                                        |
| 2to3                      | 233 ms                                                              | 252 ms: 1.08x slower                                                          |
| deepcopy_memo             | 23.5 us                                                             | 25.5 us: 1.08x slower                                                         |
| chameleon                 | 5.71 ms                                                             | 6.20 ms: 1.09x slower                                                         |
| scimark_sparse_mat_mult   | 2.87 ms                                                             | 3.12 ms: 1.09x slower                                                         |
| python_startup            | 22.2 ms                                                             | 24.2 ms: 1.09x slower                                                         |
| generators                | 21.2 ms                                                             | 23.2 ms: 1.10x slower                                                         |
| logging_format            | 8.13 us                                                             | 8.92 us: 1.10x slower                                                         |
| django_template           | 30.1 ms                                                             | 33.0 ms: 1.10x slower                                                         |
| mdp                       | 1.60 sec                                                            | 1.76 sec: 1.10x slower                                                        |
| meteor_contest            | 74.1 ms                                                             | 81.6 ms: 1.10x slower                                                         |
| sympy_integrate           | 14.6 ms                                                             | 16.2 ms: 1.10x slower                                                         |
| async_generators          | 266 ms                                                              | 294 ms: 1.11x slower                                                          |
| pycparser                 | 777 ms                                                              | 865 ms: 1.11x slower                                                          |
| logging_simple            | 7.47 us                                                             | 8.34 us: 1.12x slower                                                         |
| unpickle_pure_python      | 147 us                                                              | 166 us: 1.13x slower                                                          |
| crypto_pyaes              | 55.8 ms                                                             | 63.2 ms: 1.13x slower                                                         |
| deltablue                 | 2.23 ms                                                             | 2.55 ms: 1.14x slower                                                         |
| sqlglot_optimize          | 39.7 ms                                                             | 45.7 ms: 1.15x slower                                                         |
| regex_compile             | 99.9 ms                                                             | 115 ms: 1.15x slower                                                          |
| sqlglot_normalize         | 206 ms                                                              | 238 ms: 1.15x slower                                                          |
| thrift                    | 9.73 ms                                                             | 11.2 ms: 1.15x slower                                                         |
| fannkuch                  | 270 ms                                                              | 317 ms: 1.17x slower                                                          |
| scimark_sor               | 81.0 ms                                                             | 95.6 ms: 1.18x slower                                                         |
| pyflate                   | 308 ms                                                              | 364 ms: 1.18x slower                                                          |
| richards                  | 31.2 ms                                                             | 37.0 ms: 1.18x slower                                                         |
| richards_super            | 35.5 ms                                                             | 42.1 ms: 1.19x slower                                                         |
| scimark_fft               | 198 ms                                                              | 236 ms: 1.19x slower                                                          |
| pprint_pformat            | 1.24 sec                                                            | 1.48 sec: 1.20x slower                                                        |
| python_startup_no_site    | 18.2 ms                                                             | 21.8 ms: 1.20x slower                                                         |
| nbody                     | 76.9 ms                                                             | 92.1 ms: 1.20x slower                                                         |
| go                        | 101 ms                                                              | 121 ms: 1.20x slower                                                          |
| pprint_safe_repr          | 607 ms                                                              | 727 ms: 1.20x slower                                                          |
| comprehensions            | 11.9 us                                                             | 15.1 us: 1.27x slower                                                         |
| chaos                     | 48.0 ms                                                             | 61.8 ms: 1.29x slower                                                         |
| nqueens                   | 68.7 ms                                                             | 90.5 ms: 1.32x slower                                                         |
| scimark_monte_carlo       | 45.2 ms                                                             | 62.5 ms: 1.38x slower                                                         |
| raytrace                  | 189 ms                                                              | 265 ms: 1.40x slower                                                          |
| scimark_lu                | 59.4 ms                                                             | 86.1 ms: 1.45x slower                                                         |
| hexiom                    | 4.23 ms                                                             | 6.36 ms: 1.50x slower                                                         |
| coverage                  | 307 ms                                                              | 477 ms: 1.55x slower                                                          |
| Geometric mean            | (ref)                                                               | 1.08x slower                                                                  |

Benchmark hidden because not significant (4): unpickle, html5lib, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17.json: flaskblogging
Ignored benchmarks (1) of results/bm-20240330-3.13.0a5+-790b1f8-JIT/bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-790b1f8.json: unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: unknown