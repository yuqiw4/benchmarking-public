# Results vs. 3.13.0b2

- fork: brandtbucher
- ref: justin_ghccc_cache_1
- machine: linux-x86_64
- commit hash: b8620f7
- commit date: 2024-04-23
- overall geometric mean: 1.01x faster
- HPT reliability: 80.29%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.08x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6+-b8620f7 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 277 ms: 1.01x slower                                                         |
| chameleon      | 7.22 ms                                                    | 7.12 ms: 1.01x faster                                                        |
| docutils       | 2.83 sec                                                   | 2.90 sec: 1.03x slower                                                       |
| html5lib       | 67.2 ms                                                    | 68.8 ms: 1.02x slower                                                        |
| tornado_http   | 94.6 ms                                                    | 95.7 ms: 1.01x slower                                                        |
| Geometric mean | (ref)                                                      | 1.01x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6+-b8620f7 |
|----------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 359 ms: 1.06x faster                                                         |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 604 ms: 1.03x slower                                                         |
| Geometric mean             | (ref)                                                      | 1.00x slower                                                                 |

Benchmark hidden because not significant (6): async_tree_memoization, async_tree_memoization_tg, async_tree_cpu_io_mixed, async_tree_none_tg, async_tree_io, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6+-b8620f7 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 88.3 ms                                                    | 81.0 ms: 1.09x faster                                                        |
| float          | 78.9 ms                                                    | 73.7 ms: 1.07x faster                                                        |
| pidigits       | 191 ms                                                     | 189 ms: 1.01x faster                                                         |
| Geometric mean | (ref)                                                      | 1.06x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6+-b8620f7 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_v8       | 25.1 ms                                                    | 25.0 ms: 1.00x faster                                                        |
| regex_compile  | 137 ms                                                     | 140 ms: 1.02x slower                                                         |
| regex_dna      | 221 ms                                                     | 229 ms: 1.04x slower                                                         |
| regex_effbot   | 3.67 ms                                                    | 4.21 ms: 1.15x slower                                                        |
| Geometric mean | (ref)                                                      | 1.05x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6+-b8620f7 |
|----------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| tomli_loads          | 2.12 sec                                                   | 1.92 sec: 1.10x faster                                                       |
| xml_etree_parse      | 162 ms                                                     | 148 ms: 1.09x faster                                                         |
| xml_etree_iterparse  | 107 ms                                                     | 101 ms: 1.06x faster                                                         |
| json_loads           | 28.9 us                                                    | 27.3 us: 1.06x faster                                                        |
| unpickle_list        | 5.34 us                                                    | 5.20 us: 1.03x faster                                                        |
| pickle_list          | 5.11 us                                                    | 5.06 us: 1.01x faster                                                        |
| json_dumps           | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                                        |
| xml_etree_process    | 61.2 ms                                                    | 60.6 ms: 1.01x faster                                                        |
| pickle_pure_python   | 305 us                                                     | 309 us: 1.01x slower                                                         |
| pickle_dict          | 34.8 us                                                    | 35.6 us: 1.02x slower                                                        |
| unpickle_pure_python | 218 us                                                     | 223 us: 1.02x slower                                                         |
| pickle               | 11.5 us                                                    | 11.8 us: 1.03x slower                                                        |
| Geometric mean       | (ref)                                                      | 1.02x faster                                                                 |

