# Results vs. 3.13.0b2

- fork: python
- ref: 027fa2eccf39ddccdf7b
- machine: linux-x86_64
- commit hash: 027fa2e
- commit date: 2024-04-02
- overall geometric mean: 1.02x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.06x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 291 ms                                                           | 297 ms: 1.02x slower                                                         |
| docutils       | 2.98 sec                                                         | 3.09 sec: 1.04x slower                                                       |
| html5lib       | 74.7 ms                                                          | 72.2 ms: 1.03x faster                                                        |
| tornado_http   | 119 ms                                                           | 122 ms: 1.02x slower                                                         |
| Geometric mean | (ref)                                                            | 1.01x slower                                                                 |

Benchmark hidden because not significant (1): chameleon

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_io_tg           | 900 ms                                                           | 861 ms: 1.04x faster                                                         |
| async_tree_memoization     | 460 ms                                                           | 444 ms: 1.04x faster                                                         |
| async_tree_io              | 873 ms                                                           | 849 ms: 1.03x faster                                                         |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 592 ms: 1.03x slower                                                         |
| async_tree_none            | 365 ms                                                           | 380 ms: 1.04x slower                                                         |
| Geometric mean             | (ref)                                                            | 1.00x faster                                                                 |

Benchmark hidden because not significant (3): async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 80.2 ms                                                          | 75.9 ms: 1.06x faster                                                        |
| pidigits       | 254 ms                                                           | 262 ms: 1.03x slower                                                         |
| nbody          | 87.8 ms                                                          | 101 ms: 1.15x slower                                                         |
| Geometric mean | (ref)                                                            | 1.04x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_dna      | 249 ms                                                           | 247 ms: 1.01x faster                                                         |
| regex_v8       | 26.0 ms                                                          | 26.0 ms: 1.00x faster                                                        |
| regex_effbot   | 3.40 ms                                                          | 3.45 ms: 1.02x slower                                                        |
| regex_compile  | 144 ms                                                           | 148 ms: 1.02x slower                                                         |
| Geometric mean | (ref)                                                            | 1.01x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| tomli_loads          | 2.40 sec                                                         | 2.15 sec: 1.12x faster                                                       |
| unpickle             | 15.7 us                                                          | 15.1 us: 1.04x faster                                                        |
| unpickle_list        | 4.70 us                                                          | 4.58 us: 1.03x faster                                                        |
| xml_etree_generate   | 85.7 ms                                                          | 84.0 ms: 1.02x faster                                                        |
| xml_etree_process    | 59.7 ms                                                          | 58.6 ms: 1.02x faster                                                        |
| json_dumps           | 10.8 ms                                                          | 10.6 ms: 1.02x faster                                                        |
| pickle               | 10.6 us                                                          | 10.7 us: 1.01x slower                                                        |
| xml_etree_iterparse  | 103 ms                                                           | 104 ms: 1.01x slower                                                         |
| json_loads           | 25.0 us                                                          | 25.4 us: 1.02x slower                                                        |
| pickle_dict          | 32.8 us                                                          | 33.7 us: 1.03x slower                                                        |
| xml_etree_parse      | 144 ms                                                           | 149 ms: 1.04x slower                                                         |
| unpickle_pure_python | 224 us                                                           | 239 us: 1.06x slower                                                         |
| Geometric mean       | (ref)                                                            | 1.01x faster                                                                 |

