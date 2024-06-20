# Results vs. 3.13.0b2

- fork: gvanrossum
- ref: exp_backoff
- machine: linux-x86_64
- commit hash: dcee362
- commit date: 2024-04-03
- overall geometric mean: 1.01x faster
- HPT reliability: 99.65%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 270 ms: 1.01x faster                                              |
| chameleon      | 7.22 ms                                                    | 6.92 ms: 1.04x faster                                             |
| html5lib       | 67.2 ms                                                    | 68.2 ms: 1.02x slower                                             |
| tornado_http   | 94.6 ms                                                    | 94.2 ms: 1.00x faster                                             |
| Geometric mean | (ref)                                                      | 1.01x faster                                                      |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 350 ms: 1.08x faster                                              |
| async_tree_io              | 939 ms                                                     | 913 ms: 1.03x faster                                              |
| async_tree_none_tg         | 336 ms                                                     | 330 ms: 1.02x faster                                              |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 601 ms: 1.02x slower                                              |
| Geometric mean             | (ref)                                                      | 1.02x faster                                                      |

Benchmark hidden because not significant (4): async_tree_io_tg, async_tree_memoization_tg, async_tree_memoization, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 191 ms                                                     | 194 ms: 1.01x slower                                              |
| nbody          | 88.3 ms                                                    | 90.1 ms: 1.02x slower                                             |
| Geometric mean | (ref)                                                      | 1.01x slower                                                      |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_compile  | 137 ms                                                     | 135 ms: 1.01x faster                                              |
| regex_effbot   | 3.67 ms                                                    | 3.72 ms: 1.01x slower                                             |
| regex_dna      | 221 ms                                                     | 224 ms: 1.01x slower                                              |
| regex_v8       | 25.1 ms                                                    | 25.5 ms: 1.01x slower                                             |
| Geometric mean | (ref)                                                      | 1.01x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| pickle_list          | 5.11 us                                                    | 4.79 us: 1.07x faster                                             |
| unpickle_list        | 5.34 us                                                    | 5.02 us: 1.06x faster                                             |
| pickle_dict          | 34.8 us                                                    | 32.9 us: 1.06x faster                                             |
| json_dumps           | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                             |
| json_loads           | 28.9 us                                                    | 28.5 us: 1.02x faster                                             |
| xml_etree_process    | 61.2 ms                                                    | 60.4 ms: 1.01x faster                                             |
| unpickle             | 15.1 us                                                    | 14.9 us: 1.01x faster                                             |
| pickle_pure_python   | 305 us                                                     | 303 us: 1.01x faster                                              |
| xml_etree_generate   | 87.4 ms                                                    | 87.9 ms: 1.01x slower                                             |
| pickle               | 11.5 us                                                    | 11.6 us: 1.01x slower                                             |
| tomli_loads          | 2.12 sec                                                   | 2.16 sec: 1.02x slower                                            |
| unpickle_pure_python | 218 us                                                     | 226 us: 1.04x slower                                              |
| Geometric mean       | (ref)                                                      | 1.01x faster                                                      |

