# Results vs. 3.13.0b2

- fork: python
- ref: 550483b7e6c54b2a25d4
- machine: windows-amd64
- commit hash: 550483b
- commit date: 2024-04-22
- overall geometric mean: 1.02x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-pythonperf1-amd64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 207 ms                                                          | 211 ms: 1.02x slower                                                        |
| chameleon      | 4.80 ms                                                         | 4.69 ms: 1.02x faster                                                       |
| docutils       | 1.63 sec                                                        | 1.66 sec: 1.02x slower                                                      |
| html5lib       | 35.0 ms                                                         | 35.7 ms: 1.02x slower                                                       |
| Geometric mean | (ref)                                                           | 1.01x slower                                                                |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-pythonperf1-amd64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b |
|---------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_io_tg          | 605 ms                                                          | 624 ms: 1.03x slower                                                        |
| async_tree_memoization    | 264 ms                                                          | 273 ms: 1.03x slower                                                        |
| async_tree_none           | 218 ms                                                          | 226 ms: 1.04x slower                                                        |
| async_tree_memoization_tg | 258 ms                                                          | 269 ms: 1.04x slower                                                        |
| async_tree_none_tg        | 202 ms                                                          | 222 ms: 1.10x slower                                                        |
| Geometric mean            | (ref)                                                           | 1.03x slower                                                                |

Benchmark hidden because not significant (3): async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-pythonperf1-amd64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 150 ms                                                          | 147 ms: 1.02x faster                                                        |
| nbody          | 67.6 ms                                                         | 69.6 ms: 1.03x slower                                                       |
| float          | 49.7 ms                                                         | 51.9 ms: 1.04x slower                                                       |
| Geometric mean | (ref)                                                           | 1.02x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-pythonperf1-amd64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_dna      | 119 ms                                                          | 115 ms: 1.03x faster                                                        |
| regex_effbot   | 1.58 ms                                                         | 1.56 ms: 1.02x faster                                                       |
| Geometric mean | (ref)                                                           | 1.02x faster                                                                |

Benchmark hidden because not significant (2): regex_v8, regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-pythonperf1-amd64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b |
|----------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_loads           | 14.2 us                                                         | 13.7 us: 1.04x faster                                                       |
| unpickle             | 8.40 us                                                         | 8.24 us: 1.02x faster                                                       |
| pickle               | 7.11 us                                                         | 7.17 us: 1.01x slower                                                       |
| xml_etree_parse      | 90.9 ms                                                         | 91.7 ms: 1.01x slower                                                       |
| pickle_pure_python   | 175 us                                                          | 179 us: 1.02x slower                                                        |
| xml_etree_iterparse  | 62.3 ms                                                         | 63.6 ms: 1.02x slower                                                       |
| pickle_dict          | 18.1 us                                                         | 18.5 us: 1.02x slower                                                       |
| xml_etree_process    | 36.4 ms                                                         | 37.6 ms: 1.03x slower                                                       |
| xml_etree_generate   | 53.2 ms                                                         | 55.0 ms: 1.03x slower                                                       |
| tomli_loads          | 1.35 sec                                                        | 1.40 sec: 1.04x slower                                                      |
| unpickle_pure_python | 122 us                                                          | 128 us: 1.05x slower                                                        |
| pickle_list          | 2.90 us                                                         | 3.06 us: 1.05x slower                                                       |
| unpickle_list        | 2.62 us                                                         | 2.78 us: 1.06x slower                                                       |
| Geometric mean       | (ref)                                                           | 1.02x slower                                                                |

