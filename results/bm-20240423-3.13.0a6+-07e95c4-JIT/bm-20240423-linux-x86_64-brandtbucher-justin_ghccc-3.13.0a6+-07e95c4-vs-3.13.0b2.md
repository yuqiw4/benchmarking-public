# Results vs. 3.13.0b2

- fork: brandtbucher
- ref: justin_ghccc
- machine: linux-x86_64
- commit hash: 07e95c4
- commit date: 2024-04-23
- overall geometric mean: 1.01x faster
- HPT reliability: 83.66%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.06x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a6+-07e95c4 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 275 ms: 1.00x slower                                                 |
| chameleon      | 7.22 ms                                                    | 6.93 ms: 1.04x faster                                                |
| docutils       | 2.83 sec                                                   | 2.90 sec: 1.03x slower                                               |
| html5lib       | 67.2 ms                                                    | 67.8 ms: 1.01x slower                                                |
| tornado_http   | 94.6 ms                                                    | 96.3 ms: 1.02x slower                                                |
| Geometric mean | (ref)                                                      | 1.00x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a6+-07e95c4 |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 356 ms: 1.06x faster                                                 |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 608 ms: 1.03x slower                                                 |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                         |

Benchmark hidden because not significant (6): async_tree_io, async_tree_memoization_tg, async_tree_memoization, async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a6+-07e95c4 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| nbody          | 88.3 ms                                                    | 82.2 ms: 1.07x faster                                                |
| float          | 78.9 ms                                                    | 73.4 ms: 1.07x faster                                                |
| pidigits       | 191 ms                                                     | 197 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                      | 1.04x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a6+-07e95c4 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_v8       | 25.1 ms                                                    | 24.4 ms: 1.03x faster                                                |
| regex_effbot   | 3.67 ms                                                    | 3.57 ms: 1.03x faster                                                |
| regex_dna      | 221 ms                                                     | 218 ms: 1.02x faster                                                 |
| regex_compile  | 137 ms                                                     | 140 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                      | 1.01x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a6+-07e95c4 |
|----------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| tomli_loads          | 2.12 sec                                                   | 1.96 sec: 1.08x faster                                               |
| xml_etree_parse      | 162 ms                                                     | 150 ms: 1.08x faster                                                 |
| pickle_list          | 5.11 us                                                    | 4.75 us: 1.07x faster                                                |
| unpickle_list        | 5.34 us                                                    | 5.05 us: 1.06x faster                                                |
| xml_etree_iterparse  | 107 ms                                                     | 102 ms: 1.06x faster                                                 |
| json_loads           | 28.9 us                                                    | 27.6 us: 1.05x faster                                                |
| pickle_dict          | 34.8 us                                                    | 33.5 us: 1.04x faster                                                |
| xml_etree_process    | 61.2 ms                                                    | 60.1 ms: 1.02x faster                                                |
| xml_etree_generate   | 87.4 ms                                                    | 87.1 ms: 1.00x faster                                                |
| pickle_pure_python   | 305 us                                                     | 305 us: 1.00x faster                                                 |
| unpickle             | 15.1 us                                                    | 15.5 us: 1.03x slower                                                |
| pickle               | 11.5 us                                                    | 11.9 us: 1.03x slower                                                |
| unpickle_pure_python | 218 us                                                     | 227 us: 1.04x slower                                                 |
| Geometric mean       | (ref)                                                      | 1.02x faster                                                         |

