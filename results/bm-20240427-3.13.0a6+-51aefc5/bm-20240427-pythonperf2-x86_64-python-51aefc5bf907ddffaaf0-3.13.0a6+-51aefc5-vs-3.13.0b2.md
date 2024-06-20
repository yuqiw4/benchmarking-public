# Results vs. 3.13.0b2

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: linux-x86_64
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.01x faster
- HPT reliability: 99.16%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 291 ms                                                           | 286 ms: 1.02x faster                                                         |
| chameleon      | 7.40 ms                                                          | 7.51 ms: 1.02x slower                                                        |
| docutils       | 2.98 sec                                                         | 3.00 sec: 1.01x slower                                                       |
| html5lib       | 74.7 ms                                                          | 73.2 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                            | 1.00x faster                                                                 |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed | 604 ms                                                           | 616 ms: 1.02x slower                                                         |
| async_tree_io           | 873 ms                                                           | 907 ms: 1.04x slower                                                         |
| Geometric mean          | (ref)                                                            | 1.01x slower                                                                 |

Benchmark hidden because not significant (6): async_tree_io_tg, async_tree_none_tg, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg, async_tree_none, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 80.2 ms                                                          | 76.6 ms: 1.05x faster                                                        |
| nbody          | 87.8 ms                                                          | 85.7 ms: 1.02x faster                                                        |
| pidigits       | 254 ms                                                           | 263 ms: 1.04x slower                                                         |
| Geometric mean | (ref)                                                            | 1.01x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_dna      | 249 ms                                                           | 236 ms: 1.06x faster                                                         |
| regex_v8       | 26.0 ms                                                          | 25.7 ms: 1.01x faster                                                        |
| regex_compile  | 144 ms                                                           | 145 ms: 1.00x slower                                                         |
| regex_effbot   | 3.40 ms                                                          | 3.47 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                            | 1.01x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| tomli_loads          | 2.40 sec                                                         | 2.19 sec: 1.10x faster                                                       |
| unpickle_pure_python | 224 us                                                           | 210 us: 1.07x faster                                                         |
| pickle_dict          | 32.8 us                                                          | 31.0 us: 1.06x faster                                                        |
| pickle               | 10.6 us                                                          | 10.2 us: 1.04x faster                                                        |
| json_loads           | 25.0 us                                                          | 24.5 us: 1.02x faster                                                        |
| unpickle             | 15.7 us                                                          | 15.5 us: 1.01x faster                                                        |
| xml_etree_generate   | 85.7 ms                                                          | 84.8 ms: 1.01x faster                                                        |
| json_dumps           | 10.8 ms                                                          | 10.7 ms: 1.01x faster                                                        |
| pickle_list          | 4.44 us                                                          | 4.42 us: 1.01x faster                                                        |
| xml_etree_iterparse  | 103 ms                                                           | 103 ms: 1.01x slower                                                         |
| Geometric mean       | (ref)                                                            | 1.02x faster                                                                 |