Benchmark hidden because not significant (1): json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-pythonperf1-amd64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup | 20.3 ms                                                         | 19.7 ms: 1.03x faster                                                       |
| Geometric mean | (ref)                                                           | 1.02x faster                                                                |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-pythonperf1-amd64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b |
|-----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| django_template | 21.7 ms                                                         | 21.9 ms: 1.01x slower                                                       |
| genshi_xml      | 31.6 ms                                                         | 33.8 ms: 1.07x slower                                                       |
| genshi_text     | 14.4 ms                                                         | 15.8 ms: 1.10x slower                                                       |
| Geometric mean  | (ref)                                                           | 1.04x slower                                                                |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-pythonperf1-amd64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b |
|---------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols  | 101 us                                                          | 74.1 us: 1.36x faster                                                       |
| json_loads                | 14.2 us                                                         | 13.7 us: 1.04x faster                                                       |
| regex_dna                 | 119 ms                                                          | 115 ms: 1.03x faster                                                        |
| python_startup            | 20.3 ms                                                         | 19.7 ms: 1.03x faster                                                       |
| chameleon                 | 4.80 ms                                                         | 4.69 ms: 1.02x faster                                                       |
| deepcopy_memo             | 22.1 us                                                         | 21.7 us: 1.02x faster                                                       |
| unpickle                  | 8.40 us                                                         | 8.24 us: 1.02x faster                                                       |
| pidigits                  | 150 ms                                                          | 147 ms: 1.02x faster                                                        |
| regex_effbot              | 1.58 ms                                                         | 1.56 ms: 1.02x faster                                                       |
| aiohttp                   | 889 us                                                          | 874 us: 1.02x faster                                                        |
| bench_mp_pool             | 64.8 ms                                                         | 63.7 ms: 1.02x faster                                                       |
| scimark_sor               | 75.3 ms                                                         | 74.2 ms: 1.01x faster                                                       |
| thrift                    | 8.11 ms                                                         | 8.01 ms: 1.01x faster                                                       |
| raytrace                  | 162 ms                                                          | 161 ms: 1.01x faster                                                        |
| gc_traversal              | 1.55 ms                                                         | 1.54 ms: 1.01x faster                                                       |
| crypto_pyaes              | 45.5 ms                                                         | 45.4 ms: 1.00x faster                                                       |
| deepcopy_reduce           | 1.99 us                                                         | 2.01 us: 1.01x slower                                                       |
| pickle                    | 7.11 us                                                         | 7.17 us: 1.01x slower                                                       |
| pathlib                   | 75.9 ms                                                         | 76.5 ms: 1.01x slower                                                       |
| chaos                     | 38.4 ms                                                         | 38.7 ms: 1.01x slower                                                       |
| deepcopy                  | 220 us                                                          | 222 us: 1.01x slower                                                        |
| xml_etree_parse           | 90.9 ms                                                         | 91.7 ms: 1.01x slower                                                       |
| sympy_expand              | 271 ms                                                          | 273 ms: 1.01x slower                                                        |
| sympy_str                 | 159 ms                                                          | 161 ms: 1.01x slower                                                        |
| django_template           | 21.7 ms                                                         | 21.9 ms: 1.01x slower                                                       |
| sqlite_synth              | 1.60 us                                                         | 1.62 us: 1.01x slower                                                       |
| sqlglot_parse             | 748 us                                                          | 760 us: 1.02x slower                                                        |
| sympy_integrate           | 12.2 ms                                                         | 12.5 ms: 1.02x slower                                                       |
| sqlglot_transpile         | 955 us                                                          | 972 us: 1.02x slower                                                        |
| docutils                  | 1.63 sec                                                        | 1.66 sec: 1.02x slower                                                      |
| pickle_pure_python        | 175 us                                                          | 179 us: 1.02x slower                                                        |
| xml_etree_iterparse       | 62.3 ms                                                         | 63.6 ms: 1.02x slower                                                       |
| pickle_dict               | 18.1 us                                                         | 18.5 us: 1.02x slower                                                       |
| html5lib                  | 35.0 ms                                                         | 35.7 ms: 1.02x slower                                                       |
| 2to3                      | 207 ms                                                          | 211 ms: 1.02x slower                                                        |
| scimark_monte_carlo       | 39.1 ms                                                         | 40.0 ms: 1.02x slower                                                       |
| sqlglot_optimize          | 32.7 ms                                                         | 33.6 ms: 1.03x slower                                                       |
| async_generators          | 223 ms                                                          | 230 ms: 1.03x slower                                                        |
| pprint_pformat            | 966 ms                                                          | 994 ms: 1.03x slower                                                        |
| nbody                     | 67.6 ms                                                         | 69.6 ms: 1.03x slower                                                       |
| logging_simple            | 5.78 us                                                         | 5.95 us: 1.03x slower                                                       |
| hexiom                    | 3.72 ms                                                         | 3.84 ms: 1.03x slower                                                       |
| logging_format            | 6.22 us                                                         | 6.41 us: 1.03x slower                                                       |
| async_tree_io_tg          | 605 ms                                                          | 624 ms: 1.03x slower                                                        |
| pprint_safe_repr          | 474 ms                                                          | 489 ms: 1.03x slower                                                        |
| xml_etree_process         | 36.4 ms                                                         | 37.6 ms: 1.03x slower                                                       |
| sqlglot_normalize         | 173 ms                                                          | 179 ms: 1.03x slower                                                        |
| nqueens                   | 56.7 ms                                                         | 58.5 ms: 1.03x slower                                                       |
| async_tree_memoization    | 264 ms                                                          | 273 ms: 1.03x slower                                                        |
| xml_etree_generate        | 53.2 ms                                                         | 55.0 ms: 1.03x slower                                                       |
| coroutines                | 12.8 ms                                                         | 13.2 ms: 1.04x slower                                                       |
| async_tree_none           | 218 ms                                                          | 226 ms: 1.04x slower                                                        |
| richards                  | 26.7 ms                                                         | 27.7 ms: 1.04x slower                                                       |
| tomli_loads               | 1.35 sec                                                        | 1.40 sec: 1.04x slower                                                      |
| dulwich_log               | 38.0 ms                                                         | 39.6 ms: 1.04x slower                                                       |
| async_tree_memoization_tg | 258 ms                                                          | 269 ms: 1.04x slower                                                        |
| float                     | 49.7 ms                                                         | 51.9 ms: 1.04x slower                                                       |
| comprehensions            | 10.4 us                                                         | 10.8 us: 1.04x slower                                                       |
| richards_super            | 30.2 ms                                                         | 31.5 ms: 1.04x slower                                                       |
| pyflate                   | 279 ms                                                          | 291 ms: 1.04x slower                                                        |
| meteor_contest            | 69.9 ms                                                         | 73.0 ms: 1.04x slower                                                       |
| unpickle_pure_python      | 122 us                                                          | 128 us: 1.05x slower                                                        |
| fannkuch                  | 243 ms                                                          | 255 ms: 1.05x slower                                                        |
| telco                     | 4.67 ms                                                         | 4.89 ms: 1.05x slower                                                       |
| deltablue                 | 1.88 ms                                                         | 1.98 ms: 1.05x slower                                                       |
| go                        | 82.1 ms                                                         | 86.3 ms: 1.05x slower                                                       |
| pickle_list               | 2.90 us                                                         | 3.06 us: 1.05x slower                                                       |
| bench_thread_pool         | 768 us                                                          | 810 us: 1.06x slower                                                        |
| unpickle_list             | 2.62 us                                                         | 2.78 us: 1.06x slower                                                       |
| scimark_fft               | 171 ms                                                          | 182 ms: 1.06x slower                                                        |
| genshi_xml                | 31.6 ms                                                         | 33.8 ms: 1.07x slower                                                       |
| scimark_sparse_mat_mult   | 2.50 ms                                                         | 2.70 ms: 1.08x slower                                                       |
| coverage                  | 42.1 ms                                                         | 46.0 ms: 1.09x slower                                                       |
| async_tree_none_tg        | 202 ms                                                          | 222 ms: 1.10x slower                                                        |
| genshi_text               | 14.4 ms                                                         | 15.8 ms: 1.10x slower                                                       |
| mdp                       | 1.31 sec                                                        | 1.46 sec: 1.12x slower                                                      |
| logging_silent            | 52.9 ns                                                         | 59.1 ns: 1.12x slower                                                       |
| generators                | 19.6 ms                                                         | 22.1 ms: 1.13x slower                                                       |
| asyncio_tcp_ssl           | 1.48 sec                                                        | 1.73 sec: 1.17x slower                                                      |
| Geometric mean            | (ref)                                                           | 1.02x slower                                                                |

Benchmark hidden because not significant (18): json, regex_v8, pycparser, mako, python_startup_no_site, scimark_lu, regex_compile, tornado_http, mypy2, spectral_norm, sympy_sum, json_dumps, async_tree_cpu_io_mixed_tg, create_gc_cycles, asyncio_tcp, pylint, async_tree_cpu_io_mixed, async_tree_io
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17.json: flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: unknown