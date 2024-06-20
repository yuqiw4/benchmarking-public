# Results vs. 3.13.0b2

- fork: brandtbucher
- ref: justin_refactor
- machine: linux-x86_64
- commit hash: 8ca0f58
- commit date: 2024-04-27
- overall geometric mean: 1.00x faster
- HPT reliability: 96.25%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.06x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6+-8ca0f58 |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 276 ms: 1.01x slower                                                    |
| chameleon      | 7.22 ms                                                    | 7.02 ms: 1.03x faster                                                   |
| docutils       | 2.83 sec                                                   | 2.90 sec: 1.02x slower                                                  |
| tornado_http   | 94.6 ms                                                    | 95.6 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                      | 1.00x slower                                                            |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6+-8ca0f58 |
|----------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 355 ms: 1.06x faster                                                    |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 604 ms: 1.03x slower                                                    |
| Geometric mean             | (ref)                                                      | 1.00x faster                                                            |

Benchmark hidden because not significant (6): async_tree_io, async_tree_memoization_tg, async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_memoization, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6+-8ca0f58 |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 78.9 ms                                                    | 77.2 ms: 1.02x faster                                                   |
| pidigits       | 191 ms                                                     | 189 ms: 1.01x faster                                                    |
| nbody          | 88.3 ms                                                    | 89.9 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                      | 1.01x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6+-8ca0f58 |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.67 ms                                                    | 3.70 ms: 1.01x slower                                                   |
| regex_compile  | 137 ms                                                     | 140 ms: 1.02x slower                                                    |
| regex_dna      | 221 ms                                                     | 227 ms: 1.02x slower                                                    |
| regex_v8       | 25.1 ms                                                    | 26.2 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                      | 1.02x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6+-8ca0f58 |
|----------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_parse      | 162 ms                                                     | 153 ms: 1.06x faster                                                    |
| tomli_loads          | 2.12 sec                                                   | 2.04 sec: 1.04x faster                                                  |
| json_loads           | 28.9 us                                                    | 28.0 us: 1.03x faster                                                   |
| unpickle_list        | 5.34 us                                                    | 5.20 us: 1.03x faster                                                   |
| xml_etree_iterparse  | 107 ms                                                     | 104 ms: 1.03x faster                                                    |
| xml_etree_process    | 61.2 ms                                                    | 59.6 ms: 1.03x faster                                                   |
| json_dumps           | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                                   |
| pickle_pure_python   | 305 us                                                     | 301 us: 1.01x faster                                                    |
| xml_etree_generate   | 87.4 ms                                                    | 87.0 ms: 1.01x faster                                                   |
| pickle_list          | 5.11 us                                                    | 5.08 us: 1.01x faster                                                   |
| pickle_dict          | 34.8 us                                                    | 35.1 us: 1.01x slower                                                   |
| unpickle_pure_python | 218 us                                                     | 233 us: 1.07x slower                                                    |
| unpickle             | 15.1 us                                                    | 16.3 us: 1.07x slower                                                   |
| Geometric mean       | (ref)                                                      | 1.01x faster                                                            |

