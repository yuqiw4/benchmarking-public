# Results vs. 3.13.0b2

- fork: python
- ref: c520bf9bdf77d43c3d5d
- machine: linux-x86_64
- commit hash: c520bf9
- commit date: 2024-04-16
- overall geometric mean: 1.01x faster
- HPT reliability: 91.63%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 270 ms: 1.01x faster                                                   |
| chameleon      | 7.22 ms                                                    | 6.94 ms: 1.04x faster                                                  |
| tornado_http   | 94.6 ms                                                    | 93.9 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                      | 1.01x faster                                                           |

Benchmark hidden because not significant (2): docutils, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 |
|----------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 354 ms: 1.07x faster                                                   |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 607 ms: 1.03x slower                                                   |
| Geometric mean             | (ref)                                                      | 1.00x faster                                                           |

Benchmark hidden because not significant (6): async_tree_io, async_tree_io_tg, async_tree_cpu_io_mixed, async_tree_memoization, async_tree_memoization_tg, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 88.3 ms                                                    | 90.0 ms: 1.02x slower                                                  |
| pidigits       | 191 ms                                                     | 206 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                      | 1.03x slower                                                           |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 221 ms                                                     | 218 ms: 1.01x faster                                                   |
| regex_compile  | 137 ms                                                     | 136 ms: 1.01x faster                                                   |
| regex_v8       | 25.1 ms                                                    | 25.4 ms: 1.01x slower                                                  |
| regex_effbot   | 3.67 ms                                                    | 3.74 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                      | 1.00x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 |
|----------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| unpickle_list        | 5.34 us                                                    | 4.99 us: 1.07x faster                                                  |
| json_loads           | 28.9 us                                                    | 27.6 us: 1.05x faster                                                  |
| pickle_pure_python   | 305 us                                                     | 299 us: 1.02x faster                                                   |
| json_dumps           | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                                  |
| xml_etree_process    | 61.2 ms                                                    | 60.8 ms: 1.01x faster                                                  |
| unpickle_pure_python | 218 us                                                     | 217 us: 1.00x faster                                                   |
| unpickle             | 15.1 us                                                    | 15.2 us: 1.01x slower                                                  |
| xml_etree_generate   | 87.4 ms                                                    | 88.8 ms: 1.02x slower                                                  |
| tomli_loads          | 2.12 sec                                                   | 2.17 sec: 1.02x slower                                                 |
| pickle               | 11.5 us                                                    | 11.8 us: 1.03x slower                                                  |
| pickle_list          | 5.11 us                                                    | 5.33 us: 1.04x slower                                                  |
| Geometric mean       | (ref)                                                      | 1.00x faster                                                           |

