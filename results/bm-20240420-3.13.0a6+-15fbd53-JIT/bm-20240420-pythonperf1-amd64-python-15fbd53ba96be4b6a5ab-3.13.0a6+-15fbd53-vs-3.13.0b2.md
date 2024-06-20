# Results vs. 3.13.0b2

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: windows-amd64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.01x slower
- HPT reliability: 76.69%
- HPT 99th percentile: 1.00x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 207 ms                                                          | 216 ms: 1.04x slower                                                        |
| chameleon      | 4.80 ms                                                         | 4.69 ms: 1.03x faster                                                       |
| docutils       | 1.63 sec                                                        | 1.67 sec: 1.03x slower                                                      |
| html5lib       | 35.0 ms                                                         | 37.3 ms: 1.06x slower                                                       |
| Geometric mean | (ref)                                                           | 1.02x slower                                                                |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|--------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_none_tg | 202 ms                                                          | 211 ms: 1.04x slower                                                        |
| Geometric mean     | (ref)                                                           | 1.00x faster                                                                |

Benchmark hidden because not significant (7): async_tree_cpu_io_mixed, async_tree_memoization_tg, async_tree_none, async_tree_io, async_tree_cpu_io_mixed_tg, async_tree_memoization, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 67.6 ms                                                         | 58.2 ms: 1.16x faster                                                       |
| float          | 49.7 ms                                                         | 46.6 ms: 1.07x faster                                                       |
| pidigits       | 150 ms                                                          | 147 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                           | 1.08x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_v8       | 15.8 ms                                                         | 14.7 ms: 1.08x faster                                                       |
| regex_dna      | 119 ms                                                          | 117 ms: 1.02x faster                                                        |
| regex_compile  | 78.0 ms                                                         | 84.3 ms: 1.08x slower                                                       |
| Geometric mean | (ref)                                                           | 1.01x faster                                                                |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| tomli_loads          | 1.35 sec                                                        | 1.17 sec: 1.15x faster                                                      |
| json_loads           | 14.2 us                                                         | 13.6 us: 1.04x faster                                                       |
| xml_etree_iterparse  | 62.3 ms                                                         | 60.5 ms: 1.03x faster                                                       |
| pickle_pure_python   | 175 us                                                          | 171 us: 1.02x faster                                                        |
| xml_etree_generate   | 53.2 ms                                                         | 52.2 ms: 1.02x faster                                                       |
| xml_etree_parse      | 90.9 ms                                                         | 89.7 ms: 1.01x faster                                                       |
| xml_etree_process    | 36.4 ms                                                         | 36.0 ms: 1.01x faster                                                       |
| json_dumps           | 5.61 ms                                                         | 5.56 ms: 1.01x faster                                                       |
| unpickle_pure_python | 122 us                                                          | 124 us: 1.01x slower                                                        |
| pickle_dict          | 18.1 us                                                         | 18.6 us: 1.03x slower                                                       |
| unpickle             | 8.40 us                                                         | 8.67 us: 1.03x slower                                                       |
| pickle_list          | 2.90 us                                                         | 3.02 us: 1.04x slower                                                       |
| pickle               | 7.11 us                                                         | 7.41 us: 1.04x slower                                                       |
| unpickle_list        | 2.62 us                                                         | 2.74 us: 1.05x slower                                                       |
| Geometric mean       | (ref)                                                           | 1.01x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 20.3 ms                                                         | 21.5 ms: 1.06x slower                                                       |
| python_startup_no_site | 16.2 ms                                                         | 17.9 ms: 1.10x slower                                                       |
| Geometric mean         | (ref)                                                           | 1.08x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 6.36 ms                                                         | 5.58 ms: 1.14x faster                                                       |
| django_template | 21.7 ms                                                         | 21.5 ms: 1.01x faster                                                       |
| genshi_xml      | 31.6 ms                                                         | 32.7 ms: 1.04x slower                                                       |
| genshi_text     | 14.4 ms                                                         | 15.1 ms: 1.05x slower                                                       |
| Geometric mean  | (ref)                                                           | 1.01x faster                                                                |

All benchmarks:
===============

