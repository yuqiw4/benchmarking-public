# Results vs. 3.13.0b2

- fork: mdboom
- ref: tier2_func_simple_fr
- machine: linux-x86_64
- commit hash: c5564c1
- commit date: 2024-04-08
- overall geometric mean: 1.01x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.05x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 278 ms: 1.02x slower                                                   |
| chameleon      | 7.22 ms                                                    | 7.12 ms: 1.01x faster                                                  |
| docutils       | 2.83 sec                                                   | 2.94 sec: 1.04x slower                                                 |
| html5lib       | 67.2 ms                                                    | 68.5 ms: 1.02x slower                                                  |
| tornado_http   | 94.6 ms                                                    | 96.7 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                      | 1.02x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 357 ms: 1.06x faster                                                   |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 609 ms: 1.04x slower                                                   |
| Geometric mean             | (ref)                                                      | 1.00x slower                                                           |

Benchmark hidden because not significant (6): async_tree_memoization, async_tree_memoization_tg, async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_io_tg, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 78.9 ms                                                    | 78.4 ms: 1.01x faster                                                  |
| nbody          | 88.3 ms                                                    | 90.9 ms: 1.03x slower                                                  |
| pidigits       | 191 ms                                                     | 211 ms: 1.10x slower                                                   |
| Geometric mean | (ref)                                                      | 1.04x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8       | 25.1 ms                                                    | 26.0 ms: 1.04x slower                                                  |
| regex_effbot   | 3.67 ms                                                    | 3.80 ms: 1.04x slower                                                  |
| regex_dna      | 221 ms                                                     | 230 ms: 1.04x slower                                                   |
| regex_compile  | 137 ms                                                     | 145 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                      | 1.04x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 10.7 ms                                                    | 10.4 ms: 1.03x faster                                                  |
| tomli_loads          | 2.12 sec                                                   | 2.07 sec: 1.03x faster                                                 |
| json_loads           | 28.9 us                                                    | 28.2 us: 1.03x faster                                                  |
| xml_etree_process    | 61.2 ms                                                    | 60.2 ms: 1.02x faster                                                  |
| unpickle             | 15.1 us                                                    | 15.0 us: 1.01x faster                                                  |
| unpickle_list        | 5.34 us                                                    | 5.32 us: 1.00x faster                                                  |
| xml_etree_generate   | 87.4 ms                                                    | 87.7 ms: 1.00x slower                                                  |
| pickle_pure_python   | 305 us                                                     | 309 us: 1.01x slower                                                   |
| pickle_dict          | 34.8 us                                                    | 35.4 us: 1.02x slower                                                  |
| pickle               | 11.5 us                                                    | 11.8 us: 1.03x slower                                                  |
| pickle_list          | 5.11 us                                                    | 5.28 us: 1.03x slower                                                  |
| unpickle_pure_python | 218 us                                                     | 240 us: 1.10x slower                                                   |
| Geometric mean       | (ref)                                                      | 1.00x slower                                                           |

