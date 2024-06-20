# Results vs. 3.13.0b2

- fork: brandtbucher
- ref: justin_ghccc_cache_4
- machine: linux-x86_64
- commit hash: b309fd7
- commit date: 2024-04-24
- overall geometric mean: 1.03x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240424-linux-x86_64-brandtbucher-justin_ghccc_cache_4-3.13.0a6+-b309fd7 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 290 ms: 1.06x slower                                                         |
| docutils       | 2.83 sec                                                   | 3.00 sec: 1.06x slower                                                       |
| html5lib       | 67.2 ms                                                    | 70.0 ms: 1.04x slower                                                        |
| tornado_http   | 94.6 ms                                                    | 98.0 ms: 1.04x slower                                                        |
| Geometric mean | (ref)                                                      | 1.04x slower                                                                 |

Benchmark hidden because not significant (1): chameleon

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240424-linux-x86_64-brandtbucher-justin_ghccc_cache_4-3.13.0a6+-b309fd7 |
|----------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 367 ms: 1.03x faster                                                         |
| async_tree_none_tg         | 336 ms                                                     | 344 ms: 1.02x slower                                                         |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 612 ms: 1.04x slower                                                         |
| Geometric mean             | (ref)                                                      | 1.01x slower                                                                 |

Benchmark hidden because not significant (5): async_tree_io, async_tree_memoization_tg, async_tree_io_tg, async_tree_cpu_io_mixed, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240424-linux-x86_64-brandtbucher-justin_ghccc_cache_4-3.13.0a6+-b309fd7 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 88.3 ms                                                    | 83.1 ms: 1.06x faster                                                        |
| float          | 78.9 ms                                                    | 75.3 ms: 1.05x faster                                                        |
| pidigits       | 191 ms                                                     | 210 ms: 1.10x slower                                                         |
| Geometric mean | (ref)                                                      | 1.00x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240424-linux-x86_64-brandtbucher-justin_ghccc_cache_4-3.13.0a6+-b309fd7 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_v8       | 25.1 ms                                                    | 24.5 ms: 1.02x faster                                                        |
| regex_dna      | 221 ms                                                     | 225 ms: 1.02x slower                                                         |
| regex_effbot   | 3.67 ms                                                    | 4.23 ms: 1.15x slower                                                        |
| regex_compile  | 137 ms                                                     | 171 ms: 1.25x slower                                                         |
| Geometric mean | (ref)                                                      | 1.09x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240424-linux-x86_64-brandtbucher-justin_ghccc_cache_4-3.13.0a6+-b309fd7 |
|----------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| xml_etree_parse      | 162 ms                                                     | 148 ms: 1.09x faster                                                         |
| json_loads           | 28.9 us                                                    | 27.4 us: 1.06x faster                                                        |
| xml_etree_iterparse  | 107 ms                                                     | 104 ms: 1.04x faster                                                         |
| json_dumps           | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                                        |
| pickle_list          | 5.11 us                                                    | 5.08 us: 1.01x faster                                                        |
| xml_etree_process    | 61.2 ms                                                    | 60.9 ms: 1.01x faster                                                        |
| pickle_dict          | 34.8 us                                                    | 34.9 us: 1.00x slower                                                        |
| unpickle             | 15.1 us                                                    | 15.2 us: 1.00x slower                                                        |
| xml_etree_generate   | 87.4 ms                                                    | 88.1 ms: 1.01x slower                                                        |
| pickle_pure_python   | 305 us                                                     | 309 us: 1.01x slower                                                         |
| tomli_loads          | 2.12 sec                                                   | 2.15 sec: 1.01x slower                                                       |
| pickle               | 11.5 us                                                    | 12.0 us: 1.05x slower                                                        |
| unpickle_pure_python | 218 us                                                     | 240 us: 1.10x slower                                                         |
| Geometric mean       | (ref)                                                      | 1.00x faster                                                                 |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240424-linux-x86_64-brandtbucher-justin_ghccc_cache_4-3.13.0a6+-b309fd7 |
|------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 11.1 ms: 1.03x slower                                                        |
| python_startup_no_site | 7.11 ms                                                    | 7.71 ms: 1.08x slower                                                        |
| Geometric mean         | (ref)                                                      | 1.06x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240424-linux-x86_64-brandtbucher-justin_ghccc_cache_4-3.13.0a6+-b309fd7 |
|-----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 10.7 ms: 1.05x faster                                                        |
| genshi_text     | 23.7 ms                                                    | 25.2 ms: 1.06x slower                                                        |
| django_template | 34.8 ms                                                    | 37.5 ms: 1.08x slower                                                        |
| genshi_xml      | 51.6 ms                                                    | 61.1 ms: 1.18x slower                                                        |
| Geometric mean  | (ref)                                                      | 1.07x slower                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240424-linux-x86_64-brandtbucher-justin_ghccc_cache_4-3.13.0a6+-b309fd7 |
|----------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 116 us: 1.42x faster                                                         |
| scimark_fft                | 392 ms                                                     | 333 ms: 1.18x faster                                                         |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 4.55 ms: 1.16x faster                                                        |
| xml_etree_parse            | 162 ms                                                     | 148 ms: 1.09x faster                                                         |
| spectral_norm              | 116 ms                                                     | 108 ms: 1.07x faster                                                         |
| richards                   | 50.9 ms                                                    | 47.7 ms: 1.07x faster                                                        |
| nbody                      | 88.3 ms                                                    | 83.1 ms: 1.06x faster                                                        |
| richards_super             | 57.4 ms                                                    | 54.3 ms: 1.06x faster                                                        |
| json_loads                 | 28.9 us                                                    | 27.4 us: 1.06x faster                                                        |
| mako                       | 11.2 ms                                                    | 10.7 ms: 1.05x faster                                                        |
| crypto_pyaes               | 77.5 ms                                                    | 73.7 ms: 1.05x faster                                                        |
| float                      | 78.9 ms                                                    | 75.3 ms: 1.05x faster                                                        |
| mdp                        | 2.79 sec                                                   | 2.68 sec: 1.04x faster                                                       |
| xml_etree_iterparse        | 107 ms                                                     | 104 ms: 1.04x faster                                                         |
| deepcopy_reduce            | 3.35 us                                                    | 3.23 us: 1.04x faster                                                        |
| json                       | 5.31 ms                                                    | 5.13 ms: 1.03x faster                                                        |
| sqlite_synth               | 2.99 us                                                    | 2.89 us: 1.03x faster                                                        |
| async_tree_none            | 378 ms                                                     | 367 ms: 1.03x faster                                                         |
| logging_silent             | 105 ns                                                     | 102 ns: 1.03x faster                                                         |
| fannkuch                   | 402 ms                                                     | 391 ms: 1.03x faster                                                         |
| regex_v8                   | 25.1 ms                                                    | 24.5 ms: 1.02x faster                                                        |
| json_dumps                 | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                                        |
| create_gc_cycles           | 1.82 ms                                                    | 1.79 ms: 1.02x faster                                                        |
| coroutines                 | 23.2 ms                                                    | 22.9 ms: 1.01x faster                                                        |
| gc_traversal               | 3.98 ms                                                    | 3.93 ms: 1.01x faster                                                        |
| pickle_list                | 5.11 us                                                    | 5.08 us: 1.01x faster                                                        |
| xml_etree_process          | 61.2 ms                                                    | 60.9 ms: 1.01x faster                                                        |
| asyncio_websockets         | 567 ms                                                     | 564 ms: 1.00x faster                                                         |
| pickle_dict                | 34.8 us                                                    | 34.9 us: 1.00x slower                                                        |
| unpickle                   | 15.1 us                                                    | 15.2 us: 1.00x slower                                                        |
| thrift                     | 823 us                                                     | 829 us: 1.01x slower                                                         |
| xml_etree_generate         | 87.4 ms                                                    | 88.1 ms: 1.01x slower                                                        |
| deepcopy_memo              | 39.7 us                                                    | 40.1 us: 1.01x slower                                                        |
| deepcopy                   | 367 us                                                     | 372 us: 1.01x slower                                                         |
| pickle_pure_python         | 305 us                                                     | 309 us: 1.01x slower                                                         |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.87 sec: 1.01x slower                                                       |
| generators                 | 29.6 ms                                                    | 30.0 ms: 1.01x slower                                                        |
| tomli_loads                | 2.12 sec                                                   | 2.15 sec: 1.01x slower                                                       |
| meteor_contest             | 110 ms                                                     | 112 ms: 1.02x slower                                                         |
| regex_dna                  | 221 ms                                                     | 225 ms: 1.02x slower                                                         |
| asyncio_tcp                | 508 ms                                                     | 517 ms: 1.02x slower                                                         |
| async_tree_none_tg         | 336 ms                                                     | 344 ms: 1.02x slower                                                         |
| dask                       | 369 ms                                                     | 380 ms: 1.03x slower                                                         |
| djangocms                  | 31.5 us                                                    | 32.5 us: 1.03x slower                                                        |
| gunicorn                   | 1.28 ms                                                    | 1.32 ms: 1.03x slower                                                        |
| python_startup             | 10.8 ms                                                    | 11.1 ms: 1.03x slower                                                        |
| tornado_http               | 94.6 ms                                                    | 98.0 ms: 1.04x slower                                                        |
| logging_format             | 6.47 us                                                    | 6.70 us: 1.04x slower                                                        |
| pathlib                    | 17.3 ms                                                    | 18.0 ms: 1.04x slower                                                        |
| sqlglot_transpile          | 1.63 ms                                                    | 1.70 ms: 1.04x slower                                                        |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 612 ms: 1.04x slower                                                         |
| aiohttp                    | 1.18 ms                                                    | 1.23 ms: 1.04x slower                                                        |
| html5lib                   | 67.2 ms                                                    | 70.0 ms: 1.04x slower                                                        |
| scimark_sor                | 127 ms                                                     | 133 ms: 1.05x slower                                                         |
| pycparser                  | 1.16 sec                                                   | 1.21 sec: 1.05x slower                                                       |
| bench_thread_pool          | 834 us                                                     | 874 us: 1.05x slower                                                         |
| sqlglot_parse              | 1.32 ms                                                    | 1.38 ms: 1.05x slower                                                        |
| pickle                     | 11.5 us                                                    | 12.0 us: 1.05x slower                                                        |
| telco                      | 8.41 ms                                                    | 8.84 ms: 1.05x slower                                                        |
| sqlglot_normalize          | 110 ms                                                     | 116 ms: 1.06x slower                                                         |
| coverage                   | 93.1 ms                                                    | 98.3 ms: 1.06x slower                                                        |
| 2to3                       | 274 ms                                                     | 290 ms: 1.06x slower                                                         |
| docutils                   | 2.83 sec                                                   | 3.00 sec: 1.06x slower                                                       |
| pyflate                    | 484 ms                                                     | 514 ms: 1.06x slower                                                         |
| logging_simple             | 5.74 us                                                    | 6.11 us: 1.06x slower                                                        |
| genshi_text                | 23.7 ms                                                    | 25.2 ms: 1.06x slower                                                        |
| async_generators           | 442 ms                                                     | 471 ms: 1.07x slower                                                         |
| scimark_lu                 | 122 ms                                                     | 130 ms: 1.07x slower                                                         |
| go                         | 145 ms                                                     | 155 ms: 1.07x slower                                                         |
| sqlglot_optimize           | 55.5 ms                                                    | 59.5 ms: 1.07x slower                                                        |
| dulwich_log                | 67.2 ms                                                    | 72.2 ms: 1.08x slower                                                        |
| pylint                     | 317 ms                                                     | 341 ms: 1.08x slower                                                         |
| scimark_monte_carlo        | 69.2 ms                                                    | 74.6 ms: 1.08x slower                                                        |
| django_template            | 34.8 ms                                                    | 37.5 ms: 1.08x slower                                                        |
| raytrace                   | 267 ms                                                     | 288 ms: 1.08x slower                                                         |
| python_startup_no_site     | 7.11 ms                                                    | 7.71 ms: 1.08x slower                                                        |
| mypy2                      | 742 ms                                                     | 809 ms: 1.09x slower                                                         |
| chaos                      | 61.3 ms                                                    | 67.4 ms: 1.10x slower                                                        |
| sympy_str                  | 282 ms                                                     | 310 ms: 1.10x slower                                                         |
| pidigits                   | 191 ms                                                     | 210 ms: 1.10x slower                                                         |
| unpickle_pure_python       | 218 us                                                     | 240 us: 1.10x slower                                                         |
| sympy_expand               | 473 ms                                                     | 524 ms: 1.11x slower                                                         |
| sympy_integrate            | 20.5 ms                                                    | 22.8 ms: 1.11x slower                                                        |
| sympy_sum                  | 156 ms                                                     | 174 ms: 1.11x slower                                                         |
| comprehensions             | 16.6 us                                                    | 19.0 us: 1.14x slower                                                        |
| regex_effbot               | 3.67 ms                                                    | 4.23 ms: 1.15x slower                                                        |
| deltablue                  | 3.25 ms                                                    | 3.77 ms: 1.16x slower                                                        |
| nqueens                    | 81.4 ms                                                    | 95.5 ms: 1.17x slower                                                        |
| pprint_safe_repr           | 758 ms                                                     | 897 ms: 1.18x slower                                                         |
| genshi_xml                 | 51.6 ms                                                    | 61.1 ms: 1.18x slower                                                        |
| pprint_pformat             | 1.56 sec                                                   | 1.94 sec: 1.25x slower                                                       |
| regex_compile              | 137 ms                                                     | 171 ms: 1.25x slower                                                         |
| hexiom                     | 6.30 ms                                                    | 8.20 ms: 1.30x slower                                                        |
| Geometric mean             | (ref)                                                      | 1.03x slower                                                                 |

Benchmark hidden because not significant (8): unpickle_list, async_tree_io, chameleon, bench_mp_pool, async_tree_memoization_tg, async_tree_io_tg, async_tree_cpu_io_mixed, async_tree_memoization
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.10x