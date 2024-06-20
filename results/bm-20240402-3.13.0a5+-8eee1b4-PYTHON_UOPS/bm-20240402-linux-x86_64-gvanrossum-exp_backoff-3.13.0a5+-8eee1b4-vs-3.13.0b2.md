# Results vs. 3.13.0b2

- fork: gvanrossum
- ref: exp_backoff
- machine: linux-x86_64
- commit hash: 8eee1b4
- commit date: 2024-04-02
- overall geometric mean: 1.14x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 313 ms: 1.14x slower                                              |
| chameleon      | 7.22 ms                                                    | 7.85 ms: 1.09x slower                                             |
| docutils       | 2.83 sec                                                   | 3.16 sec: 1.12x slower                                            |
| html5lib       | 67.2 ms                                                    | 73.9 ms: 1.10x slower                                             |
| tornado_http   | 94.6 ms                                                    | 103 ms: 1.09x slower                                              |
| Geometric mean | (ref)                                                      | 1.11x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io              | 939 ms                                                     | 982 ms: 1.05x slower                                              |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 643 ms: 1.05x slower                                              |
| async_tree_memoization_tg  | 444 ms                                                     | 473 ms: 1.06x slower                                              |
| async_tree_none_tg         | 336 ms                                                     | 363 ms: 1.08x slower                                              |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 634 ms: 1.08x slower                                              |
| async_tree_io_tg           | 936 ms                                                     | 1.01 sec: 1.08x slower                                            |
| async_tree_memoization     | 463 ms                                                     | 515 ms: 1.11x slower                                              |
| Geometric mean             | (ref)                                                      | 1.06x slower                                                      |