Benchmark hidden because not significant (2): xml_etree_generate, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6+-b8620f7 |
|------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 11.1 ms: 1.04x slower                                                        |
| python_startup_no_site | 7.11 ms                                                    | 7.68 ms: 1.08x slower                                                        |
| Geometric mean         | (ref)                                                      | 1.06x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6+-b8620f7 |
|-----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 9.91 ms: 1.13x faster                                                        |
| genshi_text     | 23.7 ms                                                    | 24.1 ms: 1.02x slower                                                        |
| django_template | 34.8 ms                                                    | 35.8 ms: 1.03x slower                                                        |
| genshi_xml      | 51.6 ms                                                    | 55.9 ms: 1.08x slower                                                        |
| Geometric mean  | (ref)                                                      | 1.00x slower                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6+-b8620f7 |
|----------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 115 us: 1.43x faster                                                         |
| scimark_fft                | 392 ms                                                     | 310 ms: 1.27x faster                                                         |
| richards                   | 50.9 ms                                                    | 42.4 ms: 1.20x faster                                                        |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 4.42 ms: 1.19x faster                                                        |
| spectral_norm              | 116 ms                                                     | 98.5 ms: 1.18x faster                                                        |
| richards_super             | 57.4 ms                                                    | 49.1 ms: 1.17x faster                                                        |
| mako                       | 11.2 ms                                                    | 9.91 ms: 1.13x faster                                                        |
| fannkuch                   | 402 ms                                                     | 356 ms: 1.13x faster                                                         |
| crypto_pyaes               | 77.5 ms                                                    | 68.9 ms: 1.12x faster                                                        |
| tomli_loads                | 2.12 sec                                                   | 1.92 sec: 1.10x faster                                                       |
| pyflate                    | 484 ms                                                     | 443 ms: 1.09x faster                                                         |
| nbody                      | 88.3 ms                                                    | 81.0 ms: 1.09x faster                                                        |
| xml_etree_parse            | 162 ms                                                     | 148 ms: 1.09x faster                                                         |
| scimark_monte_carlo        | 69.2 ms                                                    | 63.6 ms: 1.09x faster                                                        |
| float                      | 78.9 ms                                                    | 73.7 ms: 1.07x faster                                                        |
| gc_traversal               | 3.98 ms                                                    | 3.74 ms: 1.06x faster                                                        |
| xml_etree_iterparse        | 107 ms                                                     | 101 ms: 1.06x faster                                                         |
| json_loads                 | 28.9 us                                                    | 27.3 us: 1.06x faster                                                        |
| pprint_safe_repr           | 758 ms                                                     | 717 ms: 1.06x faster                                                         |
| logging_silent             | 105 ns                                                     | 99.0 ns: 1.06x faster                                                        |
| mdp                        | 2.79 sec                                                   | 2.64 sec: 1.06x faster                                                       |
| async_tree_none            | 378 ms                                                     | 359 ms: 1.06x faster                                                         |
| pprint_pformat             | 1.56 sec                                                   | 1.48 sec: 1.05x faster                                                       |
| sqlite_synth               | 2.99 us                                                    | 2.85 us: 1.05x faster                                                        |
| json                       | 5.31 ms                                                    | 5.08 ms: 1.04x faster                                                        |
| deepcopy_reduce            | 3.35 us                                                    | 3.21 us: 1.04x faster                                                        |
| unpickle_list              | 5.34 us                                                    | 5.20 us: 1.03x faster                                                        |
| coroutines                 | 23.2 ms                                                    | 22.6 ms: 1.03x faster                                                        |
| create_gc_cycles           | 1.82 ms                                                    | 1.77 ms: 1.02x faster                                                        |
| deepcopy_memo              | 39.7 us                                                    | 39.1 us: 1.02x faster                                                        |
| meteor_contest             | 110 ms                                                     | 108 ms: 1.01x faster                                                         |
| pidigits                   | 191 ms                                                     | 189 ms: 1.01x faster                                                         |
| chameleon                  | 7.22 ms                                                    | 7.12 ms: 1.01x faster                                                        |
| pickle_list                | 5.11 us                                                    | 5.06 us: 1.01x faster                                                        |
| json_dumps                 | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                                        |
| xml_etree_process          | 61.2 ms                                                    | 60.6 ms: 1.01x faster                                                        |
| logging_format             | 6.47 us                                                    | 6.41 us: 1.01x faster                                                        |
| deepcopy                   | 367 us                                                     | 364 us: 1.01x faster                                                         |
| asyncio_websockets         | 567 ms                                                     | 563 ms: 1.01x faster                                                         |
| sqlglot_parse              | 1.32 ms                                                    | 1.31 ms: 1.01x faster                                                        |
| regex_v8                   | 25.1 ms                                                    | 25.0 ms: 1.00x faster                                                        |
| thrift                     | 823 us                                                     | 827 us: 1.01x slower                                                         |
| bench_mp_pool              | 23.9 ms                                                    | 24.0 ms: 1.01x slower                                                        |
| chaos                      | 61.3 ms                                                    | 61.8 ms: 1.01x slower                                                        |
| 2to3                       | 274 ms                                                     | 277 ms: 1.01x slower                                                         |
| scimark_sor                | 127 ms                                                     | 129 ms: 1.01x slower                                                         |
| generators                 | 29.6 ms                                                    | 29.9 ms: 1.01x slower                                                        |
| tornado_http               | 94.6 ms                                                    | 95.7 ms: 1.01x slower                                                        |
| pickle_pure_python         | 305 us                                                     | 309 us: 1.01x slower                                                         |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.86 sec: 1.01x slower                                                       |
| asyncio_tcp                | 508 ms                                                     | 515 ms: 1.01x slower                                                         |
| telco                      | 8.41 ms                                                    | 8.56 ms: 1.02x slower                                                        |
| gunicorn                   | 1.28 ms                                                    | 1.30 ms: 1.02x slower                                                        |
| comprehensions             | 16.6 us                                                    | 16.9 us: 1.02x slower                                                        |
| genshi_text                | 23.7 ms                                                    | 24.1 ms: 1.02x slower                                                        |
| regex_compile              | 137 ms                                                     | 140 ms: 1.02x slower                                                         |
| go                         | 145 ms                                                     | 148 ms: 1.02x slower                                                         |
| pickle_dict                | 34.8 us                                                    | 35.6 us: 1.02x slower                                                        |
| unpickle_pure_python       | 218 us                                                     | 223 us: 1.02x slower                                                         |
| html5lib                   | 67.2 ms                                                    | 68.8 ms: 1.02x slower                                                        |
| pickle                     | 11.5 us                                                    | 11.8 us: 1.03x slower                                                        |
| docutils                   | 2.83 sec                                                   | 2.90 sec: 1.03x slower                                                       |
| raytrace                   | 267 ms                                                     | 274 ms: 1.03x slower                                                         |
| djangocms                  | 31.5 us                                                    | 32.3 us: 1.03x slower                                                        |
| pathlib                    | 17.3 ms                                                    | 17.8 ms: 1.03x slower                                                        |
| aiohttp                    | 1.18 ms                                                    | 1.21 ms: 1.03x slower                                                        |
| dulwich_log                | 67.2 ms                                                    | 69.0 ms: 1.03x slower                                                        |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 604 ms: 1.03x slower                                                         |
| django_template            | 34.8 ms                                                    | 35.8 ms: 1.03x slower                                                        |
| sqlglot_optimize           | 55.5 ms                                                    | 57.1 ms: 1.03x slower                                                        |
| sqlglot_normalize          | 110 ms                                                     | 114 ms: 1.03x slower                                                         |
| scimark_lu                 | 122 ms                                                     | 125 ms: 1.03x slower                                                         |
| python_startup             | 10.8 ms                                                    | 11.1 ms: 1.04x slower                                                        |
| bench_thread_pool          | 834 us                                                     | 864 us: 1.04x slower                                                         |
| regex_dna                  | 221 ms                                                     | 229 ms: 1.04x slower                                                         |
| hexiom                     | 6.30 ms                                                    | 6.54 ms: 1.04x slower                                                        |
| sympy_str                  | 282 ms                                                     | 293 ms: 1.04x slower                                                         |
| sympy_expand               | 473 ms                                                     | 494 ms: 1.05x slower                                                         |
| coverage                   | 93.1 ms                                                    | 98.1 ms: 1.05x slower                                                        |
| async_generators           | 442 ms                                                     | 467 ms: 1.06x slower                                                         |
| mypy2                      | 742 ms                                                     | 785 ms: 1.06x slower                                                         |
| nqueens                    | 81.4 ms                                                    | 86.7 ms: 1.06x slower                                                        |
| sympy_integrate            | 20.5 ms                                                    | 21.9 ms: 1.07x slower                                                        |
| sympy_sum                  | 156 ms                                                     | 167 ms: 1.07x slower                                                         |
| python_startup_no_site     | 7.11 ms                                                    | 7.68 ms: 1.08x slower                                                        |
| genshi_xml                 | 51.6 ms                                                    | 55.9 ms: 1.08x slower                                                        |
| deltablue                  | 3.25 ms                                                    | 3.64 ms: 1.12x slower                                                        |
| regex_effbot               | 3.67 ms                                                    | 4.21 ms: 1.15x slower                                                        |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                                 |

Benchmark hidden because not significant (13): async_tree_memoization, async_tree_memoization_tg, async_tree_cpu_io_mixed, sqlglot_transpile, xml_etree_generate, logging_simple, async_tree_none_tg, pycparser, unpickle, async_tree_io, dask, async_tree_io_tg, pylint
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 80.29% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.08x