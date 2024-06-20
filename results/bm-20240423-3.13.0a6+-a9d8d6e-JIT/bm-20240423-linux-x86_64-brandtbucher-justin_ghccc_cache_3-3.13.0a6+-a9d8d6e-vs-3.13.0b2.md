# Results vs. 3.13.0b2

- fork: brandtbucher
- ref: justin_ghccc_cache_3
- machine: linux-x86_64
- commit hash: a9d8d6e
- commit date: 2024-04-23
- overall geometric mean: 1.01x faster
- HPT reliability: 81.76%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6+-a9d8d6e |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 275 ms: 1.00x slower                                                         |
| chameleon      | 7.22 ms                                                    | 6.97 ms: 1.04x faster                                                        |
| docutils       | 2.83 sec                                                   | 2.90 sec: 1.03x slower                                                       |
| html5lib       | 67.2 ms                                                    | 67.9 ms: 1.01x slower                                                        |
| tornado_http   | 94.6 ms                                                    | 96.6 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                      | 1.01x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6+-a9d8d6e |
|----------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 353 ms: 1.07x faster                                                         |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 603 ms: 1.03x slower                                                         |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                                 |

Benchmark hidden because not significant (6): async_tree_io, async_tree_memoization_tg, async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_io_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6+-a9d8d6e |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 88.3 ms                                                    | 76.0 ms: 1.16x faster                                                        |
| float          | 78.9 ms                                                    | 73.1 ms: 1.08x faster                                                        |
| pidigits       | 191 ms                                                     | 189 ms: 1.01x faster                                                         |
| Geometric mean | (ref)                                                      | 1.08x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6+-a9d8d6e |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_v8       | 25.1 ms                                                    | 24.5 ms: 1.02x faster                                                        |
| regex_dna      | 221 ms                                                     | 221 ms: 1.00x faster                                                         |
| regex_effbot   | 3.67 ms                                                    | 3.76 ms: 1.02x slower                                                        |
| regex_compile  | 137 ms                                                     | 141 ms: 1.03x slower                                                         |
| Geometric mean | (ref)                                                      | 1.01x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6+-a9d8d6e |
|----------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| tomli_loads          | 2.12 sec                                                   | 1.90 sec: 1.12x faster                                                       |
| xml_etree_parse      | 162 ms                                                     | 149 ms: 1.08x faster                                                         |
| xml_etree_iterparse  | 107 ms                                                     | 103 ms: 1.04x faster                                                         |
| json_loads           | 28.9 us                                                    | 27.7 us: 1.04x faster                                                        |
| xml_etree_process    | 61.2 ms                                                    | 59.9 ms: 1.02x faster                                                        |
| unpickle_list        | 5.34 us                                                    | 5.31 us: 1.01x faster                                                        |
| xml_etree_generate   | 87.4 ms                                                    | 87.1 ms: 1.00x faster                                                        |
| pickle_pure_python   | 305 us                                                     | 306 us: 1.00x slower                                                         |
| pickle_list          | 5.11 us                                                    | 5.18 us: 1.02x slower                                                        |
| unpickle_pure_python | 218 us                                                     | 224 us: 1.03x slower                                                         |
| pickle               | 11.5 us                                                    | 11.8 us: 1.03x slower                                                        |
| Geometric mean       | (ref)                                                      | 1.02x faster                                                                 |