Benchmark hidden because not significant (1): async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 191 ms                                                     | 197 ms: 1.03x slower                                              |
| float          | 78.9 ms                                                    | 94.6 ms: 1.20x slower                                             |
| nbody          | 88.3 ms                                                    | 132 ms: 1.49x slower                                              |
| Geometric mean | (ref)                                                      | 1.23x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_dna      | 221 ms                                                     | 227 ms: 1.03x slower                                              |
| regex_effbot   | 3.67 ms                                                    | 3.79 ms: 1.03x slower                                             |
| regex_v8       | 25.1 ms                                                    | 26.7 ms: 1.06x slower                                             |
| regex_compile  | 137 ms                                                     | 194 ms: 1.42x slower                                              |
| Geometric mean | (ref)                                                      | 1.12x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| unpickle_list        | 5.34 us                                                    | 5.16 us: 1.04x faster                                             |
| pickle_list          | 5.11 us                                                    | 5.00 us: 1.02x faster                                             |
| pickle_dict          | 34.8 us                                                    | 34.1 us: 1.02x faster                                             |
| json_loads           | 28.9 us                                                    | 28.5 us: 1.01x faster                                             |
| json_dumps           | 10.7 ms                                                    | 10.8 ms: 1.01x slower                                             |
| unpickle             | 15.1 us                                                    | 15.4 us: 1.02x slower                                             |
| pickle_pure_python   | 305 us                                                     | 316 us: 1.03x slower                                              |
| pickle               | 11.5 us                                                    | 11.9 us: 1.04x slower                                             |
| xml_etree_iterparse  | 107 ms                                                     | 115 ms: 1.07x slower                                              |
| xml_etree_process    | 61.2 ms                                                    | 65.8 ms: 1.08x slower                                             |
| xml_etree_generate   | 87.4 ms                                                    | 96.8 ms: 1.11x slower                                             |
| tomli_loads          | 2.12 sec                                                   | 2.78 sec: 1.31x slower                                            |
| unpickle_pure_python | 218 us                                                     | 309 us: 1.42x slower                                              |
| Geometric mean       | (ref)                                                      | 1.06x slower                                                      |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.7 ms: 1.00x faster                                             |
| python_startup_no_site | 7.11 ms                                                    | 9.10 ms: 1.28x slower                                             |
| Geometric mean         | (ref)                                                      | 1.13x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_text    | 23.7 ms                                                    | 26.0 ms: 1.10x slower                                             |
| genshi_xml     | 51.6 ms                                                    | 62.7 ms: 1.22x slower                                             |
| mako           | 11.2 ms                                                    | 13.9 ms: 1.23x slower                                             |
| Geometric mean | (ref)                                                      | 1.18x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 129 us: 1.28x faster                                              |
| coroutines                 | 23.2 ms                                                    | 22.3 ms: 1.04x faster                                             |
| create_gc_cycles           | 1.82 ms                                                    | 1.75 ms: 1.04x faster                                             |
| unpickle_list              | 5.34 us                                                    | 5.16 us: 1.04x faster                                             |
| pickle_list                | 5.11 us                                                    | 5.00 us: 1.02x faster                                             |
| pickle_dict                | 34.8 us                                                    | 34.1 us: 1.02x faster                                             |
| json_loads                 | 28.9 us                                                    | 28.5 us: 1.01x faster                                             |
| python_startup             | 10.8 ms                                                    | 10.7 ms: 1.00x faster                                             |
| gc_traversal               | 3.98 ms                                                    | 4.00 ms: 1.01x slower                                             |
| json_dumps                 | 10.7 ms                                                    | 10.8 ms: 1.01x slower                                             |
| generators                 | 29.6 ms                                                    | 30.0 ms: 1.01x slower                                             |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.87 sec: 1.01x slower                                            |
| unpickle                   | 15.1 us                                                    | 15.4 us: 1.02x slower                                             |
| asyncio_tcp                | 508 ms                                                     | 517 ms: 1.02x slower                                              |
| mdp                        | 2.79 sec                                                   | 2.84 sec: 1.02x slower                                            |
| regex_dna                  | 221 ms                                                     | 227 ms: 1.03x slower                                              |
| logging_silent             | 105 ns                                                     | 108 ns: 1.03x slower                                              |
| json                       | 5.31 ms                                                    | 5.47 ms: 1.03x slower                                             |
| pidigits                   | 191 ms                                                     | 197 ms: 1.03x slower                                              |
| regex_effbot               | 3.67 ms                                                    | 3.79 ms: 1.03x slower                                             |
| thrift                     | 823 us                                                     | 850 us: 1.03x slower                                              |
| pickle_pure_python         | 305 us                                                     | 316 us: 1.03x slower                                              |
| sqlite_synth               | 2.99 us                                                    | 3.09 us: 1.03x slower                                             |
| pickle                     | 11.5 us                                                    | 11.9 us: 1.04x slower                                             |
| dask                       | 369 ms                                                     | 384 ms: 1.04x slower                                              |
| async_tree_io              | 939 ms                                                     | 982 ms: 1.05x slower                                              |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 643 ms: 1.05x slower                                              |
| coverage                   | 93.1 ms                                                    | 98.2 ms: 1.06x slower                                             |
| gunicorn                   | 1.28 ms                                                    | 1.36 ms: 1.06x slower                                             |
| regex_v8                   | 25.1 ms                                                    | 26.7 ms: 1.06x slower                                             |
| aiohttp                    | 1.18 ms                                                    | 1.25 ms: 1.06x slower                                             |
| async_tree_memoization_tg  | 444 ms                                                     | 473 ms: 1.06x slower                                              |
| deepcopy                   | 367 us                                                     | 391 us: 1.07x slower                                              |
| xml_etree_iterparse        | 107 ms                                                     | 115 ms: 1.07x slower                                              |
| xml_etree_process          | 61.2 ms                                                    | 65.8 ms: 1.08x slower                                             |
| bench_thread_pool          | 834 us                                                     | 897 us: 1.08x slower                                              |
| async_tree_none_tg         | 336 ms                                                     | 363 ms: 1.08x slower                                              |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 634 ms: 1.08x slower                                              |
| async_tree_io_tg           | 936 ms                                                     | 1.01 sec: 1.08x slower                                            |
| chameleon                  | 7.22 ms                                                    | 7.85 ms: 1.09x slower                                             |
| tornado_http               | 94.6 ms                                                    | 103 ms: 1.09x slower                                              |
| async_generators           | 442 ms                                                     | 483 ms: 1.09x slower                                              |
| genshi_text                | 23.7 ms                                                    | 26.0 ms: 1.10x slower                                             |
| html5lib                   | 67.2 ms                                                    | 73.9 ms: 1.10x slower                                             |
| xml_etree_generate         | 87.4 ms                                                    | 96.8 ms: 1.11x slower                                             |
| async_tree_memoization     | 463 ms                                                     | 515 ms: 1.11x slower                                              |
| docutils                   | 2.83 sec                                                   | 3.16 sec: 1.12x slower                                            |
| mypy2                      | 742 ms                                                     | 836 ms: 1.13x slower                                              |
| dulwich_log                | 67.2 ms                                                    | 76.3 ms: 1.14x slower                                             |
| logging_format             | 6.47 us                                                    | 7.37 us: 1.14x slower                                             |
| 2to3                       | 274 ms                                                     | 313 ms: 1.14x slower                                              |
| sqlglot_transpile          | 1.63 ms                                                    | 1.88 ms: 1.15x slower                                             |
| telco                      | 8.41 ms                                                    | 9.69 ms: 1.15x slower                                             |
| meteor_contest             | 110 ms                                                     | 127 ms: 1.16x slower                                              |
| logging_simple             | 5.74 us                                                    | 6.68 us: 1.16x slower                                             |
| sympy_expand               | 473 ms                                                     | 554 ms: 1.17x slower                                              |
| sympy_integrate            | 20.5 ms                                                    | 24.1 ms: 1.17x slower                                             |
| sqlglot_parse              | 1.32 ms                                                    | 1.55 ms: 1.18x slower                                             |
| pathlib                    | 17.3 ms                                                    | 20.4 ms: 1.18x slower                                             |
| scimark_fft                | 392 ms                                                     | 463 ms: 1.18x slower                                              |
| sympy_sum                  | 156 ms                                                     | 184 ms: 1.18x slower                                              |
| richards_super             | 57.4 ms                                                    | 68.0 ms: 1.19x slower                                             |
| scimark_sor                | 127 ms                                                     | 151 ms: 1.19x slower                                              |
| sqlglot_normalize          | 110 ms                                                     | 131 ms: 1.19x slower                                              |
| sympy_str                  | 282 ms                                                     | 338 ms: 1.20x slower                                              |
| richards                   | 50.9 ms                                                    | 61.1 ms: 1.20x slower                                             |
| float                      | 78.9 ms                                                    | 94.6 ms: 1.20x slower                                             |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 6.33 ms: 1.20x slower                                             |
| crypto_pyaes               | 77.5 ms                                                    | 93.4 ms: 1.21x slower                                             |
| genshi_xml                 | 51.6 ms                                                    | 62.7 ms: 1.22x slower                                             |
| sqlglot_optimize           | 55.5 ms                                                    | 67.5 ms: 1.22x slower                                             |
| mako                       | 11.2 ms                                                    | 13.9 ms: 1.23x slower                                             |
| fannkuch                   | 402 ms                                                     | 497 ms: 1.24x slower                                              |
| pycparser                  | 1.16 sec                                                   | 1.45 sec: 1.25x slower                                            |
| deepcopy_memo              | 39.7 us                                                    | 49.9 us: 1.26x slower                                             |
| go                         | 145 ms                                                     | 185 ms: 1.28x slower                                              |
| python_startup_no_site     | 7.11 ms                                                    | 9.10 ms: 1.28x slower                                             |
| chaos                      | 61.3 ms                                                    | 79.9 ms: 1.30x slower                                             |
| scimark_monte_carlo        | 69.2 ms                                                    | 90.2 ms: 1.30x slower                                             |
| tomli_loads                | 2.12 sec                                                   | 2.78 sec: 1.31x slower                                            |
| spectral_norm              | 116 ms                                                     | 153 ms: 1.32x slower                                              |
| pyflate                    | 484 ms                                                     | 651 ms: 1.35x slower                                              |
| deltablue                  | 3.25 ms                                                    | 4.53 ms: 1.39x slower                                             |
| raytrace                   | 267 ms                                                     | 373 ms: 1.40x slower                                              |
| unpickle_pure_python       | 218 us                                                     | 309 us: 1.42x slower                                              |
| regex_compile              | 137 ms                                                     | 194 ms: 1.42x slower                                              |
| scimark_lu                 | 122 ms                                                     | 176 ms: 1.44x slower                                              |
| pprint_safe_repr           | 758 ms                                                     | 1.13 sec: 1.49x slower                                            |
| nqueens                    | 81.4 ms                                                    | 121 ms: 1.49x slower                                              |
| nbody                      | 88.3 ms                                                    | 132 ms: 1.49x slower                                              |
| pprint_pformat             | 1.56 sec                                                   | 2.35 sec: 1.51x slower                                            |
| comprehensions             | 16.6 us                                                    | 25.9 us: 1.56x slower                                             |
| hexiom                     | 6.30 ms                                                    | 10.2 ms: 1.62x slower                                             |
| Geometric mean             | (ref)                                                      | 1.14x slower                                                      |

Benchmark hidden because not significant (6): pylint, asyncio_websockets, deepcopy_reduce, bench_mp_pool, xml_etree_parse, async_tree_none
Ignored benchmarks (4) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, django_template, djangocms, flaskblogging
Ignored benchmarks (1) of results/bm-20240402-3.13.0a5+-8eee1b4-PYTHON_UOPS/bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4.json: unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.11x
- 95% likely to have a slowdown of 1.10x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 0.99x