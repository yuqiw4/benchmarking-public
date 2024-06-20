# Results vs. 3.13.0b2

- fork: brandtbucher
- ref: stitch_exhausted
- machine: windows-x86
- commit hash: 7422720
- commit date: 2024-04-04
- overall geometric mean: 1.09x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| 2to3           | 233 ms                                                              | 266 ms: 1.14x slower                                                              |
| chameleon      | 5.71 ms                                                             | 6.35 ms: 1.11x slower                                                             |
| docutils       | 1.81 sec                                                            | 1.97 sec: 1.09x slower                                                            |
| html5lib       | 45.4 ms                                                             | 46.1 ms: 1.02x slower                                                             |
| tornado_http   | 94.3 ms                                                             | 97.5 ms: 1.03x slower                                                             |
| Geometric mean | (ref)                                                               | 1.08x slower                                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 447 ms                                                              | 460 ms: 1.03x slower                                                              |
| async_tree_io              | 530 ms                                                              | 549 ms: 1.04x slower                                                              |
| async_tree_io_tg           | 529 ms                                                              | 550 ms: 1.04x slower                                                              |
| async_tree_cpu_io_mixed    | 471 ms                                                              | 491 ms: 1.04x slower                                                              |
| async_tree_memoization_tg  | 254 ms                                                              | 269 ms: 1.06x slower                                                              |
| async_tree_memoization     | 275 ms                                                              | 294 ms: 1.07x slower                                                              |
| async_tree_none            | 228 ms                                                              | 244 ms: 1.07x slower                                                              |
| async_tree_none_tg         | 203 ms                                                              | 217 ms: 1.07x slower                                                              |
| Geometric mean             | (ref)                                                               | 1.05x slower                                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| pidigits       | 199 ms                                                              | 197 ms: 1.01x faster                                                              |
| float          | 52.4 ms                                                             | 53.7 ms: 1.03x slower                                                             |
| nbody          | 76.9 ms                                                             | 96.6 ms: 1.26x slower                                                             |
| Geometric mean | (ref)                                                               | 1.09x slower                                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| regex_dna      | 118 ms                                                              | 116 ms: 1.01x faster                                                              |
| regex_effbot   | 1.88 ms                                                             | 1.91 ms: 1.01x slower                                                             |
| regex_v8       | 15.7 ms                                                             | 16.2 ms: 1.03x slower                                                             |
| regex_compile  | 99.9 ms                                                             | 110 ms: 1.10x slower                                                              |
| Geometric mean | (ref)                                                               | 1.03x slower                                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| pickle_list          | 3.57 us                                                             | 3.19 us: 1.12x faster                                                             |
| pickle_dict          | 20.8 us                                                             | 19.8 us: 1.05x faster                                                             |
| unpickle_list        | 2.93 us                                                             | 2.82 us: 1.04x faster                                                             |
| pickle               | 8.07 us                                                             | 7.90 us: 1.02x faster                                                             |
| json_loads           | 20.5 us                                                             | 20.1 us: 1.02x faster                                                             |
| unpickle             | 9.79 us                                                             | 9.93 us: 1.01x slower                                                             |
| xml_etree_iterparse  | 64.2 ms                                                             | 65.2 ms: 1.02x slower                                                             |
| json_dumps           | 6.84 ms                                                             | 6.96 ms: 1.02x slower                                                             |
| xml_etree_parse      | 104 ms                                                              | 108 ms: 1.03x slower                                                              |
| tomli_loads          | 1.65 sec                                                            | 1.70 sec: 1.03x slower                                                            |
| xml_etree_generate   | 59.6 ms                                                             | 62.3 ms: 1.04x slower                                                             |
| pickle_pure_python   | 213 us                                                              | 226 us: 1.06x slower                                                              |
| xml_etree_process    | 42.1 ms                                                             | 44.9 ms: 1.07x slower                                                             |
| unpickle_pure_python | 147 us                                                              | 172 us: 1.17x slower                                                              |
| Geometric mean       | (ref)                                                               | 1.01x slower                                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| python_startup         | 22.2 ms                                                             | 24.3 ms: 1.10x slower                                                             |
| python_startup_no_site | 18.2 ms                                                             | 22.1 ms: 1.21x slower                                                             |
| Geometric mean         | (ref)                                                               | 1.15x slower                                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| mako           | 6.94 ms                                                             | 7.00 ms: 1.01x slower                                                             |
| genshi_xml     | 44.3 ms                                                             | 48.5 ms: 1.10x slower                                                             |
| genshi_text    | 20.1 ms                                                             | 23.8 ms: 1.18x slower                                                             |
| Geometric mean | (ref)                                                               | 1.09x slower                                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------------|:-------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 136 us                                                              | 105 us: 1.29x faster                                                              |
| pickle_list                | 3.57 us                                                             | 3.19 us: 1.12x faster                                                             |
| asyncio_tcp                | 662 ms                                                              | 616 ms: 1.07x faster                                                              |
| pickle_dict                | 20.8 us                                                             | 19.8 us: 1.05x faster                                                             |
| coroutines                 | 15.5 ms                                                             | 14.9 ms: 1.04x faster                                                             |
| unpickle_list              | 2.93 us                                                             | 2.82 us: 1.04x faster                                                             |
| pickle                     | 8.07 us                                                             | 7.90 us: 1.02x faster                                                             |
| json_loads                 | 20.5 us                                                             | 20.1 us: 1.02x faster                                                             |
| regex_dna                  | 118 ms                                                              | 116 ms: 1.01x faster                                                              |
| create_gc_cycles           | 756 us                                                              | 748 us: 1.01x faster                                                              |
| sqlite_synth               | 1.96 us                                                             | 1.95 us: 1.01x faster                                                             |
| pidigits                   | 199 ms                                                              | 197 ms: 1.01x faster                                                              |
| mako                       | 6.94 ms                                                             | 7.00 ms: 1.01x slower                                                             |
| regex_effbot               | 1.88 ms                                                             | 1.91 ms: 1.01x slower                                                             |
| unpickle                   | 9.79 us                                                             | 9.93 us: 1.01x slower                                                             |
| html5lib                   | 45.4 ms                                                             | 46.1 ms: 1.02x slower                                                             |
| xml_etree_iterparse        | 64.2 ms                                                             | 65.2 ms: 1.02x slower                                                             |
| json_dumps                 | 6.84 ms                                                             | 6.96 ms: 1.02x slower                                                             |
| float                      | 52.4 ms                                                             | 53.7 ms: 1.03x slower                                                             |
| async_tree_cpu_io_mixed_tg | 447 ms                                                              | 460 ms: 1.03x slower                                                              |
| xml_etree_parse            | 104 ms                                                              | 108 ms: 1.03x slower                                                              |
| sympy_expand               | 375 ms                                                              | 387 ms: 1.03x slower                                                              |
| regex_v8                   | 15.7 ms                                                             | 16.2 ms: 1.03x slower                                                             |
| tomli_loads                | 1.65 sec                                                            | 1.70 sec: 1.03x slower                                                            |
| pathlib                    | 83.9 ms                                                             | 86.6 ms: 1.03x slower                                                             |
| tornado_http               | 94.3 ms                                                             | 97.5 ms: 1.03x slower                                                             |
| async_tree_io              | 530 ms                                                              | 549 ms: 1.04x slower                                                              |
| generators                 | 21.2 ms                                                             | 21.9 ms: 1.04x slower                                                             |
| spectral_norm              | 68.0 ms                                                             | 70.5 ms: 1.04x slower                                                             |
| async_tree_io_tg           | 529 ms                                                              | 550 ms: 1.04x slower                                                              |
| async_tree_cpu_io_mixed    | 471 ms                                                              | 491 ms: 1.04x slower                                                              |
| xml_etree_generate         | 59.6 ms                                                             | 62.3 ms: 1.04x slower                                                             |
| pylint                     | 217 ms                                                              | 228 ms: 1.05x slower                                                              |
| bench_mp_pool              | 69.4 ms                                                             | 72.8 ms: 1.05x slower                                                             |
| deepcopy_reduce            | 2.59 us                                                             | 2.72 us: 1.05x slower                                                             |
| json                       | 4.10 ms                                                             | 4.32 ms: 1.05x slower                                                             |
| async_generators           | 266 ms                                                              | 280 ms: 1.06x slower                                                              |
| sqlglot_parse              | 964 us                                                              | 1.02 ms: 1.06x slower                                                             |
| logging_silent             | 57.9 ns                                                             | 61.2 ns: 1.06x slower                                                             |
| pickle_pure_python         | 213 us                                                              | 226 us: 1.06x slower                                                              |
| async_tree_memoization_tg  | 254 ms                                                              | 269 ms: 1.06x slower                                                              |
| telco                      | 6.03 ms                                                             | 6.40 ms: 1.06x slower                                                             |
| sympy_str                  | 211 ms                                                              | 224 ms: 1.06x slower                                                              |
| xml_etree_process          | 42.1 ms                                                             | 44.9 ms: 1.07x slower                                                             |
| async_tree_memoization     | 275 ms                                                              | 294 ms: 1.07x slower                                                              |
| async_tree_none            | 228 ms                                                              | 244 ms: 1.07x slower                                                              |
| async_tree_none_tg         | 203 ms                                                              | 217 ms: 1.07x slower                                                              |
| logging_format             | 8.13 us                                                             | 8.72 us: 1.07x slower                                                             |
| pycparser                  | 777 ms                                                              | 837 ms: 1.08x slower                                                              |
| sqlglot_transpile          | 1.19 ms                                                             | 1.28 ms: 1.08x slower                                                             |
| deepcopy                   | 280 us                                                              | 302 us: 1.08x slower                                                              |
| sympy_sum                  | 105 ms                                                              | 114 ms: 1.08x slower                                                              |
| docutils                   | 1.81 sec                                                            | 1.97 sec: 1.09x slower                                                            |
| logging_simple             | 7.47 us                                                             | 8.13 us: 1.09x slower                                                             |
| python_startup             | 22.2 ms                                                             | 24.3 ms: 1.10x slower                                                             |
| genshi_xml                 | 44.3 ms                                                             | 48.5 ms: 1.10x slower                                                             |
| deepcopy_memo              | 23.5 us                                                             | 25.8 us: 1.10x slower                                                             |
| thrift                     | 9.73 ms                                                             | 10.7 ms: 1.10x slower                                                             |
| regex_compile              | 99.9 ms                                                             | 110 ms: 1.10x slower                                                              |
| chameleon                  | 5.71 ms                                                             | 6.35 ms: 1.11x slower                                                             |
| scimark_sparse_mat_mult    | 2.87 ms                                                             | 3.20 ms: 1.11x slower                                                             |
| richards_super             | 35.5 ms                                                             | 39.6 ms: 1.12x slower                                                             |
| richards                   | 31.2 ms                                                             | 34.9 ms: 1.12x slower                                                             |
| meteor_contest             | 74.1 ms                                                             | 83.4 ms: 1.13x slower                                                             |
| crypto_pyaes               | 55.8 ms                                                             | 63.0 ms: 1.13x slower                                                             |
| mdp                        | 1.60 sec                                                            | 1.81 sec: 1.13x slower                                                            |
| go                         | 101 ms                                                              | 114 ms: 1.13x slower                                                              |
| 2to3                       | 233 ms                                                              | 266 ms: 1.14x slower                                                              |
| sympy_integrate            | 14.6 ms                                                             | 17.1 ms: 1.17x slower                                                             |
| unpickle_pure_python       | 147 us                                                              | 172 us: 1.17x slower                                                              |
| pyflate                    | 308 ms                                                              | 362 ms: 1.18x slower                                                              |
| raytrace                   | 189 ms                                                              | 222 ms: 1.18x slower                                                              |
| genshi_text                | 20.1 ms                                                             | 23.8 ms: 1.18x slower                                                             |
| fannkuch                   | 270 ms                                                              | 324 ms: 1.20x slower                                                              |
| scimark_sor                | 81.0 ms                                                             | 97.2 ms: 1.20x slower                                                             |
| sqlglot_optimize           | 39.7 ms                                                             | 48.1 ms: 1.21x slower                                                             |
| python_startup_no_site     | 18.2 ms                                                             | 22.1 ms: 1.21x slower                                                             |
| pprint_safe_repr           | 607 ms                                                              | 735 ms: 1.21x slower                                                              |
| sqlglot_normalize          | 206 ms                                                              | 250 ms: 1.21x slower                                                              |
| scimark_fft                | 198 ms                                                              | 241 ms: 1.22x slower                                                              |
| pprint_pformat             | 1.24 sec                                                            | 1.52 sec: 1.22x slower                                                            |
| deltablue                  | 2.23 ms                                                             | 2.80 ms: 1.25x slower                                                             |
| nbody                      | 76.9 ms                                                             | 96.6 ms: 1.26x slower                                                             |
| chaos                      | 48.0 ms                                                             | 61.0 ms: 1.27x slower                                                             |
| nqueens                    | 68.7 ms                                                             | 95.1 ms: 1.38x slower                                                             |
| scimark_monte_carlo        | 45.2 ms                                                             | 62.7 ms: 1.39x slower                                                             |
| comprehensions             | 11.9 us                                                             | 16.5 us: 1.39x slower                                                             |
| scimark_lu                 | 59.4 ms                                                             | 87.3 ms: 1.47x slower                                                             |
| hexiom                     | 4.23 ms                                                             | 6.60 ms: 1.56x slower                                                             |
| coverage                   | 307 ms                                                              | 503 ms: 1.64x slower                                                              |
| Geometric mean             | (ref)                                                               | 1.09x slower                                                                      |

Benchmark hidden because not significant (3): asyncio_tcp_ssl, gc_traversal, bench_thread_pool
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17.json: django_template, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: unknown