# Results vs. 3.13.0b2

- fork: python
- ref: d610d821fd210dce63a1
- machine: windows-amd64
- commit hash: d610d82
- commit date: 2024-03-23
- overall geometric mean: 1.01x slower
- HPT reliability: 99.92%
- HPT 99th percentile: 1.00x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1-amd64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 207 ms                                                          | 210 ms: 1.01x slower                                                        |
| chameleon      | 4.80 ms                                                         | 4.74 ms: 1.01x faster                                                       |
| docutils       | 1.63 sec                                                        | 1.62 sec: 1.01x faster                                                      |
| html5lib       | 35.0 ms                                                         | 36.3 ms: 1.04x slower                                                       |
| tornado_http   | 81.8 ms                                                         | 83.2 ms: 1.02x slower                                                       |
| Geometric mean | (ref)                                                           | 1.01x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1-amd64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|---------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_io_tg          | 605 ms                                                          | 563 ms: 1.08x faster                                                        |
| async_tree_cpu_io_mixed   | 389 ms                                                          | 381 ms: 1.02x faster                                                        |
| async_tree_none_tg        | 202 ms                                                          | 208 ms: 1.03x slower                                                        |
| async_tree_memoization    | 264 ms                                                          | 276 ms: 1.04x slower                                                        |
| async_tree_memoization_tg | 258 ms                                                          | 271 ms: 1.05x slower                                                        |
| Geometric mean            | (ref)                                                           | 1.01x slower                                                                |

Benchmark hidden because not significant (3): async_tree_io, async_tree_cpu_io_mixed_tg, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1-amd64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 150 ms                                                          | 147 ms: 1.02x faster                                                        |
| nbody          | 67.6 ms                                                         | 68.6 ms: 1.01x slower                                                       |
| float          | 49.7 ms                                                         | 52.7 ms: 1.06x slower                                                       |
| Geometric mean | (ref)                                                           | 1.02x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1-amd64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_v8       | 15.8 ms                                                         | 14.3 ms: 1.10x faster                                                       |
| regex_dna      | 119 ms                                                          | 116 ms: 1.02x faster                                                        |
| regex_compile  | 78.0 ms                                                         | 76.8 ms: 1.02x faster                                                       |
| regex_effbot   | 1.58 ms                                                         | 1.57 ms: 1.01x faster                                                       |
| Geometric mean | (ref)                                                           | 1.04x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1-amd64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_loads           | 14.2 us                                                         | 13.8 us: 1.02x faster                                                       |
| pickle_list          | 2.90 us                                                         | 2.84 us: 1.02x faster                                                       |
| xml_etree_process    | 36.4 ms                                                         | 36.8 ms: 1.01x slower                                                       |
| xml_etree_parse      | 90.9 ms                                                         | 91.9 ms: 1.01x slower                                                       |
| xml_etree_iterparse  | 62.3 ms                                                         | 63.3 ms: 1.02x slower                                                       |
| pickle_pure_python   | 175 us                                                          | 179 us: 1.02x slower                                                        |
| unpickle_list        | 2.62 us                                                         | 2.69 us: 1.03x slower                                                       |
| unpickle_pure_python | 122 us                                                          | 127 us: 1.05x slower                                                        |
| pickle               | 7.11 us                                                         | 7.44 us: 1.05x slower                                                       |
| pickle_dict          | 18.1 us                                                         | 19.0 us: 1.05x slower                                                       |
| tomli_loads          | 1.35 sec                                                        | 1.42 sec: 1.05x slower                                                      |
| Geometric mean       | (ref)                                                           | 1.02x slower                                                                |

