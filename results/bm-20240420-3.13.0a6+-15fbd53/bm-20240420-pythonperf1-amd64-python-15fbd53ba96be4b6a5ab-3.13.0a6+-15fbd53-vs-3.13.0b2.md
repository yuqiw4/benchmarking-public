# Results vs. 3.13.0b2

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: windows-amd64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.04x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 207 ms                                                          | 211 ms: 1.02x slower                                                        |
| chameleon      | 4.80 ms                                                         | 4.91 ms: 1.02x slower                                                       |
| docutils       | 1.63 sec                                                        | 1.64 sec: 1.01x slower                                                      |
| html5lib       | 35.0 ms                                                         | 36.3 ms: 1.04x slower                                                       |
| Geometric mean | (ref)                                                           | 1.02x slower                                                                |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|---------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed   | 389 ms                                                          | 398 ms: 1.02x slower                                                        |
| async_tree_io_tg          | 605 ms                                                          | 628 ms: 1.04x slower                                                        |
| async_tree_none           | 218 ms                                                          | 227 ms: 1.04x slower                                                        |
| async_tree_memoization    | 264 ms                                                          | 275 ms: 1.04x slower                                                        |
| async_tree_memoization_tg | 258 ms                                                          | 273 ms: 1.06x slower                                                        |
| async_tree_none_tg        | 202 ms                                                          | 223 ms: 1.10x slower                                                        |
| Geometric mean            | (ref)                                                           | 1.04x slower                                                                |

Benchmark hidden because not significant (2): async_tree_io, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 150 ms                                                          | 148 ms: 1.02x faster                                                        |
| float          | 49.7 ms                                                         | 53.0 ms: 1.06x slower                                                       |
| nbody          | 67.6 ms                                                         | 72.4 ms: 1.07x slower                                                       |
| Geometric mean | (ref)                                                           | 1.04x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.58 ms                                                         | 1.60 ms: 1.01x slower                                                       |
| regex_compile  | 78.0 ms                                                         | 79.7 ms: 1.02x slower                                                       |
| regex_dna      | 119 ms                                                          | 125 ms: 1.05x slower                                                        |
| Geometric mean | (ref)                                                           | 1.01x slower                                                                |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_loads           | 14.2 us                                                         | 13.7 us: 1.04x faster                                                       |
| pickle               | 7.11 us                                                         | 7.20 us: 1.01x slower                                                       |
| pickle_dict          | 18.1 us                                                         | 18.4 us: 1.01x slower                                                       |
| unpickle             | 8.40 us                                                         | 8.54 us: 1.02x slower                                                       |
| xml_etree_parse      | 90.9 ms                                                         | 92.9 ms: 1.02x slower                                                       |
| json_dumps           | 5.61 ms                                                         | 5.76 ms: 1.03x slower                                                       |
| unpickle_list        | 2.62 us                                                         | 2.72 us: 1.04x slower                                                       |
| xml_etree_iterparse  | 62.3 ms                                                         | 65.0 ms: 1.04x slower                                                       |
| pickle_pure_python   | 175 us                                                          | 183 us: 1.05x slower                                                        |
| xml_etree_process    | 36.4 ms                                                         | 38.2 ms: 1.05x slower                                                       |
| tomli_loads          | 1.35 sec                                                        | 1.42 sec: 1.05x slower                                                      |
| xml_etree_generate   | 53.2 ms                                                         | 56.2 ms: 1.06x slower                                                       |
| pickle_list          | 2.90 us                                                         | 3.22 us: 1.11x slower                                                       |
| unpickle_pure_python | 122 us                                                          | 135 us: 1.11x slower                                                        |
| Geometric mean       | (ref)                                                           | 1.04x slower                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 16.2 ms                                                         | 16.9 ms: 1.04x slower                                                       |
| Geometric mean         | (ref)                                                           | 1.02x slower                                                                |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 6.36 ms                                                         | 6.46 ms: 1.02x slower                                                       |
| django_template | 21.7 ms                                                         | 22.4 ms: 1.03x slower                                                       |
| genshi_xml      | 31.6 ms                                                         | 35.0 ms: 1.11x slower                                                       |
| genshi_text     | 14.4 ms                                                         | 16.5 ms: 1.15x slower                                                       |
| Geometric mean  | (ref)                                                           | 1.07x slower                                                                |

All benchmarks:
===============