Benchmark hidden because not significant (1): pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6+-8ca0f58 |
|------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 11.0 ms: 1.02x slower                                                   |
| python_startup_no_site | 7.11 ms                                                    | 7.57 ms: 1.07x slower                                                   |
| Geometric mean         | (ref)                                                      | 1.04x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6+-8ca0f58 |
|-----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 10.8 ms: 1.04x faster                                                   |
| django_template | 34.8 ms                                                    | 35.7 ms: 1.03x slower                                                   |
| genshi_text     | 23.7 ms                                                    | 24.4 ms: 1.03x slower                                                   |
| genshi_xml      | 51.6 ms                                                    | 53.3 ms: 1.03x slower                                                   |
| Geometric mean  | (ref)                                                      | 1.01x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6+-8ca0f58 |
|----------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 113 us: 1.45x faster                                                    |
| richards                   | 50.9 ms                                                    | 43.1 ms: 1.18x faster                                                   |
| richards_super             | 57.4 ms                                                    | 49.0 ms: 1.17x faster                                                   |
| scimark_fft                | 392 ms                                                     | 336 ms: 1.17x faster                                                    |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 4.69 ms: 1.12x faster                                                   |
| logging_silent             | 105 ns                                                     | 98.0 ns: 1.07x faster                                                   |
| async_tree_none            | 378 ms                                                     | 355 ms: 1.06x faster                                                    |
| xml_etree_parse            | 162 ms                                                     | 153 ms: 1.06x faster                                                    |
| pyflate                    | 484 ms                                                     | 459 ms: 1.06x faster                                                    |
| deepcopy_reduce            | 3.35 us                                                    | 3.17 us: 1.05x faster                                                   |
| crypto_pyaes               | 77.5 ms                                                    | 73.7 ms: 1.05x faster                                                   |
| deepcopy_memo              | 39.7 us                                                    | 37.9 us: 1.05x faster                                                   |
| deepcopy                   | 367 us                                                     | 353 us: 1.04x faster                                                    |
| tomli_loads                | 2.12 sec                                                   | 2.04 sec: 1.04x faster                                                  |
| fannkuch                   | 402 ms                                                     | 387 ms: 1.04x faster                                                    |
| mako                       | 11.2 ms                                                    | 10.8 ms: 1.04x faster                                                   |
| json                       | 5.31 ms                                                    | 5.12 ms: 1.04x faster                                                   |
| sqlite_synth               | 2.99 us                                                    | 2.89 us: 1.04x faster                                                   |
| spectral_norm              | 116 ms                                                     | 112 ms: 1.03x faster                                                    |
| json_loads                 | 28.9 us                                                    | 28.0 us: 1.03x faster                                                   |
| create_gc_cycles           | 1.82 ms                                                    | 1.76 ms: 1.03x faster                                                   |
| unpickle_list              | 5.34 us                                                    | 5.20 us: 1.03x faster                                                   |
| chameleon                  | 7.22 ms                                                    | 7.02 ms: 1.03x faster                                                   |
| xml_etree_iterparse        | 107 ms                                                     | 104 ms: 1.03x faster                                                    |
| xml_etree_process          | 61.2 ms                                                    | 59.6 ms: 1.03x faster                                                   |
| coroutines                 | 23.2 ms                                                    | 22.6 ms: 1.03x faster                                                   |
| pprint_safe_repr           | 758 ms                                                     | 740 ms: 1.02x faster                                                    |
| json_dumps                 | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                                   |
| float                      | 78.9 ms                                                    | 77.2 ms: 1.02x faster                                                   |
| pickle_pure_python         | 305 us                                                     | 301 us: 1.01x faster                                                    |
| pidigits                   | 191 ms                                                     | 189 ms: 1.01x faster                                                    |
| thrift                     | 823 us                                                     | 817 us: 1.01x faster                                                    |
| logging_format             | 6.47 us                                                    | 6.43 us: 1.01x faster                                                   |
| xml_etree_generate         | 87.4 ms                                                    | 87.0 ms: 1.01x faster                                                   |
| pickle_list                | 5.11 us                                                    | 5.08 us: 1.01x faster                                                   |
| mdp                        | 2.79 sec                                                   | 2.78 sec: 1.00x faster                                                  |
| meteor_contest             | 110 ms                                                     | 110 ms: 1.00x slower                                                    |
| generators                 | 29.6 ms                                                    | 29.8 ms: 1.01x slower                                                   |
| 2to3                       | 274 ms                                                     | 276 ms: 1.01x slower                                                    |
| regex_effbot               | 3.67 ms                                                    | 3.70 ms: 1.01x slower                                                   |
| gc_traversal               | 3.98 ms                                                    | 4.01 ms: 1.01x slower                                                   |
| bench_mp_pool              | 23.9 ms                                                    | 24.1 ms: 1.01x slower                                                   |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.86 sec: 1.01x slower                                                  |
| tornado_http               | 94.6 ms                                                    | 95.6 ms: 1.01x slower                                                   |
| pickle_dict                | 34.8 us                                                    | 35.1 us: 1.01x slower                                                   |
| sqlglot_normalize          | 110 ms                                                     | 111 ms: 1.01x slower                                                    |
| gunicorn                   | 1.28 ms                                                    | 1.30 ms: 1.01x slower                                                   |
| telco                      | 8.41 ms                                                    | 8.56 ms: 1.02x slower                                                   |
| nbody                      | 88.3 ms                                                    | 89.9 ms: 1.02x slower                                                   |
| scimark_sor                | 127 ms                                                     | 130 ms: 1.02x slower                                                    |
| pathlib                    | 17.3 ms                                                    | 17.7 ms: 1.02x slower                                                   |
| python_startup             | 10.8 ms                                                    | 11.0 ms: 1.02x slower                                                   |
| sqlglot_optimize           | 55.5 ms                                                    | 56.7 ms: 1.02x slower                                                   |
| aiohttp                    | 1.18 ms                                                    | 1.21 ms: 1.02x slower                                                   |
| raytrace                   | 267 ms                                                     | 272 ms: 1.02x slower                                                    |
| bench_thread_pool          | 834 us                                                     | 852 us: 1.02x slower                                                    |
| regex_compile              | 137 ms                                                     | 140 ms: 1.02x slower                                                    |
| regex_dna                  | 221 ms                                                     | 227 ms: 1.02x slower                                                    |
| docutils                   | 2.83 sec                                                   | 2.90 sec: 1.02x slower                                                  |
| django_template            | 34.8 ms                                                    | 35.7 ms: 1.03x slower                                                   |
| dulwich_log                | 67.2 ms                                                    | 69.1 ms: 1.03x slower                                                   |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 604 ms: 1.03x slower                                                    |
| genshi_text                | 23.7 ms                                                    | 24.4 ms: 1.03x slower                                                   |
| djangocms                  | 31.5 us                                                    | 32.4 us: 1.03x slower                                                   |
| chaos                      | 61.3 ms                                                    | 63.2 ms: 1.03x slower                                                   |
| sympy_str                  | 282 ms                                                     | 291 ms: 1.03x slower                                                    |
| genshi_xml                 | 51.6 ms                                                    | 53.3 ms: 1.03x slower                                                   |
| sympy_expand               | 473 ms                                                     | 489 ms: 1.04x slower                                                    |
| regex_v8                   | 25.1 ms                                                    | 26.2 ms: 1.04x slower                                                   |
| async_generators           | 442 ms                                                     | 462 ms: 1.04x slower                                                    |
| pycparser                  | 1.16 sec                                                   | 1.21 sec: 1.04x slower                                                  |
| mypy2                      | 742 ms                                                     | 780 ms: 1.05x slower                                                    |
| go                         | 145 ms                                                     | 153 ms: 1.06x slower                                                    |
| coverage                   | 93.1 ms                                                    | 98.7 ms: 1.06x slower                                                   |
| sympy_sum                  | 156 ms                                                     | 165 ms: 1.06x slower                                                    |
| sympy_integrate            | 20.5 ms                                                    | 21.8 ms: 1.06x slower                                                   |
| python_startup_no_site     | 7.11 ms                                                    | 7.57 ms: 1.07x slower                                                   |
| unpickle_pure_python       | 218 us                                                     | 233 us: 1.07x slower                                                    |
| scimark_lu                 | 122 ms                                                     | 130 ms: 1.07x slower                                                    |
| unpickle                   | 15.1 us                                                    | 16.3 us: 1.07x slower                                                   |
| comprehensions             | 16.6 us                                                    | 17.9 us: 1.08x slower                                                   |
| nqueens                    | 81.4 ms                                                    | 88.6 ms: 1.09x slower                                                   |
| hexiom                     | 6.30 ms                                                    | 6.86 ms: 1.09x slower                                                   |
| deltablue                  | 3.25 ms                                                    | 3.62 ms: 1.11x slower                                                   |
| Geometric mean             | (ref)                                                      | 1.00x faster                                                            |

Benchmark hidden because not significant (17): async_tree_io, pprint_pformat, async_tree_memoization_tg, async_tree_none_tg, sqlglot_parse, async_tree_cpu_io_mixed, asyncio_websockets, scimark_monte_carlo, sqlglot_transpile, pickle, asyncio_tcp, async_tree_memoization, html5lib, logging_simple, dask, async_tree_io_tg, pylint
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 96.25% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.06x