Benchmark hidden because not significant (1): json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a6+-07e95c4 |
|------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 11.0 ms: 1.02x slower                                                |
| python_startup_no_site | 7.11 ms                                                    | 7.57 ms: 1.06x slower                                                |
| Geometric mean         | (ref)                                                      | 1.04x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a6+-07e95c4 |
|-----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 9.96 ms: 1.13x faster                                                |
| django_template | 34.8 ms                                                    | 36.2 ms: 1.04x slower                                                |
| genshi_text     | 23.7 ms                                                    | 24.7 ms: 1.05x slower                                                |
| genshi_xml      | 51.6 ms                                                    | 55.4 ms: 1.07x slower                                                |
| Geometric mean  | (ref)                                                      | 1.01x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a6+-07e95c4 |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 114 us: 1.45x faster                                                 |
| scimark_fft                | 392 ms                                                     | 316 ms: 1.24x faster                                                 |
| richards                   | 50.9 ms                                                    | 42.5 ms: 1.20x faster                                                |
| richards_super             | 57.4 ms                                                    | 48.8 ms: 1.18x faster                                                |
| spectral_norm              | 116 ms                                                     | 98.9 ms: 1.17x faster                                                |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 4.52 ms: 1.17x faster                                                |
| fannkuch                   | 402 ms                                                     | 353 ms: 1.14x faster                                                 |
| crypto_pyaes               | 77.5 ms                                                    | 68.6 ms: 1.13x faster                                                |
| mako                       | 11.2 ms                                                    | 9.96 ms: 1.13x faster                                                |
| pyflate                    | 484 ms                                                     | 442 ms: 1.09x faster                                                 |
| tomli_loads                | 2.12 sec                                                   | 1.96 sec: 1.08x faster                                               |
| scimark_monte_carlo        | 69.2 ms                                                    | 63.9 ms: 1.08x faster                                                |
| xml_etree_parse            | 162 ms                                                     | 150 ms: 1.08x faster                                                 |
| nbody                      | 88.3 ms                                                    | 82.2 ms: 1.07x faster                                                |
| pickle_list                | 5.11 us                                                    | 4.75 us: 1.07x faster                                                |
| float                      | 78.9 ms                                                    | 73.4 ms: 1.07x faster                                                |
| async_tree_none            | 378 ms                                                     | 356 ms: 1.06x faster                                                 |
| unpickle_list              | 5.34 us                                                    | 5.05 us: 1.06x faster                                                |
| xml_etree_iterparse        | 107 ms                                                     | 102 ms: 1.06x faster                                                 |
| deepcopy_reduce            | 3.35 us                                                    | 3.18 us: 1.05x faster                                                |
| sqlite_synth               | 2.99 us                                                    | 2.84 us: 1.05x faster                                                |
| gc_traversal               | 3.98 ms                                                    | 3.79 ms: 1.05x faster                                                |
| json_loads                 | 28.9 us                                                    | 27.6 us: 1.05x faster                                                |
| chameleon                  | 7.22 ms                                                    | 6.93 ms: 1.04x faster                                                |
| pickle_dict                | 34.8 us                                                    | 33.5 us: 1.04x faster                                                |
| json                       | 5.31 ms                                                    | 5.13 ms: 1.03x faster                                                |
| deepcopy_memo              | 39.7 us                                                    | 38.5 us: 1.03x faster                                                |
| regex_v8                   | 25.1 ms                                                    | 24.4 ms: 1.03x faster                                                |
| create_gc_cycles           | 1.82 ms                                                    | 1.76 ms: 1.03x faster                                                |
| regex_effbot               | 3.67 ms                                                    | 3.57 ms: 1.03x faster                                                |
| deepcopy                   | 367 us                                                     | 358 us: 1.02x faster                                                 |
| pprint_safe_repr           | 758 ms                                                     | 745 ms: 1.02x faster                                                 |
| xml_etree_process          | 61.2 ms                                                    | 60.1 ms: 1.02x faster                                                |
| regex_dna                  | 221 ms                                                     | 218 ms: 1.02x faster                                                 |
| coroutines                 | 23.2 ms                                                    | 22.9 ms: 1.01x faster                                                |
| logging_silent             | 105 ns                                                     | 104 ns: 1.01x faster                                                 |
| mdp                        | 2.79 sec                                                   | 2.76 sec: 1.01x faster                                               |
| chaos                      | 61.3 ms                                                    | 60.9 ms: 1.01x faster                                                |
| meteor_contest             | 110 ms                                                     | 109 ms: 1.01x faster                                                 |
| xml_etree_generate         | 87.4 ms                                                    | 87.1 ms: 1.00x faster                                                |
| pickle_pure_python         | 305 us                                                     | 305 us: 1.00x faster                                                 |
| 2to3                       | 274 ms                                                     | 275 ms: 1.00x slower                                                 |
| bench_mp_pool              | 23.9 ms                                                    | 24.0 ms: 1.01x slower                                                |
| html5lib                   | 67.2 ms                                                    | 67.8 ms: 1.01x slower                                                |
| logging_format             | 6.47 us                                                    | 6.52 us: 1.01x slower                                                |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.86 sec: 1.01x slower                                               |
| asyncio_tcp                | 508 ms                                                     | 513 ms: 1.01x slower                                                 |
| raytrace                   | 267 ms                                                     | 271 ms: 1.01x slower                                                 |
| pycparser                  | 1.16 sec                                                   | 1.18 sec: 1.02x slower                                               |
| tornado_http               | 94.6 ms                                                    | 96.3 ms: 1.02x slower                                                |
| logging_simple             | 5.74 us                                                    | 5.86 us: 1.02x slower                                                |
| python_startup             | 10.8 ms                                                    | 11.0 ms: 1.02x slower                                                |
| gunicorn                   | 1.28 ms                                                    | 1.30 ms: 1.02x slower                                                |
| scimark_sor                | 127 ms                                                     | 130 ms: 1.02x slower                                                 |
| dask                       | 369 ms                                                     | 378 ms: 1.02x slower                                                 |
| regex_compile              | 137 ms                                                     | 140 ms: 1.02x slower                                                 |
| comprehensions             | 16.6 us                                                    | 17.0 us: 1.02x slower                                                |
| docutils                   | 2.83 sec                                                   | 2.90 sec: 1.03x slower                                               |
| unpickle                   | 15.1 us                                                    | 15.5 us: 1.03x slower                                                |
| pathlib                    | 17.3 ms                                                    | 17.8 ms: 1.03x slower                                                |
| generators                 | 29.6 ms                                                    | 30.4 ms: 1.03x slower                                                |
| pidigits                   | 191 ms                                                     | 197 ms: 1.03x slower                                                 |
| dulwich_log                | 67.2 ms                                                    | 69.1 ms: 1.03x slower                                                |
| aiohttp                    | 1.18 ms                                                    | 1.22 ms: 1.03x slower                                                |
| sqlglot_normalize          | 110 ms                                                     | 114 ms: 1.03x slower                                                 |
| bench_thread_pool          | 834 us                                                     | 861 us: 1.03x slower                                                 |
| telco                      | 8.41 ms                                                    | 8.69 ms: 1.03x slower                                                |
| hexiom                     | 6.30 ms                                                    | 6.50 ms: 1.03x slower                                                |
| sqlglot_optimize           | 55.5 ms                                                    | 57.4 ms: 1.03x slower                                                |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 608 ms: 1.03x slower                                                 |
| pickle                     | 11.5 us                                                    | 11.9 us: 1.03x slower                                                |
| scimark_lu                 | 122 ms                                                     | 126 ms: 1.04x slower                                                 |
| django_template            | 34.8 ms                                                    | 36.2 ms: 1.04x slower                                                |
| unpickle_pure_python       | 218 us                                                     | 227 us: 1.04x slower                                                 |
| sympy_str                  | 282 ms                                                     | 294 ms: 1.04x slower                                                 |
| genshi_text                | 23.7 ms                                                    | 24.7 ms: 1.05x slower                                                |
| sympy_expand               | 473 ms                                                     | 495 ms: 1.05x slower                                                 |
| go                         | 145 ms                                                     | 153 ms: 1.06x slower                                                 |
| async_generators           | 442 ms                                                     | 469 ms: 1.06x slower                                                 |
| nqueens                    | 81.4 ms                                                    | 86.4 ms: 1.06x slower                                                |
| python_startup_no_site     | 7.11 ms                                                    | 7.57 ms: 1.06x slower                                                |
| mypy2                      | 742 ms                                                     | 790 ms: 1.07x slower                                                 |
| sympy_sum                  | 156 ms                                                     | 167 ms: 1.07x slower                                                 |
| sympy_integrate            | 20.5 ms                                                    | 22.0 ms: 1.07x slower                                                |
| genshi_xml                 | 51.6 ms                                                    | 55.4 ms: 1.07x slower                                                |
| coverage                   | 93.1 ms                                                    | 104 ms: 1.12x slower                                                 |
| deltablue                  | 3.25 ms                                                    | 3.69 ms: 1.13x slower                                                |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                         |

Benchmark hidden because not significant (14): async_tree_io, pprint_pformat, async_tree_memoization_tg, async_tree_memoization, async_tree_none_tg, thrift, json_dumps, sqlglot_parse, asyncio_websockets, sqlglot_transpile, async_tree_cpu_io_mixed, async_tree_io_tg, djangocms, pylint
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 83.66% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.06x