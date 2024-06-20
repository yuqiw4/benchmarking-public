# Results vs. 3.13.0b2

- fork: brandtbucher
- ref: stitch_exhausted
- machine: windows-x86
- commit hash: 5a3dca4
- commit date: 2024-04-02
- overall geometric mean: 1.10x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| 2to3           | 233 ms                                                              | 264 ms: 1.13x slower                                                              |
| chameleon      | 5.71 ms                                                             | 6.24 ms: 1.09x slower                                                             |
| docutils       | 1.81 sec                                                            | 1.98 sec: 1.09x slower                                                            |
| html5lib       | 45.4 ms                                                             | 45.7 ms: 1.01x slower                                                             |
| tornado_http   | 94.3 ms                                                             | 97.6 ms: 1.03x slower                                                             |
| Geometric mean | (ref)                                                               | 1.07x slower                                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 471 ms                                                              | 480 ms: 1.02x slower                                                              |
| async_tree_cpu_io_mixed_tg | 447 ms                                                              | 457 ms: 1.02x slower                                                              |
| async_tree_none            | 228 ms                                                              | 237 ms: 1.04x slower                                                              |
| async_tree_none_tg         | 203 ms                                                              | 212 ms: 1.04x slower                                                              |
| async_tree_io_tg           | 529 ms                                                              | 552 ms: 1.04x slower                                                              |
| async_tree_io              | 530 ms                                                              | 553 ms: 1.04x slower                                                              |
| async_tree_memoization     | 275 ms                                                              | 289 ms: 1.05x slower                                                              |
| async_tree_memoization_tg  | 254 ms                                                              | 267 ms: 1.05x slower                                                              |
| Geometric mean             | (ref)                                                               | 1.04x slower                                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| pidigits       | 199 ms                                                              | 198 ms: 1.00x faster                                                              |
| float          | 52.4 ms                                                             | 53.7 ms: 1.02x slower                                                             |
| nbody          | 76.9 ms                                                             | 98.7 ms: 1.28x slower                                                             |
| Geometric mean | (ref)                                                               | 1.09x slower                                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| regex_dna      | 118 ms                                                              | 122 ms: 1.03x slower                                                              |
| regex_v8       | 15.7 ms                                                             | 16.3 ms: 1.03x slower                                                             |
| regex_compile  | 99.9 ms                                                             | 115 ms: 1.15x slower                                                              |
| Geometric mean | (ref)                                                               | 1.05x slower                                                                      |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| pickle_list          | 3.57 us                                                             | 3.26 us: 1.09x faster                                                             |
| unpickle_list        | 2.93 us                                                             | 2.76 us: 1.06x faster                                                             |
| pickle_dict          | 20.8 us                                                             | 20.1 us: 1.04x faster                                                             |
| json_loads           | 20.5 us                                                             | 19.8 us: 1.03x faster                                                             |
| unpickle             | 9.79 us                                                             | 9.89 us: 1.01x slower                                                             |
| json_dumps           | 6.84 ms                                                             | 6.91 ms: 1.01x slower                                                             |
| pickle               | 8.07 us                                                             | 8.24 us: 1.02x slower                                                             |
| xml_etree_iterparse  | 64.2 ms                                                             | 66.6 ms: 1.04x slower                                                             |
| pickle_pure_python   | 213 us                                                              | 224 us: 1.05x slower                                                              |
| xml_etree_parse      | 104 ms                                                              | 110 ms: 1.05x slower                                                              |
| tomli_loads          | 1.65 sec                                                            | 1.75 sec: 1.06x slower                                                            |
| xml_etree_generate   | 59.6 ms                                                             | 64.4 ms: 1.08x slower                                                             |
| xml_etree_process    | 42.1 ms                                                             | 46.0 ms: 1.09x slower                                                             |
| unpickle_pure_python | 147 us                                                              | 178 us: 1.21x slower                                                              |
| Geometric mean       | (ref)                                                               | 1.03x slower                                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| python_startup         | 22.2 ms                                                             | 24.2 ms: 1.09x slower                                                             |
| python_startup_no_site | 18.2 ms                                                             | 22.0 ms: 1.21x slower                                                             |
| Geometric mean         | (ref)                                                               | 1.15x slower                                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|-----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| mako            | 6.94 ms                                                             | 7.18 ms: 1.03x slower                                                             |
| genshi_xml      | 44.3 ms                                                             | 49.9 ms: 1.13x slower                                                             |
| genshi_text     | 20.1 ms                                                             | 23.3 ms: 1.16x slower                                                             |
| django_template | 30.1 ms                                                             | 35.3 ms: 1.17x slower                                                             |
| Geometric mean  | (ref)                                                               | 1.12x slower                                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 136 us                                                              | 101 us: 1.34x faster                                                              |
| pickle_list                | 3.57 us                                                             | 3.26 us: 1.09x faster                                                             |
| asyncio_tcp                | 662 ms                                                              | 608 ms: 1.09x faster                                                              |
| coroutines                 | 15.5 ms                                                             | 14.5 ms: 1.07x faster                                                             |
| unpickle_list              | 2.93 us                                                             | 2.76 us: 1.06x faster                                                             |
| pickle_dict                | 20.8 us                                                             | 20.1 us: 1.04x faster                                                             |
| json_loads                 | 20.5 us                                                             | 19.8 us: 1.03x faster                                                             |
| create_gc_cycles           | 756 us                                                              | 737 us: 1.03x faster                                                              |
| sqlite_synth               | 1.96 us                                                             | 1.94 us: 1.01x faster                                                             |
| deepcopy_reduce            | 2.59 us                                                             | 2.57 us: 1.01x faster                                                             |
| pidigits                   | 199 ms                                                              | 198 ms: 1.00x faster                                                              |
| html5lib                   | 45.4 ms                                                             | 45.7 ms: 1.01x slower                                                             |
| unpickle                   | 9.79 us                                                             | 9.89 us: 1.01x slower                                                             |
| json_dumps                 | 6.84 ms                                                             | 6.91 ms: 1.01x slower                                                             |
| async_tree_cpu_io_mixed    | 471 ms                                                              | 480 ms: 1.02x slower                                                              |
| pickle                     | 8.07 us                                                             | 8.24 us: 1.02x slower                                                             |
| async_tree_cpu_io_mixed_tg | 447 ms                                                              | 457 ms: 1.02x slower                                                              |
| float                      | 52.4 ms                                                             | 53.7 ms: 1.02x slower                                                             |
| sympy_expand               | 375 ms                                                              | 386 ms: 1.03x slower                                                              |
| pathlib                    | 83.9 ms                                                             | 86.4 ms: 1.03x slower                                                             |
| regex_dna                  | 118 ms                                                              | 122 ms: 1.03x slower                                                              |
| mako                       | 6.94 ms                                                             | 7.18 ms: 1.03x slower                                                             |
| regex_v8                   | 15.7 ms                                                             | 16.3 ms: 1.03x slower                                                             |
| tornado_http               | 94.3 ms                                                             | 97.6 ms: 1.03x slower                                                             |
| logging_silent             | 57.9 ns                                                             | 59.9 ns: 1.04x slower                                                             |
| spectral_norm              | 68.0 ms                                                             | 70.5 ms: 1.04x slower                                                             |
| xml_etree_iterparse        | 64.2 ms                                                             | 66.6 ms: 1.04x slower                                                             |
| bench_thread_pool          | 985 us                                                              | 1.03 ms: 1.04x slower                                                             |
| async_tree_none            | 228 ms                                                              | 237 ms: 1.04x slower                                                              |
| sqlglot_parse              | 964 us                                                              | 1.00 ms: 1.04x slower                                                             |
| async_tree_none_tg         | 203 ms                                                              | 212 ms: 1.04x slower                                                              |
| async_tree_io_tg           | 529 ms                                                              | 552 ms: 1.04x slower                                                              |
| async_tree_io              | 530 ms                                                              | 553 ms: 1.04x slower                                                              |
| bench_mp_pool              | 69.4 ms                                                             | 72.7 ms: 1.05x slower                                                             |
| async_tree_memoization     | 275 ms                                                              | 289 ms: 1.05x slower                                                              |
| telco                      | 6.03 ms                                                             | 6.32 ms: 1.05x slower                                                             |
| sympy_str                  | 211 ms                                                              | 222 ms: 1.05x slower                                                              |
| pylint                     | 217 ms                                                              | 228 ms: 1.05x slower                                                              |
| pickle_pure_python         | 213 us                                                              | 224 us: 1.05x slower                                                              |
| xml_etree_parse            | 104 ms                                                              | 110 ms: 1.05x slower                                                              |
| async_tree_memoization_tg  | 254 ms                                                              | 267 ms: 1.05x slower                                                              |
| sqlglot_transpile          | 1.19 ms                                                             | 1.26 ms: 1.06x slower                                                             |
| generators                 | 21.2 ms                                                             | 22.4 ms: 1.06x slower                                                             |
| tomli_loads                | 1.65 sec                                                            | 1.75 sec: 1.06x slower                                                            |
| sympy_sum                  | 105 ms                                                              | 112 ms: 1.07x slower                                                              |
| deepcopy                   | 280 us                                                              | 302 us: 1.08x slower                                                              |
| xml_etree_generate         | 59.6 ms                                                             | 64.4 ms: 1.08x slower                                                             |
| python_startup             | 22.2 ms                                                             | 24.2 ms: 1.09x slower                                                             |
| docutils                   | 1.81 sec                                                            | 1.98 sec: 1.09x slower                                                            |
| chameleon                  | 5.71 ms                                                             | 6.24 ms: 1.09x slower                                                             |
| xml_etree_process          | 42.1 ms                                                             | 46.0 ms: 1.09x slower                                                             |
| scimark_sparse_mat_mult    | 2.87 ms                                                             | 3.14 ms: 1.09x slower                                                             |
| mdp                        | 1.60 sec                                                            | 1.76 sec: 1.10x slower                                                            |
| async_generators           | 266 ms                                                              | 294 ms: 1.11x slower                                                              |
| pycparser                  | 777 ms                                                              | 869 ms: 1.12x slower                                                              |
| crypto_pyaes               | 55.8 ms                                                             | 62.7 ms: 1.12x slower                                                             |
| genshi_xml                 | 44.3 ms                                                             | 49.9 ms: 1.13x slower                                                             |
| thrift                     | 9.73 ms                                                             | 11.0 ms: 1.13x slower                                                             |
| logging_format             | 8.13 us                                                             | 9.18 us: 1.13x slower                                                             |
| deepcopy_memo              | 23.5 us                                                             | 26.6 us: 1.13x slower                                                             |
| 2to3                       | 233 ms                                                              | 264 ms: 1.13x slower                                                              |
| richards_super             | 35.5 ms                                                             | 40.4 ms: 1.14x slower                                                             |
| regex_compile              | 99.9 ms                                                             | 115 ms: 1.15x slower                                                              |
| sympy_integrate            | 14.6 ms                                                             | 16.9 ms: 1.15x slower                                                             |
| logging_simple             | 7.47 us                                                             | 8.60 us: 1.15x slower                                                             |
| richards                   | 31.2 ms                                                             | 36.0 ms: 1.15x slower                                                             |
| genshi_text                | 20.1 ms                                                             | 23.3 ms: 1.16x slower                                                             |
| deltablue                  | 2.23 ms                                                             | 2.61 ms: 1.17x slower                                                             |
| django_template            | 30.1 ms                                                             | 35.3 ms: 1.17x slower                                                             |
| meteor_contest             | 74.1 ms                                                             | 87.2 ms: 1.18x slower                                                             |
| sqlglot_optimize           | 39.7 ms                                                             | 47.5 ms: 1.20x slower                                                             |
| pprint_pformat             | 1.24 sec                                                            | 1.48 sec: 1.20x slower                                                            |
| sqlglot_normalize          | 206 ms                                                              | 247 ms: 1.20x slower                                                              |
| fannkuch                   | 270 ms                                                              | 324 ms: 1.20x slower                                                              |
| pprint_safe_repr           | 607 ms                                                              | 732 ms: 1.21x slower                                                              |
| python_startup_no_site     | 18.2 ms                                                             | 22.0 ms: 1.21x slower                                                             |
| pyflate                    | 308 ms                                                              | 372 ms: 1.21x slower                                                              |
| scimark_sor                | 81.0 ms                                                             | 97.9 ms: 1.21x slower                                                             |
| unpickle_pure_python       | 147 us                                                              | 178 us: 1.21x slower                                                              |
| scimark_fft                | 198 ms                                                              | 240 ms: 1.21x slower                                                              |
| nbody                      | 76.9 ms                                                             | 98.7 ms: 1.28x slower                                                             |
| go                         | 101 ms                                                              | 130 ms: 1.29x slower                                                              |
| chaos                      | 48.0 ms                                                             | 62.5 ms: 1.30x slower                                                             |
| scimark_monte_carlo        | 45.2 ms                                                             | 61.7 ms: 1.37x slower                                                             |
| comprehensions             | 11.9 us                                                             | 16.3 us: 1.37x slower                                                             |
| raytrace                   | 189 ms                                                              | 264 ms: 1.40x slower                                                              |
| nqueens                    | 68.7 ms                                                             | 96.7 ms: 1.41x slower                                                             |
| scimark_lu                 | 59.4 ms                                                             | 88.2 ms: 1.49x slower                                                             |
| hexiom                     | 4.23 ms                                                             | 6.65 ms: 1.57x slower                                                             |
| coverage                   | 307 ms                                                              | 490 ms: 1.60x slower                                                              |
| Geometric mean             | (ref)                                                               | 1.10x slower                                                                      |

Benchmark hidden because not significant (4): asyncio_tcp_ssl, gc_traversal, regex_effbot, json
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17.json: flaskblogging
Ignored benchmarks (1) of results/bm-20240402-3.13.0a5+-5a3dca4-JIT/bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4.json: unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: unknown