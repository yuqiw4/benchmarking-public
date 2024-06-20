# Results vs. 3.13.0b2

- fork: mdboom
- ref: tier2_func_simple_fr
- machine: windows-amd64
- commit hash: c5564c1
- commit date: 2024-04-08
- overall geometric mean: 1.02x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.00x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 207 ms                                                          | 221 ms: 1.07x slower                                                        |
| chameleon      | 4.80 ms                                                         | 4.74 ms: 1.01x faster                                                       |
| docutils       | 1.63 sec                                                        | 1.70 sec: 1.05x slower                                                      |
| html5lib       | 35.0 ms                                                         | 35.3 ms: 1.01x slower                                                       |
| tornado_http   | 81.8 ms                                                         | 83.9 ms: 1.03x slower                                                       |
| Geometric mean | (ref)                                                           | 1.03x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|--------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_io_tg   | 605 ms                                                          | 618 ms: 1.02x slower                                                        |
| async_tree_none_tg | 202 ms                                                          | 214 ms: 1.06x slower                                                        |
| Geometric mean     | (ref)                                                           | 1.02x slower                                                                |

Benchmark hidden because not significant (6): async_tree_io, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_none, async_tree_memoization, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 67.6 ms                                                         | 58.1 ms: 1.16x faster                                                       |
| float          | 49.7 ms                                                         | 47.1 ms: 1.06x faster                                                       |
| pidigits       | 150 ms                                                          | 147 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                           | 1.08x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_dna      | 119 ms                                                          | 121 ms: 1.01x slower                                                        |
| regex_effbot   | 1.58 ms                                                         | 1.61 ms: 1.01x slower                                                       |
| regex_compile  | 78.0 ms                                                         | 86.4 ms: 1.11x slower                                                       |
| Geometric mean | (ref)                                                           | 1.02x slower                                                                |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| tomli_loads          | 1.35 sec                                                        | 1.20 sec: 1.12x faster                                                      |
| xml_etree_iterparse  | 62.3 ms                                                         | 60.9 ms: 1.02x faster                                                       |
| json_loads           | 14.2 us                                                         | 13.9 us: 1.02x faster                                                       |
| xml_etree_generate   | 53.2 ms                                                         | 52.7 ms: 1.01x faster                                                       |
| pickle_pure_python   | 175 us                                                          | 174 us: 1.01x faster                                                        |
| pickle_dict          | 18.1 us                                                         | 18.5 us: 1.02x slower                                                       |
| pickle               | 7.11 us                                                         | 7.26 us: 1.02x slower                                                       |
| unpickle_pure_python | 122 us                                                          | 127 us: 1.04x slower                                                        |
| unpickle_list        | 2.62 us                                                         | 2.89 us: 1.10x slower                                                       |
| unpickle             | 8.40 us                                                         | 9.30 us: 1.11x slower                                                       |
| Geometric mean       | (ref)                                                           | 1.01x slower                                                                |

Benchmark hidden because not significant (4): json_dumps, xml_etree_parse, xml_etree_process, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 20.3 ms                                                         | 21.9 ms: 1.08x slower                                                       |
| python_startup_no_site | 16.2 ms                                                         | 19.7 ms: 1.22x slower                                                       |
| Geometric mean         | (ref)                                                           | 1.15x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako           | 6.36 ms                                                         | 5.64 ms: 1.13x faster                                                       |
| genshi_text    | 14.4 ms                                                         | 15.4 ms: 1.07x slower                                                       |
| genshi_xml     | 31.6 ms                                                         | 34.3 ms: 1.09x slower                                                       |
| Geometric mean | (ref)                                                           | 1.01x slower                                                                |

All benchmarks:
===============