Benchmark hidden because not significant (2): pickle_list, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 13.2 ms                                                          | 13.5 ms: 1.02x slower                                                        |
| python_startup_no_site | 8.85 ms                                                          | 11.8 ms: 1.33x slower                                                        |
| Geometric mean         | (ref)                                                            | 1.17x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako           | 10.4 ms                                                          | 9.91 ms: 1.05x faster                                                        |
| genshi_text    | 25.9 ms                                                          | 26.8 ms: 1.03x slower                                                        |
| Geometric mean | (ref)                                                            | 1.00x faster                                                                 |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 171 us                                                           | 119 us: 1.43x faster                                                         |
| tomli_loads                | 2.40 sec                                                         | 2.15 sec: 1.12x faster                                                       |
| create_gc_cycles           | 2.00 ms                                                          | 1.84 ms: 1.09x faster                                                        |
| richards_super             | 61.2 ms                                                          | 56.8 ms: 1.08x faster                                                        |
| richards                   | 53.4 ms                                                          | 50.6 ms: 1.06x faster                                                        |
| float                      | 80.2 ms                                                          | 75.9 ms: 1.06x faster                                                        |
| telco                      | 8.40 ms                                                          | 7.98 ms: 1.05x faster                                                        |
| mako                       | 10.4 ms                                                          | 9.91 ms: 1.05x faster                                                        |
| async_tree_io_tg           | 900 ms                                                           | 861 ms: 1.04x faster                                                         |
| spectral_norm              | 97.3 ms                                                          | 93.2 ms: 1.04x faster                                                        |
| sqlite_synth               | 2.80 us                                                          | 2.68 us: 1.04x faster                                                        |
| unpickle                   | 15.7 us                                                          | 15.1 us: 1.04x faster                                                        |
| scimark_sparse_mat_mult    | 4.28 ms                                                          | 4.13 ms: 1.04x faster                                                        |
| async_tree_memoization     | 460 ms                                                           | 444 ms: 1.04x faster                                                         |
| html5lib                   | 74.7 ms                                                          | 72.2 ms: 1.03x faster                                                        |
| gc_traversal               | 4.69 ms                                                          | 4.54 ms: 1.03x faster                                                        |
| async_tree_io              | 873 ms                                                           | 849 ms: 1.03x faster                                                         |
| unpickle_list              | 4.70 us                                                          | 4.58 us: 1.03x faster                                                        |
| coverage                   | 83.5 ms                                                          | 81.8 ms: 1.02x faster                                                        |
| xml_etree_generate         | 85.7 ms                                                          | 84.0 ms: 1.02x faster                                                        |
| xml_etree_process          | 59.7 ms                                                          | 58.6 ms: 1.02x faster                                                        |
| json_dumps                 | 10.8 ms                                                          | 10.6 ms: 1.02x faster                                                        |
| asyncio_tcp                | 378 ms                                                           | 373 ms: 1.01x faster                                                         |
| regex_dna                  | 249 ms                                                           | 247 ms: 1.01x faster                                                         |
| asyncio_websockets         | 395 ms                                                           | 392 ms: 1.01x faster                                                         |
| generators                 | 33.5 ms                                                          | 33.3 ms: 1.01x faster                                                        |
| regex_v8                   | 26.0 ms                                                          | 26.0 ms: 1.00x faster                                                        |
| coroutines                 | 22.0 ms                                                          | 22.0 ms: 1.00x slower                                                        |
| deepcopy_reduce            | 3.39 us                                                          | 3.42 us: 1.01x slower                                                        |
| pickle                     | 10.6 us                                                          | 10.7 us: 1.01x slower                                                        |
| xml_etree_iterparse        | 103 ms                                                           | 104 ms: 1.01x slower                                                         |
| thrift                     | 880 us                                                           | 890 us: 1.01x slower                                                         |
| sqlglot_parse              | 1.39 ms                                                          | 1.41 ms: 1.01x slower                                                        |
| logging_format             | 7.11 us                                                          | 7.21 us: 1.01x slower                                                        |
| regex_effbot               | 3.40 ms                                                          | 3.45 ms: 1.02x slower                                                        |
| json_loads                 | 25.0 us                                                          | 25.4 us: 1.02x slower                                                        |
| sqlglot_normalize          | 120 ms                                                           | 122 ms: 1.02x slower                                                         |
| tornado_http               | 119 ms                                                           | 122 ms: 1.02x slower                                                         |
| 2to3                       | 291 ms                                                           | 297 ms: 1.02x slower                                                         |
| meteor_contest             | 128 ms                                                           | 131 ms: 1.02x slower                                                         |
| logging_simple             | 6.40 us                                                          | 6.54 us: 1.02x slower                                                        |
| python_startup             | 13.2 ms                                                          | 13.5 ms: 1.02x slower                                                        |
| regex_compile              | 144 ms                                                           | 148 ms: 1.02x slower                                                         |
| sympy_expand               | 501 ms                                                           | 514 ms: 1.03x slower                                                         |
| pickle_dict                | 32.8 us                                                          | 33.7 us: 1.03x slower                                                        |
| sqlglot_transpile          | 1.76 ms                                                          | 1.82 ms: 1.03x slower                                                        |
| json                       | 5.35 ms                                                          | 5.51 ms: 1.03x slower                                                        |
| pidigits                   | 254 ms                                                           | 262 ms: 1.03x slower                                                         |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 592 ms: 1.03x slower                                                         |
| dask                       | 391 ms                                                           | 404 ms: 1.03x slower                                                         |
| genshi_text                | 25.9 ms                                                          | 26.8 ms: 1.03x slower                                                        |
| deepcopy_memo              | 37.3 us                                                          | 38.6 us: 1.04x slower                                                        |
| dulwich_log                | 67.3 ms                                                          | 69.8 ms: 1.04x slower                                                        |
| docutils                   | 2.98 sec                                                         | 3.09 sec: 1.04x slower                                                       |
| sympy_str                  | 295 ms                                                           | 306 ms: 1.04x slower                                                         |
| xml_etree_parse            | 144 ms                                                           | 149 ms: 1.04x slower                                                         |
| pprint_safe_repr           | 818 ms                                                           | 851 ms: 1.04x slower                                                         |
| async_tree_none            | 365 ms                                                           | 380 ms: 1.04x slower                                                         |
| deepcopy                   | 377 us                                                           | 394 us: 1.04x slower                                                         |
| pprint_pformat             | 1.66 sec                                                         | 1.74 sec: 1.05x slower                                                       |
| pycparser                  | 1.22 sec                                                         | 1.28 sec: 1.05x slower                                                       |
| sqlglot_optimize           | 59.5 ms                                                          | 62.3 ms: 1.05x slower                                                        |
| gunicorn                   | 1.04 ms                                                          | 1.09 ms: 1.05x slower                                                        |
| crypto_pyaes               | 73.6 ms                                                          | 77.1 ms: 1.05x slower                                                        |
| aiohttp                    | 1.07 ms                                                          | 1.13 ms: 1.05x slower                                                        |
| sympy_sum                  | 155 ms                                                           | 164 ms: 1.06x slower                                                         |
| deltablue                  | 3.37 ms                                                          | 3.58 ms: 1.06x slower                                                        |
| unpickle_pure_python       | 224 us                                                           | 239 us: 1.06x slower                                                         |
| async_generators           | 363 ms                                                           | 388 ms: 1.07x slower                                                         |
| mdp                        | 2.46 sec                                                         | 2.64 sec: 1.07x slower                                                       |
| go                         | 165 ms                                                           | 177 ms: 1.07x slower                                                         |
| chaos                      | 59.6 ms                                                          | 64.1 ms: 1.08x slower                                                        |
| mypy2                      | 764 ms                                                           | 826 ms: 1.08x slower                                                         |
| fannkuch                   | 353 ms                                                           | 385 ms: 1.09x slower                                                         |
| scimark_monte_carlo        | 65.5 ms                                                          | 71.5 ms: 1.09x slower                                                        |
| raytrace                   | 260 ms                                                           | 285 ms: 1.09x slower                                                         |
| sympy_integrate            | 23.2 ms                                                          | 25.5 ms: 1.10x slower                                                        |
| pathlib                    | 17.1 ms                                                          | 19.4 ms: 1.13x slower                                                        |
| nbody                      | 87.8 ms                                                          | 101 ms: 1.15x slower                                                         |
| comprehensions             | 17.0 us                                                          | 19.5 us: 1.15x slower                                                        |
| hexiom                     | 6.35 ms                                                          | 7.39 ms: 1.16x slower                                                        |
| nqueens                    | 88.4 ms                                                          | 105 ms: 1.19x slower                                                         |
| bench_thread_pool          | 908 us                                                           | 1.11 ms: 1.22x slower                                                        |
| scimark_lu                 | 97.5 ms                                                          | 121 ms: 1.24x slower                                                         |
| scimark_sor                | 119 ms                                                           | 154 ms: 1.30x slower                                                         |
| python_startup_no_site     | 8.85 ms                                                          | 11.8 ms: 1.33x slower                                                        |
| Geometric mean             | (ref)                                                            | 1.02x slower                                                                 |

Benchmark hidden because not significant (13): async_tree_none_tg, pylint, pickle_list, logging_silent, asyncio_tcp_ssl, pyflate, chameleon, pickle_pure_python, async_tree_cpu_io_mixed, scimark_fft, genshi_xml, async_tree_memoization_tg, bench_mp_pool
Ignored benchmarks (3) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, django_template, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.06x