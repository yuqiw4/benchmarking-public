# Results vs. 3.13.0b2

- fork: gvanrossum
- ref: exp_backoff
- machine: linux-x86_64
- commit hash: 8eee1b4
- commit date: 2024-04-02
- overall geometric mean: 1.01x slower
- HPT reliability: 99.29%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.06x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 279 ms: 1.02x slower                                              |
| chameleon      | 7.22 ms                                                    | 6.88 ms: 1.05x faster                                             |
| docutils       | 2.83 sec                                                   | 2.91 sec: 1.03x slower                                            |
| html5lib       | 67.2 ms                                                    | 65.7 ms: 1.02x faster                                             |
| tornado_http   | 94.6 ms                                                    | 95.7 ms: 1.01x slower                                             |
| Geometric mean | (ref)                                                      | 1.00x faster                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 353 ms: 1.07x faster                                              |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 602 ms: 1.03x slower                                              |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                      |

Benchmark hidden because not significant (6): async_tree_memoization, async_tree_io, async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_memoization_tg, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| float          | 78.9 ms                                                    | 78.1 ms: 1.01x faster                                             |
| pidigits       | 191 ms                                                     | 194 ms: 1.01x slower                                              |
| nbody          | 88.3 ms                                                    | 91.9 ms: 1.04x slower                                             |
| Geometric mean | (ref)                                                      | 1.01x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 3.67 ms                                                    | 3.75 ms: 1.02x slower                                             |
| regex_v8       | 25.1 ms                                                    | 26.1 ms: 1.04x slower                                             |
| regex_dna      | 221 ms                                                     | 233 ms: 1.05x slower                                              |
| regex_compile  | 137 ms                                                     | 145 ms: 1.06x slower                                              |
| Geometric mean | (ref)                                                      | 1.04x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| tomli_loads          | 2.12 sec                                                   | 2.07 sec: 1.02x faster                                            |
| json_dumps           | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                             |
| pickle_dict          | 34.8 us                                                    | 34.1 us: 1.02x faster                                             |
| unpickle_list        | 5.34 us                                                    | 5.24 us: 1.02x faster                                             |
| json_loads           | 28.9 us                                                    | 28.6 us: 1.01x faster                                             |
| xml_etree_process    | 61.2 ms                                                    | 60.6 ms: 1.01x faster                                             |
| pickle_list          | 5.11 us                                                    | 5.06 us: 1.01x faster                                             |
| pickle_pure_python   | 305 us                                                     | 304 us: 1.01x faster                                              |
| pickle               | 11.5 us                                                    | 11.8 us: 1.02x slower                                             |
| unpickle             | 15.1 us                                                    | 15.9 us: 1.05x slower                                             |
| unpickle_pure_python | 218 us                                                     | 240 us: 1.10x slower                                              |
| Geometric mean       | (ref)                                                      | 1.00x slower                                                      |