Benchmark hidden because not significant (2): xml_etree_parse, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 11.0 ms: 1.02x slower                                                  |
| python_startup_no_site | 7.11 ms                                                    | 9.51 ms: 1.34x slower                                                  |
| Geometric mean         | (ref)                                                      | 1.17x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako           | 11.2 ms                                                    | 10.8 ms: 1.04x faster                                                  |
| genshi_xml     | 51.6 ms                                                    | 53.7 ms: 1.04x slower                                                  |
| genshi_text    | 23.7 ms                                                    | 25.0 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                      | 1.02x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 113 us: 1.45x faster                                                   |
| richards                   | 50.9 ms                                                    | 44.1 ms: 1.15x faster                                                  |
| richards_super             | 57.4 ms                                                    | 49.8 ms: 1.15x faster                                                  |
| scimark_fft                | 392 ms                                                     | 349 ms: 1.12x faster                                                   |
| pylint                     | 317 ms                                                     | 296 ms: 1.07x faster                                                   |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 4.93 ms: 1.07x faster                                                  |
| async_tree_none            | 378 ms                                                     | 357 ms: 1.06x faster                                                   |
| coroutines                 | 23.2 ms                                                    | 22.1 ms: 1.05x faster                                                  |
| mako                       | 11.2 ms                                                    | 10.8 ms: 1.04x faster                                                  |
| sqlite_synth               | 2.99 us                                                    | 2.89 us: 1.04x faster                                                  |
| create_gc_cycles           | 1.82 ms                                                    | 1.76 ms: 1.03x faster                                                  |
| deepcopy_reduce            | 3.35 us                                                    | 3.25 us: 1.03x faster                                                  |
| json_dumps                 | 10.7 ms                                                    | 10.4 ms: 1.03x faster                                                  |
| deepcopy_memo              | 39.7 us                                                    | 38.5 us: 1.03x faster                                                  |
| pyflate                    | 484 ms                                                     | 471 ms: 1.03x faster                                                   |
| tomli_loads                | 2.12 sec                                                   | 2.07 sec: 1.03x faster                                                 |
| json_loads                 | 28.9 us                                                    | 28.2 us: 1.03x faster                                                  |
| crypto_pyaes               | 77.5 ms                                                    | 75.6 ms: 1.03x faster                                                  |
| gc_traversal               | 3.98 ms                                                    | 3.88 ms: 1.02x faster                                                  |
| xml_etree_process          | 61.2 ms                                                    | 60.2 ms: 1.02x faster                                                  |
| logging_silent             | 105 ns                                                     | 103 ns: 1.02x faster                                                   |
| asyncio_tcp                | 508 ms                                                     | 501 ms: 1.01x faster                                                   |
| deepcopy                   | 367 us                                                     | 362 us: 1.01x faster                                                   |
| chameleon                  | 7.22 ms                                                    | 7.12 ms: 1.01x faster                                                  |
| fannkuch                   | 402 ms                                                     | 397 ms: 1.01x faster                                                   |
| spectral_norm              | 116 ms                                                     | 115 ms: 1.01x faster                                                   |
| unpickle                   | 15.1 us                                                    | 15.0 us: 1.01x faster                                                  |
| float                      | 78.9 ms                                                    | 78.4 ms: 1.01x faster                                                  |
| unpickle_list              | 5.34 us                                                    | 5.32 us: 1.00x faster                                                  |
| xml_etree_generate         | 87.4 ms                                                    | 87.7 ms: 1.00x slower                                                  |
| generators                 | 29.6 ms                                                    | 29.8 ms: 1.00x slower                                                  |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.85 sec: 1.01x slower                                                 |
| sqlglot_parse              | 1.32 ms                                                    | 1.33 ms: 1.01x slower                                                  |
| pickle_pure_python         | 305 us                                                     | 309 us: 1.01x slower                                                   |
| sqlglot_transpile          | 1.63 ms                                                    | 1.65 ms: 1.01x slower                                                  |
| chaos                      | 61.3 ms                                                    | 62.2 ms: 1.01x slower                                                  |
| pprint_pformat             | 1.56 sec                                                   | 1.58 sec: 1.02x slower                                                 |
| 2to3                       | 274 ms                                                     | 278 ms: 1.02x slower                                                   |
| logging_simple             | 5.74 us                                                    | 5.84 us: 1.02x slower                                                  |
| pickle_dict                | 34.8 us                                                    | 35.4 us: 1.02x slower                                                  |
| mdp                        | 2.79 sec                                                   | 2.83 sec: 1.02x slower                                                 |
| dask                       | 369 ms                                                     | 376 ms: 1.02x slower                                                   |
| html5lib                   | 67.2 ms                                                    | 68.5 ms: 1.02x slower                                                  |
| gunicorn                   | 1.28 ms                                                    | 1.30 ms: 1.02x slower                                                  |
| tornado_http               | 94.6 ms                                                    | 96.7 ms: 1.02x slower                                                  |
| python_startup             | 10.8 ms                                                    | 11.0 ms: 1.02x slower                                                  |
| raytrace                   | 267 ms                                                     | 274 ms: 1.03x slower                                                   |
| bench_thread_pool          | 834 us                                                     | 856 us: 1.03x slower                                                   |
| meteor_contest             | 110 ms                                                     | 113 ms: 1.03x slower                                                   |
| aiohttp                    | 1.18 ms                                                    | 1.21 ms: 1.03x slower                                                  |
| nbody                      | 88.3 ms                                                    | 90.9 ms: 1.03x slower                                                  |
| pickle                     | 11.5 us                                                    | 11.8 us: 1.03x slower                                                  |
| telco                      | 8.41 ms                                                    | 8.68 ms: 1.03x slower                                                  |
| sqlglot_normalize          | 110 ms                                                     | 114 ms: 1.03x slower                                                   |
| pickle_list                | 5.11 us                                                    | 5.28 us: 1.03x slower                                                  |
| sqlglot_optimize           | 55.5 ms                                                    | 57.4 ms: 1.03x slower                                                  |
| regex_v8                   | 25.1 ms                                                    | 26.0 ms: 1.04x slower                                                  |
| regex_effbot               | 3.67 ms                                                    | 3.80 ms: 1.04x slower                                                  |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 609 ms: 1.04x slower                                                   |
| docutils                   | 2.83 sec                                                   | 2.94 sec: 1.04x slower                                                 |
| async_generators           | 442 ms                                                     | 459 ms: 1.04x slower                                                   |
| regex_dna                  | 221 ms                                                     | 230 ms: 1.04x slower                                                   |
| genshi_xml                 | 51.6 ms                                                    | 53.7 ms: 1.04x slower                                                  |
| dulwich_log                | 67.2 ms                                                    | 70.2 ms: 1.05x slower                                                  |
| scimark_sor                | 127 ms                                                     | 134 ms: 1.05x slower                                                   |
| sympy_str                  | 282 ms                                                     | 298 ms: 1.05x slower                                                   |
| sympy_expand               | 473 ms                                                     | 498 ms: 1.05x slower                                                   |
| coverage                   | 93.1 ms                                                    | 98.3 ms: 1.06x slower                                                  |
| genshi_text                | 23.7 ms                                                    | 25.0 ms: 1.06x slower                                                  |
| regex_compile              | 137 ms                                                     | 145 ms: 1.06x slower                                                   |
| mypy2                      | 742 ms                                                     | 786 ms: 1.06x slower                                                   |
| pycparser                  | 1.16 sec                                                   | 1.23 sec: 1.06x slower                                                 |
| sympy_sum                  | 156 ms                                                     | 168 ms: 1.08x slower                                                   |
| comprehensions             | 16.6 us                                                    | 17.9 us: 1.08x slower                                                  |
| sympy_integrate            | 20.5 ms                                                    | 22.2 ms: 1.08x slower                                                  |
| go                         | 145 ms                                                     | 157 ms: 1.08x slower                                                   |
| scimark_lu                 | 122 ms                                                     | 134 ms: 1.10x slower                                                   |
| unpickle_pure_python       | 218 us                                                     | 240 us: 1.10x slower                                                   |
| pidigits                   | 191 ms                                                     | 211 ms: 1.10x slower                                                   |
| pathlib                    | 17.3 ms                                                    | 19.1 ms: 1.10x slower                                                  |
| nqueens                    | 81.4 ms                                                    | 90.9 ms: 1.12x slower                                                  |
| hexiom                     | 6.30 ms                                                    | 7.04 ms: 1.12x slower                                                  |
| deltablue                  | 3.25 ms                                                    | 3.68 ms: 1.13x slower                                                  |
| python_startup_no_site     | 7.11 ms                                                    | 9.51 ms: 1.34x slower                                                  |
| Geometric mean             | (ref)                                                      | 1.01x slower                                                           |

Benchmark hidden because not significant (15): xml_etree_parse, scimark_monte_carlo, xml_etree_iterparse, thrift, json, asyncio_websockets, async_tree_memoization, async_tree_memoization_tg, bench_mp_pool, async_tree_none_tg, pprint_safe_repr, logging_format, async_tree_cpu_io_mixed, async_tree_io_tg, async_tree_io
Ignored benchmarks (4) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, django_template, djangocms, flaskblogging

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.05x