Benchmark hidden because not significant (3): pickle_dict, json_dumps, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6+-a9d8d6e |
|------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 11.1 ms: 1.03x slower                                                        |
| python_startup_no_site | 7.11 ms                                                    | 7.65 ms: 1.08x slower                                                        |
| Geometric mean         | (ref)                                                      | 1.05x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6+-a9d8d6e |
|-----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 10.0 ms: 1.12x faster                                                        |
| django_template | 34.8 ms                                                    | 35.9 ms: 1.03x slower                                                        |
| genshi_text     | 23.7 ms                                                    | 24.6 ms: 1.04x slower                                                        |
| genshi_xml      | 51.6 ms                                                    | 53.7 ms: 1.04x slower                                                        |
| Geometric mean  | (ref)                                                      | 1.00x faster                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6+-a9d8d6e |
|----------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 115 us: 1.43x faster                                                         |
| scimark_fft                | 392 ms                                                     | 302 ms: 1.30x faster                                                         |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 4.22 ms: 1.25x faster                                                        |
| richards                   | 50.9 ms                                                    | 43.2 ms: 1.18x faster                                                        |
| spectral_norm              | 116 ms                                                     | 99.2 ms: 1.17x faster                                                        |
| nbody                      | 88.3 ms                                                    | 76.0 ms: 1.16x faster                                                        |
| richards_super             | 57.4 ms                                                    | 49.5 ms: 1.16x faster                                                        |
| fannkuch                   | 402 ms                                                     | 349 ms: 1.15x faster                                                         |
| crypto_pyaes               | 77.5 ms                                                    | 67.9 ms: 1.14x faster                                                        |
| mako                       | 11.2 ms                                                    | 10.0 ms: 1.12x faster                                                        |
| tomli_loads                | 2.12 sec                                                   | 1.90 sec: 1.12x faster                                                       |
| scimark_monte_carlo        | 69.2 ms                                                    | 62.6 ms: 1.10x faster                                                        |
| xml_etree_parse            | 162 ms                                                     | 149 ms: 1.08x faster                                                         |
| pyflate                    | 484 ms                                                     | 447 ms: 1.08x faster                                                         |
| float                      | 78.9 ms                                                    | 73.1 ms: 1.08x faster                                                        |
| async_tree_none            | 378 ms                                                     | 353 ms: 1.07x faster                                                         |
| sqlite_synth               | 2.99 us                                                    | 2.84 us: 1.05x faster                                                        |
| mdp                        | 2.79 sec                                                   | 2.65 sec: 1.05x faster                                                       |
| xml_etree_iterparse        | 107 ms                                                     | 103 ms: 1.04x faster                                                         |
| pprint_pformat             | 1.56 sec                                                   | 1.49 sec: 1.04x faster                                                       |
| json_loads                 | 28.9 us                                                    | 27.7 us: 1.04x faster                                                        |
| chameleon                  | 7.22 ms                                                    | 6.97 ms: 1.04x faster                                                        |
| deepcopy_reduce            | 3.35 us                                                    | 3.23 us: 1.04x faster                                                        |
| logging_silent             | 105 ns                                                     | 101 ns: 1.03x faster                                                         |
| pprint_safe_repr           | 758 ms                                                     | 738 ms: 1.03x faster                                                         |
| create_gc_cycles           | 1.82 ms                                                    | 1.77 ms: 1.03x faster                                                        |
| coroutines                 | 23.2 ms                                                    | 22.6 ms: 1.03x faster                                                        |
| regex_v8                   | 25.1 ms                                                    | 24.5 ms: 1.02x faster                                                        |
| json                       | 5.31 ms                                                    | 5.20 ms: 1.02x faster                                                        |
| xml_etree_process          | 61.2 ms                                                    | 59.9 ms: 1.02x faster                                                        |
| deepcopy                   | 367 us                                                     | 361 us: 1.02x faster                                                         |
| pidigits                   | 191 ms                                                     | 189 ms: 1.01x faster                                                         |
| chaos                      | 61.3 ms                                                    | 60.6 ms: 1.01x faster                                                        |
| unpickle_list              | 5.34 us                                                    | 5.31 us: 1.01x faster                                                        |
| deepcopy_memo              | 39.7 us                                                    | 39.5 us: 1.01x faster                                                        |
| xml_etree_generate         | 87.4 ms                                                    | 87.1 ms: 1.00x faster                                                        |
| asyncio_websockets         | 567 ms                                                     | 564 ms: 1.00x faster                                                         |
| regex_dna                  | 221 ms                                                     | 221 ms: 1.00x faster                                                         |
| pickle_pure_python         | 305 us                                                     | 306 us: 1.00x slower                                                         |
| 2to3                       | 274 ms                                                     | 275 ms: 1.00x slower                                                         |
| sqlglot_transpile          | 1.63 ms                                                    | 1.64 ms: 1.01x slower                                                        |
| bench_mp_pool              | 23.9 ms                                                    | 24.0 ms: 1.01x slower                                                        |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.86 sec: 1.01x slower                                                       |
| html5lib                   | 67.2 ms                                                    | 67.9 ms: 1.01x slower                                                        |
| scimark_lu                 | 122 ms                                                     | 123 ms: 1.01x slower                                                         |
| telco                      | 8.41 ms                                                    | 8.53 ms: 1.01x slower                                                        |
| asyncio_tcp                | 508 ms                                                     | 516 ms: 1.01x slower                                                         |
| pickle_list                | 5.11 us                                                    | 5.18 us: 1.02x slower                                                        |
| logging_format             | 6.47 us                                                    | 6.57 us: 1.02x slower                                                        |
| thrift                     | 823 us                                                     | 836 us: 1.02x slower                                                         |
| dask                       | 369 ms                                                     | 376 ms: 1.02x slower                                                         |
| gunicorn                   | 1.28 ms                                                    | 1.30 ms: 1.02x slower                                                        |
| tornado_http               | 94.6 ms                                                    | 96.6 ms: 1.02x slower                                                        |
| gc_traversal               | 3.98 ms                                                    | 4.06 ms: 1.02x slower                                                        |
| regex_effbot               | 3.67 ms                                                    | 3.76 ms: 1.02x slower                                                        |
| docutils                   | 2.83 sec                                                   | 2.90 sec: 1.03x slower                                                       |
| djangocms                  | 31.5 us                                                    | 32.4 us: 1.03x slower                                                        |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 603 ms: 1.03x slower                                                         |
| unpickle_pure_python       | 218 us                                                     | 224 us: 1.03x slower                                                         |
| pathlib                    | 17.3 ms                                                    | 17.8 ms: 1.03x slower                                                        |
| python_startup             | 10.8 ms                                                    | 11.1 ms: 1.03x slower                                                        |
| sqlglot_optimize           | 55.5 ms                                                    | 57.2 ms: 1.03x slower                                                        |
| django_template            | 34.8 ms                                                    | 35.9 ms: 1.03x slower                                                        |
| regex_compile              | 137 ms                                                     | 141 ms: 1.03x slower                                                         |
| pickle                     | 11.5 us                                                    | 11.8 us: 1.03x slower                                                        |
| go                         | 145 ms                                                     | 149 ms: 1.03x slower                                                         |
| aiohttp                    | 1.18 ms                                                    | 1.22 ms: 1.03x slower                                                        |
| logging_simple             | 5.74 us                                                    | 5.93 us: 1.03x slower                                                        |
| sqlglot_normalize          | 110 ms                                                     | 114 ms: 1.04x slower                                                         |
| raytrace                   | 267 ms                                                     | 277 ms: 1.04x slower                                                         |
| genshi_text                | 23.7 ms                                                    | 24.6 ms: 1.04x slower                                                        |
| genshi_xml                 | 51.6 ms                                                    | 53.7 ms: 1.04x slower                                                        |
| sympy_str                  | 282 ms                                                     | 294 ms: 1.04x slower                                                         |
| dulwich_log                | 67.2 ms                                                    | 70.1 ms: 1.04x slower                                                        |
| bench_thread_pool          | 834 us                                                     | 872 us: 1.05x slower                                                         |
| comprehensions             | 16.6 us                                                    | 17.4 us: 1.05x slower                                                        |
| sympy_expand               | 473 ms                                                     | 495 ms: 1.05x slower                                                         |
| hexiom                     | 6.30 ms                                                    | 6.61 ms: 1.05x slower                                                        |
| coverage                   | 93.1 ms                                                    | 98.4 ms: 1.06x slower                                                        |
| mypy2                      | 742 ms                                                     | 786 ms: 1.06x slower                                                         |
| async_generators           | 442 ms                                                     | 468 ms: 1.06x slower                                                         |
| nqueens                    | 81.4 ms                                                    | 87.1 ms: 1.07x slower                                                        |
| sympy_sum                  | 156 ms                                                     | 167 ms: 1.07x slower                                                         |
| sympy_integrate            | 20.5 ms                                                    | 22.1 ms: 1.08x slower                                                        |
| python_startup_no_site     | 7.11 ms                                                    | 7.65 ms: 1.08x slower                                                        |
| deltablue                  | 3.25 ms                                                    | 3.72 ms: 1.15x slower                                                        |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                                 |

Benchmark hidden because not significant (15): async_tree_io, async_tree_memoization_tg, async_tree_none_tg, meteor_contest, pickle_dict, sqlglot_parse, generators, async_tree_cpu_io_mixed, scimark_sor, json_dumps, async_tree_io_tg, pycparser, unpickle, async_tree_memoization, pylint
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 81.76% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.09x