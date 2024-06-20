# Results vs. 3.12.0

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: linux-x86_64
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.01x faster
- HPT reliability: 76.77%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.91x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 285 ms                                                       | 286 ms: 1.00x slower                                                         |
| chameleon      | 7.23 ms                                                      | 7.51 ms: 1.04x slower                                                        |
| docutils       | 2.87 sec                                                     | 3.00 sec: 1.05x slower                                                       |
| tornado_http   | 121 ms                                                       | 120 ms: 1.01x faster                                                         |
| Geometric mean | (ref)                                                        | 1.02x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 540 ms                                                       | 417 ms: 1.30x faster                                                         |
| async_tree_none_tg         | 431 ms                                                       | 336 ms: 1.28x faster                                                         |
| async_tree_none            | 452 ms                                                       | 369 ms: 1.22x faster                                                         |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 576 ms: 1.21x faster                                                         |
| async_tree_io_tg           | 1.05 sec                                                     | 883 ms: 1.19x faster                                                         |
| async_tree_memoization     | 544 ms                                                       | 466 ms: 1.17x faster                                                         |
| async_tree_io              | 1.04 sec                                                     | 907 ms: 1.15x faster                                                         |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 616 ms: 1.13x faster                                                         |
| Geometric mean             | (ref)                                                        | 1.21x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 88.0 ms                                                      | 85.7 ms: 1.03x faster                                                        |
| pidigits       | 265 ms                                                       | 263 ms: 1.01x faster                                                         |
| Geometric mean | (ref)                                                        | 1.01x faster                                                                 |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_effbot   | 3.57 ms                                                      | 3.47 ms: 1.03x faster                                                        |
| regex_dna      | 239 ms                                                       | 236 ms: 1.01x faster                                                         |
| regex_compile  | 144 ms                                                       | 145 ms: 1.00x slower                                                         |
| regex_v8       | 23.6 ms                                                      | 25.7 ms: 1.09x slower                                                        |
| Geometric mean | (ref)                                                        | 1.01x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pickle_dict          | 32.5 us                                                      | 31.0 us: 1.05x faster                                                        |
| pickle_pure_python   | 318 us                                                       | 308 us: 1.03x faster                                                         |
| pickle               | 10.5 us                                                      | 10.2 us: 1.03x faster                                                        |
| xml_etree_generate   | 86.1 ms                                                      | 84.8 ms: 1.02x faster                                                        |
| unpickle_pure_python | 210 us                                                       | 210 us: 1.00x slower                                                         |
| json_loads           | 24.4 us                                                      | 24.5 us: 1.01x slower                                                        |
| unpickle_list        | 4.66 us                                                      | 4.72 us: 1.01x slower                                                        |
| tomli_loads          | 2.16 sec                                                     | 2.19 sec: 1.02x slower                                                       |
| xml_etree_process    | 58.4 ms                                                      | 59.8 ms: 1.02x slower                                                        |
| json_dumps           | 10.2 ms                                                      | 10.7 ms: 1.04x slower                                                        |
| unpickle             | 14.8 us                                                      | 15.5 us: 1.05x slower                                                        |
| Geometric mean       | (ref)                                                        | 1.00x slower                                                                 |