Benchmark hidden because not significant (4): xml_etree_process, xml_etree_parse, pickle_pure_python, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 13.2 ms                                                          | 12.9 ms: 1.02x faster                                                        |
| python_startup_no_site | 8.85 ms                                                          | 8.84 ms: 1.00x faster                                                        |
| Geometric mean         | (ref)                                                            | 1.01x faster                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| genshi_xml      | 58.1 ms                                                          | 57.1 ms: 1.02x faster                                                        |
| django_template | 39.0 ms                                                          | 38.4 ms: 1.01x faster                                                        |
| mako            | 10.4 ms                                                          | 10.3 ms: 1.01x faster                                                        |
| Geometric mean  | (ref)                                                            | 1.01x faster                                                                 |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|--------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| tomli_loads              | 2.40 sec                                                         | 2.19 sec: 1.10x faster                                                       |
| scimark_monte_carlo      | 65.5 ms                                                          | 60.7 ms: 1.08x faster                                                        |
| bench_mp_pool            | 4.91 ms                                                          | 4.56 ms: 1.08x faster                                                        |
| coverage                 | 83.5 ms                                                          | 78.1 ms: 1.07x faster                                                        |
| unpickle_pure_python     | 224 us                                                           | 210 us: 1.07x faster                                                         |
| coroutines               | 22.0 ms                                                          | 20.6 ms: 1.07x faster                                                        |
| telco                    | 8.40 ms                                                          | 7.90 ms: 1.06x faster                                                        |
| richards_super           | 61.2 ms                                                          | 57.6 ms: 1.06x faster                                                        |
| pickle_dict              | 32.8 us                                                          | 31.0 us: 1.06x faster                                                        |
| regex_dna                | 249 ms                                                           | 236 ms: 1.06x faster                                                         |
| deltablue                | 3.37 ms                                                          | 3.20 ms: 1.06x faster                                                        |
| hexiom                   | 6.35 ms                                                          | 6.02 ms: 1.06x faster                                                        |
| richards                 | 53.4 ms                                                          | 50.9 ms: 1.05x faster                                                        |
| go                       | 165 ms                                                           | 157 ms: 1.05x faster                                                         |
| float                    | 80.2 ms                                                          | 76.6 ms: 1.05x faster                                                        |
| raytrace                 | 260 ms                                                           | 249 ms: 1.04x faster                                                         |
| pickle                   | 10.6 us                                                          | 10.2 us: 1.04x faster                                                        |
| logging_silent           | 96.3 ns                                                          | 93.4 ns: 1.03x faster                                                        |
| sqlglot_normalize        | 120 ms                                                           | 117 ms: 1.03x faster                                                         |
| bench_thread_pool        | 908 us                                                           | 886 us: 1.03x faster                                                         |
| python_startup           | 13.2 ms                                                          | 12.9 ms: 1.02x faster                                                        |
| pprint_safe_repr         | 818 ms                                                           | 798 ms: 1.02x faster                                                         |
| nbody                    | 87.8 ms                                                          | 85.7 ms: 1.02x faster                                                        |
| sqlite_synth             | 2.80 us                                                          | 2.73 us: 1.02x faster                                                        |
| sqlglot_optimize         | 59.5 ms                                                          | 58.3 ms: 1.02x faster                                                        |
| dulwich_log              | 67.3 ms                                                          | 65.9 ms: 1.02x faster                                                        |
| json_loads               | 25.0 us                                                          | 24.5 us: 1.02x faster                                                        |
| pprint_pformat           | 1.66 sec                                                         | 1.63 sec: 1.02x faster                                                       |
| 2to3                     | 291 ms                                                           | 286 ms: 1.02x faster                                                         |
| html5lib                 | 74.7 ms                                                          | 73.2 ms: 1.02x faster                                                        |
| scimark_lu               | 97.5 ms                                                          | 95.7 ms: 1.02x faster                                                        |
| crypto_pyaes             | 73.6 ms                                                          | 72.3 ms: 1.02x faster                                                        |
| asyncio_websockets       | 395 ms                                                           | 388 ms: 1.02x faster                                                         |
| genshi_xml               | 58.1 ms                                                          | 57.1 ms: 1.02x faster                                                        |
| generators               | 33.5 ms                                                          | 33.0 ms: 1.02x faster                                                        |
| nqueens                  | 88.4 ms                                                          | 87.0 ms: 1.02x faster                                                        |
| asyncio_tcp              | 378 ms                                                           | 372 ms: 1.01x faster                                                         |
| django_template          | 39.0 ms                                                          | 38.4 ms: 1.01x faster                                                        |
| async_generators         | 363 ms                                                           | 358 ms: 1.01x faster                                                         |
| unpickle                 | 15.7 us                                                          | 15.5 us: 1.01x faster                                                        |
| regex_v8                 | 26.0 ms                                                          | 25.7 ms: 1.01x faster                                                        |
| xml_etree_generate       | 85.7 ms                                                          | 84.8 ms: 1.01x faster                                                        |
| typing_runtime_protocols | 171 us                                                           | 169 us: 1.01x faster                                                         |
| mako                     | 10.4 ms                                                          | 10.3 ms: 1.01x faster                                                        |
| meteor_contest           | 128 ms                                                           | 127 ms: 1.01x faster                                                         |
| aiohttp                  | 1.07 ms                                                          | 1.06 ms: 1.01x faster                                                        |
| json_dumps               | 10.8 ms                                                          | 10.7 ms: 1.01x faster                                                        |
| sympy_sum                | 155 ms                                                           | 154 ms: 1.01x faster                                                         |
| chaos                    | 59.6 ms                                                          | 59.2 ms: 1.01x faster                                                        |
| pickle_list              | 4.44 us                                                          | 4.42 us: 1.01x faster                                                        |
| asyncio_tcp_ssl          | 1.58 sec                                                         | 1.57 sec: 1.00x faster                                                       |
| python_startup_no_site   | 8.85 ms                                                          | 8.84 ms: 1.00x faster                                                        |
| regex_compile            | 144 ms                                                           | 145 ms: 1.00x slower                                                         |
| sympy_str                | 295 ms                                                           | 296 ms: 1.00x slower                                                         |
| pathlib                  | 17.1 ms                                                          | 17.2 ms: 1.00x slower                                                        |
| docutils                 | 2.98 sec                                                         | 3.00 sec: 1.01x slower                                                       |
| xml_etree_iterparse      | 103 ms                                                           | 103 ms: 1.01x slower                                                         |
| sqlglot_transpile        | 1.76 ms                                                          | 1.78 ms: 1.01x slower                                                        |
| json                     | 5.35 ms                                                          | 5.41 ms: 1.01x slower                                                        |
| gc_traversal             | 4.69 ms                                                          | 4.75 ms: 1.01x slower                                                        |
| mdp                      | 2.46 sec                                                         | 2.50 sec: 1.01x slower                                                       |
| chameleon                | 7.40 ms                                                          | 7.51 ms: 1.02x slower                                                        |
| thrift                   | 880 us                                                           | 896 us: 1.02x slower                                                         |
| deepcopy_memo            | 37.3 us                                                          | 38.0 us: 1.02x slower                                                        |
| async_tree_cpu_io_mixed  | 604 ms                                                           | 616 ms: 1.02x slower                                                         |
| scimark_sparse_mat_mult  | 4.28 ms                                                          | 4.37 ms: 1.02x slower                                                        |
| regex_effbot             | 3.40 ms                                                          | 3.47 ms: 1.02x slower                                                        |
| pycparser                | 1.22 sec                                                         | 1.26 sec: 1.03x slower                                                       |
| logging_simple           | 6.40 us                                                          | 6.58 us: 1.03x slower                                                        |
| deepcopy                 | 377 us                                                           | 388 us: 1.03x slower                                                         |
| async_tree_io            | 873 ms                                                           | 907 ms: 1.04x slower                                                         |
| pidigits                 | 254 ms                                                           | 263 ms: 1.04x slower                                                         |
| deepcopy_reduce          | 3.39 us                                                          | 3.52 us: 1.04x slower                                                        |
| Geometric mean           | (ref)                                                            | 1.01x faster                                                                 |

Benchmark hidden because not significant (27): async_tree_io_tg, async_tree_none_tg, scimark_fft, create_gc_cycles, async_tree_memoization_tg, gunicorn, comprehensions, scimark_sor, sympy_integrate, xml_etree_process, fannkuch, sympy_expand, xml_etree_parse, tornado_http, pyflate, pickle_pure_python, genshi_text, sqlglot_parse, unpickle_list, logging_format, async_tree_cpu_io_mixed_tg, dask, spectral_norm, async_tree_none, mypy2, async_tree_memoization, pylint
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 99.16% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.98x