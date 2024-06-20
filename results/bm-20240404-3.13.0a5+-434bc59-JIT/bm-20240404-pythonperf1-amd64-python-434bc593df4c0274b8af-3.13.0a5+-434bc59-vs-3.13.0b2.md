# Results vs. 3.13.0b2

- fork: python
- ref: 434bc593df4c0274b8af
- machine: windows-amd64
- commit hash: 434bc59
- commit date: 2024-04-04
- overall geometric mean: 1.01x slower
- HPT reliability: 92.86%
- HPT 99th percentile: 1.00x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 207 ms                                                          | 218 ms: 1.05x slower                                                        |
| chameleon      | 4.80 ms                                                         | 4.69 ms: 1.02x faster                                                       |
| docutils       | 1.63 sec                                                        | 1.69 sec: 1.04x slower                                                      |
| tornado_http   | 81.8 ms                                                         | 82.8 ms: 1.01x slower                                                       |
| Geometric mean | (ref)                                                           | 1.02x slower                                                                |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|--------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_none_tg | 202 ms                                                          | 212 ms: 1.05x slower                                                        |
| Geometric mean     | (ref)                                                           | 1.00x slower                                                                |

Benchmark hidden because not significant (7): async_tree_cpu_io_mixed, async_tree_io, async_tree_none, async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 67.6 ms                                                         | 57.0 ms: 1.19x faster                                                       |
| float          | 49.7 ms                                                         | 46.7 ms: 1.07x faster                                                       |
| pidigits       | 150 ms                                                          | 146 ms: 1.03x faster                                                        |
| Geometric mean | (ref)                                                           | 1.09x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_v8       | 15.8 ms                                                         | 14.6 ms: 1.08x faster                                                       |
| regex_effbot   | 1.58 ms                                                         | 1.57 ms: 1.01x faster                                                       |
| regex_compile  | 78.0 ms                                                         | 86.5 ms: 1.11x slower                                                       |
| Geometric mean | (ref)                                                           | 1.01x slower                                                                |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| tomli_loads          | 1.35 sec                                                        | 1.17 sec: 1.15x faster                                                      |
| xml_etree_iterparse  | 62.3 ms                                                         | 59.7 ms: 1.04x faster                                                       |
| json_loads           | 14.2 us                                                         | 13.7 us: 1.04x faster                                                       |
| pickle_pure_python   | 175 us                                                          | 172 us: 1.02x faster                                                        |
| xml_etree_parse      | 90.9 ms                                                         | 89.5 ms: 1.02x faster                                                       |
| xml_etree_generate   | 53.2 ms                                                         | 52.4 ms: 1.02x faster                                                       |
| xml_etree_process    | 36.4 ms                                                         | 36.2 ms: 1.01x faster                                                       |
| json_dumps           | 5.61 ms                                                         | 5.58 ms: 1.01x faster                                                       |
| pickle_dict          | 18.1 us                                                         | 18.6 us: 1.02x slower                                                       |
| unpickle             | 8.40 us                                                         | 8.66 us: 1.03x slower                                                       |
| pickle               | 7.11 us                                                         | 7.33 us: 1.03x slower                                                       |
| unpickle_list        | 2.62 us                                                         | 2.77 us: 1.06x slower                                                       |
| unpickle_pure_python | 122 us                                                          | 129 us: 1.06x slower                                                        |
| Geometric mean       | (ref)                                                           | 1.01x faster                                                                |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 20.3 ms                                                         | 21.9 ms: 1.08x slower                                                       |
| python_startup_no_site | 16.2 ms                                                         | 19.7 ms: 1.22x slower                                                       |
| Geometric mean         | (ref)                                                           | 1.15x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako           | 6.36 ms                                                         | 5.73 ms: 1.11x faster                                                       |
| genshi_xml     | 31.6 ms                                                         | 32.4 ms: 1.03x slower                                                       |
| genshi_text    | 14.4 ms                                                         | 14.8 ms: 1.03x slower                                                       |
| Geometric mean | (ref)                                                           | 1.02x faster                                                                |

All benchmarks:
===============

