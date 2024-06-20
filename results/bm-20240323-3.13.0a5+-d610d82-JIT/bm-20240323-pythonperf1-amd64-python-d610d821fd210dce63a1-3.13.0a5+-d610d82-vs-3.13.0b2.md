# Results vs. 3.13.0b2

- fork: python
- ref: d610d821fd210dce63a1
- machine: windows-amd64
- commit hash: d610d82
- commit date: 2024-03-23
- overall geometric mean: 1.02x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1-amd64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 207 ms                                                          | 220 ms: 1.06x slower                                                        |
| chameleon      | 4.80 ms                                                         | 4.58 ms: 1.05x faster                                                       |
| docutils       | 1.63 sec                                                        | 1.68 sec: 1.03x slower                                                      |
| html5lib       | 35.0 ms                                                         | 35.8 ms: 1.02x slower                                                       |
| tornado_http   | 81.8 ms                                                         | 85.1 ms: 1.04x slower                                                       |
| Geometric mean | (ref)                                                           | 1.02x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1-amd64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|---------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_io_tg          | 605 ms                                                          | 563 ms: 1.08x faster                                                        |
| async_tree_none_tg        | 202 ms                                                          | 208 ms: 1.03x slower                                                        |
| async_tree_memoization    | 264 ms                                                          | 275 ms: 1.04x slower                                                        |
| async_tree_memoization_tg | 258 ms                                                          | 270 ms: 1.05x slower                                                        |
| Geometric mean            | (ref)                                                           | 1.01x slower                                                                |

Benchmark hidden because not significant (4): async_tree_cpu_io_mixed, async_tree_io, async_tree_cpu_io_mixed_tg, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1-amd64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 67.6 ms                                                         | 57.0 ms: 1.19x faster                                                       |
| float          | 49.7 ms                                                         | 46.2 ms: 1.08x faster                                                       |
| Geometric mean | (ref)                                                           | 1.08x faster                                                                |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1-amd64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.58 ms                                                         | 1.60 ms: 1.01x slower                                                       |
| regex_dna      | 119 ms                                                          | 121 ms: 1.02x slower                                                        |
| regex_compile  | 78.0 ms                                                         | 83.7 ms: 1.07x slower                                                       |
| Geometric mean | (ref)                                                           | 1.02x slower                                                                |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1-amd64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| tomli_loads          | 1.35 sec                                                        | 1.20 sec: 1.13x faster                                                      |
| pickle_dict          | 18.1 us                                                         | 17.4 us: 1.04x faster                                                       |
| json_loads           | 14.2 us                                                         | 13.8 us: 1.03x faster                                                       |
| pickle_pure_python   | 175 us                                                          | 173 us: 1.01x faster                                                        |
| xml_etree_generate   | 53.2 ms                                                         | 52.6 ms: 1.01x faster                                                       |
| xml_etree_iterparse  | 62.3 ms                                                         | 61.8 ms: 1.01x faster                                                       |
| xml_etree_process    | 36.4 ms                                                         | 36.2 ms: 1.01x faster                                                       |
| json_dumps           | 5.61 ms                                                         | 5.59 ms: 1.00x faster                                                       |
| xml_etree_parse      | 90.9 ms                                                         | 92.2 ms: 1.01x slower                                                       |
| unpickle             | 8.40 us                                                         | 8.67 us: 1.03x slower                                                       |
| pickle               | 7.11 us                                                         | 7.36 us: 1.03x slower                                                       |
| unpickle_pure_python | 122 us                                                          | 126 us: 1.04x slower                                                        |
| unpickle_list        | 2.62 us                                                         | 2.78 us: 1.06x slower                                                       |
| Geometric mean       | (ref)                                                           | 1.00x faster                                                                |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1-amd64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 20.3 ms                                                         | 23.2 ms: 1.14x slower                                                       |
| python_startup_no_site | 16.2 ms                                                         | 20.8 ms: 1.29x slower                                                       |
| Geometric mean         | (ref)                                                           | 1.21x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1-amd64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|-----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 6.36 ms                                                         | 5.71 ms: 1.11x faster                                                       |
| genshi_text     | 14.4 ms                                                         | 15.1 ms: 1.05x slower                                                       |
| django_template | 21.7 ms                                                         | 23.2 ms: 1.07x slower                                                       |
| genshi_xml      | 31.6 ms                                                         | 35.4 ms: 1.12x slower                                                       |
| Geometric mean  | (ref)                                                           | 1.03x slower                                                                |

All benchmarks:
===============

