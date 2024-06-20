# Results vs. 3.13.0b2

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: linux-x86_64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.00x faster
- HPT reliability: 95.93%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.06x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 277 ms: 1.01x slower                                                   |
| chameleon      | 7.22 ms                                                    | 7.09 ms: 1.02x faster                                                  |
| docutils       | 2.83 sec                                                   | 2.89 sec: 1.02x slower                                                 |
| html5lib       | 67.2 ms                                                    | 66.5 ms: 1.01x faster                                                  |
| tornado_http   | 94.6 ms                                                    | 94.9 ms: 1.00x slower                                                  |
| Geometric mean | (ref)                                                      | 1.00x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 356 ms: 1.06x faster                                                   |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 602 ms: 1.02x slower                                                   |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                           |

Benchmark hidden because not significant (6): async_tree_io, async_tree_memoization, async_tree_memoization_tg, async_tree_cpu_io_mixed, async_tree_none_tg, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 78.9 ms                                                    | 76.6 ms: 1.03x faster                                                  |
| pidigits       | 191 ms                                                     | 189 ms: 1.01x faster                                                   |
| nbody          | 88.3 ms                                                    | 94.3 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                      | 1.01x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 137 ms                                                     | 140 ms: 1.02x slower                                                   |
| regex_dna      | 221 ms                                                     | 228 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                      | 1.01x slower                                                           |