| Benchmark                | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|--------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols | 101 us                                                          | 70.1 us: 1.44x faster                                                       |
| spectral_norm            | 63.7 ms                                                         | 50.0 ms: 1.28x faster                                                       |
| nbody                    | 67.6 ms                                                         | 58.2 ms: 1.16x faster                                                       |
| tomli_loads              | 1.35 sec                                                        | 1.17 sec: 1.15x faster                                                      |
| mako                     | 6.36 ms                                                         | 5.58 ms: 1.14x faster                                                       |
| scimark_sparse_mat_mult  | 2.50 ms                                                         | 2.21 ms: 1.13x faster                                                       |
| pycparser                | 754 ms                                                          | 692 ms: 1.09x faster                                                        |
| regex_v8                 | 15.8 ms                                                         | 14.7 ms: 1.08x faster                                                       |
| float                    | 49.7 ms                                                         | 46.6 ms: 1.07x faster                                                       |
| crypto_pyaes             | 45.5 ms                                                         | 42.8 ms: 1.06x faster                                                       |
| json                     | 3.19 ms                                                         | 3.01 ms: 1.06x faster                                                       |
| pyflate                  | 279 ms                                                          | 264 ms: 1.06x faster                                                        |
| fannkuch                 | 243 ms                                                          | 231 ms: 1.05x faster                                                        |
| deepcopy_reduce          | 1.99 us                                                         | 1.91 us: 1.04x faster                                                       |
| json_loads               | 14.2 us                                                         | 13.6 us: 1.04x faster                                                       |
| deepcopy_memo            | 22.1 us                                                         | 21.2 us: 1.04x faster                                                       |
| pprint_safe_repr         | 474 ms                                                          | 457 ms: 1.04x faster                                                        |
| scimark_fft              | 171 ms                                                          | 165 ms: 1.04x faster                                                        |
| pprint_pformat           | 966 ms                                                          | 935 ms: 1.03x faster                                                        |
| xml_etree_iterparse      | 62.3 ms                                                         | 60.5 ms: 1.03x faster                                                       |
| chameleon                | 4.80 ms                                                         | 4.69 ms: 1.03x faster                                                       |
| pickle_pure_python       | 175 us                                                          | 171 us: 1.02x faster                                                        |
| deepcopy                 | 220 us                                                          | 215 us: 1.02x faster                                                        |
| pidigits                 | 150 ms                                                          | 147 ms: 1.02x faster                                                        |
| xml_etree_generate       | 53.2 ms                                                         | 52.2 ms: 1.02x faster                                                       |
| regex_dna                | 119 ms                                                          | 117 ms: 1.02x faster                                                        |
| logging_simple           | 5.78 us                                                         | 5.69 us: 1.02x faster                                                       |
| scimark_monte_carlo      | 39.1 ms                                                         | 38.6 ms: 1.01x faster                                                       |
| xml_etree_parse          | 90.9 ms                                                         | 89.7 ms: 1.01x faster                                                       |
| xml_etree_process        | 36.4 ms                                                         | 36.0 ms: 1.01x faster                                                       |
| logging_format           | 6.22 us                                                         | 6.16 us: 1.01x faster                                                       |
| json_dumps               | 5.61 ms                                                         | 5.56 ms: 1.01x faster                                                       |
| django_template          | 21.7 ms                                                         | 21.5 ms: 1.01x faster                                                       |
| gc_traversal             | 1.55 ms                                                         | 1.54 ms: 1.01x faster                                                       |
| chaos                    | 38.4 ms                                                         | 38.2 ms: 1.00x faster                                                       |
| generators               | 19.6 ms                                                         | 19.5 ms: 1.00x faster                                                       |
| sqlite_synth             | 1.60 us                                                         | 1.61 us: 1.00x slower                                                       |
| logging_silent           | 52.9 ns                                                         | 53.5 ns: 1.01x slower                                                       |
| unpickle_pure_python     | 122 us                                                          | 124 us: 1.01x slower                                                        |
| comprehensions           | 10.4 us                                                         | 10.6 us: 1.02x slower                                                       |
| telco                    | 4.67 ms                                                         | 4.76 ms: 1.02x slower                                                       |
| richards_super           | 30.2 ms                                                         | 30.9 ms: 1.02x slower                                                       |
| bench_thread_pool        | 768 us                                                          | 787 us: 1.03x slower                                                        |
| richards                 | 26.7 ms                                                         | 27.4 ms: 1.03x slower                                                       |
| docutils                 | 1.63 sec                                                        | 1.67 sec: 1.03x slower                                                      |
| pickle_dict              | 18.1 us                                                         | 18.6 us: 1.03x slower                                                       |
| sqlglot_parse            | 748 us                                                          | 772 us: 1.03x slower                                                        |
| sqlglot_transpile        | 955 us                                                          | 985 us: 1.03x slower                                                        |
| unpickle                 | 8.40 us                                                         | 8.67 us: 1.03x slower                                                       |
| coroutines               | 12.8 ms                                                         | 13.2 ms: 1.03x slower                                                       |
| genshi_xml               | 31.6 ms                                                         | 32.7 ms: 1.04x slower                                                       |
| bench_mp_pool            | 64.8 ms                                                         | 67.2 ms: 1.04x slower                                                       |
| dulwich_log              | 38.0 ms                                                         | 39.5 ms: 1.04x slower                                                       |
| pickle_list              | 2.90 us                                                         | 3.02 us: 1.04x slower                                                       |
| pickle                   | 7.11 us                                                         | 7.41 us: 1.04x slower                                                       |
| sqlglot_normalize        | 173 ms                                                          | 180 ms: 1.04x slower                                                        |
| sympy_sum                | 84.4 ms                                                         | 87.9 ms: 1.04x slower                                                       |
| 2to3                     | 207 ms                                                          | 216 ms: 1.04x slower                                                        |
| async_tree_none_tg       | 202 ms                                                          | 211 ms: 1.04x slower                                                        |
| meteor_contest           | 69.9 ms                                                         | 72.9 ms: 1.04x slower                                                       |
| sympy_str                | 159 ms                                                          | 166 ms: 1.04x slower                                                        |
| unpickle_list            | 2.62 us                                                         | 2.74 us: 1.05x slower                                                       |
| sympy_expand             | 271 ms                                                          | 285 ms: 1.05x slower                                                        |
| async_generators         | 223 ms                                                          | 235 ms: 1.05x slower                                                        |
| genshi_text              | 14.4 ms                                                         | 15.1 ms: 1.05x slower                                                       |
| mypy2                    | 418 ms                                                          | 441 ms: 1.06x slower                                                        |
| python_startup           | 20.3 ms                                                         | 21.5 ms: 1.06x slower                                                       |
| sqlglot_optimize         | 32.7 ms                                                         | 34.7 ms: 1.06x slower                                                       |
| scimark_sor              | 75.3 ms                                                         | 80.2 ms: 1.06x slower                                                       |
| html5lib                 | 35.0 ms                                                         | 37.3 ms: 1.06x slower                                                       |
| nqueens                  | 56.7 ms                                                         | 60.4 ms: 1.07x slower                                                       |
| thrift                   | 8.11 ms                                                         | 8.70 ms: 1.07x slower                                                       |
| sympy_integrate          | 12.2 ms                                                         | 13.2 ms: 1.08x slower                                                       |
| regex_compile            | 78.0 ms                                                         | 84.3 ms: 1.08x slower                                                       |
| python_startup_no_site   | 16.2 ms                                                         | 17.9 ms: 1.10x slower                                                       |
| go                       | 82.1 ms                                                         | 91.0 ms: 1.11x slower                                                       |
| deltablue                | 1.88 ms                                                         | 2.12 ms: 1.12x slower                                                       |
| mdp                      | 1.31 sec                                                        | 1.48 sec: 1.13x slower                                                      |
| coverage                 | 42.1 ms                                                         | 48.9 ms: 1.16x slower                                                       |
| hexiom                   | 3.72 ms                                                         | 4.35 ms: 1.17x slower                                                       |
| scimark_lu               | 56.6 ms                                                         | 75.0 ms: 1.33x slower                                                       |
| Geometric mean           | (ref)                                                           | 1.01x slower                                                                |

Benchmark hidden because not significant (16): async_tree_cpu_io_mixed, async_tree_memoization_tg, async_tree_none, regex_effbot, raytrace, async_tree_io, async_tree_cpu_io_mixed_tg, async_tree_memoization, tornado_http, async_tree_io_tg, aiohttp, pathlib, create_gc_cycles, asyncio_tcp, asyncio_tcp_ssl, pylint
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17.json: flaskblogging

# HPT report

- Reliability score: 76.69% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: unknown