| Benchmark                | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|--------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols | 101 us                                                          | 70.8 us: 1.43x faster                                                       |
| spectral_norm            | 63.7 ms                                                         | 52.2 ms: 1.22x faster                                                       |
| nbody                    | 67.6 ms                                                         | 58.1 ms: 1.16x faster                                                       |
| mako                     | 6.36 ms                                                         | 5.64 ms: 1.13x faster                                                       |
| tomli_loads              | 1.35 sec                                                        | 1.20 sec: 1.12x faster                                                      |
| scimark_sparse_mat_mult  | 2.50 ms                                                         | 2.26 ms: 1.10x faster                                                       |
| json                     | 3.19 ms                                                         | 2.90 ms: 1.10x faster                                                       |
| fannkuch                 | 243 ms                                                          | 230 ms: 1.06x faster                                                        |
| pylint                   | 205 ms                                                          | 194 ms: 1.06x faster                                                        |
| float                    | 49.7 ms                                                         | 47.1 ms: 1.06x faster                                                       |
| deepcopy_memo            | 22.1 us                                                         | 21.0 us: 1.05x faster                                                       |
| pyflate                  | 279 ms                                                          | 268 ms: 1.04x faster                                                        |
| crypto_pyaes             | 45.5 ms                                                         | 44.0 ms: 1.03x faster                                                       |
| scimark_fft              | 171 ms                                                          | 166 ms: 1.03x faster                                                        |
| xml_etree_iterparse      | 62.3 ms                                                         | 60.9 ms: 1.02x faster                                                       |
| json_loads               | 14.2 us                                                         | 13.9 us: 1.02x faster                                                       |
| pidigits                 | 150 ms                                                          | 147 ms: 1.02x faster                                                        |
| deepcopy_reduce          | 1.99 us                                                         | 1.96 us: 1.02x faster                                                       |
| sqlite_synth             | 1.60 us                                                         | 1.57 us: 1.02x faster                                                       |
| chameleon                | 4.80 ms                                                         | 4.74 ms: 1.01x faster                                                       |
| chaos                    | 38.4 ms                                                         | 37.9 ms: 1.01x faster                                                       |
| xml_etree_generate       | 53.2 ms                                                         | 52.7 ms: 1.01x faster                                                       |
| pickle_pure_python       | 175 us                                                          | 174 us: 1.01x faster                                                        |
| gc_traversal             | 1.55 ms                                                         | 1.55 ms: 1.00x faster                                                       |
| generators               | 19.6 ms                                                         | 19.5 ms: 1.00x faster                                                       |
| logging_format           | 6.22 us                                                         | 6.26 us: 1.01x slower                                                       |
| html5lib                 | 35.0 ms                                                         | 35.3 ms: 1.01x slower                                                       |
| logging_simple           | 5.78 us                                                         | 5.83 us: 1.01x slower                                                       |
| pprint_pformat           | 966 ms                                                          | 976 ms: 1.01x slower                                                        |
| pprint_safe_repr         | 474 ms                                                          | 480 ms: 1.01x slower                                                        |
| richards_super           | 30.2 ms                                                         | 30.6 ms: 1.01x slower                                                       |
| regex_dna                | 119 ms                                                          | 121 ms: 1.01x slower                                                        |
| regex_effbot             | 1.58 ms                                                         | 1.61 ms: 1.01x slower                                                       |
| pickle_dict              | 18.1 us                                                         | 18.5 us: 1.02x slower                                                       |
| async_tree_io_tg         | 605 ms                                                          | 618 ms: 1.02x slower                                                        |
| aiohttp                  | 889 us                                                          | 907 us: 1.02x slower                                                        |
| pickle                   | 7.11 us                                                         | 7.26 us: 1.02x slower                                                       |
| create_gc_cycles         | 888 us                                                          | 909 us: 1.02x slower                                                        |
| tornado_http             | 81.8 ms                                                         | 83.9 ms: 1.03x slower                                                       |
| coroutines               | 12.8 ms                                                         | 13.1 ms: 1.03x slower                                                       |
| pathlib                  | 75.9 ms                                                         | 78.1 ms: 1.03x slower                                                       |
| sqlglot_parse            | 748 us                                                          | 772 us: 1.03x slower                                                        |
| telco                    | 4.67 ms                                                         | 4.84 ms: 1.04x slower                                                       |
| sqlglot_transpile        | 955 us                                                          | 992 us: 1.04x slower                                                        |
| sqlglot_normalize        | 173 ms                                                          | 180 ms: 1.04x slower                                                        |
| unpickle_pure_python     | 122 us                                                          | 127 us: 1.04x slower                                                        |
| sympy_expand             | 271 ms                                                          | 282 ms: 1.04x slower                                                        |
| comprehensions           | 10.4 us                                                         | 10.8 us: 1.04x slower                                                       |
| meteor_contest           | 69.9 ms                                                         | 73.1 ms: 1.05x slower                                                       |
| docutils                 | 1.63 sec                                                        | 1.70 sec: 1.05x slower                                                      |
| sympy_sum                | 84.4 ms                                                         | 88.2 ms: 1.05x slower                                                       |
| sympy_str                | 159 ms                                                          | 167 ms: 1.05x slower                                                        |
| async_tree_none_tg       | 202 ms                                                          | 214 ms: 1.06x slower                                                        |
| async_generators         | 223 ms                                                          | 237 ms: 1.06x slower                                                        |
| bench_mp_pool            | 64.8 ms                                                         | 68.9 ms: 1.06x slower                                                       |
| bench_thread_pool        | 768 us                                                          | 818 us: 1.07x slower                                                        |
| 2to3                     | 207 ms                                                          | 221 ms: 1.07x slower                                                        |
| sqlglot_optimize         | 32.7 ms                                                         | 35.0 ms: 1.07x slower                                                       |
| coverage                 | 42.1 ms                                                         | 45.1 ms: 1.07x slower                                                       |
| mypy2                    | 418 ms                                                          | 448 ms: 1.07x slower                                                        |
| genshi_text              | 14.4 ms                                                         | 15.4 ms: 1.07x slower                                                       |
| nqueens                  | 56.7 ms                                                         | 60.9 ms: 1.08x slower                                                       |
| asyncio_tcp_ssl          | 1.48 sec                                                        | 1.60 sec: 1.08x slower                                                      |
| python_startup           | 20.3 ms                                                         | 21.9 ms: 1.08x slower                                                       |
| genshi_xml               | 31.6 ms                                                         | 34.3 ms: 1.09x slower                                                       |
| sympy_integrate          | 12.2 ms                                                         | 13.3 ms: 1.09x slower                                                       |
| dulwich_log              | 38.0 ms                                                         | 41.4 ms: 1.09x slower                                                       |
| thrift                   | 8.11 ms                                                         | 8.84 ms: 1.09x slower                                                       |
| unpickle_list            | 2.62 us                                                         | 2.89 us: 1.10x slower                                                       |
| regex_compile            | 78.0 ms                                                         | 86.4 ms: 1.11x slower                                                       |
| unpickle                 | 8.40 us                                                         | 9.30 us: 1.11x slower                                                       |
| scimark_sor              | 75.3 ms                                                         | 83.5 ms: 1.11x slower                                                       |
| go                       | 82.1 ms                                                         | 91.4 ms: 1.11x slower                                                       |
| deltablue                | 1.88 ms                                                         | 2.14 ms: 1.14x slower                                                       |
| mdp                      | 1.31 sec                                                        | 1.53 sec: 1.17x slower                                                      |
| hexiom                   | 3.72 ms                                                         | 4.47 ms: 1.20x slower                                                       |
| python_startup_no_site   | 16.2 ms                                                         | 19.7 ms: 1.22x slower                                                       |
| scimark_lu               | 56.6 ms                                                         | 75.0 ms: 1.33x slower                                                       |
| Geometric mean           | (ref)                                                           | 1.02x slower                                                                |

Benchmark hidden because not significant (18): pycparser, regex_v8, async_tree_io, json_dumps, scimark_monte_carlo, xml_etree_parse, xml_etree_process, deepcopy, logging_silent, richards, raytrace, asyncio_tcp, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, pickle_list, async_tree_none, async_tree_memoization, async_tree_memoization_tg
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17.json: django_template, flaskblogging

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: unknown