Benchmark hidden because not significant (2): regex_effbot, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 162 ms                                                     | 152 ms: 1.07x faster                                                   |
| json_loads           | 28.9 us                                                    | 27.7 us: 1.04x faster                                                  |
| xml_etree_iterparse  | 107 ms                                                     | 104 ms: 1.03x faster                                                   |
| tomli_loads          | 2.12 sec                                                   | 2.07 sec: 1.03x faster                                                 |
| xml_etree_process    | 61.2 ms                                                    | 59.8 ms: 1.02x faster                                                  |
| pickle_list          | 5.11 us                                                    | 5.00 us: 1.02x faster                                                  |
| json_dumps           | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                                  |
| xml_etree_generate   | 87.4 ms                                                    | 86.7 ms: 1.01x faster                                                  |
| pickle_pure_python   | 305 us                                                     | 304 us: 1.01x faster                                                   |
| pickle_dict          | 34.8 us                                                    | 35.1 us: 1.01x slower                                                  |
| pickle               | 11.5 us                                                    | 11.7 us: 1.02x slower                                                  |
| unpickle_pure_python | 218 us                                                     | 233 us: 1.07x slower                                                   |
| unpickle             | 15.1 us                                                    | 16.2 us: 1.07x slower                                                  |
| Geometric mean       | (ref)                                                      | 1.01x faster                                                           |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 11.0 ms: 1.02x slower                                                  |
| python_startup_no_site | 7.11 ms                                                    | 7.57 ms: 1.07x slower                                                  |
| Geometric mean         | (ref)                                                      | 1.04x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 10.7 ms: 1.05x faster                                                  |
| genshi_text     | 23.7 ms                                                    | 24.3 ms: 1.03x slower                                                  |
| genshi_xml      | 51.6 ms                                                    | 53.8 ms: 1.04x slower                                                  |
| django_template | 34.8 ms                                                    | 36.7 ms: 1.06x slower                                                  |
| Geometric mean  | (ref)                                                      | 1.02x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 113 us: 1.46x faster                                                   |
| richards                   | 50.9 ms                                                    | 42.6 ms: 1.20x faster                                                  |
| richards_super             | 57.4 ms                                                    | 48.8 ms: 1.18x faster                                                  |
| scimark_fft                | 392 ms                                                     | 339 ms: 1.16x faster                                                   |
| gc_traversal               | 3.98 ms                                                    | 3.57 ms: 1.11x faster                                                  |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 4.78 ms: 1.10x faster                                                  |
| xml_etree_parse            | 162 ms                                                     | 152 ms: 1.07x faster                                                   |
| async_tree_none            | 378 ms                                                     | 356 ms: 1.06x faster                                                   |
| deepcopy_reduce            | 3.35 us                                                    | 3.19 us: 1.05x faster                                                  |
| mako                       | 11.2 ms                                                    | 10.7 ms: 1.05x faster                                                  |
| json_loads                 | 28.9 us                                                    | 27.7 us: 1.04x faster                                                  |
| crypto_pyaes               | 77.5 ms                                                    | 74.4 ms: 1.04x faster                                                  |
| fannkuch                   | 402 ms                                                     | 388 ms: 1.04x faster                                                   |
| spectral_norm              | 116 ms                                                     | 112 ms: 1.03x faster                                                   |
| json                       | 5.31 ms                                                    | 5.13 ms: 1.03x faster                                                  |
| deepcopy_memo              | 39.7 us                                                    | 38.5 us: 1.03x faster                                                  |
| create_gc_cycles           | 1.82 ms                                                    | 1.76 ms: 1.03x faster                                                  |
| xml_etree_iterparse        | 107 ms                                                     | 104 ms: 1.03x faster                                                   |
| float                      | 78.9 ms                                                    | 76.6 ms: 1.03x faster                                                  |
| tomli_loads                | 2.12 sec                                                   | 2.07 sec: 1.03x faster                                                 |
| xml_etree_process          | 61.2 ms                                                    | 59.8 ms: 1.02x faster                                                  |
| deepcopy                   | 367 us                                                     | 359 us: 1.02x faster                                                   |
| sqlite_synth               | 2.99 us                                                    | 2.93 us: 1.02x faster                                                  |
| thrift                     | 823 us                                                     | 806 us: 1.02x faster                                                   |
| pickle_list                | 5.11 us                                                    | 5.00 us: 1.02x faster                                                  |
| json_dumps                 | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                                  |
| coroutines                 | 23.2 ms                                                    | 22.7 ms: 1.02x faster                                                  |
| chameleon                  | 7.22 ms                                                    | 7.09 ms: 1.02x faster                                                  |
| pyflate                    | 484 ms                                                     | 476 ms: 1.02x faster                                                   |
| pprint_pformat             | 1.56 sec                                                   | 1.54 sec: 1.01x faster                                                 |
| html5lib                   | 67.2 ms                                                    | 66.5 ms: 1.01x faster                                                  |
| pidigits                   | 191 ms                                                     | 189 ms: 1.01x faster                                                   |
| xml_etree_generate         | 87.4 ms                                                    | 86.7 ms: 1.01x faster                                                  |
| sqlglot_transpile          | 1.63 ms                                                    | 1.62 ms: 1.01x faster                                                  |
| pickle_pure_python         | 305 us                                                     | 304 us: 1.01x faster                                                   |
| sqlglot_parse              | 1.32 ms                                                    | 1.31 ms: 1.01x faster                                                  |
| tornado_http               | 94.6 ms                                                    | 94.9 ms: 1.00x slower                                                  |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.85 sec: 1.01x slower                                                 |
| bench_mp_pool              | 23.9 ms                                                    | 24.0 ms: 1.01x slower                                                  |
| meteor_contest             | 110 ms                                                     | 111 ms: 1.01x slower                                                   |
| pickle_dict                | 34.8 us                                                    | 35.1 us: 1.01x slower                                                  |
| 2to3                       | 274 ms                                                     | 277 ms: 1.01x slower                                                   |
| pycparser                  | 1.16 sec                                                   | 1.17 sec: 1.01x slower                                                 |
| gunicorn                   | 1.28 ms                                                    | 1.29 ms: 1.01x slower                                                  |
| logging_simple             | 5.74 us                                                    | 5.82 us: 1.01x slower                                                  |
| generators                 | 29.6 ms                                                    | 30.0 ms: 1.01x slower                                                  |
| sqlglot_normalize          | 110 ms                                                     | 112 ms: 1.01x slower                                                   |
| raytrace                   | 267 ms                                                     | 270 ms: 1.01x slower                                                   |
| aiohttp                    | 1.18 ms                                                    | 1.20 ms: 1.01x slower                                                  |
| chaos                      | 61.3 ms                                                    | 62.3 ms: 1.02x slower                                                  |
| telco                      | 8.41 ms                                                    | 8.56 ms: 1.02x slower                                                  |
| python_startup             | 10.8 ms                                                    | 11.0 ms: 1.02x slower                                                  |
| mdp                        | 2.79 sec                                                   | 2.84 sec: 1.02x slower                                                 |
| docutils                   | 2.83 sec                                                   | 2.89 sec: 1.02x slower                                                 |
| pathlib                    | 17.3 ms                                                    | 17.7 ms: 1.02x slower                                                  |
| pickle                     | 11.5 us                                                    | 11.7 us: 1.02x slower                                                  |
| bench_thread_pool          | 834 us                                                     | 852 us: 1.02x slower                                                   |
| dulwich_log                | 67.2 ms                                                    | 68.7 ms: 1.02x slower                                                  |
| regex_compile              | 137 ms                                                     | 140 ms: 1.02x slower                                                   |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 602 ms: 1.02x slower                                                   |
| sqlglot_optimize           | 55.5 ms                                                    | 56.9 ms: 1.02x slower                                                  |
| scimark_sor                | 127 ms                                                     | 131 ms: 1.03x slower                                                   |
| genshi_text                | 23.7 ms                                                    | 24.3 ms: 1.03x slower                                                  |
| regex_dna                  | 221 ms                                                     | 228 ms: 1.03x slower                                                   |
| sympy_str                  | 282 ms                                                     | 292 ms: 1.04x slower                                                   |
| async_generators           | 442 ms                                                     | 458 ms: 1.04x slower                                                   |
| sympy_expand               | 473 ms                                                     | 490 ms: 1.04x slower                                                   |
| genshi_xml                 | 51.6 ms                                                    | 53.8 ms: 1.04x slower                                                  |
| coverage                   | 93.1 ms                                                    | 97.3 ms: 1.05x slower                                                  |
| mypy2                      | 742 ms                                                     | 782 ms: 1.05x slower                                                   |
| django_template            | 34.8 ms                                                    | 36.7 ms: 1.06x slower                                                  |
| go                         | 145 ms                                                     | 153 ms: 1.06x slower                                                   |
| sympy_sum                  | 156 ms                                                     | 166 ms: 1.06x slower                                                   |
| sympy_integrate            | 20.5 ms                                                    | 21.8 ms: 1.06x slower                                                  |
| python_startup_no_site     | 7.11 ms                                                    | 7.57 ms: 1.07x slower                                                  |
| unpickle_pure_python       | 218 us                                                     | 233 us: 1.07x slower                                                   |
| nbody                      | 88.3 ms                                                    | 94.3 ms: 1.07x slower                                                  |
| unpickle                   | 15.1 us                                                    | 16.2 us: 1.07x slower                                                  |
| comprehensions             | 16.6 us                                                    | 17.9 us: 1.08x slower                                                  |
| hexiom                     | 6.30 ms                                                    | 6.80 ms: 1.08x slower                                                  |
| scimark_lu                 | 122 ms                                                     | 133 ms: 1.09x slower                                                   |
| nqueens                    | 81.4 ms                                                    | 89.2 ms: 1.10x slower                                                  |
| deltablue                  | 3.25 ms                                                    | 3.61 ms: 1.11x slower                                                  |
| Geometric mean             | (ref)                                                      | 1.00x faster                                                           |

Benchmark hidden because not significant (18): async_tree_io, pprint_safe_repr, async_tree_memoization, unpickle_list, async_tree_memoization_tg, logging_format, async_tree_cpu_io_mixed, logging_silent, scimark_monte_carlo, asyncio_websockets, regex_effbot, asyncio_tcp, regex_v8, async_tree_none_tg, dask, async_tree_io_tg, djangocms, pylint
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 95.93% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.06x