Benchmark hidden because not significant (3): xml_etree_iterparse, xml_etree_generate, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 11.1 ms: 1.03x slower                                             |
| python_startup_no_site | 7.11 ms                                                    | 9.55 ms: 1.34x slower                                             |
| Geometric mean         | (ref)                                                      | 1.18x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| mako           | 11.2 ms                                                    | 10.9 ms: 1.04x faster                                             |
| genshi_text    | 23.7 ms                                                    | 24.2 ms: 1.02x slower                                             |
| genshi_xml     | 51.6 ms                                                    | 53.2 ms: 1.03x slower                                             |
| Geometric mean | (ref)                                                      | 1.01x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 113 us: 1.45x faster                                              |
| scimark_fft                | 392 ms                                                     | 338 ms: 1.16x faster                                              |
| richards                   | 50.9 ms                                                    | 46.7 ms: 1.09x faster                                             |
| richards_super             | 57.4 ms                                                    | 53.1 ms: 1.08x faster                                             |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 4.89 ms: 1.08x faster                                             |
| async_tree_none            | 378 ms                                                     | 353 ms: 1.07x faster                                              |
| pylint                     | 317 ms                                                     | 298 ms: 1.07x faster                                              |
| chameleon                  | 7.22 ms                                                    | 6.88 ms: 1.05x faster                                             |
| gc_traversal               | 3.98 ms                                                    | 3.79 ms: 1.05x faster                                             |
| coroutines                 | 23.2 ms                                                    | 22.1 ms: 1.05x faster                                             |
| deepcopy_memo              | 39.7 us                                                    | 38.0 us: 1.04x faster                                             |
| deepcopy                   | 367 us                                                     | 353 us: 1.04x faster                                              |
| create_gc_cycles           | 1.82 ms                                                    | 1.75 ms: 1.04x faster                                             |
| mako                       | 11.2 ms                                                    | 10.9 ms: 1.04x faster                                             |
| sqlite_synth               | 2.99 us                                                    | 2.89 us: 1.03x faster                                             |
| mdp                        | 2.79 sec                                                   | 2.70 sec: 1.03x faster                                            |
| deepcopy_reduce            | 3.35 us                                                    | 3.24 us: 1.03x faster                                             |
| logging_silent             | 105 ns                                                     | 101 ns: 1.03x faster                                              |
| crypto_pyaes               | 77.5 ms                                                    | 75.4 ms: 1.03x faster                                             |
| tomli_loads                | 2.12 sec                                                   | 2.07 sec: 1.02x faster                                            |
| spectral_norm              | 116 ms                                                     | 113 ms: 1.02x faster                                              |
| html5lib                   | 67.2 ms                                                    | 65.7 ms: 1.02x faster                                             |
| json_dumps                 | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                             |
| pickle_dict                | 34.8 us                                                    | 34.1 us: 1.02x faster                                             |
| unpickle_list              | 5.34 us                                                    | 5.24 us: 1.02x faster                                             |
| pprint_safe_repr           | 758 ms                                                     | 745 ms: 1.02x faster                                              |
| json_loads                 | 28.9 us                                                    | 28.6 us: 1.01x faster                                             |
| xml_etree_process          | 61.2 ms                                                    | 60.6 ms: 1.01x faster                                             |
| float                      | 78.9 ms                                                    | 78.1 ms: 1.01x faster                                             |
| pickle_list                | 5.11 us                                                    | 5.06 us: 1.01x faster                                             |
| fannkuch                   | 402 ms                                                     | 399 ms: 1.01x faster                                              |
| scimark_monte_carlo        | 69.2 ms                                                    | 68.7 ms: 1.01x faster                                             |
| pyflate                    | 484 ms                                                     | 481 ms: 1.01x faster                                              |
| pickle_pure_python         | 305 us                                                     | 304 us: 1.01x faster                                              |
| asyncio_websockets         | 567 ms                                                     | 564 ms: 1.00x faster                                              |
| thrift                     | 823 us                                                     | 827 us: 1.00x slower                                              |
| chaos                      | 61.3 ms                                                    | 61.7 ms: 1.01x slower                                             |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.86 sec: 1.01x slower                                            |
| asyncio_tcp                | 508 ms                                                     | 513 ms: 1.01x slower                                              |
| tornado_http               | 94.6 ms                                                    | 95.7 ms: 1.01x slower                                             |
| pidigits                   | 191 ms                                                     | 194 ms: 1.01x slower                                              |
| gunicorn                   | 1.28 ms                                                    | 1.30 ms: 1.01x slower                                             |
| json                       | 5.31 ms                                                    | 5.39 ms: 1.02x slower                                             |
| 2to3                       | 274 ms                                                     | 279 ms: 1.02x slower                                              |
| logging_format             | 6.47 us                                                    | 6.59 us: 1.02x slower                                             |
| dask                       | 369 ms                                                     | 377 ms: 1.02x slower                                              |
| meteor_contest             | 110 ms                                                     | 112 ms: 1.02x slower                                              |
| regex_effbot               | 3.67 ms                                                    | 3.75 ms: 1.02x slower                                             |
| genshi_text                | 23.7 ms                                                    | 24.2 ms: 1.02x slower                                             |
| sqlglot_normalize          | 110 ms                                                     | 113 ms: 1.02x slower                                              |
| aiohttp                    | 1.18 ms                                                    | 1.21 ms: 1.02x slower                                             |
| scimark_sor                | 127 ms                                                     | 130 ms: 1.02x slower                                              |
| bench_thread_pool          | 834 us                                                     | 854 us: 1.02x slower                                              |
| pickle                     | 11.5 us                                                    | 11.8 us: 1.02x slower                                             |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 602 ms: 1.03x slower                                              |
| telco                      | 8.41 ms                                                    | 8.65 ms: 1.03x slower                                             |
| docutils                   | 2.83 sec                                                   | 2.91 sec: 1.03x slower                                            |
| genshi_xml                 | 51.6 ms                                                    | 53.2 ms: 1.03x slower                                             |
| python_startup             | 10.8 ms                                                    | 11.1 ms: 1.03x slower                                             |
| go                         | 145 ms                                                     | 150 ms: 1.04x slower                                              |
| sqlglot_optimize           | 55.5 ms                                                    | 57.6 ms: 1.04x slower                                             |
| regex_v8                   | 25.1 ms                                                    | 26.1 ms: 1.04x slower                                             |
| async_generators           | 442 ms                                                     | 459 ms: 1.04x slower                                              |
| nbody                      | 88.3 ms                                                    | 91.9 ms: 1.04x slower                                             |
| raytrace                   | 267 ms                                                     | 278 ms: 1.04x slower                                              |
| sympy_str                  | 282 ms                                                     | 295 ms: 1.05x slower                                              |
| pycparser                  | 1.16 sec                                                   | 1.21 sec: 1.05x slower                                            |
| sympy_expand               | 473 ms                                                     | 496 ms: 1.05x slower                                              |
| regex_dna                  | 221 ms                                                     | 233 ms: 1.05x slower                                              |
| unpickle                   | 15.1 us                                                    | 15.9 us: 1.05x slower                                             |
| logging_simple             | 5.74 us                                                    | 6.08 us: 1.06x slower                                             |
| regex_compile              | 137 ms                                                     | 145 ms: 1.06x slower                                              |
| dulwich_log                | 67.2 ms                                                    | 71.3 ms: 1.06x slower                                             |
| mypy2                      | 742 ms                                                     | 788 ms: 1.06x slower                                              |
| sympy_integrate            | 20.5 ms                                                    | 21.9 ms: 1.07x slower                                             |
| comprehensions             | 16.6 us                                                    | 17.8 us: 1.07x slower                                             |
| sympy_sum                  | 156 ms                                                     | 168 ms: 1.08x slower                                              |
| scimark_lu                 | 122 ms                                                     | 131 ms: 1.08x slower                                              |
| coverage                   | 93.1 ms                                                    | 101 ms: 1.08x slower                                              |
| nqueens                    | 81.4 ms                                                    | 89.0 ms: 1.09x slower                                             |
| pathlib                    | 17.3 ms                                                    | 19.1 ms: 1.10x slower                                             |
| unpickle_pure_python       | 218 us                                                     | 240 us: 1.10x slower                                              |
| hexiom                     | 6.30 ms                                                    | 6.93 ms: 1.10x slower                                             |
| deltablue                  | 3.25 ms                                                    | 3.76 ms: 1.16x slower                                             |
| python_startup_no_site     | 7.11 ms                                                    | 9.55 ms: 1.34x slower                                             |
| Geometric mean             | (ref)                                                      | 1.01x slower                                                      |

Benchmark hidden because not significant (14): async_tree_memoization, pprint_pformat, async_tree_io, async_tree_none_tg, async_tree_cpu_io_mixed, xml_etree_iterparse, sqlglot_transpile, xml_etree_generate, sqlglot_parse, async_tree_memoization_tg, generators, xml_etree_parse, bench_mp_pool, async_tree_io_tg
Ignored benchmarks (4) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, django_template, djangocms, flaskblogging
Ignored benchmarks (1) of results/bm-20240402-3.13.0a5+-8eee1b4-JIT/bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4.json: unpack_sequence

# HPT report

- Reliability score: 99.29% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.06x