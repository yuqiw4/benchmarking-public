# Results vs. 3.13.0b2

- fork: mdboom
- ref: tier2_func_simple_fr
- machine: linux-x86_64
- commit hash: c181b59
- commit date: 2024-04-10
- overall geometric mean: 1.01x slower
- HPT reliability: 99.97%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.06x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 279 ms: 1.02x slower                                                   |
| chameleon      | 7.22 ms                                                    | 7.06 ms: 1.02x faster                                                  |
| docutils       | 2.83 sec                                                   | 2.92 sec: 1.03x slower                                                 |
| html5lib       | 67.2 ms                                                    | 68.0 ms: 1.01x slower                                                  |
| tornado_http   | 94.6 ms                                                    | 96.9 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                      | 1.01x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 353 ms: 1.07x faster                                                   |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 606 ms: 1.03x slower                                                   |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                           |

Benchmark hidden because not significant (6): async_tree_io, async_tree_memoization, async_tree_memoization_tg, async_tree_none_tg, async_tree_io_tg, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 78.9 ms                                                    | 78.0 ms: 1.01x faster                                                  |
| pidigits       | 191 ms                                                     | 189 ms: 1.01x faster                                                   |
| nbody          | 88.3 ms                                                    | 91.4 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                      | 1.00x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.67 ms                                                    | 3.59 ms: 1.02x faster                                                  |
| regex_dna      | 221 ms                                                     | 221 ms: 1.00x faster                                                   |
| regex_compile  | 137 ms                                                     | 144 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                      | 1.01x slower                                                           |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| unpickle_list        | 5.34 us                                                    | 5.15 us: 1.04x faster                                                  |
| json_dumps           | 10.7 ms                                                    | 10.4 ms: 1.04x faster                                                  |
| tomli_loads          | 2.12 sec                                                   | 2.07 sec: 1.02x faster                                                 |
| pickle_list          | 5.11 us                                                    | 5.01 us: 1.02x faster                                                  |
| json_loads           | 28.9 us                                                    | 28.4 us: 1.02x faster                                                  |
| unpickle             | 15.1 us                                                    | 14.9 us: 1.01x faster                                                  |
| xml_etree_process    | 61.2 ms                                                    | 61.5 ms: 1.01x slower                                                  |
| pickle_pure_python   | 305 us                                                     | 307 us: 1.01x slower                                                   |
| pickle_dict          | 34.8 us                                                    | 35.1 us: 1.01x slower                                                  |
| xml_etree_generate   | 87.4 ms                                                    | 88.7 ms: 1.02x slower                                                  |
| pickle               | 11.5 us                                                    | 11.9 us: 1.04x slower                                                  |
| unpickle_pure_python | 218 us                                                     | 242 us: 1.11x slower                                                   |
| Geometric mean       | (ref)                                                      | 1.00x slower                                                           |

