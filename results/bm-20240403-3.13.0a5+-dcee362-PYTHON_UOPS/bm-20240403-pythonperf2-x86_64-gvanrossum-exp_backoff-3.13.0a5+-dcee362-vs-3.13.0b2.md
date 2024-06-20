# Results vs. 3.13.0b2

- fork: gvanrossum
- ref: exp_backoff
- machine: linux-x86_64
- commit hash: dcee362
- commit date: 2024-04-03
- overall geometric mean: 1.10x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-pythonperf2-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:----------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 291 ms                                                           | 316 ms: 1.09x slower                                                    |
| chameleon      | 7.40 ms                                                          | 7.77 ms: 1.05x slower                                                   |
| docutils       | 2.98 sec                                                         | 3.24 sec: 1.09x slower                                                  |
| html5lib       | 74.7 ms                                                          | 79.7 ms: 1.07x slower                                                   |
| tornado_http   | 119 ms                                                           | 129 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                            | 1.07x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-pythonperf2-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------------------|:----------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 604 ms                                                           | 628 ms: 1.04x slower                                                    |
| async_tree_none_tg         | 340 ms                                                           | 354 ms: 1.04x slower                                                    |
| async_tree_io              | 873 ms                                                           | 912 ms: 1.04x slower                                                    |
| async_tree_memoization_tg  | 421 ms                                                           | 447 ms: 1.06x slower                                                    |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 612 ms: 1.07x slower                                                    |
| async_tree_none            | 365 ms                                                           | 395 ms: 1.08x slower                                                    |
| Geometric mean             | (ref)                                                            | 1.04x slower                                                            |

