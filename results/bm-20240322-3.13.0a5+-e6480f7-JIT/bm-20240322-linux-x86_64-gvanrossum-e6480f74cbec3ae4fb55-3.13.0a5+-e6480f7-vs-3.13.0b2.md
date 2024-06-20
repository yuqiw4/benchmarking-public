# Results vs. 3.13.0b2

- fork: gvanrossum
- ref: e6480f74cbec3ae4fb55
- machine: linux-x86_64
- commit hash: e6480f7
- commit date: 2024-03-22
- overall geometric mean: 1.03x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240322-linux-x86_64-gvanrossum-e6480f74cbec3ae4fb55-3.13.0a5+-e6480f7 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 280 ms: 1.02x slower                                                       |
| chameleon      | 7.22 ms                                                    | 7.11 ms: 1.02x faster                                                      |
| docutils       | 2.83 sec                                                   | 2.80 sec: 1.01x faster                                                     |
| html5lib       | 67.2 ms                                                    | 68.4 ms: 1.02x slower                                                      |
| tornado_http   | 94.6 ms                                                    | 99.3 ms: 1.05x slower                                                      |
| Geometric mean | (ref)                                                      | 1.01x slower                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240322-linux-x86_64-gvanrossum-e6480f74cbec3ae4fb55-3.13.0a5+-e6480f7 |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 611 ms                                                     | 728 ms: 1.19x slower                                                       |
| async_tree_none            | 378 ms                                                     | 453 ms: 1.20x slower                                                       |
| async_tree_memoization     | 463 ms                                                     | 581 ms: 1.25x slower                                                       |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 743 ms: 1.26x slower                                                       |
| async_tree_io              | 939 ms                                                     | 1.23 sec: 1.30x slower                                                     |
| async_tree_io_tg           | 936 ms                                                     | 1.24 sec: 1.33x slower                                                     |
| async_tree_memoization_tg  | 444 ms                                                     | 596 ms: 1.34x slower                                                       |
| async_tree_none_tg         | 336 ms                                                     | 464 ms: 1.38x slower                                                       |
| Geometric mean             | (ref)                                                      | 1.28x slower                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240322-linux-x86_64-gvanrossum-e6480f74cbec3ae4fb55-3.13.0a5+-e6480f7 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| pidigits       | 191 ms                                                     | 190 ms: 1.01x faster                                                       |
| float          | 78.9 ms                                                    | 80.6 ms: 1.02x slower                                                      |
| nbody          | 88.3 ms                                                    | 92.9 ms: 1.05x slower                                                      |
| Geometric mean | (ref)                                                      | 1.02x slower                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240322-linux-x86_64-gvanrossum-e6480f74cbec3ae4fb55-3.13.0a5+-e6480f7 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 137 ms                                                     | 143 ms: 1.05x slower                                                       |
| regex_effbot   | 3.67 ms                                                    | 3.85 ms: 1.05x slower                                                      |
| regex_dna      | 221 ms                                                     | 233 ms: 1.05x slower                                                       |
| Geometric mean | (ref)                                                      | 1.04x slower                                                               |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240322-linux-x86_64-gvanrossum-e6480f74cbec3ae4fb55-3.13.0a5+-e6480f7 |
|----------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| unpickle_list        | 5.34 us                                                    | 4.85 us: 1.10x faster                                                      |
| json_loads           | 28.9 us                                                    | 28.0 us: 1.03x faster                                                      |
| xml_etree_process    | 61.2 ms                                                    | 59.6 ms: 1.03x faster                                                      |
| json_dumps           | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                                      |
| tomli_loads          | 2.12 sec                                                   | 2.08 sec: 1.02x faster                                                     |
| xml_etree_iterparse  | 107 ms                                                     | 109 ms: 1.01x slower                                                       |
| pickle_dict          | 34.8 us                                                    | 35.6 us: 1.02x slower                                                      |
| pickle               | 11.5 us                                                    | 11.9 us: 1.04x slower                                                      |
| pickle_list          | 5.11 us                                                    | 5.36 us: 1.05x slower                                                      |
| unpickle_pure_python | 218 us                                                     | 239 us: 1.10x slower                                                       |
| Geometric mean       | (ref)                                                      | 1.00x faster                                                               |

