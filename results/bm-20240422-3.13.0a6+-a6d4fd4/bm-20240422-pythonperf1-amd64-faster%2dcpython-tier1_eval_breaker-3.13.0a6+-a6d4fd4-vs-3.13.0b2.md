# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: tier1_eval_breaker
- machine: windows-amd64
- commit hash: a6d4fd4
- commit date: 2024-04-22
- overall geometric mean: 1.03x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-pythonperf1-amd64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| 2to3           | 207 ms                                                          | 213 ms: 1.03x slower                                                                |
| chameleon      | 4.80 ms                                                         | 4.97 ms: 1.03x slower                                                               |
| docutils       | 1.63 sec                                                        | 1.65 sec: 1.01x slower                                                              |
| html5lib       | 35.0 ms                                                         | 35.6 ms: 1.02x slower                                                               |
| Geometric mean | (ref)                                                           | 1.02x slower                                                                        |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-pythonperf1-amd64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|---------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| async_tree_io_tg          | 605 ms                                                          | 619 ms: 1.02x slower                                                                |
| async_tree_none           | 218 ms                                                          | 224 ms: 1.03x slower                                                                |
| async_tree_memoization    | 264 ms                                                          | 274 ms: 1.04x slower                                                                |
| async_tree_memoization_tg | 258 ms                                                          | 271 ms: 1.05x slower                                                                |
| async_tree_none_tg        | 202 ms                                                          | 220 ms: 1.09x slower                                                                |
| Geometric mean            | (ref)                                                           | 1.03x slower                                                                        |

Benchmark hidden because not significant (3): async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-pythonperf1-amd64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| pidigits       | 150 ms                                                          | 147 ms: 1.02x faster                                                                |
| nbody          | 67.6 ms                                                         | 69.8 ms: 1.03x slower                                                               |
| float          | 49.7 ms                                                         | 51.7 ms: 1.04x slower                                                               |
| Geometric mean | (ref)                                                           | 1.02x slower                                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-pythonperf1-amd64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| regex_effbot   | 1.58 ms                                                         | 1.61 ms: 1.02x slower                                                               |
| regex_dna      | 119 ms                                                          | 121 ms: 1.02x slower                                                                |
| regex_compile  | 78.0 ms                                                         | 80.5 ms: 1.03x slower                                                               |
| Geometric mean | (ref)                                                           | 1.02x slower                                                                        |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-pythonperf1-amd64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| json_loads           | 14.2 us                                                         | 13.8 us: 1.03x faster                                                               |
| xml_etree_parse      | 90.9 ms                                                         | 90.2 ms: 1.01x faster                                                               |
| json_dumps           | 5.61 ms                                                         | 5.66 ms: 1.01x slower                                                               |
| unpickle             | 8.40 us                                                         | 8.49 us: 1.01x slower                                                               |
| pickle               | 7.11 us                                                         | 7.24 us: 1.02x slower                                                               |
| xml_etree_iterparse  | 62.3 ms                                                         | 63.9 ms: 1.03x slower                                                               |
| xml_etree_generate   | 53.2 ms                                                         | 55.0 ms: 1.03x slower                                                               |
| tomli_loads          | 1.35 sec                                                        | 1.40 sec: 1.03x slower                                                              |
| pickle_dict          | 18.1 us                                                         | 18.8 us: 1.04x slower                                                               |
| xml_etree_process    | 36.4 ms                                                         | 37.9 ms: 1.04x slower                                                               |
| pickle_pure_python   | 175 us                                                          | 184 us: 1.05x slower                                                                |
| unpickle_list        | 2.62 us                                                         | 2.76 us: 1.05x slower                                                               |
| unpickle_pure_python | 122 us                                                          | 133 us: 1.09x slower                                                                |
| Geometric mean       | (ref)                                                           | 1.03x slower                                                                        |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-pythonperf1-amd64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| python_startup | 20.3 ms                                                         | 19.8 ms: 1.02x faster                                                               |
| Geometric mean | (ref)                                                           | 1.01x faster                                                                        |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-pythonperf1-amd64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|-----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| mako            | 6.36 ms                                                         | 6.56 ms: 1.03x slower                                                               |
| django_template | 21.7 ms                                                         | 22.5 ms: 1.04x slower                                                               |
| genshi_xml      | 31.6 ms                                                         | 33.6 ms: 1.06x slower                                                               |
| genshi_text     | 14.4 ms                                                         | 15.8 ms: 1.10x slower                                                               |
| Geometric mean  | (ref)                                                           | 1.06x slower                                                                        |

