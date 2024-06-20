# Results vs. 3.13.0b2

- fork: mdboom
- ref: dont_inline
- machine: linux-x86_64
- commit hash: c35ee28
- commit date: 2024-04-04
- overall geometric mean: 1.01x slower
- HPT reliability: 99.87%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.06x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------|:----------------------------------------------------------:|:-------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 277 ms: 1.01x slower                                          |
| chameleon      | 7.22 ms                                                    | 6.86 ms: 1.05x faster                                         |
| docutils       | 2.83 sec                                                   | 2.92 sec: 1.03x slower                                        |
| html5lib       | 67.2 ms                                                    | 67.7 ms: 1.01x slower                                         |
| tornado_http   | 94.6 ms                                                    | 96.1 ms: 1.02x slower                                         |
| Geometric mean | (ref)                                                      | 1.00x slower                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------------------|:----------------------------------------------------------:|:-------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 355 ms: 1.07x faster                                          |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 602 ms: 1.02x slower                                          |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                  |

Benchmark hidden because not significant (6): async_tree_memoization, async_tree_io, async_tree_memoization_tg, async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------|:----------------------------------------------------------:|:-------------------------------------------------------------:|
| float          | 78.9 ms                                                    | 76.9 ms: 1.03x faster                                         |
| nbody          | 88.3 ms                                                    | 91.1 ms: 1.03x slower                                         |
| pidigits       | 191 ms                                                     | 207 ms: 1.08x slower                                          |
| Geometric mean | (ref)                                                      | 1.03x slower                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------|:----------------------------------------------------------:|:-------------------------------------------------------------:|
| regex_effbot   | 3.67 ms                                                    | 3.78 ms: 1.03x slower                                         |
| regex_v8       | 25.1 ms                                                    | 25.8 ms: 1.03x slower                                         |
| regex_dna      | 221 ms                                                     | 233 ms: 1.05x slower                                          |
| regex_compile  | 137 ms                                                     | 147 ms: 1.07x slower                                          |
| Geometric mean | (ref)                                                      | 1.05x slower                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------------|:----------------------------------------------------------:|:-------------------------------------------------------------:|
| json_dumps           | 10.7 ms                                                    | 10.4 ms: 1.03x faster                                         |
| pickle_list          | 5.11 us                                                    | 4.96 us: 1.03x faster                                         |
| tomli_loads          | 2.12 sec                                                   | 2.07 sec: 1.03x faster                                        |
| xml_etree_process    | 61.2 ms                                                    | 59.6 ms: 1.03x faster                                         |
| pickle_dict          | 34.8 us                                                    | 33.9 us: 1.03x faster                                         |
| json_loads           | 28.9 us                                                    | 28.6 us: 1.01x faster                                         |
| xml_etree_generate   | 87.4 ms                                                    | 86.5 ms: 1.01x faster                                         |
| unpickle_list        | 5.34 us                                                    | 5.29 us: 1.01x faster                                         |
| xml_etree_iterparse  | 107 ms                                                     | 107 ms: 1.01x faster                                          |
| pickle               | 11.5 us                                                    | 11.7 us: 1.02x slower                                         |
| unpickle             | 15.1 us                                                    | 16.2 us: 1.07x slower                                         |
| unpickle_pure_python | 218 us                                                     | 239 us: 1.10x slower                                          |
| Geometric mean       | (ref)                                                      | 1.00x slower                                                  |

