# Results vs. 3.13.0b2

- fork: man-group
- ref: io_flush_full_buffer
- machine: linux-x86_64
- commit hash: 9cf294a
- commit date: 2024-03-26
- overall geometric mean: 1.01x slower
- HPT reliability: 98.02%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.06x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240326-linux-x86_64-man%2dgroup-io_flush_full_buffer-3.13.0a5+-9cf294a |
|----------------|:----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 278 ms: 1.02x slower                                                        |
| chameleon      | 7.22 ms                                                    | 6.93 ms: 1.04x faster                                                       |
| docutils       | 2.83 sec                                                   | 2.87 sec: 1.02x slower                                                      |
| html5lib       | 67.2 ms                                                    | 66.0 ms: 1.02x faster                                                       |
| tornado_http   | 94.6 ms                                                    | 96.4 ms: 1.02x slower                                                       |
| Geometric mean | (ref)                                                      | 1.00x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240326-linux-x86_64-man%2dgroup-io_flush_full_buffer-3.13.0a5+-9cf294a |
|----------------------------|:----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 611 ms                                                     | 594 ms: 1.03x faster                                                        |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 605 ms: 1.03x slower                                                        |
| async_tree_none_tg         | 336 ms                                                     | 351 ms: 1.05x slower                                                        |
| Geometric mean             | (ref)                                                      | 1.00x faster                                                                |

Benchmark hidden because not significant (5): async_tree_io, async_tree_io_tg, async_tree_none, async_tree_memoization, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240326-linux-x86_64-man%2dgroup-io_flush_full_buffer-3.13.0a5+-9cf294a |
|----------------|:----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 78.9 ms                                                    | 77.5 ms: 1.02x faster                                                       |
| pidigits       | 191 ms                                                     | 189 ms: 1.01x faster                                                        |
| nbody          | 88.3 ms                                                    | 93.8 ms: 1.06x slower                                                       |
| Geometric mean | (ref)                                                      | 1.01x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240326-linux-x86_64-man%2dgroup-io_flush_full_buffer-3.13.0a5+-9cf294a |
|----------------|:----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 3.67 ms                                                    | 3.69 ms: 1.00x slower                                                       |
| regex_dna      | 221 ms                                                     | 230 ms: 1.04x slower                                                        |
| regex_v8       | 25.1 ms                                                    | 26.2 ms: 1.04x slower                                                       |
| regex_compile  | 137 ms                                                     | 146 ms: 1.07x slower                                                        |
| Geometric mean | (ref)                                                      | 1.04x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240326-linux-x86_64-man%2dgroup-io_flush_full_buffer-3.13.0a5+-9cf294a |
|----------------------|:----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| unpickle_list        | 5.34 us                                                    | 5.11 us: 1.04x faster                                                       |
| pickle_dict          | 34.8 us                                                    | 33.5 us: 1.04x faster                                                       |
| json_loads           | 28.9 us                                                    | 28.3 us: 1.02x faster                                                       |
| pickle_list          | 5.11 us                                                    | 5.02 us: 1.02x faster                                                       |
| tomli_loads          | 2.12 sec                                                   | 2.09 sec: 1.01x faster                                                      |
| json_dumps           | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                                       |
| xml_etree_generate   | 87.4 ms                                                    | 86.7 ms: 1.01x faster                                                       |
| pickle_pure_python   | 305 us                                                     | 309 us: 1.01x slower                                                        |
| pickle               | 11.5 us                                                    | 11.8 us: 1.03x slower                                                       |
| unpickle_pure_python | 218 us                                                     | 243 us: 1.11x slower                                                        |
| Geometric mean       | (ref)                                                      | 1.00x faster                                                                |