| Benchmark                | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|--------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols | 101 us                                                          | 71.8 us: 1.41x faster                                                       |
| spectral_norm            | 63.7 ms                                                         | 50.7 ms: 1.26x faster                                                       |
| nbody                    | 67.6 ms                                                         | 57.0 ms: 1.19x faster                                                       |
| tomli_loads              | 1.35 sec                                                        | 1.17 sec: 1.15x faster                                                      |
| scimark_sparse_mat_mult  | 2.50 ms                                                         | 2.22 ms: 1.13x faster                                                       |
| json                     | 3.19 ms                                                         | 2.86 ms: 1.11x faster                                                       |
| mako                     | 6.36 ms                                                         | 5.73 ms: 1.11x faster                                                       |
| pycparser                | 754 ms                                                          | 690 ms: 1.09x faster                                                        |
| regex_v8                 | 15.8 ms                                                         | 14.6 ms: 1.08x faster                                                       |
| float                    | 49.7 ms                                                         | 46.7 ms: 1.07x faster                                                       |
| pylint                   | 205 ms                                                          | 193 ms: 1.06x faster                                                        |
| deepcopy_memo            | 22.1 us                                                         | 21.0 us: 1.05x faster                                                       |
| xml_etree_iterparse      | 62.3 ms                                                         | 59.7 ms: 1.04x faster                                                       |
| fannkuch                 | 243 ms                                                          | 234 ms: 1.04x faster                                                        |
| json_loads               | 14.2 us                                                         | 13.7 us: 1.04x faster                                                       |
| pyflate                  | 279 ms                                                          | 271 ms: 1.03x faster                                                        |
| scimark_fft              | 171 ms                                                          | 166 ms: 1.03x faster                                                        |
| pidigits                 | 150 ms                                                          | 146 ms: 1.03x faster                                                        |
| pprint_pformat           | 966 ms                                                          | 942 ms: 1.03x faster                                                        |
| deepcopy_reduce          | 1.99 us                                                         | 1.95 us: 1.03x faster                                                       |
| chameleon                | 4.80 ms                                                         | 4.69 ms: 1.02x faster                                                       |
| pprint_safe_repr         | 474 ms                                                          | 463 ms: 1.02x faster                                                        |
| crypto_pyaes             | 45.5 ms                                                         | 44.5 ms: 1.02x faster                                                       |
| logging_format           | 6.22 us                                                         | 6.10 us: 1.02x faster                                                       |
| logging_simple           | 5.78 us                                                         | 5.68 us: 1.02x faster                                                       |
| sqlite_synth             | 1.60 us                                                         | 1.57 us: 1.02x faster                                                       |
| pickle_pure_python       | 175 us                                                          | 172 us: 1.02x faster                                                        |
| xml_etree_parse          | 90.9 ms                                                         | 89.5 ms: 1.02x faster                                                       |
| xml_etree_generate       | 53.2 ms                                                         | 52.4 ms: 1.02x faster                                                       |
| xml_etree_process        | 36.4 ms                                                         | 36.2 ms: 1.01x faster                                                       |
| regex_effbot             | 1.58 ms                                                         | 1.57 ms: 1.01x faster                                                       |
| gc_traversal             | 1.55 ms                                                         | 1.54 ms: 1.01x faster                                                       |
| json_dumps               | 5.61 ms                                                         | 5.58 ms: 1.01x faster                                                       |
| generators               | 19.6 ms                                                         | 19.6 ms: 1.00x slower                                                       |
| logging_silent           | 52.9 ns                                                         | 53.4 ns: 1.01x slower                                                       |
| tornado_http             | 81.8 ms                                                         | 82.8 ms: 1.01x slower                                                       |
| raytrace                 | 162 ms                                                          | 164 ms: 1.01x slower                                                        |
| coroutines               | 12.8 ms                                                         | 13.0 ms: 1.02x slower                                                       |
| create_gc_cycles         | 888 us                                                          | 904 us: 1.02x slower                                                        |
| pathlib                  | 75.9 ms                                                         | 77.6 ms: 1.02x slower                                                       |
| pickle_dict              | 18.1 us                                                         | 18.6 us: 1.02x slower                                                       |
| meteor_contest           | 69.9 ms                                                         | 71.5 ms: 1.02x slower                                                       |
| genshi_xml               | 31.6 ms                                                         | 32.4 ms: 1.03x slower                                                       |
| genshi_text              | 14.4 ms                                                         | 14.8 ms: 1.03x slower                                                       |
| sqlglot_parse            | 748 us                                                          | 769 us: 1.03x slower                                                        |
| telco                    | 4.67 ms                                                         | 4.80 ms: 1.03x slower                                                       |
| unpickle                 | 8.40 us                                                         | 8.66 us: 1.03x slower                                                       |
| pickle                   | 7.11 us                                                         | 7.33 us: 1.03x slower                                                       |
| sqlglot_transpile        | 955 us                                                          | 985 us: 1.03x slower                                                        |
| sqlglot_normalize        | 173 ms                                                          | 178 ms: 1.03x slower                                                        |
| docutils                 | 1.63 sec                                                        | 1.69 sec: 1.04x slower                                                      |
| sympy_sum                | 84.4 ms                                                         | 87.7 ms: 1.04x slower                                                       |
| sympy_str                | 159 ms                                                          | 166 ms: 1.04x slower                                                        |
| bench_mp_pool            | 64.8 ms                                                         | 67.7 ms: 1.04x slower                                                       |
| sympy_expand             | 271 ms                                                          | 283 ms: 1.05x slower                                                        |
| mdp                      | 1.31 sec                                                        | 1.38 sec: 1.05x slower                                                      |
| async_generators         | 223 ms                                                          | 234 ms: 1.05x slower                                                        |
| async_tree_none_tg       | 202 ms                                                          | 212 ms: 1.05x slower                                                        |
| sqlglot_optimize         | 32.7 ms                                                         | 34.4 ms: 1.05x slower                                                       |
| bench_thread_pool        | 768 us                                                          | 808 us: 1.05x slower                                                        |
| 2to3                     | 207 ms                                                          | 218 ms: 1.05x slower                                                        |
| unpickle_list            | 2.62 us                                                         | 2.77 us: 1.06x slower                                                       |
| unpickle_pure_python     | 122 us                                                          | 129 us: 1.06x slower                                                        |
| scimark_sor              | 75.3 ms                                                         | 80.0 ms: 1.06x slower                                                       |
| comprehensions           | 10.4 us                                                         | 11.1 us: 1.07x slower                                                       |
| mypy2                    | 418 ms                                                          | 446 ms: 1.07x slower                                                        |
| dulwich_log              | 38.0 ms                                                         | 40.9 ms: 1.08x slower                                                       |
| nqueens                  | 56.7 ms                                                         | 61.0 ms: 1.08x slower                                                       |
| sympy_integrate          | 12.2 ms                                                         | 13.2 ms: 1.08x slower                                                       |
| python_startup           | 20.3 ms                                                         | 21.9 ms: 1.08x slower                                                       |
| thrift                   | 8.11 ms                                                         | 8.76 ms: 1.08x slower                                                       |
| coverage                 | 42.1 ms                                                         | 46.7 ms: 1.11x slower                                                       |
| regex_compile            | 78.0 ms                                                         | 86.5 ms: 1.11x slower                                                       |
| go                       | 82.1 ms                                                         | 92.1 ms: 1.12x slower                                                       |
| deltablue                | 1.88 ms                                                         | 2.14 ms: 1.14x slower                                                       |
| hexiom                   | 3.72 ms                                                         | 4.41 ms: 1.18x slower                                                       |
| python_startup_no_site   | 16.2 ms                                                         | 19.7 ms: 1.22x slower                                                       |
| scimark_lu               | 56.6 ms                                                         | 69.5 ms: 1.23x slower                                                       |
| Geometric mean           | (ref)                                                           | 1.01x slower                                                                |

Benchmark hidden because not significant (18): async_tree_cpu_io_mixed, async_tree_io, async_tree_none, pickle_list, asyncio_tcp_ssl, deepcopy, scimark_monte_carlo, async_tree_cpu_io_mixed_tg, chaos, async_tree_io_tg, richards, html5lib, regex_dna, richards_super, aiohttp, async_tree_memoization, asyncio_tcp, async_tree_memoization_tg
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17.json: django_template, flaskblogging

# HPT report

- Reliability score: 92.86% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: unknown