Benchmark hidden because not significant (2): async_tree_io_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-pythonperf2-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:----------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 254 ms                                                           | 266 ms: 1.05x slower                                                    |
| float          | 80.2 ms                                                          | 91.6 ms: 1.14x slower                                                   |
| nbody          | 87.8 ms                                                          | 114 ms: 1.30x slower                                                    |
| Geometric mean | (ref)                                                            | 1.16x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-pythonperf2-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:----------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_dna      | 249 ms                                                           | 236 ms: 1.06x faster                                                    |
| regex_v8       | 26.0 ms                                                          | 25.6 ms: 1.02x faster                                                   |
| regex_effbot   | 3.40 ms                                                          | 3.58 ms: 1.05x slower                                                   |
| regex_compile  | 144 ms                                                           | 196 ms: 1.36x slower                                                    |
| Geometric mean | (ref)                                                            | 1.07x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-pythonperf2-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------------|:----------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| unpickle             | 15.7 us                                                          | 14.8 us: 1.06x faster                                                   |
| pickle_dict          | 32.8 us                                                          | 31.2 us: 1.05x faster                                                   |
| pickle               | 10.6 us                                                          | 10.4 us: 1.02x faster                                                   |
| pickle_list          | 4.44 us                                                          | 4.38 us: 1.02x faster                                                   |
| json_dumps           | 10.8 ms                                                          | 10.7 ms: 1.01x faster                                                   |
| json_loads           | 25.0 us                                                          | 25.3 us: 1.01x slower                                                   |
| unpickle_list        | 4.70 us                                                          | 4.77 us: 1.02x slower                                                   |
| xml_etree_process    | 59.7 ms                                                          | 62.5 ms: 1.05x slower                                                   |
| xml_etree_generate   | 85.7 ms                                                          | 90.3 ms: 1.05x slower                                                   |
| xml_etree_iterparse  | 103 ms                                                           | 108 ms: 1.06x slower                                                    |
| pickle_pure_python   | 307 us                                                           | 326 us: 1.06x slower                                                    |
| tomli_loads          | 2.40 sec                                                         | 2.74 sec: 1.14x slower                                                  |
| unpickle_pure_python | 224 us                                                           | 293 us: 1.31x slower                                                    |
| Geometric mean       | (ref)                                                            | 1.03x slower                                                            |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-pythonperf2-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|------------------------|:----------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 13.2 ms                                                          | 13.0 ms: 1.02x faster                                                   |
| python_startup_no_site | 8.85 ms                                                          | 11.2 ms: 1.27x slower                                                   |
| Geometric mean         | (ref)                                                            | 1.12x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-pythonperf2-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:----------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml     | 58.1 ms                                                          | 62.3 ms: 1.07x slower                                                   |
| genshi_text    | 25.9 ms                                                          | 27.9 ms: 1.08x slower                                                   |
| mako           | 10.4 ms                                                          | 13.2 ms: 1.27x slower                                                   |
| Geometric mean | (ref)                                                            | 1.14x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-pythonperf2-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------------------|:----------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| typing_runtime_protocols   | 171 us                                                           | 127 us: 1.35x faster                                                    |
| create_gc_cycles           | 2.00 ms                                                          | 1.85 ms: 1.08x faster                                                   |
| unpickle                   | 15.7 us                                                          | 14.8 us: 1.06x faster                                                   |
| regex_dna                  | 249 ms                                                           | 236 ms: 1.06x faster                                                    |
| pickle_dict                | 32.8 us                                                          | 31.2 us: 1.05x faster                                                   |
| pickle                     | 10.6 us                                                          | 10.4 us: 1.02x faster                                                   |
| python_startup             | 13.2 ms                                                          | 13.0 ms: 1.02x faster                                                   |
| regex_v8                   | 26.0 ms                                                          | 25.6 ms: 1.02x faster                                                   |
| pickle_list                | 4.44 us                                                          | 4.38 us: 1.02x faster                                                   |
| json_dumps                 | 10.8 ms                                                          | 10.7 ms: 1.01x faster                                                   |
| asyncio_websockets         | 395 ms                                                           | 392 ms: 1.01x faster                                                    |
| sqlite_synth               | 2.80 us                                                          | 2.78 us: 1.01x faster                                                   |
| richards_super             | 61.2 ms                                                          | 60.9 ms: 1.01x faster                                                   |
| generators                 | 33.5 ms                                                          | 33.7 ms: 1.00x slower                                                   |
| json_loads                 | 25.0 us                                                          | 25.3 us: 1.01x slower                                                   |
| asyncio_tcp_ssl            | 1.58 sec                                                         | 1.60 sec: 1.01x slower                                                  |
| asyncio_tcp                | 378 ms                                                           | 383 ms: 1.01x slower                                                    |
| json                       | 5.35 ms                                                          | 5.43 ms: 1.01x slower                                                   |
| richards                   | 53.4 ms                                                          | 54.2 ms: 1.01x slower                                                   |
| unpickle_list              | 4.70 us                                                          | 4.77 us: 1.02x slower                                                   |
| telco                      | 8.40 ms                                                          | 8.59 ms: 1.02x slower                                                   |
| logging_format             | 7.11 us                                                          | 7.29 us: 1.03x slower                                                   |
| coroutines                 | 22.0 ms                                                          | 22.6 ms: 1.03x slower                                                   |
| logging_simple             | 6.40 us                                                          | 6.59 us: 1.03x slower                                                   |
| async_tree_cpu_io_mixed    | 604 ms                                                           | 628 ms: 1.04x slower                                                    |
| async_tree_none_tg         | 340 ms                                                           | 354 ms: 1.04x slower                                                    |
| async_tree_io              | 873 ms                                                           | 912 ms: 1.04x slower                                                    |
| xml_etree_process          | 59.7 ms                                                          | 62.5 ms: 1.05x slower                                                   |
| pidigits                   | 254 ms                                                           | 266 ms: 1.05x slower                                                    |
| chameleon                  | 7.40 ms                                                          | 7.77 ms: 1.05x slower                                                   |
| bench_thread_pool          | 908 us                                                           | 954 us: 1.05x slower                                                    |
| coverage                   | 83.5 ms                                                          | 87.8 ms: 1.05x slower                                                   |
| regex_effbot               | 3.40 ms                                                          | 3.58 ms: 1.05x slower                                                   |
| xml_etree_generate         | 85.7 ms                                                          | 90.3 ms: 1.05x slower                                                   |
| xml_etree_iterparse        | 103 ms                                                           | 108 ms: 1.06x slower                                                    |
| pickle_pure_python         | 307 us                                                           | 326 us: 1.06x slower                                                    |
| async_generators           | 363 ms                                                           | 385 ms: 1.06x slower                                                    |
| async_tree_memoization_tg  | 421 ms                                                           | 447 ms: 1.06x slower                                                    |
| aiohttp                    | 1.07 ms                                                          | 1.14 ms: 1.07x slower                                                   |
| html5lib                   | 74.7 ms                                                          | 79.7 ms: 1.07x slower                                                   |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 612 ms: 1.07x slower                                                    |
| gunicorn                   | 1.04 ms                                                          | 1.12 ms: 1.07x slower                                                   |
| dask                       | 391 ms                                                           | 419 ms: 1.07x slower                                                    |
| genshi_xml                 | 58.1 ms                                                          | 62.3 ms: 1.07x slower                                                   |
| logging_silent             | 96.3 ns                                                          | 103 ns: 1.07x slower                                                    |
| sqlglot_normalize          | 120 ms                                                           | 129 ms: 1.07x slower                                                    |
| genshi_text                | 25.9 ms                                                          | 27.9 ms: 1.08x slower                                                   |
| tornado_http               | 119 ms                                                           | 129 ms: 1.08x slower                                                    |
| deepcopy_reduce            | 3.39 us                                                          | 3.66 us: 1.08x slower                                                   |
| async_tree_none            | 365 ms                                                           | 395 ms: 1.08x slower                                                    |
| mdp                        | 2.46 sec                                                         | 2.67 sec: 1.08x slower                                                  |
| 2to3                       | 291 ms                                                           | 316 ms: 1.09x slower                                                    |
| docutils                   | 2.98 sec                                                         | 3.24 sec: 1.09x slower                                                  |
| pycparser                  | 1.22 sec                                                         | 1.35 sec: 1.10x slower                                                  |
| deepcopy                   | 377 us                                                           | 417 us: 1.10x slower                                                    |
| sqlglot_transpile          | 1.76 ms                                                          | 1.95 ms: 1.11x slower                                                   |
| meteor_contest             | 128 ms                                                           | 142 ms: 1.11x slower                                                    |
| mypy2                      | 764 ms                                                           | 852 ms: 1.11x slower                                                    |
| sqlglot_parse              | 1.39 ms                                                          | 1.55 ms: 1.12x slower                                                   |
| sqlglot_optimize           | 59.5 ms                                                          | 67.0 ms: 1.13x slower                                                   |
| tomli_loads                | 2.40 sec                                                         | 2.74 sec: 1.14x slower                                                  |
| float                      | 80.2 ms                                                          | 91.6 ms: 1.14x slower                                                   |
| sympy_integrate            | 23.2 ms                                                          | 26.5 ms: 1.15x slower                                                   |
| dulwich_log                | 67.3 ms                                                          | 77.1 ms: 1.15x slower                                                   |
| sympy_expand               | 501 ms                                                           | 577 ms: 1.15x slower                                                    |
| sympy_sum                  | 155 ms                                                           | 180 ms: 1.16x slower                                                    |
| raytrace                   | 260 ms                                                           | 304 ms: 1.17x slower                                                    |
| deepcopy_memo              | 37.3 us                                                          | 43.7 us: 1.17x slower                                                   |
| sympy_str                  | 295 ms                                                           | 347 ms: 1.18x slower                                                    |
| pprint_safe_repr           | 818 ms                                                           | 971 ms: 1.19x slower                                                    |
| crypto_pyaes               | 73.6 ms                                                          | 87.7 ms: 1.19x slower                                                   |
| pprint_pformat             | 1.66 sec                                                         | 1.98 sec: 1.20x slower                                                  |
| pathlib                    | 17.1 ms                                                          | 20.6 ms: 1.20x slower                                                   |
| chaos                      | 59.6 ms                                                          | 72.5 ms: 1.22x slower                                                   |
| deltablue                  | 3.37 ms                                                          | 4.14 ms: 1.23x slower                                                   |
| pyflate                    | 482 ms                                                           | 604 ms: 1.25x slower                                                    |
| python_startup_no_site     | 8.85 ms                                                          | 11.2 ms: 1.27x slower                                                   |
| go                         | 165 ms                                                           | 210 ms: 1.27x slower                                                    |
| mako                       | 10.4 ms                                                          | 13.2 ms: 1.27x slower                                                   |
| nqueens                    | 88.4 ms                                                          | 114 ms: 1.29x slower                                                    |
| scimark_fft                | 312 ms                                                           | 404 ms: 1.30x slower                                                    |
| nbody                      | 87.8 ms                                                          | 114 ms: 1.30x slower                                                    |
| unpickle_pure_python       | 224 us                                                           | 293 us: 1.31x slower                                                    |
| fannkuch                   | 353 ms                                                           | 466 ms: 1.32x slower                                                    |
| scimark_sor                | 119 ms                                                           | 159 ms: 1.34x slower                                                    |
| regex_compile              | 144 ms                                                           | 196 ms: 1.36x slower                                                    |
| scimark_lu                 | 97.5 ms                                                          | 135 ms: 1.39x slower                                                    |
| scimark_monte_carlo        | 65.5 ms                                                          | 92.2 ms: 1.41x slower                                                   |
| scimark_sparse_mat_mult    | 4.28 ms                                                          | 6.14 ms: 1.43x slower                                                   |
| spectral_norm              | 97.3 ms                                                          | 140 ms: 1.44x slower                                                    |
| comprehensions             | 17.0 us                                                          | 24.7 us: 1.46x slower                                                   |
| hexiom                     | 6.35 ms                                                          | 9.76 ms: 1.54x slower                                                   |
| Geometric mean             | (ref)                                                            | 1.10x slower                                                            |

Benchmark hidden because not significant (7): bench_mp_pool, async_tree_io_tg, xml_etree_parse, gc_traversal, thrift, async_tree_memoization, pylint
Ignored benchmarks (3) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, django_template, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 0.98x