Benchmark hidden because not significant (4): xml_etree_parse, xml_etree_iterparse, xml_etree_process, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240326-linux-x86_64-man%2dgroup-io_flush_full_buffer-3.13.0a5+-9cf294a |
|------------------------|:----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 11.0 ms: 1.03x slower                                                       |
| python_startup_no_site | 7.11 ms                                                    | 9.50 ms: 1.34x slower                                                       |
| Geometric mean         | (ref)                                                      | 1.17x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240326-linux-x86_64-man%2dgroup-io_flush_full_buffer-3.13.0a5+-9cf294a |
|-----------------|:----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 10.7 ms: 1.05x faster                                                       |
| django_template | 34.8 ms                                                    | 36.3 ms: 1.04x slower                                                       |
| genshi_text     | 23.7 ms                                                    | 25.3 ms: 1.07x slower                                                       |
| genshi_xml      | 51.6 ms                                                    | 56.3 ms: 1.09x slower                                                       |
| Geometric mean  | (ref)                                                      | 1.04x slower                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240326-linux-x86_64-man%2dgroup-io_flush_full_buffer-3.13.0a5+-9cf294a |
|----------------------------|:----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 113 us: 1.45x faster                                                        |
| scimark_fft                | 392 ms                                                     | 347 ms: 1.13x faster                                                        |
| richards_super             | 57.4 ms                                                    | 52.3 ms: 1.10x faster                                                       |
| richards                   | 50.9 ms                                                    | 46.4 ms: 1.10x faster                                                       |
| create_gc_cycles           | 1.82 ms                                                    | 1.69 ms: 1.07x faster                                                       |
| deepcopy_reduce            | 3.35 us                                                    | 3.17 us: 1.06x faster                                                       |
| mako                       | 11.2 ms                                                    | 10.7 ms: 1.05x faster                                                       |
| mdp                        | 2.79 sec                                                   | 2.65 sec: 1.05x faster                                                      |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 5.04 ms: 1.05x faster                                                       |
| unpickle_list              | 5.34 us                                                    | 5.11 us: 1.04x faster                                                       |
| sqlite_synth               | 2.99 us                                                    | 2.87 us: 1.04x faster                                                       |
| chameleon                  | 7.22 ms                                                    | 6.93 ms: 1.04x faster                                                       |
| pickle_dict                | 34.8 us                                                    | 33.5 us: 1.04x faster                                                       |
| crypto_pyaes               | 77.5 ms                                                    | 74.6 ms: 1.04x faster                                                       |
| coroutines                 | 23.2 ms                                                    | 22.5 ms: 1.03x faster                                                       |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 594 ms: 1.03x faster                                                        |
| logging_silent             | 105 ns                                                     | 102 ns: 1.02x faster                                                        |
| json_loads                 | 28.9 us                                                    | 28.3 us: 1.02x faster                                                       |
| html5lib                   | 67.2 ms                                                    | 66.0 ms: 1.02x faster                                                       |
| spectral_norm              | 116 ms                                                     | 114 ms: 1.02x faster                                                        |
| float                      | 78.9 ms                                                    | 77.5 ms: 1.02x faster                                                       |
| pickle_list                | 5.11 us                                                    | 5.02 us: 1.02x faster                                                       |
| pprint_pformat             | 1.56 sec                                                   | 1.53 sec: 1.02x faster                                                      |
| tomli_loads                | 2.12 sec                                                   | 2.09 sec: 1.01x faster                                                      |
| pprint_safe_repr           | 758 ms                                                     | 748 ms: 1.01x faster                                                        |
| json_dumps                 | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                                       |
| fannkuch                   | 402 ms                                                     | 397 ms: 1.01x faster                                                        |
| pidigits                   | 191 ms                                                     | 189 ms: 1.01x faster                                                        |
| gc_traversal               | 3.98 ms                                                    | 3.94 ms: 1.01x faster                                                       |
| pyflate                    | 484 ms                                                     | 480 ms: 1.01x faster                                                        |
| xml_etree_generate         | 87.4 ms                                                    | 86.7 ms: 1.01x faster                                                       |
| asyncio_tcp                | 508 ms                                                     | 504 ms: 1.01x faster                                                        |
| deepcopy                   | 367 us                                                     | 364 us: 1.01x faster                                                        |
| thrift                     | 823 us                                                     | 818 us: 1.01x faster                                                        |
| regex_effbot               | 3.67 ms                                                    | 3.69 ms: 1.00x slower                                                       |
| asyncio_websockets         | 567 ms                                                     | 570 ms: 1.01x slower                                                        |
| bench_mp_pool              | 23.9 ms                                                    | 24.0 ms: 1.01x slower                                                       |
| meteor_contest             | 110 ms                                                     | 111 ms: 1.01x slower                                                        |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.86 sec: 1.01x slower                                                      |
| pickle_pure_python         | 305 us                                                     | 309 us: 1.01x slower                                                        |
| generators                 | 29.6 ms                                                    | 30.0 ms: 1.01x slower                                                       |
| sqlglot_transpile          | 1.63 ms                                                    | 1.66 ms: 1.01x slower                                                       |
| docutils                   | 2.83 sec                                                   | 2.87 sec: 1.02x slower                                                      |
| 2to3                       | 274 ms                                                     | 278 ms: 1.02x slower                                                        |
| sqlglot_parse              | 1.32 ms                                                    | 1.34 ms: 1.02x slower                                                       |
| tornado_http               | 94.6 ms                                                    | 96.4 ms: 1.02x slower                                                       |
| telco                      | 8.41 ms                                                    | 8.59 ms: 1.02x slower                                                       |
| sqlglot_normalize          | 110 ms                                                     | 113 ms: 1.02x slower                                                        |
| gunicorn                   | 1.28 ms                                                    | 1.31 ms: 1.02x slower                                                       |
| logging_format             | 6.47 us                                                    | 6.62 us: 1.02x slower                                                       |
| python_startup             | 10.8 ms                                                    | 11.0 ms: 1.03x slower                                                       |
| pickle                     | 11.5 us                                                    | 11.8 us: 1.03x slower                                                       |
| bench_thread_pool          | 834 us                                                     | 858 us: 1.03x slower                                                        |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 605 ms: 1.03x slower                                                        |
| aiohttp                    | 1.18 ms                                                    | 1.22 ms: 1.03x slower                                                       |
| scimark_monte_carlo        | 69.2 ms                                                    | 71.4 ms: 1.03x slower                                                       |
| sympy_str                  | 282 ms                                                     | 292 ms: 1.03x slower                                                        |
| regex_dna                  | 221 ms                                                     | 230 ms: 1.04x slower                                                        |
| sqlglot_optimize           | 55.5 ms                                                    | 57.9 ms: 1.04x slower                                                       |
| regex_v8                   | 25.1 ms                                                    | 26.2 ms: 1.04x slower                                                       |
| django_template            | 34.8 ms                                                    | 36.3 ms: 1.04x slower                                                       |
| sympy_expand               | 473 ms                                                     | 494 ms: 1.04x slower                                                        |
| async_tree_none_tg         | 336 ms                                                     | 351 ms: 1.05x slower                                                        |
| logging_simple             | 5.74 us                                                    | 6.00 us: 1.05x slower                                                       |
| async_generators           | 442 ms                                                     | 462 ms: 1.05x slower                                                        |
| scimark_sor                | 127 ms                                                     | 133 ms: 1.05x slower                                                        |
| dulwich_log                | 67.2 ms                                                    | 70.6 ms: 1.05x slower                                                       |
| chaos                      | 61.3 ms                                                    | 64.6 ms: 1.05x slower                                                       |
| sympy_sum                  | 156 ms                                                     | 165 ms: 1.06x slower                                                        |
| coverage                   | 93.1 ms                                                    | 98.7 ms: 1.06x slower                                                       |
| mypy2                      | 742 ms                                                     | 787 ms: 1.06x slower                                                        |
| sympy_integrate            | 20.5 ms                                                    | 21.8 ms: 1.06x slower                                                       |
| nbody                      | 88.3 ms                                                    | 93.8 ms: 1.06x slower                                                       |
| pycparser                  | 1.16 sec                                                   | 1.23 sec: 1.06x slower                                                      |
| regex_compile              | 137 ms                                                     | 146 ms: 1.07x slower                                                        |
| deltablue                  | 3.25 ms                                                    | 3.47 ms: 1.07x slower                                                       |
| genshi_text                | 23.7 ms                                                    | 25.3 ms: 1.07x slower                                                       |
| go                         | 145 ms                                                     | 156 ms: 1.08x slower                                                        |
| pathlib                    | 17.3 ms                                                    | 18.9 ms: 1.09x slower                                                       |
| genshi_xml                 | 51.6 ms                                                    | 56.3 ms: 1.09x slower                                                       |
| scimark_lu                 | 122 ms                                                     | 133 ms: 1.10x slower                                                        |
| comprehensions             | 16.6 us                                                    | 18.2 us: 1.10x slower                                                       |
| raytrace                   | 267 ms                                                     | 293 ms: 1.10x slower                                                        |
| nqueens                    | 81.4 ms                                                    | 90.4 ms: 1.11x slower                                                       |
| unpickle_pure_python       | 218 us                                                     | 243 us: 1.11x slower                                                        |
| hexiom                     | 6.30 ms                                                    | 7.20 ms: 1.14x slower                                                       |
| python_startup_no_site     | 7.11 ms                                                    | 9.50 ms: 1.34x slower                                                       |
| Geometric mean             | (ref)                                                      | 1.01x slower                                                                |

Benchmark hidden because not significant (14): async_tree_io, async_tree_io_tg, async_tree_none, djangocms, xml_etree_parse, xml_etree_iterparse, xml_etree_process, json, async_tree_memoization, async_tree_memoization_tg, deepcopy_memo, unpickle, dask, pylint
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 98.02% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.06x