Benchmark hidden because not significant (3): unpickle, json_dumps, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1-amd64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 16.2 ms                                                         | 18.7 ms: 1.15x slower                                                       |
| Geometric mean         | (ref)                                                           | 1.07x slower                                                                |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1-amd64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako           | 6.36 ms                                                         | 6.23 ms: 1.02x faster                                                       |
| genshi_text    | 14.4 ms                                                         | 15.8 ms: 1.10x slower                                                       |
| genshi_xml     | 31.6 ms                                                         | 35.0 ms: 1.11x slower                                                       |
| Geometric mean | (ref)                                                           | 1.04x slower                                                                |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1-amd64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|---------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols  | 101 us                                                          | 70.7 us: 1.43x faster                                                       |
| create_gc_cycles          | 888 us                                                          | 717 us: 1.24x faster                                                        |
| pycparser                 | 754 ms                                                          | 663 ms: 1.14x faster                                                        |
| regex_v8                  | 15.8 ms                                                         | 14.3 ms: 1.10x faster                                                       |
| json                      | 3.19 ms                                                         | 2.92 ms: 1.09x faster                                                       |
| async_tree_io_tg          | 605 ms                                                          | 563 ms: 1.08x faster                                                        |
| gc_traversal              | 1.55 ms                                                         | 1.46 ms: 1.06x faster                                                       |
| crypto_pyaes              | 45.5 ms                                                         | 43.2 ms: 1.05x faster                                                       |
| spectral_norm             | 63.7 ms                                                         | 61.2 ms: 1.04x faster                                                       |
| scimark_sparse_mat_mult   | 2.50 ms                                                         | 2.40 ms: 1.04x faster                                                       |
| scimark_lu                | 56.6 ms                                                         | 54.4 ms: 1.04x faster                                                       |
| json_loads                | 14.2 us                                                         | 13.8 us: 1.02x faster                                                       |
| regex_dna                 | 119 ms                                                          | 116 ms: 1.02x faster                                                        |
| pickle_list               | 2.90 us                                                         | 2.84 us: 1.02x faster                                                       |
| async_tree_cpu_io_mixed   | 389 ms                                                          | 381 ms: 1.02x faster                                                        |
| pidigits                  | 150 ms                                                          | 147 ms: 1.02x faster                                                        |
| mako                      | 6.36 ms                                                         | 6.23 ms: 1.02x faster                                                       |
| bench_mp_pool             | 64.8 ms                                                         | 63.6 ms: 1.02x faster                                                       |
| regex_compile             | 78.0 ms                                                         | 76.8 ms: 1.02x faster                                                       |
| chameleon                 | 4.80 ms                                                         | 4.74 ms: 1.01x faster                                                       |
| regex_effbot              | 1.58 ms                                                         | 1.57 ms: 1.01x faster                                                       |
| sympy_sum                 | 84.4 ms                                                         | 83.5 ms: 1.01x faster                                                       |
| thrift                    | 8.11 ms                                                         | 8.04 ms: 1.01x faster                                                       |
| deepcopy_memo             | 22.1 us                                                         | 21.9 us: 1.01x faster                                                       |
| docutils                  | 1.63 sec                                                        | 1.62 sec: 1.01x faster                                                      |
| scimark_monte_carlo       | 39.1 ms                                                         | 38.9 ms: 1.01x faster                                                       |
| sympy_integrate           | 12.2 ms                                                         | 12.3 ms: 1.00x slower                                                       |
| fannkuch                  | 243 ms                                                          | 244 ms: 1.00x slower                                                        |
| raytrace                  | 162 ms                                                          | 163 ms: 1.01x slower                                                        |
| xml_etree_process         | 36.4 ms                                                         | 36.8 ms: 1.01x slower                                                       |
| sqlite_synth              | 1.60 us                                                         | 1.61 us: 1.01x slower                                                       |
| xml_etree_parse           | 90.9 ms                                                         | 91.9 ms: 1.01x slower                                                       |
| sympy_expand              | 271 ms                                                          | 274 ms: 1.01x slower                                                        |
| nbody                     | 67.6 ms                                                         | 68.6 ms: 1.01x slower                                                       |
| hexiom                    | 3.72 ms                                                         | 3.78 ms: 1.01x slower                                                       |
| 2to3                      | 207 ms                                                          | 210 ms: 1.01x slower                                                        |
| xml_etree_iterparse       | 62.3 ms                                                         | 63.3 ms: 1.02x slower                                                       |
| nqueens                   | 56.7 ms                                                         | 57.6 ms: 1.02x slower                                                       |
| sqlglot_parse             | 748 us                                                          | 761 us: 1.02x slower                                                        |
| pathlib                   | 75.9 ms                                                         | 77.2 ms: 1.02x slower                                                       |
| tornado_http              | 81.8 ms                                                         | 83.2 ms: 1.02x slower                                                       |
| sqlglot_transpile         | 955 us                                                          | 972 us: 1.02x slower                                                        |
| telco                     | 4.67 ms                                                         | 4.75 ms: 1.02x slower                                                       |
| chaos                     | 38.4 ms                                                         | 39.1 ms: 1.02x slower                                                       |
| async_generators          | 223 ms                                                          | 227 ms: 1.02x slower                                                        |
| richards_super            | 30.2 ms                                                         | 30.7 ms: 1.02x slower                                                       |
| pyflate                   | 279 ms                                                          | 284 ms: 1.02x slower                                                        |
| pickle_pure_python        | 175 us                                                          | 179 us: 1.02x slower                                                        |
| richards                  | 26.7 ms                                                         | 27.3 ms: 1.02x slower                                                       |
| async_tree_none_tg        | 202 ms                                                          | 208 ms: 1.03x slower                                                        |
| unpickle_list             | 2.62 us                                                         | 2.69 us: 1.03x slower                                                       |
| go                        | 82.1 ms                                                         | 84.5 ms: 1.03x slower                                                       |
| pprint_safe_repr          | 474 ms                                                          | 489 ms: 1.03x slower                                                        |
| scimark_sor               | 75.3 ms                                                         | 77.7 ms: 1.03x slower                                                       |
| deepcopy_reduce           | 1.99 us                                                         | 2.06 us: 1.03x slower                                                       |
| sqlglot_normalize         | 173 ms                                                          | 179 ms: 1.03x slower                                                        |
| sqlglot_optimize          | 32.7 ms                                                         | 33.8 ms: 1.03x slower                                                       |
| comprehensions            | 10.4 us                                                         | 10.7 us: 1.03x slower                                                       |
| pprint_pformat            | 966 ms                                                          | 1.00 sec: 1.04x slower                                                      |
| deepcopy                  | 220 us                                                          | 227 us: 1.04x slower                                                        |
| html5lib                  | 35.0 ms                                                         | 36.3 ms: 1.04x slower                                                       |
| coroutines                | 12.8 ms                                                         | 13.3 ms: 1.04x slower                                                       |
| meteor_contest            | 69.9 ms                                                         | 72.9 ms: 1.04x slower                                                       |
| logging_format            | 6.22 us                                                         | 6.49 us: 1.04x slower                                                       |
| mypy2                     | 418 ms                                                          | 436 ms: 1.04x slower                                                        |
| async_tree_memoization    | 264 ms                                                          | 276 ms: 1.04x slower                                                        |
| unpickle_pure_python      | 122 us                                                          | 127 us: 1.05x slower                                                        |
| pickle                    | 7.11 us                                                         | 7.44 us: 1.05x slower                                                       |
| logging_silent            | 52.9 ns                                                         | 55.4 ns: 1.05x slower                                                       |
| pickle_dict               | 18.1 us                                                         | 19.0 us: 1.05x slower                                                       |
| async_tree_memoization_tg | 258 ms                                                          | 271 ms: 1.05x slower                                                        |
| bench_thread_pool         | 768 us                                                          | 807 us: 1.05x slower                                                        |
| deltablue                 | 1.88 ms                                                         | 1.98 ms: 1.05x slower                                                       |
| mdp                       | 1.31 sec                                                        | 1.38 sec: 1.05x slower                                                      |
| tomli_loads               | 1.35 sec                                                        | 1.42 sec: 1.05x slower                                                      |
| float                     | 49.7 ms                                                         | 52.7 ms: 1.06x slower                                                       |
| logging_simple            | 5.78 us                                                         | 6.14 us: 1.06x slower                                                       |
| dulwich_log               | 38.0 ms                                                         | 40.5 ms: 1.06x slower                                                       |
| genshi_text               | 14.4 ms                                                         | 15.8 ms: 1.10x slower                                                       |
| genshi_xml                | 31.6 ms                                                         | 35.0 ms: 1.11x slower                                                       |
| coverage                  | 42.1 ms                                                         | 46.9 ms: 1.12x slower                                                       |
| generators                | 19.6 ms                                                         | 22.4 ms: 1.14x slower                                                       |
| python_startup_no_site    | 16.2 ms                                                         | 18.7 ms: 1.15x slower                                                       |
| asyncio_tcp_ssl           | 1.48 sec                                                        | 1.81 sec: 1.22x slower                                                      |
| Geometric mean            | (ref)                                                           | 1.01x slower                                                                |

Benchmark hidden because not significant (13): asyncio_tcp, aiohttp, async_tree_io, python_startup, sympy_str, unpickle, django_template, json_dumps, xml_etree_generate, scimark_fft, async_tree_cpu_io_mixed_tg, async_tree_none, pylint
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17.json: flaskblogging
Ignored benchmarks (1) of results/bm-20240323-3.13.0a5+-d610d82/bm-20240323-pythonperf1-amd64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82.json: unpack_sequence

# HPT report

- Reliability score: 99.92% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: unknown