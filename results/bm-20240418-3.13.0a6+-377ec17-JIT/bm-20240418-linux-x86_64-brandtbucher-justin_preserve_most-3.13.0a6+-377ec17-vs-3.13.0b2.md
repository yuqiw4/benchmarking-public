# Results vs. 3.13.0b2

- fork: brandtbucher
- ref: justin_preserve_most
- machine: linux-x86_64
- commit hash: 377ec17
- commit date: 2024-04-18
- overall geometric mean: 1.00x slower
- HPT reliability: 99.17%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.06x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6+-377ec17 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 276 ms: 1.01x slower                                                         |
| chameleon      | 7.22 ms                                                    | 6.92 ms: 1.04x faster                                                        |
| docutils       | 2.83 sec                                                   | 2.90 sec: 1.02x slower                                                       |
| tornado_http   | 94.6 ms                                                    | 96.0 ms: 1.01x slower                                                        |
| Geometric mean | (ref)                                                      | 1.00x slower                                                                 |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6+-377ec17 |
|----------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 354 ms: 1.07x faster                                                         |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 605 ms: 1.03x slower                                                         |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                                 |

Benchmark hidden because not significant (6): async_tree_io, async_tree_memoization_tg, async_tree_cpu_io_mixed, async_tree_none_tg, async_tree_memoization, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6+-377ec17 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 78.9 ms                                                    | 76.6 ms: 1.03x faster                                                        |
| pidigits       | 191 ms                                                     | 190 ms: 1.01x faster                                                         |
| nbody          | 88.3 ms                                                    | 95.1 ms: 1.08x slower                                                        |
| Geometric mean | (ref)                                                      | 1.01x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6+-377ec17 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_v8       | 25.1 ms                                                    | 25.3 ms: 1.01x slower                                                        |
| regex_effbot   | 3.67 ms                                                    | 3.78 ms: 1.03x slower                                                        |
| regex_dna      | 221 ms                                                     | 228 ms: 1.03x slower                                                         |
| regex_compile  | 137 ms                                                     | 142 ms: 1.04x slower                                                         |
| Geometric mean | (ref)                                                      | 1.03x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6+-377ec17 |
|----------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| unpickle_list        | 5.34 us                                                    | 5.00 us: 1.07x faster                                                        |
| tomli_loads          | 2.12 sec                                                   | 1.99 sec: 1.07x faster                                                       |
| json_loads           | 28.9 us                                                    | 27.8 us: 1.04x faster                                                        |
| xml_etree_process    | 61.2 ms                                                    | 60.0 ms: 1.02x faster                                                        |
| json_dumps           | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                                        |
| pickle_pure_python   | 305 us                                                     | 304 us: 1.01x faster                                                         |
| xml_etree_generate   | 87.4 ms                                                    | 87.2 ms: 1.00x faster                                                        |
| pickle_list          | 5.11 us                                                    | 5.15 us: 1.01x slower                                                        |
| pickle               | 11.5 us                                                    | 11.7 us: 1.02x slower                                                        |
| pickle_dict          | 34.8 us                                                    | 35.7 us: 1.03x slower                                                        |
| unpickle_pure_python | 218 us                                                     | 231 us: 1.06x slower                                                         |
| Geometric mean       | (ref)                                                      | 1.01x faster                                                                 |