Benchmark hidden because not significant (2): xml_etree_parse, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 11.0 ms: 1.03x slower                                                  |
| python_startup_no_site | 7.11 ms                                                    | 9.50 ms: 1.34x slower                                                  |
| Geometric mean         | (ref)                                                      | 1.17x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako           | 11.2 ms                                                    | 10.7 ms: 1.05x faster                                                  |
| genshi_text    | 23.7 ms                                                    | 24.2 ms: 1.02x slower                                                  |
| genshi_xml     | 51.6 ms                                                    | 53.5 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                      | 1.00x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 113 us: 1.45x faster                                                   |
| richards                   | 50.9 ms                                                    | 44.0 ms: 1.16x faster                                                  |
| scimark_fft                | 392 ms                                                     | 342 ms: 1.15x faster                                                   |
| richards_super             | 57.4 ms                                                    | 50.1 ms: 1.15x faster                                                  |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 4.91 ms: 1.07x faster                                                  |
| async_tree_none            | 378 ms                                                     | 353 ms: 1.07x faster                                                   |
| pylint                     | 317 ms                                                     | 296 ms: 1.07x faster                                                   |
| mako                       | 11.2 ms                                                    | 10.7 ms: 1.05x faster                                                  |
| pyflate                    | 484 ms                                                     | 464 ms: 1.04x faster                                                   |
| deepcopy_reduce            | 3.35 us                                                    | 3.21 us: 1.04x faster                                                  |
| sqlite_synth               | 2.99 us                                                    | 2.87 us: 1.04x faster                                                  |
| unpickle_list              | 5.34 us                                                    | 5.15 us: 1.04x faster                                                  |
| json_dumps                 | 10.7 ms                                                    | 10.4 ms: 1.04x faster                                                  |
| deepcopy_memo              | 39.7 us                                                    | 38.4 us: 1.03x faster                                                  |
| create_gc_cycles           | 1.82 ms                                                    | 1.76 ms: 1.03x faster                                                  |
| logging_silent             | 105 ns                                                     | 102 ns: 1.03x faster                                                   |
| crypto_pyaes               | 77.5 ms                                                    | 75.6 ms: 1.02x faster                                                  |
| tomli_loads                | 2.12 sec                                                   | 2.07 sec: 1.02x faster                                                 |
| regex_effbot               | 3.67 ms                                                    | 3.59 ms: 1.02x faster                                                  |
| chameleon                  | 7.22 ms                                                    | 7.06 ms: 1.02x faster                                                  |
| pickle_list                | 5.11 us                                                    | 5.01 us: 1.02x faster                                                  |
| json_loads                 | 28.9 us                                                    | 28.4 us: 1.02x faster                                                  |
| coroutines                 | 23.2 ms                                                    | 22.8 ms: 1.02x faster                                                  |
| unpickle                   | 15.1 us                                                    | 14.9 us: 1.01x faster                                                  |
| deepcopy                   | 367 us                                                     | 363 us: 1.01x faster                                                   |
| logging_format             | 6.47 us                                                    | 6.40 us: 1.01x faster                                                  |
| float                      | 78.9 ms                                                    | 78.0 ms: 1.01x faster                                                  |
| pidigits                   | 191 ms                                                     | 189 ms: 1.01x faster                                                   |
| thrift                     | 823 us                                                     | 817 us: 1.01x faster                                                   |
| gc_traversal               | 3.98 ms                                                    | 3.96 ms: 1.00x faster                                                  |
| spectral_norm              | 116 ms                                                     | 116 ms: 1.00x faster                                                   |
| regex_dna                  | 221 ms                                                     | 221 ms: 1.00x faster                                                   |
| pprint_pformat             | 1.56 sec                                                   | 1.56 sec: 1.00x slower                                                 |
| xml_etree_process          | 61.2 ms                                                    | 61.5 ms: 1.01x slower                                                  |
| pickle_pure_python         | 305 us                                                     | 307 us: 1.01x slower                                                   |
| sqlglot_transpile          | 1.63 ms                                                    | 1.64 ms: 1.01x slower                                                  |
| asyncio_tcp                | 508 ms                                                     | 512 ms: 1.01x slower                                                   |
| pickle_dict                | 34.8 us                                                    | 35.1 us: 1.01x slower                                                  |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.86 sec: 1.01x slower                                                 |
| logging_simple             | 5.74 us                                                    | 5.80 us: 1.01x slower                                                  |
| html5lib                   | 67.2 ms                                                    | 68.0 ms: 1.01x slower                                                  |
| mdp                        | 2.79 sec                                                   | 2.82 sec: 1.01x slower                                                 |
| xml_etree_generate         | 87.4 ms                                                    | 88.7 ms: 1.02x slower                                                  |
| dask                       | 369 ms                                                     | 375 ms: 1.02x slower                                                   |
| 2to3                       | 274 ms                                                     | 279 ms: 1.02x slower                                                   |
| gunicorn                   | 1.28 ms                                                    | 1.30 ms: 1.02x slower                                                  |
| chaos                      | 61.3 ms                                                    | 62.6 ms: 1.02x slower                                                  |
| generators                 | 29.6 ms                                                    | 30.2 ms: 1.02x slower                                                  |
| pprint_safe_repr           | 758 ms                                                     | 775 ms: 1.02x slower                                                   |
| genshi_text                | 23.7 ms                                                    | 24.2 ms: 1.02x slower                                                  |
| tornado_http               | 94.6 ms                                                    | 96.9 ms: 1.02x slower                                                  |
| pycparser                  | 1.16 sec                                                   | 1.19 sec: 1.02x slower                                                 |
| python_startup             | 10.8 ms                                                    | 11.0 ms: 1.03x slower                                                  |
| aiohttp                    | 1.18 ms                                                    | 1.21 ms: 1.03x slower                                                  |
| bench_thread_pool          | 834 us                                                     | 858 us: 1.03x slower                                                   |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 606 ms: 1.03x slower                                                   |
| docutils                   | 2.83 sec                                                   | 2.92 sec: 1.03x slower                                                 |
| nbody                      | 88.3 ms                                                    | 91.4 ms: 1.03x slower                                                  |
| genshi_xml                 | 51.6 ms                                                    | 53.5 ms: 1.04x slower                                                  |
| pickle                     | 11.5 us                                                    | 11.9 us: 1.04x slower                                                  |
| raytrace                   | 267 ms                                                     | 278 ms: 1.04x slower                                                   |
| telco                      | 8.41 ms                                                    | 8.79 ms: 1.04x slower                                                  |
| async_generators           | 442 ms                                                     | 462 ms: 1.05x slower                                                   |
| sqlglot_normalize          | 110 ms                                                     | 115 ms: 1.05x slower                                                   |
| sqlglot_optimize           | 55.5 ms                                                    | 58.2 ms: 1.05x slower                                                  |
| scimark_sor                | 127 ms                                                     | 134 ms: 1.05x slower                                                   |
| dulwich_log                | 67.2 ms                                                    | 70.6 ms: 1.05x slower                                                  |
| sympy_expand               | 473 ms                                                     | 497 ms: 1.05x slower                                                   |
| sympy_str                  | 282 ms                                                     | 297 ms: 1.05x slower                                                   |
| regex_compile              | 137 ms                                                     | 144 ms: 1.05x slower                                                   |
| coverage                   | 93.1 ms                                                    | 99.0 ms: 1.06x slower                                                  |
| mypy2                      | 742 ms                                                     | 789 ms: 1.06x slower                                                   |
| go                         | 145 ms                                                     | 155 ms: 1.07x slower                                                   |
| comprehensions             | 16.6 us                                                    | 17.9 us: 1.08x slower                                                  |
| sympy_integrate            | 20.5 ms                                                    | 22.1 ms: 1.08x slower                                                  |
| sympy_sum                  | 156 ms                                                     | 168 ms: 1.08x slower                                                   |
| scimark_lu                 | 122 ms                                                     | 134 ms: 1.10x slower                                                   |
| unpickle_pure_python       | 218 us                                                     | 242 us: 1.11x slower                                                   |
| pathlib                    | 17.3 ms                                                    | 19.3 ms: 1.11x slower                                                  |
| nqueens                    | 81.4 ms                                                    | 90.9 ms: 1.12x slower                                                  |
| hexiom                     | 6.30 ms                                                    | 7.04 ms: 1.12x slower                                                  |
| deltablue                  | 3.25 ms                                                    | 3.69 ms: 1.14x slower                                                  |
| python_startup_no_site     | 7.11 ms                                                    | 9.50 ms: 1.34x slower                                                  |
| Geometric mean             | (ref)                                                      | 1.01x slower                                                           |

Benchmark hidden because not significant (16): async_tree_io, async_tree_memoization, xml_etree_parse, async_tree_memoization_tg, fannkuch, json, xml_etree_iterparse, regex_v8, scimark_monte_carlo, async_tree_none_tg, async_tree_io_tg, asyncio_websockets, meteor_contest, async_tree_cpu_io_mixed, bench_mp_pool, sqlglot_parse
Ignored benchmarks (4) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, django_template, djangocms, flaskblogging

# HPT report

- Reliability score: 99.97% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.06x