# Results vs. 3.13.0b2

- fork: brandtbucher
- ref: justin_ghccc_cache_2
- machine: linux-x86_64
- commit hash: 7fbb9a2
- commit date: 2024-04-23
- overall geometric mean: 1.02x faster
- HPT reliability: 58.91%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.08x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_2-3.13.0a6+-7fbb9a2 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 275 ms: 1.00x slower                                                         |
| chameleon      | 7.22 ms                                                    | 6.88 ms: 1.05x faster                                                        |
| docutils       | 2.83 sec                                                   | 2.89 sec: 1.02x slower                                                       |
| html5lib       | 67.2 ms                                                    | 68.0 ms: 1.01x slower                                                        |
| tornado_http   | 94.6 ms                                                    | 96.2 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                      | 1.00x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_2-3.13.0a6+-7fbb9a2 |
|----------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 356 ms: 1.06x faster                                                         |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 612 ms: 1.04x slower                                                         |
| Geometric mean             | (ref)                                                      | 1.00x slower                                                                 |

Benchmark hidden because not significant (6): async_tree_memoization, async_tree_io, async_tree_memoization_tg, async_tree_none_tg, async_tree_io_tg, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_2-3.13.0a6+-7fbb9a2 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 88.3 ms                                                    | 77.3 ms: 1.14x faster                                                        |
| float          | 78.9 ms                                                    | 72.4 ms: 1.09x faster                                                        |
| pidigits       | 191 ms                                                     | 189 ms: 1.01x faster                                                         |
| Geometric mean | (ref)                                                      | 1.08x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_2-3.13.0a6+-7fbb9a2 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_v8       | 25.1 ms                                                    | 24.7 ms: 1.02x faster                                                        |
| regex_dna      | 221 ms                                                     | 218 ms: 1.01x faster                                                         |
| regex_effbot   | 3.67 ms                                                    | 3.71 ms: 1.01x slower                                                        |
| regex_compile  | 137 ms                                                     | 139 ms: 1.02x slower                                                         |
| Geometric mean | (ref)                                                      | 1.00x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_2-3.13.0a6+-7fbb9a2 |
|----------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| tomli_loads          | 2.12 sec                                                   | 1.92 sec: 1.11x faster                                                       |
| xml_etree_parse      | 162 ms                                                     | 150 ms: 1.08x faster                                                         |
| json_loads           | 28.9 us                                                    | 27.5 us: 1.05x faster                                                        |
| xml_etree_iterparse  | 107 ms                                                     | 103 ms: 1.04x faster                                                         |
| xml_etree_process    | 61.2 ms                                                    | 59.2 ms: 1.03x faster                                                        |
| json_dumps           | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                                        |
| xml_etree_generate   | 87.4 ms                                                    | 86.7 ms: 1.01x faster                                                        |
| unpickle             | 15.1 us                                                    | 15.0 us: 1.01x faster                                                        |
| pickle_pure_python   | 305 us                                                     | 304 us: 1.00x faster                                                         |
| unpickle_list        | 5.34 us                                                    | 5.42 us: 1.01x slower                                                        |
| unpickle_pure_python | 218 us                                                     | 221 us: 1.02x slower                                                         |
| pickle               | 11.5 us                                                    | 11.9 us: 1.04x slower                                                        |
| pickle_list          | 5.11 us                                                    | 5.38 us: 1.05x slower                                                        |
| pickle_dict          | 34.8 us                                                    | 36.8 us: 1.06x slower                                                        |
| Geometric mean       | (ref)                                                      | 1.01x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_2-3.13.0a6+-7fbb9a2 |
|------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 11.1 ms: 1.03x slower                                                        |
| python_startup_no_site | 7.11 ms                                                    | 7.63 ms: 1.07x slower                                                        |
| Geometric mean         | (ref)                                                      | 1.05x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_2-3.13.0a6+-7fbb9a2 |
|-----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 10.1 ms: 1.11x faster                                                        |
| genshi_text     | 23.7 ms                                                    | 24.1 ms: 1.02x slower                                                        |
| django_template | 34.8 ms                                                    | 35.6 ms: 1.02x slower                                                        |
| genshi_xml      | 51.6 ms                                                    | 53.7 ms: 1.04x slower                                                        |
| Geometric mean  | (ref)                                                      | 1.01x faster                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_2-3.13.0a6+-7fbb9a2 |
|----------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 111 us: 1.48x faster                                                         |
| scimark_fft                | 392 ms                                                     | 302 ms: 1.30x faster                                                         |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 4.29 ms: 1.23x faster                                                        |
| richards                   | 50.9 ms                                                    | 42.0 ms: 1.21x faster                                                        |
| richards_super             | 57.4 ms                                                    | 48.2 ms: 1.19x faster                                                        |
| spectral_norm              | 116 ms                                                     | 97.7 ms: 1.19x faster                                                        |
| fannkuch                   | 402 ms                                                     | 349 ms: 1.15x faster                                                         |
| nbody                      | 88.3 ms                                                    | 77.3 ms: 1.14x faster                                                        |
| crypto_pyaes               | 77.5 ms                                                    | 68.3 ms: 1.13x faster                                                        |
| mako                       | 11.2 ms                                                    | 10.1 ms: 1.11x faster                                                        |
| tomli_loads                | 2.12 sec                                                   | 1.92 sec: 1.11x faster                                                       |
| scimark_monte_carlo        | 69.2 ms                                                    | 63.3 ms: 1.09x faster                                                        |
| float                      | 78.9 ms                                                    | 72.4 ms: 1.09x faster                                                        |
| xml_etree_parse            | 162 ms                                                     | 150 ms: 1.08x faster                                                         |
| pyflate                    | 484 ms                                                     | 450 ms: 1.08x faster                                                         |
| gc_traversal               | 3.98 ms                                                    | 3.70 ms: 1.07x faster                                                        |
| async_tree_none            | 378 ms                                                     | 356 ms: 1.06x faster                                                         |
| deepcopy_reduce            | 3.35 us                                                    | 3.16 us: 1.06x faster                                                        |
| mdp                        | 2.79 sec                                                   | 2.63 sec: 1.06x faster                                                       |
| pprint_safe_repr           | 758 ms                                                     | 718 ms: 1.06x faster                                                         |
| json                       | 5.31 ms                                                    | 5.05 ms: 1.05x faster                                                        |
| json_loads                 | 28.9 us                                                    | 27.5 us: 1.05x faster                                                        |
| chameleon                  | 7.22 ms                                                    | 6.88 ms: 1.05x faster                                                        |
| sqlite_synth               | 2.99 us                                                    | 2.85 us: 1.05x faster                                                        |
| xml_etree_iterparse        | 107 ms                                                     | 103 ms: 1.04x faster                                                         |
| pprint_pformat             | 1.56 sec                                                   | 1.50 sec: 1.04x faster                                                       |
| create_gc_cycles           | 1.82 ms                                                    | 1.75 ms: 1.03x faster                                                        |
| xml_etree_process          | 61.2 ms                                                    | 59.2 ms: 1.03x faster                                                        |
| deepcopy_memo              | 39.7 us                                                    | 38.4 us: 1.03x faster                                                        |
| logging_silent             | 105 ns                                                     | 102 ns: 1.03x faster                                                         |
| coroutines                 | 23.2 ms                                                    | 22.5 ms: 1.03x faster                                                        |
| deepcopy                   | 367 us                                                     | 358 us: 1.03x faster                                                         |
| json_dumps                 | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                                        |
| regex_v8                   | 25.1 ms                                                    | 24.7 ms: 1.02x faster                                                        |
| regex_dna                  | 221 ms                                                     | 218 ms: 1.01x faster                                                         |
| pidigits                   | 191 ms                                                     | 189 ms: 1.01x faster                                                         |
| sqlglot_parse              | 1.32 ms                                                    | 1.30 ms: 1.01x faster                                                        |
| meteor_contest             | 110 ms                                                     | 109 ms: 1.01x faster                                                         |
| chaos                      | 61.3 ms                                                    | 60.8 ms: 1.01x faster                                                        |
| xml_etree_generate         | 87.4 ms                                                    | 86.7 ms: 1.01x faster                                                        |
| asyncio_tcp                | 508 ms                                                     | 504 ms: 1.01x faster                                                         |
| unpickle                   | 15.1 us                                                    | 15.0 us: 1.01x faster                                                        |
| pickle_pure_python         | 305 us                                                     | 304 us: 1.00x faster                                                         |
| sqlglot_transpile          | 1.63 ms                                                    | 1.63 ms: 1.00x faster                                                        |
| 2to3                       | 274 ms                                                     | 275 ms: 1.00x slower                                                         |
| bench_mp_pool              | 23.9 ms                                                    | 24.0 ms: 1.01x slower                                                        |
| regex_effbot               | 3.67 ms                                                    | 3.71 ms: 1.01x slower                                                        |
| generators                 | 29.6 ms                                                    | 30.0 ms: 1.01x slower                                                        |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.86 sec: 1.01x slower                                                       |
| html5lib                   | 67.2 ms                                                    | 68.0 ms: 1.01x slower                                                        |
| telco                      | 8.41 ms                                                    | 8.53 ms: 1.01x slower                                                        |
| unpickle_list              | 5.34 us                                                    | 5.42 us: 1.01x slower                                                        |
| dask                       | 369 ms                                                     | 375 ms: 1.01x slower                                                         |
| unpickle_pure_python       | 218 us                                                     | 221 us: 1.02x slower                                                         |
| tornado_http               | 94.6 ms                                                    | 96.2 ms: 1.02x slower                                                        |
| scimark_lu                 | 122 ms                                                     | 124 ms: 1.02x slower                                                         |
| gunicorn                   | 1.28 ms                                                    | 1.30 ms: 1.02x slower                                                        |
| logging_simple             | 5.74 us                                                    | 5.84 us: 1.02x slower                                                        |
| regex_compile              | 137 ms                                                     | 139 ms: 1.02x slower                                                         |
| genshi_text                | 23.7 ms                                                    | 24.1 ms: 1.02x slower                                                        |
| sqlglot_normalize          | 110 ms                                                     | 112 ms: 1.02x slower                                                         |
| go                         | 145 ms                                                     | 147 ms: 1.02x slower                                                         |
| aiohttp                    | 1.18 ms                                                    | 1.20 ms: 1.02x slower                                                        |
| sqlglot_optimize           | 55.5 ms                                                    | 56.7 ms: 1.02x slower                                                        |
| django_template            | 34.8 ms                                                    | 35.6 ms: 1.02x slower                                                        |
| docutils                   | 2.83 sec                                                   | 2.89 sec: 1.02x slower                                                       |
| comprehensions             | 16.6 us                                                    | 17.1 us: 1.03x slower                                                        |
| python_startup             | 10.8 ms                                                    | 11.1 ms: 1.03x slower                                                        |
| sympy_str                  | 282 ms                                                     | 290 ms: 1.03x slower                                                         |
| dulwich_log                | 67.2 ms                                                    | 69.1 ms: 1.03x slower                                                        |
| pathlib                    | 17.3 ms                                                    | 17.8 ms: 1.03x slower                                                        |
| bench_thread_pool          | 834 us                                                     | 862 us: 1.03x slower                                                         |
| raytrace                   | 267 ms                                                     | 276 ms: 1.04x slower                                                         |
| pickle                     | 11.5 us                                                    | 11.9 us: 1.04x slower                                                        |
| scimark_sor                | 127 ms                                                     | 132 ms: 1.04x slower                                                         |
| genshi_xml                 | 51.6 ms                                                    | 53.7 ms: 1.04x slower                                                        |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 612 ms: 1.04x slower                                                         |
| hexiom                     | 6.30 ms                                                    | 6.56 ms: 1.04x slower                                                        |
| sympy_expand               | 473 ms                                                     | 493 ms: 1.04x slower                                                         |
| coverage                   | 93.1 ms                                                    | 97.2 ms: 1.04x slower                                                        |
| nqueens                    | 81.4 ms                                                    | 85.1 ms: 1.05x slower                                                        |
| mypy2                      | 742 ms                                                     | 778 ms: 1.05x slower                                                         |
| pickle_list                | 5.11 us                                                    | 5.38 us: 1.05x slower                                                        |
| pickle_dict                | 34.8 us                                                    | 36.8 us: 1.06x slower                                                        |
| sympy_integrate            | 20.5 ms                                                    | 21.8 ms: 1.06x slower                                                        |
| async_generators           | 442 ms                                                     | 470 ms: 1.06x slower                                                         |
| sympy_sum                  | 156 ms                                                     | 166 ms: 1.06x slower                                                         |
| python_startup_no_site     | 7.11 ms                                                    | 7.63 ms: 1.07x slower                                                        |
| deltablue                  | 3.25 ms                                                    | 3.67 ms: 1.13x slower                                                        |
| Geometric mean             | (ref)                                                      | 1.02x faster                                                                 |

Benchmark hidden because not significant (12): async_tree_memoization, thrift, asyncio_websockets, pycparser, logging_format, async_tree_io, async_tree_memoization_tg, async_tree_none_tg, async_tree_io_tg, async_tree_cpu_io_mixed, djangocms, pylint
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 58.91% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.08x