Benchmark hidden because not significant (3): xml_etree_parse, xml_etree_iterparse, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                  |
| Geometric mean | (ref)                                                      | 1.01x faster                                                           |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 |
|-----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 11.1 ms: 1.02x faster                                                  |
| genshi_text     | 23.7 ms                                                    | 23.4 ms: 1.01x faster                                                  |
| genshi_xml      | 51.6 ms                                                    | 52.1 ms: 1.01x slower                                                  |
| django_template | 34.8 ms                                                    | 35.8 ms: 1.03x slower                                                  |
| Geometric mean  | (ref)                                                      | 1.00x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 |
|----------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 115 us: 1.43x faster                                                   |
| mdp                        | 2.79 sec                                                   | 2.60 sec: 1.07x faster                                                 |
| unpickle_list              | 5.34 us                                                    | 4.99 us: 1.07x faster                                                  |
| async_tree_none            | 378 ms                                                     | 354 ms: 1.07x faster                                                   |
| richards_super             | 57.4 ms                                                    | 53.7 ms: 1.07x faster                                                  |
| richards                   | 50.9 ms                                                    | 47.9 ms: 1.06x faster                                                  |
| scimark_fft                | 392 ms                                                     | 369 ms: 1.06x faster                                                   |
| deepcopy_memo              | 39.7 us                                                    | 37.7 us: 1.05x faster                                                  |
| json_loads                 | 28.9 us                                                    | 27.6 us: 1.05x faster                                                  |
| scimark_lu                 | 122 ms                                                     | 117 ms: 1.04x faster                                                   |
| chameleon                  | 7.22 ms                                                    | 6.94 ms: 1.04x faster                                                  |
| scimark_sor                | 127 ms                                                     | 123 ms: 1.04x faster                                                   |
| create_gc_cycles           | 1.82 ms                                                    | 1.75 ms: 1.04x faster                                                  |
| deepcopy_reduce            | 3.35 us                                                    | 3.23 us: 1.04x faster                                                  |
| deepcopy                   | 367 us                                                     | 356 us: 1.03x faster                                                   |
| json                       | 5.31 ms                                                    | 5.15 ms: 1.03x faster                                                  |
| spectral_norm              | 116 ms                                                     | 113 ms: 1.03x faster                                                   |
| fannkuch                   | 402 ms                                                     | 391 ms: 1.03x faster                                                   |
| gc_traversal               | 3.98 ms                                                    | 3.87 ms: 1.03x faster                                                  |
| pyflate                    | 484 ms                                                     | 471 ms: 1.03x faster                                                   |
| sqlglot_transpile          | 1.63 ms                                                    | 1.60 ms: 1.02x faster                                                  |
| pickle_pure_python         | 305 us                                                     | 299 us: 1.02x faster                                                   |
| python_startup             | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                  |
| sqlglot_parse              | 1.32 ms                                                    | 1.29 ms: 1.02x faster                                                  |
| json_dumps                 | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                                  |
| coroutines                 | 23.2 ms                                                    | 22.7 ms: 1.02x faster                                                  |
| sqlite_synth               | 2.99 us                                                    | 2.93 us: 1.02x faster                                                  |
| chaos                      | 61.3 ms                                                    | 60.2 ms: 1.02x faster                                                  |
| crypto_pyaes               | 77.5 ms                                                    | 76.3 ms: 1.02x faster                                                  |
| mako                       | 11.2 ms                                                    | 11.1 ms: 1.02x faster                                                  |
| regex_dna                  | 221 ms                                                     | 218 ms: 1.01x faster                                                   |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 5.20 ms: 1.01x faster                                                  |
| pprint_pformat             | 1.56 sec                                                   | 1.53 sec: 1.01x faster                                                 |
| 2to3                       | 274 ms                                                     | 270 ms: 1.01x faster                                                   |
| scimark_monte_carlo        | 69.2 ms                                                    | 68.4 ms: 1.01x faster                                                  |
| logging_format             | 6.47 us                                                    | 6.40 us: 1.01x faster                                                  |
| dulwich_log                | 67.2 ms                                                    | 66.4 ms: 1.01x faster                                                  |
| genshi_text                | 23.7 ms                                                    | 23.4 ms: 1.01x faster                                                  |
| raytrace                   | 267 ms                                                     | 264 ms: 1.01x faster                                                   |
| regex_compile              | 137 ms                                                     | 136 ms: 1.01x faster                                                   |
| aiohttp                    | 1.18 ms                                                    | 1.17 ms: 1.01x faster                                                  |
| tornado_http               | 94.6 ms                                                    | 93.9 ms: 1.01x faster                                                  |
| sympy_integrate            | 20.5 ms                                                    | 20.3 ms: 1.01x faster                                                  |
| gunicorn                   | 1.28 ms                                                    | 1.27 ms: 1.01x faster                                                  |
| xml_etree_process          | 61.2 ms                                                    | 60.8 ms: 1.01x faster                                                  |
| pprint_safe_repr           | 758 ms                                                     | 754 ms: 1.01x faster                                                   |
| asyncio_websockets         | 567 ms                                                     | 563 ms: 1.01x faster                                                   |
| unpickle_pure_python       | 218 us                                                     | 217 us: 1.00x faster                                                   |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.85 sec: 1.00x slower                                                 |
| nqueens                    | 81.4 ms                                                    | 81.7 ms: 1.00x slower                                                  |
| sympy_expand               | 473 ms                                                     | 475 ms: 1.00x slower                                                   |
| sympy_sum                  | 156 ms                                                     | 157 ms: 1.00x slower                                                   |
| unpickle                   | 15.1 us                                                    | 15.2 us: 1.01x slower                                                  |
| async_generators           | 442 ms                                                     | 445 ms: 1.01x slower                                                   |
| pathlib                    | 17.3 ms                                                    | 17.5 ms: 1.01x slower                                                  |
| bench_thread_pool          | 834 us                                                     | 841 us: 1.01x slower                                                   |
| logging_simple             | 5.74 us                                                    | 5.80 us: 1.01x slower                                                  |
| genshi_xml                 | 51.6 ms                                                    | 52.1 ms: 1.01x slower                                                  |
| regex_v8                   | 25.1 ms                                                    | 25.4 ms: 1.01x slower                                                  |
| meteor_contest             | 110 ms                                                     | 111 ms: 1.01x slower                                                   |
| sqlglot_normalize          | 110 ms                                                     | 112 ms: 1.01x slower                                                   |
| xml_etree_generate         | 87.4 ms                                                    | 88.8 ms: 1.02x slower                                                  |
| telco                      | 8.41 ms                                                    | 8.55 ms: 1.02x slower                                                  |
| comprehensions             | 16.6 us                                                    | 16.9 us: 1.02x slower                                                  |
| regex_effbot               | 3.67 ms                                                    | 3.74 ms: 1.02x slower                                                  |
| nbody                      | 88.3 ms                                                    | 90.0 ms: 1.02x slower                                                  |
| hexiom                     | 6.30 ms                                                    | 6.43 ms: 1.02x slower                                                  |
| tomli_loads                | 2.12 sec                                                   | 2.17 sec: 1.02x slower                                                 |
| pickle                     | 11.5 us                                                    | 11.8 us: 1.03x slower                                                  |
| django_template            | 34.8 ms                                                    | 35.8 ms: 1.03x slower                                                  |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 607 ms: 1.03x slower                                                   |
| generators                 | 29.6 ms                                                    | 30.9 ms: 1.04x slower                                                  |
| pickle_list                | 5.11 us                                                    | 5.33 us: 1.04x slower                                                  |
| coverage                   | 93.1 ms                                                    | 98.6 ms: 1.06x slower                                                  |
| pidigits                   | 191 ms                                                     | 206 ms: 1.08x slower                                                   |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                           |

Benchmark hidden because not significant (26): xml_etree_parse, pycparser, logging_silent, mypy2, thrift, async_tree_io, go, sympy_str, float, asyncio_tcp, async_tree_io_tg, async_tree_cpu_io_mixed, xml_etree_iterparse, python_startup_no_site, bench_mp_pool, sqlglot_optimize, docutils, djangocms, async_tree_memoization, html5lib, async_tree_memoization_tg, deltablue, async_tree_none_tg, dask, pylint, pickle_dict
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 91.63% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.98x