Benchmark hidden because not significant (2): xml_etree_parse, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                             |
| python_startup_no_site | 7.11 ms                                                    | 8.98 ms: 1.26x slower                                             |
| Geometric mean         | (ref)                                                      | 1.11x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| mako           | 11.2 ms                                                    | 10.7 ms: 1.05x faster                                             |
| genshi_xml     | 51.6 ms                                                    | 52.1 ms: 1.01x slower                                             |
| genshi_text    | 23.7 ms                                                    | 24.0 ms: 1.01x slower                                             |
| Geometric mean | (ref)                                                      | 1.01x faster                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 114 us: 1.45x faster                                              |
| pylint                     | 317 ms                                                     | 281 ms: 1.13x faster                                              |
| richards                   | 50.9 ms                                                    | 47.0 ms: 1.08x faster                                             |
| async_tree_none            | 378 ms                                                     | 350 ms: 1.08x faster                                              |
| richards_super             | 57.4 ms                                                    | 53.1 ms: 1.08x faster                                             |
| pickle_list                | 5.11 us                                                    | 4.79 us: 1.07x faster                                             |
| scimark_lu                 | 122 ms                                                     | 114 ms: 1.07x faster                                              |
| unpickle_list              | 5.34 us                                                    | 5.02 us: 1.06x faster                                             |
| pickle_dict                | 34.8 us                                                    | 32.9 us: 1.06x faster                                             |
| mdp                        | 2.79 sec                                                   | 2.65 sec: 1.05x faster                                            |
| create_gc_cycles           | 1.82 ms                                                    | 1.73 ms: 1.05x faster                                             |
| logging_silent             | 105 ns                                                     | 99.5 ns: 1.05x faster                                             |
| scimark_fft                | 392 ms                                                     | 374 ms: 1.05x faster                                              |
| mako                       | 11.2 ms                                                    | 10.7 ms: 1.05x faster                                             |
| deepcopy_memo              | 39.7 us                                                    | 37.9 us: 1.05x faster                                             |
| chameleon                  | 7.22 ms                                                    | 6.92 ms: 1.04x faster                                             |
| coroutines                 | 23.2 ms                                                    | 22.2 ms: 1.04x faster                                             |
| pyflate                    | 484 ms                                                     | 465 ms: 1.04x faster                                              |
| deepcopy_reduce            | 3.35 us                                                    | 3.22 us: 1.04x faster                                             |
| scimark_sor                | 127 ms                                                     | 123 ms: 1.04x faster                                              |
| spectral_norm              | 116 ms                                                     | 112 ms: 1.03x faster                                              |
| async_tree_io              | 939 ms                                                     | 913 ms: 1.03x faster                                              |
| sqlglot_transpile          | 1.63 ms                                                    | 1.60 ms: 1.02x faster                                             |
| deepcopy                   | 367 us                                                     | 359 us: 1.02x faster                                              |
| thrift                     | 823 us                                                     | 804 us: 1.02x faster                                              |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 5.15 ms: 1.02x faster                                             |
| sqlglot_parse              | 1.32 ms                                                    | 1.29 ms: 1.02x faster                                             |
| go                         | 145 ms                                                     | 142 ms: 1.02x faster                                              |
| python_startup             | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                             |
| json_dumps                 | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                             |
| async_tree_none_tg         | 336 ms                                                     | 330 ms: 1.02x faster                                              |
| logging_format             | 6.47 us                                                    | 6.36 us: 1.02x faster                                             |
| deltablue                  | 3.25 ms                                                    | 3.20 ms: 1.02x faster                                             |
| pprint_pformat             | 1.56 sec                                                   | 1.53 sec: 1.02x faster                                            |
| crypto_pyaes               | 77.5 ms                                                    | 76.3 ms: 1.02x faster                                             |
| json_loads                 | 28.9 us                                                    | 28.5 us: 1.02x faster                                             |
| aiohttp                    | 1.18 ms                                                    | 1.16 ms: 1.02x faster                                             |
| gunicorn                   | 1.28 ms                                                    | 1.26 ms: 1.02x faster                                             |
| fannkuch                   | 402 ms                                                     | 396 ms: 1.01x faster                                              |
| 2to3                       | 274 ms                                                     | 270 ms: 1.01x faster                                              |
| xml_etree_process          | 61.2 ms                                                    | 60.4 ms: 1.01x faster                                             |
| unpickle                   | 15.1 us                                                    | 14.9 us: 1.01x faster                                             |
| sqlite_synth               | 2.99 us                                                    | 2.95 us: 1.01x faster                                             |
| regex_compile              | 137 ms                                                     | 135 ms: 1.01x faster                                              |
| sympy_str                  | 282 ms                                                     | 279 ms: 1.01x faster                                              |
| pprint_safe_repr           | 758 ms                                                     | 751 ms: 1.01x faster                                              |
| pickle_pure_python         | 305 us                                                     | 303 us: 1.01x faster                                              |
| raytrace                   | 267 ms                                                     | 264 ms: 1.01x faster                                              |
| comprehensions             | 16.6 us                                                    | 16.5 us: 1.01x faster                                             |
| chaos                      | 61.3 ms                                                    | 60.9 ms: 1.01x faster                                             |
| sympy_expand               | 473 ms                                                     | 470 ms: 1.01x faster                                              |
| sqlglot_optimize           | 55.5 ms                                                    | 55.2 ms: 1.01x faster                                             |
| tornado_http               | 94.6 ms                                                    | 94.2 ms: 1.00x faster                                             |
| asyncio_tcp                | 508 ms                                                     | 506 ms: 1.00x faster                                              |
| sympy_integrate            | 20.5 ms                                                    | 20.4 ms: 1.00x faster                                             |
| scimark_monte_carlo        | 69.2 ms                                                    | 68.9 ms: 1.00x faster                                             |
| hexiom                     | 6.30 ms                                                    | 6.28 ms: 1.00x faster                                             |
| xml_etree_generate         | 87.4 ms                                                    | 87.9 ms: 1.01x slower                                             |
| async_generators           | 442 ms                                                     | 445 ms: 1.01x slower                                              |
| genshi_xml                 | 51.6 ms                                                    | 52.1 ms: 1.01x slower                                             |
| regex_effbot               | 3.67 ms                                                    | 3.72 ms: 1.01x slower                                             |
| generators                 | 29.6 ms                                                    | 30.0 ms: 1.01x slower                                             |
| pickle                     | 11.5 us                                                    | 11.6 us: 1.01x slower                                             |
| regex_dna                  | 221 ms                                                     | 224 ms: 1.01x slower                                              |
| pidigits                   | 191 ms                                                     | 194 ms: 1.01x slower                                              |
| regex_v8                   | 25.1 ms                                                    | 25.5 ms: 1.01x slower                                             |
| genshi_text                | 23.7 ms                                                    | 24.0 ms: 1.01x slower                                             |
| html5lib                   | 67.2 ms                                                    | 68.2 ms: 1.02x slower                                             |
| json                       | 5.31 ms                                                    | 5.39 ms: 1.02x slower                                             |
| tomli_loads                | 2.12 sec                                                   | 2.16 sec: 1.02x slower                                            |
| nbody                      | 88.3 ms                                                    | 90.1 ms: 1.02x slower                                             |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 601 ms: 1.02x slower                                              |
| nqueens                    | 81.4 ms                                                    | 83.5 ms: 1.03x slower                                             |
| telco                      | 8.41 ms                                                    | 8.65 ms: 1.03x slower                                             |
| coverage                   | 93.1 ms                                                    | 96.2 ms: 1.03x slower                                             |
| unpickle_pure_python       | 218 us                                                     | 226 us: 1.04x slower                                              |
| pathlib                    | 17.3 ms                                                    | 19.1 ms: 1.10x slower                                             |
| python_startup_no_site     | 7.11 ms                                                    | 8.98 ms: 1.26x slower                                             |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                      |

Benchmark hidden because not significant (21): async_tree_io_tg, async_tree_memoization_tg, xml_etree_parse, mypy2, async_tree_memoization, async_tree_cpu_io_mixed, docutils, meteor_contest, dask, xml_etree_iterparse, gc_traversal, bench_thread_pool, asyncio_websockets, sympy_sum, asyncio_tcp_ssl, sqlglot_normalize, dulwich_log, bench_mp_pool, pycparser, logging_simple, float
Ignored benchmarks (4) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, django_template, djangocms, flaskblogging

# HPT report

- Reliability score: 99.65% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.98x