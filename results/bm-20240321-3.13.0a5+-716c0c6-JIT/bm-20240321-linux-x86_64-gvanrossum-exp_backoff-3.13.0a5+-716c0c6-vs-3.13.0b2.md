# Results vs. 3.13.0b2

- fork: gvanrossum
- ref: exp_backoff
- machine: linux-x86_64
- commit hash: 716c0c6
- commit date: 2024-03-21
- overall geometric mean: 1.27x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x slower
- Memory change: 1.08x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240321-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-716c0c6 |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 304 ms: 1.11x slower                                              |
| chameleon      | 7.22 ms                                                    | 6.98 ms: 1.03x faster                                             |
| docutils       | 2.83 sec                                                   | 4.82 sec: 1.70x slower                                            |
| html5lib       | 67.2 ms                                                    | 75.8 ms: 1.13x slower                                             |
| tornado_http   | 94.6 ms                                                    | 101 ms: 1.06x slower                                              |
| Geometric mean | (ref)                                                      | 1.17x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240321-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-716c0c6 |
|----------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 611 ms                                                     | 4.17 sec: 6.83x slower                                            |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 4.55 sec: 7.75x slower                                            |
| async_tree_none            | 378 ms                                                     | 3.39 sec: 8.95x slower                                            |
| async_tree_memoization     | 463 ms                                                     | 4.37 sec: 9.43x slower                                            |
| async_tree_memoization_tg  | 444 ms                                                     | 4.65 sec: 10.47x slower                                           |
| async_tree_none_tg         | 336 ms                                                     | 3.70 sec: 11.00x slower                                           |
| async_tree_io              | 939 ms                                                     | 13.1 sec: 13.96x slower                                           |
| async_tree_io_tg           | 936 ms                                                     | 13.9 sec: 14.85x slower                                           |
| Geometric mean             | (ref)                                                      | 10.08x slower                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240321-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-716c0c6 |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 191 ms                                                     | 190 ms: 1.01x faster                                              |
| nbody          | 88.3 ms                                                    | 94.2 ms: 1.07x slower                                             |
| float          | 78.9 ms                                                    | 143 ms: 1.81x slower                                              |
| Geometric mean | (ref)                                                      | 1.24x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240321-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-716c0c6 |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_v8       | 25.1 ms                                                    | 24.2 ms: 1.04x faster                                             |
| regex_dna      | 221 ms                                                     | 218 ms: 1.02x faster                                              |
| regex_compile  | 137 ms                                                     | 142 ms: 1.04x slower                                              |
| regex_effbot   | 3.67 ms                                                    | 3.81 ms: 1.04x slower                                             |
| Geometric mean | (ref)                                                      | 1.00x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240321-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-716c0c6 |
|----------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| pickle_list          | 5.11 us                                                    | 4.80 us: 1.06x faster                                             |
| json_loads           | 28.9 us                                                    | 27.7 us: 1.04x faster                                             |
| json_dumps           | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                             |
| unpickle_list        | 5.34 us                                                    | 5.27 us: 1.01x faster                                             |
| pickle_dict          | 34.8 us                                                    | 34.5 us: 1.01x faster                                             |
| tomli_loads          | 2.12 sec                                                   | 2.10 sec: 1.01x faster                                            |
| pickle_pure_python   | 305 us                                                     | 303 us: 1.01x faster                                              |
| pickle               | 11.5 us                                                    | 11.6 us: 1.01x slower                                             |
| unpickle             | 15.1 us                                                    | 15.5 us: 1.02x slower                                             |
| unpickle_pure_python | 218 us                                                     | 241 us: 1.10x slower                                              |
| xml_etree_process    | 61.2 ms                                                    | 68.8 ms: 1.12x slower                                             |
| xml_etree_generate   | 87.4 ms                                                    | 99.6 ms: 1.14x slower                                             |
| xml_etree_parse      | 162 ms                                                     | 216 ms: 1.33x slower                                              |
| xml_etree_iterparse  | 107 ms                                                     | 163 ms: 1.52x slower                                              |
| Geometric mean       | (ref)                                                      | 1.07x slower                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240321-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-716c0c6 |
|------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 11.8 ms: 1.10x slower                                             |
| python_startup_no_site | 7.11 ms                                                    | 10.1 ms: 1.42x slower                                             |
| Geometric mean         | (ref)                                                      | 1.25x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240321-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-716c0c6 |
|-----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 11.1 ms: 1.01x faster                                             |
| genshi_text     | 23.7 ms                                                    | 24.2 ms: 1.02x slower                                             |
| django_template | 34.8 ms                                                    | 36.0 ms: 1.03x slower                                             |
| genshi_xml      | 51.6 ms                                                    | 59.8 ms: 1.16x slower                                             |
| Geometric mean  | (ref)                                                      | 1.05x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240321-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-716c0c6 |
|----------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 111 us: 1.48x faster                                              |
| create_gc_cycles           | 1.82 ms                                                    | 1.49 ms: 1.22x faster                                             |
| scimark_fft                | 392 ms                                                     | 341 ms: 1.15x faster                                              |
| richards                   | 50.9 ms                                                    | 44.3 ms: 1.15x faster                                             |
| richards_super             | 57.4 ms                                                    | 50.0 ms: 1.15x faster                                             |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 4.79 ms: 1.10x faster                                             |
| gc_traversal               | 3.98 ms                                                    | 3.74 ms: 1.06x faster                                             |
| pickle_list                | 5.11 us                                                    | 4.80 us: 1.06x faster                                             |
| deepcopy_reduce            | 3.35 us                                                    | 3.18 us: 1.05x faster                                             |
| sqlite_synth               | 2.99 us                                                    | 2.86 us: 1.05x faster                                             |
| json_loads                 | 28.9 us                                                    | 27.7 us: 1.04x faster                                             |
| regex_v8                   | 25.1 ms                                                    | 24.2 ms: 1.04x faster                                             |
| chameleon                  | 7.22 ms                                                    | 6.98 ms: 1.03x faster                                             |
| logging_silent             | 105 ns                                                     | 102 ns: 1.03x faster                                              |
| deepcopy                   | 367 us                                                     | 358 us: 1.02x faster                                              |
| pprint_pformat             | 1.56 sec                                                   | 1.52 sec: 1.02x faster                                            |
| json_dumps                 | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                             |
| deepcopy_memo              | 39.7 us                                                    | 39.0 us: 1.02x faster                                             |
| regex_dna                  | 221 ms                                                     | 218 ms: 1.02x faster                                              |
| crypto_pyaes               | 77.5 ms                                                    | 76.3 ms: 1.02x faster                                             |
| unpickle_list              | 5.34 us                                                    | 5.27 us: 1.01x faster                                             |
| thrift                     | 823 us                                                     | 813 us: 1.01x faster                                              |
| pidigits                   | 191 ms                                                     | 190 ms: 1.01x faster                                              |
| pickle_dict                | 34.8 us                                                    | 34.5 us: 1.01x faster                                             |
| tomli_loads                | 2.12 sec                                                   | 2.10 sec: 1.01x faster                                            |
| mako                       | 11.2 ms                                                    | 11.1 ms: 1.01x faster                                             |
| coroutines                 | 23.2 ms                                                    | 23.0 ms: 1.01x faster                                             |
| pickle_pure_python         | 305 us                                                     | 303 us: 1.01x faster                                              |
| spectral_norm              | 116 ms                                                     | 115 ms: 1.01x faster                                              |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.85 sec: 1.00x slower                                            |
| asyncio_websockets         | 567 ms                                                     | 570 ms: 1.01x slower                                              |
| pickle                     | 11.5 us                                                    | 11.6 us: 1.01x slower                                             |
| meteor_contest             | 110 ms                                                     | 111 ms: 1.01x slower                                              |
| bench_mp_pool              | 23.9 ms                                                    | 24.1 ms: 1.01x slower                                             |
| fannkuch                   | 402 ms                                                     | 407 ms: 1.01x slower                                              |
| bench_thread_pool          | 834 us                                                     | 847 us: 1.02x slower                                              |
| generators                 | 29.6 ms                                                    | 30.2 ms: 1.02x slower                                             |
| pyflate                    | 484 ms                                                     | 493 ms: 1.02x slower                                              |
| logging_simple             | 5.74 us                                                    | 5.85 us: 1.02x slower                                             |
| sympy_str                  | 282 ms                                                     | 288 ms: 1.02x slower                                              |
| genshi_text                | 23.7 ms                                                    | 24.2 ms: 1.02x slower                                             |
| unpickle                   | 15.1 us                                                    | 15.5 us: 1.02x slower                                             |
| mdp                        | 2.79 sec                                                   | 2.86 sec: 1.02x slower                                            |
| dulwich_log                | 67.2 ms                                                    | 69.0 ms: 1.03x slower                                             |
| scimark_sor                | 127 ms                                                     | 131 ms: 1.03x slower                                              |
| sqlglot_normalize          | 110 ms                                                     | 114 ms: 1.03x slower                                              |
| django_template            | 34.8 ms                                                    | 36.0 ms: 1.03x slower                                             |
| regex_compile              | 137 ms                                                     | 142 ms: 1.04x slower                                              |
| regex_effbot               | 3.67 ms                                                    | 3.81 ms: 1.04x slower                                             |
| sympy_expand               | 473 ms                                                     | 491 ms: 1.04x slower                                              |
| coverage                   | 93.1 ms                                                    | 96.9 ms: 1.04x slower                                             |
| sympy_integrate            | 20.5 ms                                                    | 21.4 ms: 1.04x slower                                             |
| chaos                      | 61.3 ms                                                    | 64.5 ms: 1.05x slower                                             |
| sympy_sum                  | 156 ms                                                     | 165 ms: 1.06x slower                                              |
| comprehensions             | 16.6 us                                                    | 17.6 us: 1.06x slower                                             |
| sqlglot_optimize           | 55.5 ms                                                    | 58.8 ms: 1.06x slower                                             |
| scimark_lu                 | 122 ms                                                     | 129 ms: 1.06x slower                                              |
| tornado_http               | 94.6 ms                                                    | 101 ms: 1.06x slower                                              |
| raytrace                   | 267 ms                                                     | 284 ms: 1.06x slower                                              |
| gunicorn                   | 1.28 ms                                                    | 1.36 ms: 1.06x slower                                             |
| nbody                      | 88.3 ms                                                    | 94.2 ms: 1.07x slower                                             |
| go                         | 145 ms                                                     | 155 ms: 1.07x slower                                              |
| aiohttp                    | 1.18 ms                                                    | 1.27 ms: 1.07x slower                                             |
| djangocms                  | 31.5 us                                                    | 34.1 us: 1.08x slower                                             |
| nqueens                    | 81.4 ms                                                    | 88.4 ms: 1.09x slower                                             |
| sqlglot_parse              | 1.32 ms                                                    | 1.44 ms: 1.09x slower                                             |
| python_startup             | 10.8 ms                                                    | 11.8 ms: 1.10x slower                                             |
| sqlglot_transpile          | 1.63 ms                                                    | 1.80 ms: 1.10x slower                                             |
| unpickle_pure_python       | 218 us                                                     | 241 us: 1.10x slower                                              |
| pathlib                    | 17.3 ms                                                    | 19.1 ms: 1.10x slower                                             |
| hexiom                     | 6.30 ms                                                    | 6.96 ms: 1.11x slower                                             |
| 2to3                       | 274 ms                                                     | 304 ms: 1.11x slower                                              |
| xml_etree_process          | 61.2 ms                                                    | 68.8 ms: 1.12x slower                                             |
| html5lib                   | 67.2 ms                                                    | 75.8 ms: 1.13x slower                                             |
| xml_etree_generate         | 87.4 ms                                                    | 99.6 ms: 1.14x slower                                             |
| mypy2                      | 742 ms                                                     | 851 ms: 1.15x slower                                              |
| genshi_xml                 | 51.6 ms                                                    | 59.8 ms: 1.16x slower                                             |
| deltablue                  | 3.25 ms                                                    | 3.90 ms: 1.20x slower                                             |
| async_generators           | 442 ms                                                     | 556 ms: 1.26x slower                                              |
| pycparser                  | 1.16 sec                                                   | 1.47 sec: 1.27x slower                                            |
| xml_etree_parse            | 162 ms                                                     | 216 ms: 1.33x slower                                              |
| python_startup_no_site     | 7.11 ms                                                    | 10.1 ms: 1.42x slower                                             |
| xml_etree_iterparse        | 107 ms                                                     | 163 ms: 1.52x slower                                              |
| docutils                   | 2.83 sec                                                   | 4.82 sec: 1.70x slower                                            |
| float                      | 78.9 ms                                                    | 143 ms: 1.81x slower                                              |
| dask                       | 369 ms                                                     | 759 ms: 2.06x slower                                              |
| pylint                     | 317 ms                                                     | 1.01 sec: 3.18x slower                                            |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 4.17 sec: 6.83x slower                                            |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 4.55 sec: 7.75x slower                                            |
| async_tree_none            | 378 ms                                                     | 3.39 sec: 8.95x slower                                            |
| async_tree_memoization     | 463 ms                                                     | 4.37 sec: 9.43x slower                                            |
| async_tree_memoization_tg  | 444 ms                                                     | 4.65 sec: 10.47x slower                                           |
| async_tree_none_tg         | 336 ms                                                     | 3.70 sec: 11.00x slower                                           |
| async_tree_io              | 939 ms                                                     | 13.1 sec: 13.96x slower                                           |
| async_tree_io_tg           | 936 ms                                                     | 13.9 sec: 14.85x slower                                           |
| Geometric mean             | (ref)                                                      | 1.27x slower                                                      |

Benchmark hidden because not significant (6): pprint_safe_repr, logging_format, asyncio_tcp, telco, json, scimark_monte_carlo
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging
Ignored benchmarks (1) of results/bm-20240321-3.13.0a5+-716c0c6-JIT/bm-20240321-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-716c0c6.json: unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 1.08x