Benchmark hidden because not significant (4): xml_etree_parse, pickle_pure_python, unpickle, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240322-linux-x86_64-gvanrossum-e6480f74cbec3ae4fb55-3.13.0a5+-e6480f7 |
|------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 11.5 ms: 1.07x slower                                                      |
| python_startup_no_site | 7.11 ms                                                    | 10.1 ms: 1.42x slower                                                      |
| Geometric mean         | (ref)                                                      | 1.23x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240322-linux-x86_64-gvanrossum-e6480f74cbec3ae4fb55-3.13.0a5+-e6480f7 |
|-----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 11.0 ms: 1.02x faster                                                      |
| django_template | 34.8 ms                                                    | 36.2 ms: 1.04x slower                                                      |
| genshi_text     | 23.7 ms                                                    | 24.7 ms: 1.04x slower                                                      |
| genshi_xml      | 51.6 ms                                                    | 54.8 ms: 1.06x slower                                                      |
| Geometric mean  | (ref)                                                      | 1.03x slower                                                               |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240322-linux-x86_64-gvanrossum-e6480f74cbec3ae4fb55-3.13.0a5+-e6480f7 |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 112 us: 1.47x faster                                                       |
| create_gc_cycles           | 1.82 ms                                                    | 1.53 ms: 1.18x faster                                                      |
| scimark_fft                | 392 ms                                                     | 341 ms: 1.15x faster                                                       |
| richards                   | 50.9 ms                                                    | 45.9 ms: 1.11x faster                                                      |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 4.78 ms: 1.10x faster                                                      |
| unpickle_list              | 5.34 us                                                    | 4.85 us: 1.10x faster                                                      |
| richards_super             | 57.4 ms                                                    | 52.7 ms: 1.09x faster                                                      |
| deepcopy_reduce            | 3.35 us                                                    | 3.15 us: 1.06x faster                                                      |
| mdp                        | 2.79 sec                                                   | 2.64 sec: 1.06x faster                                                     |
| sqlite_synth               | 2.99 us                                                    | 2.85 us: 1.05x faster                                                      |
| deepcopy                   | 367 us                                                     | 355 us: 1.03x faster                                                       |
| json_loads                 | 28.9 us                                                    | 28.0 us: 1.03x faster                                                      |
| crypto_pyaes               | 77.5 ms                                                    | 75.3 ms: 1.03x faster                                                      |
| xml_etree_process          | 61.2 ms                                                    | 59.6 ms: 1.03x faster                                                      |
| pprint_safe_repr           | 758 ms                                                     | 743 ms: 1.02x faster                                                       |
| json_dumps                 | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                                      |
| mako                       | 11.2 ms                                                    | 11.0 ms: 1.02x faster                                                      |
| tomli_loads                | 2.12 sec                                                   | 2.08 sec: 1.02x faster                                                     |
| thrift                     | 823 us                                                     | 808 us: 1.02x faster                                                       |
| chameleon                  | 7.22 ms                                                    | 7.11 ms: 1.02x faster                                                      |
| logging_silent             | 105 ns                                                     | 103 ns: 1.01x faster                                                       |
| gc_traversal               | 3.98 ms                                                    | 3.93 ms: 1.01x faster                                                      |
| docutils                   | 2.83 sec                                                   | 2.80 sec: 1.01x faster                                                     |
| pidigits                   | 191 ms                                                     | 190 ms: 1.01x faster                                                       |
| fannkuch                   | 402 ms                                                     | 399 ms: 1.01x faster                                                       |
| asyncio_websockets         | 567 ms                                                     | 563 ms: 1.01x faster                                                       |
| generators                 | 29.6 ms                                                    | 29.5 ms: 1.00x faster                                                      |
| asyncio_tcp                | 508 ms                                                     | 509 ms: 1.00x slower                                                       |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.85 sec: 1.00x slower                                                     |
| logging_format             | 6.47 us                                                    | 6.53 us: 1.01x slower                                                      |
| pyflate                    | 484 ms                                                     | 489 ms: 1.01x slower                                                       |
| xml_etree_iterparse        | 107 ms                                                     | 109 ms: 1.01x slower                                                       |
| sqlglot_transpile          | 1.63 ms                                                    | 1.66 ms: 1.01x slower                                                      |
| dask                       | 369 ms                                                     | 375 ms: 1.02x slower                                                       |
| html5lib                   | 67.2 ms                                                    | 68.4 ms: 1.02x slower                                                      |
| telco                      | 8.41 ms                                                    | 8.57 ms: 1.02x slower                                                      |
| bench_thread_pool          | 834 us                                                     | 850 us: 1.02x slower                                                       |
| logging_simple             | 5.74 us                                                    | 5.86 us: 1.02x slower                                                      |
| sqlglot_normalize          | 110 ms                                                     | 112 ms: 1.02x slower                                                       |
| scimark_monte_carlo        | 69.2 ms                                                    | 70.6 ms: 1.02x slower                                                      |
| sympy_str                  | 282 ms                                                     | 288 ms: 1.02x slower                                                       |
| float                      | 78.9 ms                                                    | 80.6 ms: 1.02x slower                                                      |
| aiohttp                    | 1.18 ms                                                    | 1.21 ms: 1.02x slower                                                      |
| pickle_dict                | 34.8 us                                                    | 35.6 us: 1.02x slower                                                      |
| 2to3                       | 274 ms                                                     | 280 ms: 1.02x slower                                                       |
| gunicorn                   | 1.28 ms                                                    | 1.31 ms: 1.02x slower                                                      |
| scimark_sor                | 127 ms                                                     | 131 ms: 1.03x slower                                                       |
| pickle                     | 11.5 us                                                    | 11.9 us: 1.04x slower                                                      |
| sympy_expand               | 473 ms                                                     | 490 ms: 1.04x slower                                                       |
| sqlglot_optimize           | 55.5 ms                                                    | 57.7 ms: 1.04x slower                                                      |
| dulwich_log                | 67.2 ms                                                    | 69.8 ms: 1.04x slower                                                      |
| django_template            | 34.8 ms                                                    | 36.2 ms: 1.04x slower                                                      |
| chaos                      | 61.3 ms                                                    | 63.9 ms: 1.04x slower                                                      |
| genshi_text                | 23.7 ms                                                    | 24.7 ms: 1.04x slower                                                      |
| regex_compile              | 137 ms                                                     | 143 ms: 1.05x slower                                                       |
| regex_effbot               | 3.67 ms                                                    | 3.85 ms: 1.05x slower                                                      |
| tornado_http               | 94.6 ms                                                    | 99.3 ms: 1.05x slower                                                      |
| pickle_list                | 5.11 us                                                    | 5.36 us: 1.05x slower                                                      |
| nbody                      | 88.3 ms                                                    | 92.9 ms: 1.05x slower                                                      |
| regex_dna                  | 221 ms                                                     | 233 ms: 1.05x slower                                                       |
| coverage                   | 93.1 ms                                                    | 98.2 ms: 1.05x slower                                                      |
| sympy_sum                  | 156 ms                                                     | 164 ms: 1.05x slower                                                       |
| sympy_integrate            | 20.5 ms                                                    | 21.7 ms: 1.06x slower                                                      |
| genshi_xml                 | 51.6 ms                                                    | 54.8 ms: 1.06x slower                                                      |
| pycparser                  | 1.16 sec                                                   | 1.23 sec: 1.07x slower                                                     |
| python_startup             | 10.8 ms                                                    | 11.5 ms: 1.07x slower                                                      |
| deltablue                  | 3.25 ms                                                    | 3.49 ms: 1.07x slower                                                      |
| go                         | 145 ms                                                     | 155 ms: 1.07x slower                                                       |
| async_generators           | 442 ms                                                     | 475 ms: 1.07x slower                                                       |
| comprehensions             | 16.6 us                                                    | 17.9 us: 1.08x slower                                                      |
| scimark_lu                 | 122 ms                                                     | 131 ms: 1.08x slower                                                       |
| pathlib                    | 17.3 ms                                                    | 18.7 ms: 1.08x slower                                                      |
| unpickle_pure_python       | 218 us                                                     | 239 us: 1.10x slower                                                       |
| nqueens                    | 81.4 ms                                                    | 89.8 ms: 1.10x slower                                                      |
| raytrace                   | 267 ms                                                     | 294 ms: 1.10x slower                                                       |
| hexiom                     | 6.30 ms                                                    | 7.02 ms: 1.11x slower                                                      |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 728 ms: 1.19x slower                                                       |
| async_tree_none            | 378 ms                                                     | 453 ms: 1.20x slower                                                       |
| mypy2                      | 742 ms                                                     | 905 ms: 1.22x slower                                                       |
| async_tree_memoization     | 463 ms                                                     | 581 ms: 1.25x slower                                                       |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 743 ms: 1.26x slower                                                       |
| async_tree_io              | 939 ms                                                     | 1.23 sec: 1.30x slower                                                     |
| async_tree_io_tg           | 936 ms                                                     | 1.24 sec: 1.33x slower                                                     |
| async_tree_memoization_tg  | 444 ms                                                     | 596 ms: 1.34x slower                                                       |
| async_tree_none_tg         | 336 ms                                                     | 464 ms: 1.38x slower                                                       |
| python_startup_no_site     | 7.11 ms                                                    | 10.1 ms: 1.42x slower                                                      |
| Geometric mean             | (ref)                                                      | 1.03x slower                                                               |

Benchmark hidden because not significant (15): xml_etree_parse, pickle_pure_python, pprint_pformat, unpickle, spectral_norm, meteor_contest, djangocms, xml_etree_generate, regex_v8, json, deepcopy_memo, coroutines, sqlglot_parse, bench_mp_pool, pylint
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging
Ignored benchmarks (1) of results/bm-20240322-3.13.0a5+-e6480f7-JIT/bm-20240322-linux-x86_64-gvanrossum-e6480f74cbec3ae4fb55-3.13.0a5+-e6480f7.json: unpack_sequence

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.09x