Benchmark hidden because not significant (3): pickle_list, xml_etree_parse, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup_no_site | 8.64 ms                                                      | 8.84 ms: 1.02x slower                                                        |
| python_startup         | 11.6 ms                                                      | 12.9 ms: 1.11x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.07x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| django_template | 38.2 ms                                                      | 38.4 ms: 1.01x slower                                                        |
| mako            | 10.0 ms                                                      | 10.3 ms: 1.03x slower                                                        |
| Geometric mean  | (ref)                                                        | 1.02x slower                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 540 ms                                                       | 417 ms: 1.30x faster                                                         |
| comprehensions             | 21.9 us                                                      | 16.9 us: 1.30x faster                                                        |
| async_tree_none_tg         | 431 ms                                                       | 336 ms: 1.28x faster                                                         |
| async_tree_none            | 452 ms                                                       | 369 ms: 1.22x faster                                                         |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 576 ms: 1.21x faster                                                         |
| raytrace                   | 298 ms                                                       | 249 ms: 1.19x faster                                                         |
| async_tree_io_tg           | 1.05 sec                                                     | 883 ms: 1.19x faster                                                         |
| async_tree_memoization     | 544 ms                                                       | 466 ms: 1.17x faster                                                         |
| async_tree_io              | 1.04 sec                                                     | 907 ms: 1.15x faster                                                         |
| scimark_monte_carlo        | 69.0 ms                                                      | 60.7 ms: 1.14x faster                                                        |
| generators                 | 37.4 ms                                                      | 33.0 ms: 1.13x faster                                                        |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 616 ms: 1.13x faster                                                         |
| coroutines                 | 23.0 ms                                                      | 20.6 ms: 1.12x faster                                                        |
| crypto_pyaes               | 80.3 ms                                                      | 72.3 ms: 1.11x faster                                                        |
| pathlib                    | 18.9 ms                                                      | 17.2 ms: 1.10x faster                                                        |
| async_generators           | 390 ms                                                       | 358 ms: 1.09x faster                                                         |
| chaos                      | 64.0 ms                                                      | 59.2 ms: 1.08x faster                                                        |
| bench_thread_pool          | 950 us                                                       | 886 us: 1.07x faster                                                         |
| mypy2                      | 830 ms                                                       | 774 ms: 1.07x faster                                                         |
| sympy_sum                  | 162 ms                                                       | 154 ms: 1.05x faster                                                         |
| pickle_dict                | 32.5 us                                                      | 31.0 us: 1.05x faster                                                        |
| logging_format             | 7.48 us                                                      | 7.15 us: 1.05x faster                                                        |
| bench_mp_pool              | 4.76 ms                                                      | 4.56 ms: 1.05x faster                                                        |
| pickle_pure_python         | 318 us                                                       | 308 us: 1.03x faster                                                         |
| nqueens                    | 89.9 ms                                                      | 87.0 ms: 1.03x faster                                                        |
| scimark_lu                 | 98.8 ms                                                      | 95.7 ms: 1.03x faster                                                        |
| sympy_integrate            | 23.9 ms                                                      | 23.2 ms: 1.03x faster                                                        |
| mdp                        | 2.57 sec                                                     | 2.50 sec: 1.03x faster                                                       |
| regex_effbot               | 3.57 ms                                                      | 3.47 ms: 1.03x faster                                                        |
| pickle                     | 10.5 us                                                      | 10.2 us: 1.03x faster                                                        |
| nbody                      | 88.0 ms                                                      | 85.7 ms: 1.03x faster                                                        |
| sympy_str                  | 302 ms                                                       | 296 ms: 1.02x faster                                                         |
| logging_simple             | 6.71 us                                                      | 6.58 us: 1.02x faster                                                        |
| pprint_pformat             | 1.65 sec                                                     | 1.63 sec: 1.02x faster                                                       |
| sqlite_synth               | 2.77 us                                                      | 2.73 us: 1.02x faster                                                        |
| xml_etree_generate         | 86.1 ms                                                      | 84.8 ms: 1.02x faster                                                        |
| asyncio_tcp                | 378 ms                                                       | 372 ms: 1.02x faster                                                         |
| tornado_http               | 121 ms                                                       | 120 ms: 1.01x faster                                                         |
| regex_dna                  | 239 ms                                                       | 236 ms: 1.01x faster                                                         |
| deltablue                  | 3.24 ms                                                      | 3.20 ms: 1.01x faster                                                        |
| pprint_safe_repr           | 807 ms                                                       | 798 ms: 1.01x faster                                                         |
| logging_silent             | 94.4 ns                                                      | 93.4 ns: 1.01x faster                                                        |
| meteor_contest             | 128 ms                                                       | 127 ms: 1.01x faster                                                         |
| asyncio_tcp_ssl            | 1.59 sec                                                     | 1.57 sec: 1.01x faster                                                       |
| pidigits                   | 265 ms                                                       | 263 ms: 1.01x faster                                                         |
| 2to3                       | 285 ms                                                       | 286 ms: 1.00x slower                                                         |
| unpickle_pure_python       | 210 us                                                       | 210 us: 1.00x slower                                                         |
| regex_compile              | 144 ms                                                       | 145 ms: 1.00x slower                                                         |
| json_loads                 | 24.4 us                                                      | 24.5 us: 1.01x slower                                                        |
| django_template            | 38.2 ms                                                      | 38.4 ms: 1.01x slower                                                        |
| dulwich_log                | 65.4 ms                                                      | 65.9 ms: 1.01x slower                                                        |
| fannkuch                   | 350 ms                                                       | 353 ms: 1.01x slower                                                         |
| sqlglot_normalize          | 116 ms                                                       | 117 ms: 1.01x slower                                                         |
| hexiom                     | 5.96 ms                                                      | 6.02 ms: 1.01x slower                                                        |
| sqlglot_optimize           | 57.5 ms                                                      | 58.3 ms: 1.01x slower                                                        |
| unpickle_list              | 4.66 us                                                      | 4.72 us: 1.01x slower                                                        |
| sqlglot_parse              | 1.38 ms                                                      | 1.40 ms: 1.02x slower                                                        |
| tomli_loads                | 2.16 sec                                                     | 2.19 sec: 1.02x slower                                                       |
| pycparser                  | 1.23 sec                                                     | 1.26 sec: 1.02x slower                                                       |
| python_startup_no_site     | 8.64 ms                                                      | 8.84 ms: 1.02x slower                                                        |
| scimark_fft                | 301 ms                                                       | 308 ms: 1.02x slower                                                         |
| xml_etree_process          | 58.4 ms                                                      | 59.8 ms: 1.02x slower                                                        |
| mako                       | 10.0 ms                                                      | 10.3 ms: 1.03x slower                                                        |
| deepcopy_memo              | 36.8 us                                                      | 38.0 us: 1.03x slower                                                        |
| sympy_expand               | 484 ms                                                       | 502 ms: 1.04x slower                                                         |
| gunicorn                   | 1.00 ms                                                      | 1.04 ms: 1.04x slower                                                        |
| scimark_sparse_mat_mult    | 4.21 ms                                                      | 4.37 ms: 1.04x slower                                                        |
| chameleon                  | 7.23 ms                                                      | 7.51 ms: 1.04x slower                                                        |
| aiohttp                    | 1.02 ms                                                      | 1.06 ms: 1.04x slower                                                        |
| json_dumps                 | 10.2 ms                                                      | 10.7 ms: 1.04x slower                                                        |
| deepcopy_reduce            | 3.37 us                                                      | 3.52 us: 1.05x slower                                                        |
| unpickle                   | 14.8 us                                                      | 15.5 us: 1.05x slower                                                        |
| docutils                   | 2.87 sec                                                     | 3.00 sec: 1.05x slower                                                       |
| go                         | 150 ms                                                       | 157 ms: 1.05x slower                                                         |
| deepcopy                   | 368 us                                                       | 388 us: 1.05x slower                                                         |
| json                       | 5.12 ms                                                      | 5.41 ms: 1.06x slower                                                        |
| spectral_norm              | 91.6 ms                                                      | 98.1 ms: 1.07x slower                                                        |
| scimark_sor                | 109 ms                                                       | 118 ms: 1.09x slower                                                         |
| regex_v8                   | 23.6 ms                                                      | 25.7 ms: 1.09x slower                                                        |
| pyflate                    | 439 ms                                                       | 483 ms: 1.10x slower                                                         |
| python_startup             | 11.6 ms                                                      | 12.9 ms: 1.11x slower                                                        |
| richards                   | 45.7 ms                                                      | 50.9 ms: 1.11x slower                                                        |
| typing_runtime_protocols   | 152 us                                                       | 169 us: 1.11x slower                                                         |
| richards_super             | 51.3 ms                                                      | 57.6 ms: 1.12x slower                                                        |
| telco                      | 6.96 ms                                                      | 7.90 ms: 1.13x slower                                                        |
| coverage                   | 66.7 ms                                                      | 78.1 ms: 1.17x slower                                                        |
| create_gc_cycles           | 1.59 ms                                                      | 1.98 ms: 1.25x slower                                                        |
| gc_traversal               | 3.48 ms                                                      | 4.75 ms: 1.37x slower                                                        |
| Geometric mean             | (ref)                                                        | 1.01x faster                                                                 |

Benchmark hidden because not significant (7): pickle_list, float, xml_etree_parse, asyncio_websockets, sqlglot_transpile, dask, xml_etree_iterparse
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240427-3.13.0a6+-51aefc5/bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 76.77% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.91x