| Benchmark                 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|---------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols  | 101 us                                                          | 74.9 us: 1.35x faster                                                       |
| json                      | 3.19 ms                                                         | 2.87 ms: 1.11x faster                                                       |
| json_loads                | 14.2 us                                                         | 13.7 us: 1.04x faster                                                       |
| pidigits                  | 150 ms                                                          | 148 ms: 1.02x faster                                                        |
| gc_traversal              | 1.55 ms                                                         | 1.54 ms: 1.01x faster                                                       |
| mypy2                     | 418 ms                                                          | 415 ms: 1.01x faster                                                        |
| bench_mp_pool             | 64.8 ms                                                         | 64.3 ms: 1.01x faster                                                       |
| pathlib                   | 75.9 ms                                                         | 75.4 ms: 1.01x faster                                                       |
| thrift                    | 8.11 ms                                                         | 8.13 ms: 1.00x slower                                                       |
| scimark_lu                | 56.6 ms                                                         | 56.9 ms: 1.00x slower                                                       |
| crypto_pyaes              | 45.5 ms                                                         | 45.7 ms: 1.01x slower                                                       |
| spectral_norm             | 63.7 ms                                                         | 64.2 ms: 1.01x slower                                                       |
| docutils                  | 1.63 sec                                                        | 1.64 sec: 1.01x slower                                                      |
| sympy_sum                 | 84.4 ms                                                         | 85.0 ms: 1.01x slower                                                       |
| sqlite_synth              | 1.60 us                                                         | 1.61 us: 1.01x slower                                                       |
| regex_effbot              | 1.58 ms                                                         | 1.60 ms: 1.01x slower                                                       |
| pickle                    | 7.11 us                                                         | 7.20 us: 1.01x slower                                                       |
| pickle_dict               | 18.1 us                                                         | 18.4 us: 1.01x slower                                                       |
| create_gc_cycles          | 888 us                                                          | 901 us: 1.01x slower                                                        |
| sympy_expand              | 271 ms                                                          | 275 ms: 1.02x slower                                                        |
| mako                      | 6.36 ms                                                         | 6.46 ms: 1.02x slower                                                       |
| unpickle                  | 8.40 us                                                         | 8.54 us: 1.02x slower                                                       |
| sympy_str                 | 159 ms                                                          | 162 ms: 1.02x slower                                                        |
| deepcopy_reduce           | 1.99 us                                                         | 2.03 us: 1.02x slower                                                       |
| xml_etree_parse           | 90.9 ms                                                         | 92.9 ms: 1.02x slower                                                       |
| async_tree_cpu_io_mixed   | 389 ms                                                          | 398 ms: 1.02x slower                                                        |
| 2to3                      | 207 ms                                                          | 211 ms: 1.02x slower                                                        |
| regex_compile             | 78.0 ms                                                         | 79.7 ms: 1.02x slower                                                       |
| chameleon                 | 4.80 ms                                                         | 4.91 ms: 1.02x slower                                                       |
| json_dumps                | 5.61 ms                                                         | 5.76 ms: 1.03x slower                                                       |
| deepcopy                  | 220 us                                                          | 226 us: 1.03x slower                                                        |
| sqlglot_normalize         | 173 ms                                                          | 178 ms: 1.03x slower                                                        |
| sqlglot_optimize          | 32.7 ms                                                         | 33.6 ms: 1.03x slower                                                       |
| sympy_integrate           | 12.2 ms                                                         | 12.6 ms: 1.03x slower                                                       |
| django_template           | 21.7 ms                                                         | 22.4 ms: 1.03x slower                                                       |
| async_generators          | 223 ms                                                          | 231 ms: 1.03x slower                                                        |
| sqlglot_transpile         | 955 us                                                          | 988 us: 1.03x slower                                                        |
| mdp                       | 1.31 sec                                                        | 1.36 sec: 1.03x slower                                                      |
| html5lib                  | 35.0 ms                                                         | 36.3 ms: 1.04x slower                                                       |
| chaos                     | 38.4 ms                                                         | 39.8 ms: 1.04x slower                                                       |
| async_tree_io_tg          | 605 ms                                                          | 628 ms: 1.04x slower                                                        |
| unpickle_list             | 2.62 us                                                         | 2.72 us: 1.04x slower                                                       |
| python_startup_no_site    | 16.2 ms                                                         | 16.9 ms: 1.04x slower                                                       |
| logging_format            | 6.22 us                                                         | 6.47 us: 1.04x slower                                                       |
| pprint_pformat            | 966 ms                                                          | 1.01 sec: 1.04x slower                                                      |
| async_tree_none           | 218 ms                                                          | 227 ms: 1.04x slower                                                        |
| pprint_safe_repr          | 474 ms                                                          | 494 ms: 1.04x slower                                                        |
| dulwich_log               | 38.0 ms                                                         | 39.7 ms: 1.04x slower                                                       |
| logging_simple            | 5.78 us                                                         | 6.03 us: 1.04x slower                                                       |
| async_tree_memoization    | 264 ms                                                          | 275 ms: 1.04x slower                                                        |
| xml_etree_iterparse       | 62.3 ms                                                         | 65.0 ms: 1.04x slower                                                       |
| sqlglot_parse             | 748 us                                                          | 781 us: 1.04x slower                                                        |
| nqueens                   | 56.7 ms                                                         | 59.2 ms: 1.04x slower                                                       |
| pickle_pure_python        | 175 us                                                          | 183 us: 1.05x slower                                                        |
| deepcopy_memo             | 22.1 us                                                         | 23.1 us: 1.05x slower                                                       |
| regex_dna                 | 119 ms                                                          | 125 ms: 1.05x slower                                                        |
| xml_etree_process         | 36.4 ms                                                         | 38.2 ms: 1.05x slower                                                       |
| tomli_loads               | 1.35 sec                                                        | 1.42 sec: 1.05x slower                                                      |
| scimark_sor               | 75.3 ms                                                         | 79.1 ms: 1.05x slower                                                       |
| pyflate                   | 279 ms                                                          | 293 ms: 1.05x slower                                                        |
| async_tree_memoization_tg | 258 ms                                                          | 273 ms: 1.06x slower                                                        |
| generators                | 19.6 ms                                                         | 20.7 ms: 1.06x slower                                                       |
| xml_etree_generate        | 53.2 ms                                                         | 56.2 ms: 1.06x slower                                                       |
| raytrace                  | 162 ms                                                          | 172 ms: 1.06x slower                                                        |
| bench_thread_pool         | 768 us                                                          | 815 us: 1.06x slower                                                        |
| coroutines                | 12.8 ms                                                         | 13.6 ms: 1.06x slower                                                       |
| fannkuch                  | 243 ms                                                          | 259 ms: 1.06x slower                                                        |
| meteor_contest            | 69.9 ms                                                         | 74.3 ms: 1.06x slower                                                       |
| float                     | 49.7 ms                                                         | 53.0 ms: 1.06x slower                                                       |
| telco                     | 4.67 ms                                                         | 5.00 ms: 1.07x slower                                                       |
| nbody                     | 67.6 ms                                                         | 72.4 ms: 1.07x slower                                                       |
| hexiom                    | 3.72 ms                                                         | 3.99 ms: 1.07x slower                                                       |
| comprehensions            | 10.4 us                                                         | 11.1 us: 1.07x slower                                                       |
| scimark_monte_carlo       | 39.1 ms                                                         | 42.1 ms: 1.08x slower                                                       |
| scimark_sparse_mat_mult   | 2.50 ms                                                         | 2.70 ms: 1.08x slower                                                       |
| scimark_fft               | 171 ms                                                          | 185 ms: 1.08x slower                                                        |
| logging_silent            | 52.9 ns                                                         | 57.4 ns: 1.09x slower                                                       |
| coverage                  | 42.1 ms                                                         | 45.8 ms: 1.09x slower                                                       |
| richards_super            | 30.2 ms                                                         | 33.2 ms: 1.10x slower                                                       |
| richards                  | 26.7 ms                                                         | 29.5 ms: 1.10x slower                                                       |
| async_tree_none_tg        | 202 ms                                                          | 223 ms: 1.10x slower                                                        |
| pickle_list               | 2.90 us                                                         | 3.22 us: 1.11x slower                                                       |
| genshi_xml                | 31.6 ms                                                         | 35.0 ms: 1.11x slower                                                       |
| unpickle_pure_python      | 122 us                                                          | 135 us: 1.11x slower                                                        |
| go                        | 82.1 ms                                                         | 91.4 ms: 1.11x slower                                                       |
| deltablue                 | 1.88 ms                                                         | 2.10 ms: 1.12x slower                                                       |
| genshi_text               | 14.4 ms                                                         | 16.5 ms: 1.15x slower                                                       |
| asyncio_tcp_ssl           | 1.48 sec                                                        | 1.72 sec: 1.16x slower                                                      |
| Geometric mean            | (ref)                                                           | 1.04x slower                                                                |

Benchmark hidden because not significant (9): regex_v8, pycparser, tornado_http, aiohttp, python_startup, asyncio_tcp, async_tree_io, async_tree_cpu_io_mixed_tg, pylint
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17.json: flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: unknown