Benchmark hidden because not significant (2): xml_etree_parse, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|------------------------|:----------------------------------------------------------:|:-------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 11.1 ms: 1.03x slower                                         |
| python_startup_no_site | 7.11 ms                                                    | 9.52 ms: 1.34x slower                                         |
| Geometric mean         | (ref)                                                      | 1.18x slower                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------|:----------------------------------------------------------:|:-------------------------------------------------------------:|
| mako           | 11.2 ms                                                    | 10.8 ms: 1.04x faster                                         |
| genshi_text    | 23.7 ms                                                    | 24.8 ms: 1.05x slower                                         |
| genshi_xml     | 51.6 ms                                                    | 55.4 ms: 1.07x slower                                         |
| Geometric mean | (ref)                                                      | 1.03x slower                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------------------|:----------------------------------------------------------:|:-------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 114 us: 1.44x faster                                          |
| scimark_fft                | 392 ms                                                     | 343 ms: 1.14x faster                                          |
| richards                   | 50.9 ms                                                    | 46.3 ms: 1.10x faster                                         |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 4.84 ms: 1.09x faster                                         |
| richards_super             | 57.4 ms                                                    | 52.7 ms: 1.09x faster                                         |
| pylint                     | 317 ms                                                     | 297 ms: 1.07x faster                                          |
| async_tree_none            | 378 ms                                                     | 355 ms: 1.07x faster                                          |
| chameleon                  | 7.22 ms                                                    | 6.86 ms: 1.05x faster                                         |
| gc_traversal               | 3.98 ms                                                    | 3.80 ms: 1.05x faster                                         |
| mako                       | 11.2 ms                                                    | 10.8 ms: 1.04x faster                                         |
| sqlite_synth               | 2.99 us                                                    | 2.88 us: 1.04x faster                                         |
| create_gc_cycles           | 1.82 ms                                                    | 1.75 ms: 1.04x faster                                         |
| json_dumps                 | 10.7 ms                                                    | 10.4 ms: 1.03x faster                                         |
| pickle_list                | 5.11 us                                                    | 4.96 us: 1.03x faster                                         |
| tomli_loads                | 2.12 sec                                                   | 2.07 sec: 1.03x faster                                        |
| crypto_pyaes               | 77.5 ms                                                    | 75.5 ms: 1.03x faster                                         |
| xml_etree_process          | 61.2 ms                                                    | 59.6 ms: 1.03x faster                                         |
| deepcopy                   | 367 us                                                     | 358 us: 1.03x faster                                          |
| pickle_dict                | 34.8 us                                                    | 33.9 us: 1.03x faster                                         |
| float                      | 78.9 ms                                                    | 76.9 ms: 1.03x faster                                         |
| pprint_pformat             | 1.56 sec                                                   | 1.52 sec: 1.03x faster                                        |
| deepcopy_memo              | 39.7 us                                                    | 38.8 us: 1.02x faster                                         |
| deepcopy_reduce            | 3.35 us                                                    | 3.27 us: 1.02x faster                                         |
| logging_silent             | 105 ns                                                     | 103 ns: 1.02x faster                                          |
| coroutines                 | 23.2 ms                                                    | 22.7 ms: 1.02x faster                                         |
| pyflate                    | 484 ms                                                     | 476 ms: 1.02x faster                                          |
| pprint_safe_repr           | 758 ms                                                     | 748 ms: 1.01x faster                                          |
| json_loads                 | 28.9 us                                                    | 28.6 us: 1.01x faster                                         |
| xml_etree_generate         | 87.4 ms                                                    | 86.5 ms: 1.01x faster                                         |
| unpickle_list              | 5.34 us                                                    | 5.29 us: 1.01x faster                                         |
| xml_etree_iterparse        | 107 ms                                                     | 107 ms: 1.01x faster                                          |
| spectral_norm              | 116 ms                                                     | 115 ms: 1.01x faster                                          |
| scimark_monte_carlo        | 69.2 ms                                                    | 68.8 ms: 1.01x faster                                         |
| generators                 | 29.6 ms                                                    | 29.5 ms: 1.00x faster                                         |
| html5lib                   | 67.2 ms                                                    | 67.7 ms: 1.01x slower                                         |
| bench_mp_pool              | 23.9 ms                                                    | 24.1 ms: 1.01x slower                                         |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.86 sec: 1.01x slower                                        |
| chaos                      | 61.3 ms                                                    | 61.8 ms: 1.01x slower                                         |
| telco                      | 8.41 ms                                                    | 8.49 ms: 1.01x slower                                         |
| json                       | 5.31 ms                                                    | 5.36 ms: 1.01x slower                                         |
| 2to3                       | 274 ms                                                     | 277 ms: 1.01x slower                                          |
| dask                       | 369 ms                                                     | 374 ms: 1.01x slower                                          |
| asyncio_tcp                | 508 ms                                                     | 515 ms: 1.01x slower                                          |
| mdp                        | 2.79 sec                                                   | 2.83 sec: 1.01x slower                                        |
| tornado_http               | 94.6 ms                                                    | 96.1 ms: 1.02x slower                                         |
| meteor_contest             | 110 ms                                                     | 112 ms: 1.02x slower                                          |
| pickle                     | 11.5 us                                                    | 11.7 us: 1.02x slower                                         |
| gunicorn                   | 1.28 ms                                                    | 1.31 ms: 1.02x slower                                         |
| logging_format             | 6.47 us                                                    | 6.62 us: 1.02x slower                                         |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 602 ms: 1.02x slower                                          |
| sqlglot_normalize          | 110 ms                                                     | 113 ms: 1.02x slower                                          |
| aiohttp                    | 1.18 ms                                                    | 1.21 ms: 1.03x slower                                         |
| regex_effbot               | 3.67 ms                                                    | 3.78 ms: 1.03x slower                                         |
| regex_v8                   | 25.1 ms                                                    | 25.8 ms: 1.03x slower                                         |
| bench_thread_pool          | 834 us                                                     | 858 us: 1.03x slower                                          |
| python_startup             | 10.8 ms                                                    | 11.1 ms: 1.03x slower                                         |
| nbody                      | 88.3 ms                                                    | 91.1 ms: 1.03x slower                                         |
| docutils                   | 2.83 sec                                                   | 2.92 sec: 1.03x slower                                        |
| sqlglot_optimize           | 55.5 ms                                                    | 57.7 ms: 1.04x slower                                         |
| sympy_expand               | 473 ms                                                     | 493 ms: 1.04x slower                                          |
| async_generators           | 442 ms                                                     | 461 ms: 1.04x slower                                          |
| logging_simple             | 5.74 us                                                    | 5.99 us: 1.04x slower                                         |
| sympy_str                  | 282 ms                                                     | 295 ms: 1.04x slower                                          |
| pycparser                  | 1.16 sec                                                   | 1.21 sec: 1.05x slower                                        |
| raytrace                   | 267 ms                                                     | 279 ms: 1.05x slower                                          |
| genshi_text                | 23.7 ms                                                    | 24.8 ms: 1.05x slower                                         |
| regex_dna                  | 221 ms                                                     | 233 ms: 1.05x slower                                          |
| dulwich_log                | 67.2 ms                                                    | 70.9 ms: 1.06x slower                                         |
| deltablue                  | 3.25 ms                                                    | 3.45 ms: 1.06x slower                                         |
| mypy2                      | 742 ms                                                     | 788 ms: 1.06x slower                                          |
| scimark_sor                | 127 ms                                                     | 136 ms: 1.06x slower                                          |
| sympy_integrate            | 20.5 ms                                                    | 21.9 ms: 1.07x slower                                         |
| go                         | 145 ms                                                     | 154 ms: 1.07x slower                                          |
| sympy_sum                  | 156 ms                                                     | 167 ms: 1.07x slower                                          |
| genshi_xml                 | 51.6 ms                                                    | 55.4 ms: 1.07x slower                                         |
| unpickle                   | 15.1 us                                                    | 16.2 us: 1.07x slower                                         |
| coverage                   | 93.1 ms                                                    | 100 ms: 1.07x slower                                          |
| regex_compile              | 137 ms                                                     | 147 ms: 1.07x slower                                          |
| pidigits                   | 191 ms                                                     | 207 ms: 1.08x slower                                          |
| comprehensions             | 16.6 us                                                    | 18.1 us: 1.09x slower                                         |
| pathlib                    | 17.3 ms                                                    | 18.9 ms: 1.09x slower                                         |
| scimark_lu                 | 122 ms                                                     | 133 ms: 1.10x slower                                          |
| unpickle_pure_python       | 218 us                                                     | 239 us: 1.10x slower                                          |
| hexiom                     | 6.30 ms                                                    | 7.10 ms: 1.13x slower                                         |
| nqueens                    | 81.4 ms                                                    | 92.2 ms: 1.13x slower                                         |
| python_startup_no_site     | 7.11 ms                                                    | 9.52 ms: 1.34x slower                                         |
| Geometric mean             | (ref)                                                      | 1.01x slower                                                  |

Benchmark hidden because not significant (13): async_tree_memoization, async_tree_io, async_tree_memoization_tg, async_tree_none_tg, sqlglot_transpile, fannkuch, xml_etree_parse, asyncio_websockets, thrift, async_tree_cpu_io_mixed, async_tree_io_tg, sqlglot_parse, pickle_pure_python
Ignored benchmarks (4) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, django_template, djangocms, flaskblogging

# HPT report

- Reliability score: 99.87% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.06x