| Benchmark                 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1-amd64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|---------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols  | 101 us                                                          | 69.9 us: 1.44x faster                                                       |
| spectral_norm             | 63.7 ms                                                         | 50.9 ms: 1.25x faster                                                       |
| create_gc_cycles          | 888 us                                                          | 733 us: 1.21x faster                                                        |
| nbody                     | 67.6 ms                                                         | 57.0 ms: 1.19x faster                                                       |
| tomli_loads               | 1.35 sec                                                        | 1.20 sec: 1.13x faster                                                      |
| scimark_sparse_mat_mult   | 2.50 ms                                                         | 2.23 ms: 1.12x faster                                                       |
| pycparser                 | 754 ms                                                          | 676 ms: 1.11x faster                                                        |
| mako                      | 6.36 ms                                                         | 5.71 ms: 1.11x faster                                                       |
| json                      | 3.19 ms                                                         | 2.90 ms: 1.10x faster                                                       |
| fannkuch                  | 243 ms                                                          | 222 ms: 1.10x faster                                                        |
| float                     | 49.7 ms                                                         | 46.2 ms: 1.08x faster                                                       |
| async_tree_io_tg          | 605 ms                                                          | 563 ms: 1.08x faster                                                        |
| gc_traversal              | 1.55 ms                                                         | 1.48 ms: 1.05x faster                                                       |
| crypto_pyaes              | 45.5 ms                                                         | 43.3 ms: 1.05x faster                                                       |
| chameleon                 | 4.80 ms                                                         | 4.58 ms: 1.05x faster                                                       |
| deepcopy_memo             | 22.1 us                                                         | 21.2 us: 1.04x faster                                                       |
| pickle_dict               | 18.1 us                                                         | 17.4 us: 1.04x faster                                                       |
| deepcopy_reduce           | 1.99 us                                                         | 1.94 us: 1.03x faster                                                       |
| json_loads                | 14.2 us                                                         | 13.8 us: 1.03x faster                                                       |
| pickle_pure_python        | 175 us                                                          | 173 us: 1.01x faster                                                        |
| xml_etree_generate        | 53.2 ms                                                         | 52.6 ms: 1.01x faster                                                       |
| scimark_fft               | 171 ms                                                          | 169 ms: 1.01x faster                                                        |
| xml_etree_iterparse       | 62.3 ms                                                         | 61.8 ms: 1.01x faster                                                       |
| xml_etree_process         | 36.4 ms                                                         | 36.2 ms: 1.01x faster                                                       |
| json_dumps                | 5.61 ms                                                         | 5.59 ms: 1.00x faster                                                       |
| pprint_safe_repr          | 474 ms                                                          | 476 ms: 1.01x slower                                                        |
| regex_effbot              | 1.58 ms                                                         | 1.60 ms: 1.01x slower                                                       |
| pprint_pformat            | 966 ms                                                          | 975 ms: 1.01x slower                                                        |
| aiohttp                   | 889 us                                                          | 899 us: 1.01x slower                                                        |
| xml_etree_parse           | 90.9 ms                                                         | 92.2 ms: 1.01x slower                                                       |
| pathlib                   | 75.9 ms                                                         | 76.9 ms: 1.01x slower                                                       |
| pyflate                   | 279 ms                                                          | 283 ms: 1.02x slower                                                        |
| regex_dna                 | 119 ms                                                          | 121 ms: 1.02x slower                                                        |
| html5lib                  | 35.0 ms                                                         | 35.8 ms: 1.02x slower                                                       |
| telco                     | 4.67 ms                                                         | 4.77 ms: 1.02x slower                                                       |
| chaos                     | 38.4 ms                                                         | 39.3 ms: 1.02x slower                                                       |
| logging_format            | 6.22 us                                                         | 6.39 us: 1.03x slower                                                       |
| async_tree_none_tg        | 202 ms                                                          | 208 ms: 1.03x slower                                                        |
| logging_simple            | 5.78 us                                                         | 5.96 us: 1.03x slower                                                       |
| unpickle                  | 8.40 us                                                         | 8.67 us: 1.03x slower                                                       |
| docutils                  | 1.63 sec                                                        | 1.68 sec: 1.03x slower                                                      |
| pickle                    | 7.11 us                                                         | 7.36 us: 1.03x slower                                                       |
| sympy_str                 | 159 ms                                                          | 165 ms: 1.04x slower                                                        |
| logging_silent            | 52.9 ns                                                         | 54.8 ns: 1.04x slower                                                       |
| unpickle_pure_python      | 122 us                                                          | 126 us: 1.04x slower                                                        |
| tornado_http              | 81.8 ms                                                         | 85.1 ms: 1.04x slower                                                       |
| async_tree_memoization    | 264 ms                                                          | 275 ms: 1.04x slower                                                        |
| comprehensions            | 10.4 us                                                         | 10.8 us: 1.04x slower                                                       |
| sympy_sum                 | 84.4 ms                                                         | 87.9 ms: 1.04x slower                                                       |
| generators                | 19.6 ms                                                         | 20.4 ms: 1.04x slower                                                       |
| richards_super            | 30.2 ms                                                         | 31.5 ms: 1.04x slower                                                       |
| async_tree_memoization_tg | 258 ms                                                          | 270 ms: 1.05x slower                                                        |
| sqlglot_parse             | 748 us                                                          | 783 us: 1.05x slower                                                        |
| sqlglot_transpile         | 955 us                                                          | 1.00 ms: 1.05x slower                                                       |
| richards                  | 26.7 ms                                                         | 28.0 ms: 1.05x slower                                                       |
| sympy_expand              | 271 ms                                                          | 284 ms: 1.05x slower                                                        |
| genshi_text               | 14.4 ms                                                         | 15.1 ms: 1.05x slower                                                       |
| sqlglot_normalize         | 173 ms                                                          | 183 ms: 1.06x slower                                                        |
| scimark_monte_carlo       | 39.1 ms                                                         | 41.3 ms: 1.06x slower                                                       |
| unpickle_list             | 2.62 us                                                         | 2.78 us: 1.06x slower                                                       |
| coroutines                | 12.8 ms                                                         | 13.5 ms: 1.06x slower                                                       |
| bench_mp_pool             | 64.8 ms                                                         | 68.7 ms: 1.06x slower                                                       |
| meteor_contest            | 69.9 ms                                                         | 74.2 ms: 1.06x slower                                                       |
| 2to3                      | 207 ms                                                          | 220 ms: 1.06x slower                                                        |
| dulwich_log               | 38.0 ms                                                         | 40.6 ms: 1.07x slower                                                       |
| django_template           | 21.7 ms                                                         | 23.2 ms: 1.07x slower                                                       |
| nqueens                   | 56.7 ms                                                         | 60.7 ms: 1.07x slower                                                       |
| regex_compile             | 78.0 ms                                                         | 83.7 ms: 1.07x slower                                                       |
| sympy_integrate           | 12.2 ms                                                         | 13.2 ms: 1.08x slower                                                       |
| scimark_sor               | 75.3 ms                                                         | 81.3 ms: 1.08x slower                                                       |
| sqlglot_optimize          | 32.7 ms                                                         | 35.4 ms: 1.08x slower                                                       |
| bench_thread_pool         | 768 us                                                          | 837 us: 1.09x slower                                                        |
| thrift                    | 8.11 ms                                                         | 8.86 ms: 1.09x slower                                                       |
| async_generators          | 223 ms                                                          | 244 ms: 1.09x slower                                                        |
| coverage                  | 42.1 ms                                                         | 46.4 ms: 1.10x slower                                                       |
| deltablue                 | 1.88 ms                                                         | 2.08 ms: 1.10x slower                                                       |
| mypy2                     | 418 ms                                                          | 462 ms: 1.10x slower                                                        |
| raytrace                  | 162 ms                                                          | 181 ms: 1.12x slower                                                        |
| genshi_xml                | 31.6 ms                                                         | 35.4 ms: 1.12x slower                                                       |
| asyncio_tcp_ssl           | 1.48 sec                                                        | 1.67 sec: 1.12x slower                                                      |
| go                        | 82.1 ms                                                         | 92.6 ms: 1.13x slower                                                       |
| python_startup            | 20.3 ms                                                         | 23.2 ms: 1.14x slower                                                       |
| hexiom                    | 3.72 ms                                                         | 4.37 ms: 1.17x slower                                                       |
| mdp                       | 1.31 sec                                                        | 1.55 sec: 1.18x slower                                                      |
| scimark_lu                | 56.6 ms                                                         | 70.4 ms: 1.24x slower                                                       |
| python_startup_no_site    | 16.2 ms                                                         | 20.8 ms: 1.29x slower                                                       |
| Geometric mean            | (ref)                                                           | 1.02x slower                                                                |

Benchmark hidden because not significant (11): regex_v8, asyncio_tcp, pickle_list, async_tree_cpu_io_mixed, sqlite_synth, async_tree_io, deepcopy, pidigits, async_tree_cpu_io_mixed_tg, async_tree_none, pylint
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17.json: flaskblogging
Ignored benchmarks (1) of results/bm-20240323-3.13.0a5+-d610d82-JIT/bm-20240323-pythonperf1-amd64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82.json: unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: unknown