Benchmark hidden because not significant (3): xml_etree_parse, xml_etree_iterparse, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6+-377ec17 |
|------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.9 ms: 1.02x slower                                                        |
| python_startup_no_site | 7.11 ms                                                    | 7.55 ms: 1.06x slower                                                        |
| Geometric mean         | (ref)                                                      | 1.04x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6+-377ec17 |
|-----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 10.6 ms: 1.06x faster                                                        |
| genshi_text     | 23.7 ms                                                    | 24.0 ms: 1.02x slower                                                        |
| django_template | 34.8 ms                                                    | 35.9 ms: 1.03x slower                                                        |
| genshi_xml      | 51.6 ms                                                    | 53.9 ms: 1.04x slower                                                        |
| Geometric mean  | (ref)                                                      | 1.01x slower                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6+-377ec17 |
|----------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 114 us: 1.45x faster                                                         |
| richards                   | 50.9 ms                                                    | 42.1 ms: 1.21x faster                                                        |
| richards_super             | 57.4 ms                                                    | 48.4 ms: 1.18x faster                                                        |
| scimark_fft                | 392 ms                                                     | 353 ms: 1.11x faster                                                         |
| async_tree_none            | 378 ms                                                     | 354 ms: 1.07x faster                                                         |
| unpickle_list              | 5.34 us                                                    | 5.00 us: 1.07x faster                                                        |
| tomli_loads                | 2.12 sec                                                   | 1.99 sec: 1.07x faster                                                       |
| deepcopy_reduce            | 3.35 us                                                    | 3.14 us: 1.07x faster                                                        |
| mdp                        | 2.79 sec                                                   | 2.62 sec: 1.06x faster                                                       |
| mako                       | 11.2 ms                                                    | 10.6 ms: 1.06x faster                                                        |
| pyflate                    | 484 ms                                                     | 463 ms: 1.05x faster                                                         |
| crypto_pyaes               | 77.5 ms                                                    | 74.1 ms: 1.04x faster                                                        |
| chameleon                  | 7.22 ms                                                    | 6.92 ms: 1.04x faster                                                        |
| json_loads                 | 28.9 us                                                    | 27.8 us: 1.04x faster                                                        |
| deepcopy_memo              | 39.7 us                                                    | 38.3 us: 1.04x faster                                                        |
| create_gc_cycles           | 1.82 ms                                                    | 1.76 ms: 1.03x faster                                                        |
| json                       | 5.31 ms                                                    | 5.15 ms: 1.03x faster                                                        |
| deepcopy                   | 367 us                                                     | 356 us: 1.03x faster                                                         |
| logging_silent             | 105 ns                                                     | 102 ns: 1.03x faster                                                         |
| float                      | 78.9 ms                                                    | 76.6 ms: 1.03x faster                                                        |
| sqlite_synth               | 2.99 us                                                    | 2.91 us: 1.03x faster                                                        |
| fannkuch                   | 402 ms                                                     | 392 ms: 1.02x faster                                                         |
| gc_traversal               | 3.98 ms                                                    | 3.89 ms: 1.02x faster                                                        |
| scimark_monte_carlo        | 69.2 ms                                                    | 67.8 ms: 1.02x faster                                                        |
| xml_etree_process          | 61.2 ms                                                    | 60.0 ms: 1.02x faster                                                        |
| coroutines                 | 23.2 ms                                                    | 22.8 ms: 1.02x faster                                                        |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 5.19 ms: 1.02x faster                                                        |
| logging_format             | 6.47 us                                                    | 6.38 us: 1.01x faster                                                        |
| pprint_safe_repr           | 758 ms                                                     | 748 ms: 1.01x faster                                                         |
| json_dumps                 | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                                        |
| pidigits                   | 191 ms                                                     | 190 ms: 1.01x faster                                                         |
| pickle_pure_python         | 305 us                                                     | 304 us: 1.01x faster                                                         |
| xml_etree_generate         | 87.4 ms                                                    | 87.2 ms: 1.00x faster                                                        |
| asyncio_tcp                | 508 ms                                                     | 510 ms: 1.00x slower                                                         |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.85 sec: 1.00x slower                                                       |
| 2to3                       | 274 ms                                                     | 276 ms: 1.01x slower                                                         |
| raytrace                   | 267 ms                                                     | 269 ms: 1.01x slower                                                         |
| pickle_list                | 5.11 us                                                    | 5.15 us: 1.01x slower                                                        |
| regex_v8                   | 25.1 ms                                                    | 25.3 ms: 1.01x slower                                                        |
| logging_simple             | 5.74 us                                                    | 5.81 us: 1.01x slower                                                        |
| generators                 | 29.6 ms                                                    | 30.0 ms: 1.01x slower                                                        |
| tornado_http               | 94.6 ms                                                    | 96.0 ms: 1.01x slower                                                        |
| genshi_text                | 23.7 ms                                                    | 24.0 ms: 1.02x slower                                                        |
| chaos                      | 61.3 ms                                                    | 62.3 ms: 1.02x slower                                                        |
| dask                       | 369 ms                                                     | 375 ms: 1.02x slower                                                         |
| python_startup             | 10.8 ms                                                    | 10.9 ms: 1.02x slower                                                        |
| gunicorn                   | 1.28 ms                                                    | 1.30 ms: 1.02x slower                                                        |
| meteor_contest             | 110 ms                                                     | 112 ms: 1.02x slower                                                         |
| pickle                     | 11.5 us                                                    | 11.7 us: 1.02x slower                                                        |
| aiohttp                    | 1.18 ms                                                    | 1.20 ms: 1.02x slower                                                        |
| spectral_norm              | 116 ms                                                     | 119 ms: 1.02x slower                                                         |
| docutils                   | 2.83 sec                                                   | 2.90 sec: 1.02x slower                                                       |
| bench_thread_pool          | 834 us                                                     | 855 us: 1.02x slower                                                         |
| telco                      | 8.41 ms                                                    | 8.64 ms: 1.03x slower                                                        |
| pickle_dict                | 34.8 us                                                    | 35.7 us: 1.03x slower                                                        |
| djangocms                  | 31.5 us                                                    | 32.4 us: 1.03x slower                                                        |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 605 ms: 1.03x slower                                                         |
| regex_effbot               | 3.67 ms                                                    | 3.78 ms: 1.03x slower                                                        |
| pathlib                    | 17.3 ms                                                    | 17.9 ms: 1.03x slower                                                        |
| dulwich_log                | 67.2 ms                                                    | 69.3 ms: 1.03x slower                                                        |
| django_template            | 34.8 ms                                                    | 35.9 ms: 1.03x slower                                                        |
| regex_dna                  | 221 ms                                                     | 228 ms: 1.03x slower                                                         |
| sqlglot_normalize          | 110 ms                                                     | 114 ms: 1.03x slower                                                         |
| sqlglot_optimize           | 55.5 ms                                                    | 57.6 ms: 1.04x slower                                                        |
| regex_compile              | 137 ms                                                     | 142 ms: 1.04x slower                                                         |
| scimark_sor                | 127 ms                                                     | 133 ms: 1.04x slower                                                         |
| pycparser                  | 1.16 sec                                                   | 1.21 sec: 1.04x slower                                                       |
| genshi_xml                 | 51.6 ms                                                    | 53.9 ms: 1.04x slower                                                        |
| async_generators           | 442 ms                                                     | 462 ms: 1.05x slower                                                         |
| comprehensions             | 16.6 us                                                    | 17.4 us: 1.05x slower                                                        |
| sympy_str                  | 282 ms                                                     | 297 ms: 1.05x slower                                                         |
| mypy2                      | 742 ms                                                     | 781 ms: 1.05x slower                                                         |
| sympy_expand               | 473 ms                                                     | 498 ms: 1.05x slower                                                         |
| coverage                   | 93.1 ms                                                    | 98.4 ms: 1.06x slower                                                        |
| unpickle_pure_python       | 218 us                                                     | 231 us: 1.06x slower                                                         |
| go                         | 145 ms                                                     | 153 ms: 1.06x slower                                                         |
| python_startup_no_site     | 7.11 ms                                                    | 7.55 ms: 1.06x slower                                                        |
| sympy_integrate            | 20.5 ms                                                    | 21.9 ms: 1.07x slower                                                        |
| scimark_lu                 | 122 ms                                                     | 131 ms: 1.08x slower                                                         |
| nbody                      | 88.3 ms                                                    | 95.1 ms: 1.08x slower                                                        |
| sympy_sum                  | 156 ms                                                     | 168 ms: 1.08x slower                                                         |
| hexiom                     | 6.30 ms                                                    | 6.86 ms: 1.09x slower                                                        |
| nqueens                    | 81.4 ms                                                    | 89.6 ms: 1.10x slower                                                        |
| deltablue                  | 3.25 ms                                                    | 3.62 ms: 1.11x slower                                                        |
| Geometric mean             | (ref)                                                      | 1.00x slower                                                                 |

Benchmark hidden because not significant (17): async_tree_io, xml_etree_parse, async_tree_memoization_tg, pprint_pformat, async_tree_cpu_io_mixed, async_tree_none_tg, sqlglot_transpile, xml_etree_iterparse, asyncio_websockets, html5lib, sqlglot_parse, bench_mp_pool, unpickle, async_tree_memoization, thrift, async_tree_io_tg, pylint
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 99.17% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.06x