All benchmarks:
===============

| Benchmark                 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-pythonperf1-amd64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|---------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| typing_runtime_protocols  | 101 us                                                          | 74.8 us: 1.35x faster                                                               |
| json                      | 3.19 ms                                                         | 2.87 ms: 1.11x faster                                                               |
| pycparser                 | 754 ms                                                          | 696 ms: 1.08x faster                                                                |
| json_loads                | 14.2 us                                                         | 13.8 us: 1.03x faster                                                               |
| python_startup            | 20.3 ms                                                         | 19.8 ms: 1.02x faster                                                               |
| pidigits                  | 150 ms                                                          | 147 ms: 1.02x faster                                                                |
| raytrace                  | 162 ms                                                          | 160 ms: 1.02x faster                                                                |
| bench_mp_pool             | 64.8 ms                                                         | 64.0 ms: 1.01x faster                                                               |
| xml_etree_parse           | 90.9 ms                                                         | 90.2 ms: 1.01x faster                                                               |
| spectral_norm             | 63.7 ms                                                         | 64.1 ms: 1.01x slower                                                               |
| sympy_sum                 | 84.4 ms                                                         | 85.0 ms: 1.01x slower                                                               |
| pathlib                   | 75.9 ms                                                         | 76.5 ms: 1.01x slower                                                               |
| json_dumps                | 5.61 ms                                                         | 5.66 ms: 1.01x slower                                                               |
| unpickle                  | 8.40 us                                                         | 8.49 us: 1.01x slower                                                               |
| richards_super            | 30.2 ms                                                         | 30.5 ms: 1.01x slower                                                               |
| sqlglot_transpile         | 955 us                                                          | 968 us: 1.01x slower                                                                |
| mypy2                     | 418 ms                                                          | 424 ms: 1.01x slower                                                                |
| docutils                  | 1.63 sec                                                        | 1.65 sec: 1.01x slower                                                              |
| sqlglot_parse             | 748 us                                                          | 760 us: 1.02x slower                                                                |
| crypto_pyaes              | 45.5 ms                                                         | 46.2 ms: 1.02x slower                                                               |
| chaos                     | 38.4 ms                                                         | 39.0 ms: 1.02x slower                                                               |
| deepcopy                  | 220 us                                                          | 223 us: 1.02x slower                                                                |
| pickle                    | 7.11 us                                                         | 7.24 us: 1.02x slower                                                               |
| html5lib                  | 35.0 ms                                                         | 35.6 ms: 1.02x slower                                                               |
| regex_effbot              | 1.58 ms                                                         | 1.61 ms: 1.02x slower                                                               |
| mdp                       | 1.31 sec                                                        | 1.34 sec: 1.02x slower                                                              |
| regex_dna                 | 119 ms                                                          | 121 ms: 1.02x slower                                                                |
| logging_format            | 6.22 us                                                         | 6.35 us: 1.02x slower                                                               |
| pprint_pformat            | 966 ms                                                          | 986 ms: 1.02x slower                                                                |
| deepcopy_reduce           | 1.99 us                                                         | 2.04 us: 1.02x slower                                                               |
| scimark_lu                | 56.6 ms                                                         | 57.9 ms: 1.02x slower                                                               |
| async_tree_io_tg          | 605 ms                                                          | 619 ms: 1.02x slower                                                                |
| xml_etree_iterparse       | 62.3 ms                                                         | 63.9 ms: 1.03x slower                                                               |
| pprint_safe_repr          | 474 ms                                                          | 486 ms: 1.03x slower                                                                |
| sqlglot_normalize         | 173 ms                                                          | 177 ms: 1.03x slower                                                                |
| thrift                    | 8.11 ms                                                         | 8.32 ms: 1.03x slower                                                               |
| logging_simple            | 5.78 us                                                         | 5.94 us: 1.03x slower                                                               |
| async_tree_none           | 218 ms                                                          | 224 ms: 1.03x slower                                                                |
| scimark_sor               | 75.3 ms                                                         | 77.5 ms: 1.03x slower                                                               |
| 2to3                      | 207 ms                                                          | 213 ms: 1.03x slower                                                                |
| sqlglot_optimize          | 32.7 ms                                                         | 33.8 ms: 1.03x slower                                                               |
| sympy_integrate           | 12.2 ms                                                         | 12.6 ms: 1.03x slower                                                               |
| nbody                     | 67.6 ms                                                         | 69.8 ms: 1.03x slower                                                               |
| coroutines                | 12.8 ms                                                         | 13.2 ms: 1.03x slower                                                               |
| regex_compile             | 78.0 ms                                                         | 80.5 ms: 1.03x slower                                                               |
| mako                      | 6.36 ms                                                         | 6.56 ms: 1.03x slower                                                               |
| xml_etree_generate        | 53.2 ms                                                         | 55.0 ms: 1.03x slower                                                               |
| tomli_loads               | 1.35 sec                                                        | 1.40 sec: 1.03x slower                                                              |
| sympy_str                 | 159 ms                                                          | 165 ms: 1.03x slower                                                                |
| chameleon                 | 4.80 ms                                                         | 4.97 ms: 1.03x slower                                                               |
| pickle_dict               | 18.1 us                                                         | 18.8 us: 1.04x slower                                                               |
| sympy_expand              | 271 ms                                                          | 281 ms: 1.04x slower                                                                |
| django_template           | 21.7 ms                                                         | 22.5 ms: 1.04x slower                                                               |
| sqlite_synth              | 1.60 us                                                         | 1.66 us: 1.04x slower                                                               |
| async_tree_memoization    | 264 ms                                                          | 274 ms: 1.04x slower                                                                |
| float                     | 49.7 ms                                                         | 51.7 ms: 1.04x slower                                                               |
| xml_etree_process         | 36.4 ms                                                         | 37.9 ms: 1.04x slower                                                               |
| deepcopy_memo             | 22.1 us                                                         | 23.0 us: 1.04x slower                                                               |
| hexiom                    | 3.72 ms                                                         | 3.90 ms: 1.05x slower                                                               |
| async_tree_memoization_tg | 258 ms                                                          | 271 ms: 1.05x slower                                                                |
| go                        | 82.1 ms                                                         | 86.1 ms: 1.05x slower                                                               |
| pickle_pure_python        | 175 us                                                          | 184 us: 1.05x slower                                                                |
| unpickle_list             | 2.62 us                                                         | 2.76 us: 1.05x slower                                                               |
| bench_thread_pool         | 768 us                                                          | 810 us: 1.05x slower                                                                |
| pyflate                   | 279 ms                                                          | 295 ms: 1.06x slower                                                                |
| nqueens                   | 56.7 ms                                                         | 60.0 ms: 1.06x slower                                                               |
| genshi_xml                | 31.6 ms                                                         | 33.6 ms: 1.06x slower                                                               |
| dulwich_log               | 38.0 ms                                                         | 40.5 ms: 1.06x slower                                                               |
| deltablue                 | 1.88 ms                                                         | 2.00 ms: 1.06x slower                                                               |
| meteor_contest            | 69.9 ms                                                         | 74.3 ms: 1.06x slower                                                               |
| logging_silent            | 52.9 ns                                                         | 56.4 ns: 1.07x slower                                                               |
| fannkuch                  | 243 ms                                                          | 259 ms: 1.07x slower                                                                |
| generators                | 19.6 ms                                                         | 21.0 ms: 1.07x slower                                                               |
| async_generators          | 223 ms                                                          | 240 ms: 1.07x slower                                                                |
| comprehensions            | 10.4 us                                                         | 11.2 us: 1.08x slower                                                               |
| scimark_sparse_mat_mult   | 2.50 ms                                                         | 2.72 ms: 1.09x slower                                                               |
| async_tree_none_tg        | 202 ms                                                          | 220 ms: 1.09x slower                                                                |
| unpickle_pure_python      | 122 us                                                          | 133 us: 1.09x slower                                                                |
| genshi_text               | 14.4 ms                                                         | 15.8 ms: 1.10x slower                                                               |
| scimark_fft               | 171 ms                                                          | 189 ms: 1.10x slower                                                                |
| telco                     | 4.67 ms                                                         | 5.18 ms: 1.11x slower                                                               |
| scimark_monte_carlo       | 39.1 ms                                                         | 44.1 ms: 1.13x slower                                                               |
| coverage                  | 42.1 ms                                                         | 48.1 ms: 1.14x slower                                                               |
| asyncio_tcp_ssl           | 1.48 sec                                                        | 1.70 sec: 1.15x slower                                                              |
| Geometric mean            | (ref)                                                           | 1.03x slower                                                                        |

Benchmark hidden because not significant (13): aiohttp, gc_traversal, richards, tornado_http, create_gc_cycles, python_startup_no_site, pickle_list, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_io, regex_v8, asyncio_tcp, pylint
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17.json: flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: unknown