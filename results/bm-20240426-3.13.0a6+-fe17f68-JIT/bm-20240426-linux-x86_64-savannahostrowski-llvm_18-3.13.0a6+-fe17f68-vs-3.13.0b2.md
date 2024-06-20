# Results vs. 3.13.0b2

- fork: savannahostrowski
- ref: llvm_18
- machine: linux-x86_64
- commit hash: fe17f68
- commit date: 2024-04-26
- overall geometric mean: 1.01x slower
- HPT reliability: 99.70%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.07x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 280 ms: 1.02x slower                                                 |
| chameleon      | 7.22 ms                                                    | 7.16 ms: 1.01x faster                                                |
| docutils       | 2.83 sec                                                   | 2.95 sec: 1.04x slower                                               |
| html5lib       | 67.2 ms                                                    | 68.5 ms: 1.02x slower                                                |
| tornado_http   | 94.6 ms                                                    | 96.2 ms: 1.02x slower                                                |
| Geometric mean | (ref)                                                      | 1.02x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 359 ms: 1.05x faster                                                 |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 612 ms: 1.04x slower                                                 |
| Geometric mean             | (ref)                                                      | 1.01x slower                                                         |

Benchmark hidden because not significant (6): async_tree_io, async_tree_memoization_tg, async_tree_memoization, async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 78.9 ms                                                    | 76.5 ms: 1.03x faster                                                |
| nbody          | 88.3 ms                                                    | 90.9 ms: 1.03x slower                                                |
| pidigits       | 191 ms                                                     | 210 ms: 1.10x slower                                                 |
| Geometric mean | (ref)                                                      | 1.03x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.67 ms                                                    | 3.62 ms: 1.01x faster                                                |
| regex_v8       | 25.1 ms                                                    | 25.2 ms: 1.00x slower                                                |
| regex_dna      | 221 ms                                                     | 223 ms: 1.01x slower                                                 |
| regex_compile  | 137 ms                                                     | 140 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                      | 1.01x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|----------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_parse      | 162 ms                                                     | 151 ms: 1.07x faster                                                 |
| tomli_loads          | 2.12 sec                                                   | 2.03 sec: 1.05x faster                                               |
| json_loads           | 28.9 us                                                    | 27.6 us: 1.05x faster                                                |
| xml_etree_iterparse  | 107 ms                                                     | 103 ms: 1.04x faster                                                 |
| pickle_list          | 5.11 us                                                    | 5.02 us: 1.02x faster                                                |
| json_dumps           | 10.7 ms                                                    | 10.6 ms: 1.02x faster                                                |
| xml_etree_process    | 61.2 ms                                                    | 60.3 ms: 1.01x faster                                                |
| unpickle_list        | 5.34 us                                                    | 5.27 us: 1.01x faster                                                |
| pickle_pure_python   | 305 us                                                     | 306 us: 1.00x slower                                                 |
| pickle_dict          | 34.8 us                                                    | 35.0 us: 1.01x slower                                                |
| pickle               | 11.5 us                                                    | 11.9 us: 1.04x slower                                                |
| unpickle_pure_python | 218 us                                                     | 231 us: 1.06x slower                                                 |
| unpickle             | 15.1 us                                                    | 16.4 us: 1.09x slower                                                |
| Geometric mean       | (ref)                                                      | 1.01x faster                                                         |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 11.1 ms: 1.03x slower                                                |
| python_startup_no_site | 7.11 ms                                                    | 7.63 ms: 1.07x slower                                                |
| Geometric mean         | (ref)                                                      | 1.05x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|-----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 10.4 ms: 1.08x faster                                                |
| django_template | 34.8 ms                                                    | 36.8 ms: 1.06x slower                                                |
| genshi_text     | 23.7 ms                                                    | 25.7 ms: 1.09x slower                                                |
| genshi_xml      | 51.6 ms                                                    | 57.2 ms: 1.11x slower                                                |
| Geometric mean  | (ref)                                                      | 1.04x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| richards                   | 50.9 ms                                                    | 42.4 ms: 1.20x faster                                                |
| richards_super             | 57.4 ms                                                    | 48.5 ms: 1.18x faster                                                |
| scimark_fft                | 392 ms                                                     | 338 ms: 1.16x faster                                                 |
| mako                       | 11.2 ms                                                    | 10.4 ms: 1.08x faster                                                |
| fannkuch                   | 402 ms                                                     | 372 ms: 1.08x faster                                                 |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 4.93 ms: 1.07x faster                                                |
| xml_etree_parse            | 162 ms                                                     | 151 ms: 1.07x faster                                                 |
| spectral_norm              | 116 ms                                                     | 109 ms: 1.06x faster                                                 |
| mdp                        | 2.79 sec                                                   | 2.63 sec: 1.06x faster                                               |
| async_tree_none            | 378 ms                                                     | 359 ms: 1.05x faster                                                 |
| gc_traversal               | 3.98 ms                                                    | 3.79 ms: 1.05x faster                                                |
| crypto_pyaes               | 77.5 ms                                                    | 73.9 ms: 1.05x faster                                                |
| tomli_loads                | 2.12 sec                                                   | 2.03 sec: 1.05x faster                                               |
| json_loads                 | 28.9 us                                                    | 27.6 us: 1.05x faster                                                |
| xml_etree_iterparse        | 107 ms                                                     | 103 ms: 1.04x faster                                                 |
| deepcopy_reduce            | 3.35 us                                                    | 3.22 us: 1.04x faster                                                |
| sqlite_synth               | 2.99 us                                                    | 2.88 us: 1.04x faster                                                |
| pyflate                    | 484 ms                                                     | 468 ms: 1.04x faster                                                 |
| logging_silent             | 105 ns                                                     | 101 ns: 1.03x faster                                                 |
| float                      | 78.9 ms                                                    | 76.5 ms: 1.03x faster                                                |
| json                       | 5.31 ms                                                    | 5.15 ms: 1.03x faster                                                |
| create_gc_cycles           | 1.82 ms                                                    | 1.77 ms: 1.03x faster                                                |
| pprint_pformat             | 1.56 sec                                                   | 1.52 sec: 1.02x faster                                               |
| deepcopy_memo              | 39.7 us                                                    | 38.9 us: 1.02x faster                                                |
| scimark_monte_carlo        | 69.2 ms                                                    | 67.8 ms: 1.02x faster                                                |
| pprint_safe_repr           | 758 ms                                                     | 744 ms: 1.02x faster                                                 |
| pickle_list                | 5.11 us                                                    | 5.02 us: 1.02x faster                                                |
| json_dumps                 | 10.7 ms                                                    | 10.6 ms: 1.02x faster                                                |
| xml_etree_process          | 61.2 ms                                                    | 60.3 ms: 1.01x faster                                                |
| regex_effbot               | 3.67 ms                                                    | 3.62 ms: 1.01x faster                                                |
| unpickle_list              | 5.34 us                                                    | 5.27 us: 1.01x faster                                                |
| chameleon                  | 7.22 ms                                                    | 7.16 ms: 1.01x faster                                                |
| asyncio_websockets         | 567 ms                                                     | 564 ms: 1.00x faster                                                 |
| pickle_pure_python         | 305 us                                                     | 306 us: 1.00x slower                                                 |
| regex_v8                   | 25.1 ms                                                    | 25.2 ms: 1.00x slower                                                |
| thrift                     | 823 us                                                     | 828 us: 1.01x slower                                                 |
| logging_format             | 6.47 us                                                    | 6.52 us: 1.01x slower                                                |
| sqlglot_transpile          | 1.63 ms                                                    | 1.65 ms: 1.01x slower                                                |
| pickle_dict                | 34.8 us                                                    | 35.0 us: 1.01x slower                                                |
| telco                      | 8.41 ms                                                    | 8.48 ms: 1.01x slower                                                |
| regex_dna                  | 221 ms                                                     | 223 ms: 1.01x slower                                                 |
| meteor_contest             | 110 ms                                                     | 111 ms: 1.01x slower                                                 |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.86 sec: 1.01x slower                                               |
| tornado_http               | 94.6 ms                                                    | 96.2 ms: 1.02x slower                                                |
| pycparser                  | 1.16 sec                                                   | 1.18 sec: 1.02x slower                                               |
| generators                 | 29.6 ms                                                    | 30.1 ms: 1.02x slower                                                |
| html5lib                   | 67.2 ms                                                    | 68.5 ms: 1.02x slower                                                |
| 2to3                       | 274 ms                                                     | 280 ms: 1.02x slower                                                 |
| pathlib                    | 17.3 ms                                                    | 17.7 ms: 1.02x slower                                                |
| dask                       | 369 ms                                                     | 377 ms: 1.02x slower                                                 |
| regex_compile              | 137 ms                                                     | 140 ms: 1.02x slower                                                 |
| gunicorn                   | 1.28 ms                                                    | 1.31 ms: 1.02x slower                                                |
| logging_simple             | 5.74 us                                                    | 5.89 us: 1.02x slower                                                |
| sqlglot_normalize          | 110 ms                                                     | 113 ms: 1.03x slower                                                 |
| python_startup             | 10.8 ms                                                    | 11.1 ms: 1.03x slower                                                |
| scimark_sor                | 127 ms                                                     | 131 ms: 1.03x slower                                                 |
| nbody                      | 88.3 ms                                                    | 90.9 ms: 1.03x slower                                                |
| djangocms                  | 31.5 us                                                    | 32.4 us: 1.03x slower                                                |
| asyncio_tcp                | 508 ms                                                     | 523 ms: 1.03x slower                                                 |
| aiohttp                    | 1.18 ms                                                    | 1.22 ms: 1.03x slower                                                |
| sqlglot_optimize           | 55.5 ms                                                    | 57.4 ms: 1.03x slower                                                |
| chaos                      | 61.3 ms                                                    | 63.5 ms: 1.03x slower                                                |
| bench_thread_pool          | 834 us                                                     | 863 us: 1.04x slower                                                 |
| pickle                     | 11.5 us                                                    | 11.9 us: 1.04x slower                                                |
| dulwich_log                | 67.2 ms                                                    | 69.8 ms: 1.04x slower                                                |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 612 ms: 1.04x slower                                                 |
| raytrace                   | 267 ms                                                     | 278 ms: 1.04x slower                                                 |
| docutils                   | 2.83 sec                                                   | 2.95 sec: 1.04x slower                                               |
| typing_runtime_protocols   | 165 us                                                     | 173 us: 1.05x slower                                                 |
| sympy_str                  | 282 ms                                                     | 297 ms: 1.05x slower                                                 |
| async_generators           | 442 ms                                                     | 465 ms: 1.05x slower                                                 |
| sympy_expand               | 473 ms                                                     | 498 ms: 1.05x slower                                                 |
| django_template            | 34.8 ms                                                    | 36.8 ms: 1.06x slower                                                |
| unpickle_pure_python       | 218 us                                                     | 231 us: 1.06x slower                                                 |
| go                         | 145 ms                                                     | 155 ms: 1.07x slower                                                 |
| python_startup_no_site     | 7.11 ms                                                    | 7.63 ms: 1.07x slower                                                |
| sympy_sum                  | 156 ms                                                     | 168 ms: 1.08x slower                                                 |
| pylint                     | 317 ms                                                     | 343 ms: 1.08x slower                                                 |
| comprehensions             | 16.6 us                                                    | 18.0 us: 1.08x slower                                                |
| genshi_text                | 23.7 ms                                                    | 25.7 ms: 1.09x slower                                                |
| unpickle                   | 15.1 us                                                    | 16.4 us: 1.09x slower                                                |
| sympy_integrate            | 20.5 ms                                                    | 22.3 ms: 1.09x slower                                                |
| mypy2                      | 742 ms                                                     | 806 ms: 1.09x slower                                                 |
| hexiom                     | 6.30 ms                                                    | 6.90 ms: 1.10x slower                                                |
| pidigits                   | 191 ms                                                     | 210 ms: 1.10x slower                                                 |
| scimark_lu                 | 122 ms                                                     | 134 ms: 1.10x slower                                                 |
| nqueens                    | 81.4 ms                                                    | 90.2 ms: 1.11x slower                                                |
| genshi_xml                 | 51.6 ms                                                    | 57.2 ms: 1.11x slower                                                |
| deltablue                  | 3.25 ms                                                    | 3.89 ms: 1.20x slower                                                |
| Geometric mean             | (ref)                                                      | 1.01x slower                                                         |

Benchmark hidden because not significant (12): coverage, async_tree_io, deepcopy, xml_etree_generate, bench_mp_pool, coroutines, sqlglot_parse, async_tree_memoization_tg, async_tree_memoization, async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_io_tg
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 99.70% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.07x