# Results vs. 3.13.0b2

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 1e4a4c4
- commit date: 2024-04-19
- overall geometric mean: 1.09x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240419-linux-x86_64-python-main-3.13.0a6+-1e4a4c4 |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 301 ms: 1.10x slower                                   |
| chameleon      | 7.22 ms                                                    | 7.65 ms: 1.06x slower                                  |
| docutils       | 2.83 sec                                                   | 3.08 sec: 1.09x slower                                 |
| html5lib       | 67.2 ms                                                    | 72.5 ms: 1.08x slower                                  |
| tornado_http   | 94.6 ms                                                    | 103 ms: 1.09x slower                                   |
| Geometric mean | (ref)                                                      | 1.08x slower                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240419-linux-x86_64-python-main-3.13.0a6+-1e4a4c4 |
|----------------------------|:----------------------------------------------------------:|:------------------------------------------------------:|
| async_tree_io_tg           | 936 ms                                                     | 973 ms: 1.04x slower                                   |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 636 ms: 1.04x slower                                   |
| async_tree_io              | 939 ms                                                     | 984 ms: 1.05x slower                                   |
| async_tree_memoization_tg  | 444 ms                                                     | 466 ms: 1.05x slower                                   |
| async_tree_none_tg         | 336 ms                                                     | 356 ms: 1.06x slower                                   |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 627 ms: 1.07x slower                                   |
| async_tree_memoization     | 463 ms                                                     | 501 ms: 1.08x slower                                   |
| Geometric mean             | (ref)                                                      | 1.05x slower                                           |

Benchmark hidden because not significant (1): async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240419-linux-x86_64-python-main-3.13.0a6+-1e4a4c4 |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------:|
| pidigits       | 191 ms                                                     | 208 ms: 1.09x slower                                   |
| float          | 78.9 ms                                                    | 89.3 ms: 1.13x slower                                  |
| nbody          | 88.3 ms                                                    | 119 ms: 1.35x slower                                   |
| Geometric mean | (ref)                                                      | 1.18x slower                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240419-linux-x86_64-python-main-3.13.0a6+-1e4a4c4 |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------:|
| regex_v8       | 25.1 ms                                                    | 26.2 ms: 1.04x slower                                  |
| regex_effbot   | 3.67 ms                                                    | 3.88 ms: 1.06x slower                                  |
| regex_dna      | 221 ms                                                     | 234 ms: 1.06x slower                                   |
| regex_compile  | 137 ms                                                     | 177 ms: 1.30x slower                                   |
| Geometric mean | (ref)                                                      | 1.11x slower                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240419-linux-x86_64-python-main-3.13.0a6+-1e4a4c4 |
|----------------------|:----------------------------------------------------------:|:------------------------------------------------------:|
| xml_etree_parse      | 162 ms                                                     | 152 ms: 1.07x faster                                   |
| json_loads           | 28.9 us                                                    | 28.0 us: 1.03x faster                                  |
| pickle_list          | 5.11 us                                                    | 5.07 us: 1.01x faster                                  |
| pickle_dict          | 34.8 us                                                    | 34.6 us: 1.01x faster                                  |
| pickle_pure_python   | 305 us                                                     | 311 us: 1.02x slower                                   |
| unpickle             | 15.1 us                                                    | 15.4 us: 1.02x slower                                  |
| xml_etree_iterparse  | 107 ms                                                     | 110 ms: 1.02x slower                                   |
| pickle               | 11.5 us                                                    | 11.8 us: 1.03x slower                                  |
| unpickle_list        | 5.34 us                                                    | 5.49 us: 1.03x slower                                  |
| xml_etree_process    | 61.2 ms                                                    | 63.8 ms: 1.04x slower                                  |
| xml_etree_generate   | 87.4 ms                                                    | 93.5 ms: 1.07x slower                                  |
| tomli_loads          | 2.12 sec                                                   | 2.51 sec: 1.18x slower                                 |
| unpickle_pure_python | 218 us                                                     | 282 us: 1.29x slower                                   |
| Geometric mean       | (ref)                                                      | 1.04x slower                                           |

Benchmark hidden because not significant (1): json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240419-linux-x86_64-python-main-3.13.0a6+-1e4a4c4 |
|------------------------|:----------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                  |
| python_startup_no_site | 7.11 ms                                                    | 7.13 ms: 1.00x slower                                  |
| Geometric mean         | (ref)                                                      | 1.01x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240419-linux-x86_64-python-main-3.13.0a6+-1e4a4c4 |
|-----------------|:----------------------------------------------------------:|:------------------------------------------------------:|
| genshi_text     | 23.7 ms                                                    | 25.7 ms: 1.09x slower                                  |
| django_template | 34.8 ms                                                    | 39.5 ms: 1.13x slower                                  |
| genshi_xml      | 51.6 ms                                                    | 59.0 ms: 1.14x slower                                  |
| mako            | 11.2 ms                                                    | 13.6 ms: 1.21x slower                                  |
| Geometric mean  | (ref)                                                      | 1.14x slower                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240419-linux-x86_64-python-main-3.13.0a6+-1e4a4c4 |
|----------------------------|:----------------------------------------------------------:|:------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 119 us: 1.38x faster                                   |
| xml_etree_parse            | 162 ms                                                     | 152 ms: 1.07x faster                                   |
| json_loads                 | 28.9 us                                                    | 28.0 us: 1.03x faster                                  |
| create_gc_cycles           | 1.82 ms                                                    | 1.77 ms: 1.02x faster                                  |
| json                       | 5.31 ms                                                    | 5.19 ms: 1.02x faster                                  |
| python_startup             | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                  |
| deepcopy_reduce            | 3.35 us                                                    | 3.30 us: 1.01x faster                                  |
| gc_traversal               | 3.98 ms                                                    | 3.94 ms: 1.01x faster                                  |
| pickle_list                | 5.11 us                                                    | 5.07 us: 1.01x faster                                  |
| pickle_dict                | 34.8 us                                                    | 34.6 us: 1.01x faster                                  |
| asyncio_websockets         | 567 ms                                                     | 564 ms: 1.00x faster                                   |
| python_startup_no_site     | 7.11 ms                                                    | 7.13 ms: 1.00x slower                                  |
| coroutines                 | 23.2 ms                                                    | 23.3 ms: 1.01x slower                                  |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.86 sec: 1.01x slower                                 |
| logging_silent             | 105 ns                                                     | 106 ns: 1.01x slower                                   |
| generators                 | 29.6 ms                                                    | 30.0 ms: 1.01x slower                                  |
| sqlite_synth               | 2.99 us                                                    | 3.04 us: 1.02x slower                                  |
| pickle_pure_python         | 305 us                                                     | 311 us: 1.02x slower                                   |
| thrift                     | 823 us                                                     | 838 us: 1.02x slower                                   |
| unpickle                   | 15.1 us                                                    | 15.4 us: 1.02x slower                                  |
| xml_etree_iterparse        | 107 ms                                                     | 110 ms: 1.02x slower                                   |
| dask                       | 369 ms                                                     | 379 ms: 1.03x slower                                   |
| asyncio_tcp                | 508 ms                                                     | 522 ms: 1.03x slower                                   |
| pickle                     | 11.5 us                                                    | 11.8 us: 1.03x slower                                  |
| unpickle_list              | 5.34 us                                                    | 5.49 us: 1.03x slower                                  |
| deepcopy                   | 367 us                                                     | 378 us: 1.03x slower                                   |
| gunicorn                   | 1.28 ms                                                    | 1.32 ms: 1.04x slower                                  |
| djangocms                  | 31.5 us                                                    | 32.7 us: 1.04x slower                                  |
| async_tree_io_tg           | 936 ms                                                     | 973 ms: 1.04x slower                                   |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 636 ms: 1.04x slower                                   |
| regex_v8                   | 25.1 ms                                                    | 26.2 ms: 1.04x slower                                  |
| xml_etree_process          | 61.2 ms                                                    | 63.8 ms: 1.04x slower                                  |
| aiohttp                    | 1.18 ms                                                    | 1.23 ms: 1.04x slower                                  |
| mdp                        | 2.79 sec                                                   | 2.91 sec: 1.05x slower                                 |
| async_tree_io              | 939 ms                                                     | 984 ms: 1.05x slower                                   |
| async_tree_memoization_tg  | 444 ms                                                     | 466 ms: 1.05x slower                                   |
| pathlib                    | 17.3 ms                                                    | 18.2 ms: 1.05x slower                                  |
| regex_effbot               | 3.67 ms                                                    | 3.88 ms: 1.06x slower                                  |
| bench_thread_pool          | 834 us                                                     | 882 us: 1.06x slower                                   |
| regex_dna                  | 221 ms                                                     | 234 ms: 1.06x slower                                   |
| chameleon                  | 7.22 ms                                                    | 7.65 ms: 1.06x slower                                  |
| async_tree_none_tg         | 336 ms                                                     | 356 ms: 1.06x slower                                   |
| coverage                   | 93.1 ms                                                    | 99.4 ms: 1.07x slower                                  |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 627 ms: 1.07x slower                                   |
| xml_etree_generate         | 87.4 ms                                                    | 93.5 ms: 1.07x slower                                  |
| async_generators           | 442 ms                                                     | 476 ms: 1.08x slower                                   |
| html5lib                   | 67.2 ms                                                    | 72.5 ms: 1.08x slower                                  |
| pylint                     | 317 ms                                                     | 342 ms: 1.08x slower                                   |
| richards                   | 50.9 ms                                                    | 55.0 ms: 1.08x slower                                  |
| richards_super             | 57.4 ms                                                    | 62.0 ms: 1.08x slower                                  |
| async_tree_memoization     | 463 ms                                                     | 501 ms: 1.08x slower                                   |
| mypy2                      | 742 ms                                                     | 803 ms: 1.08x slower                                   |
| logging_format             | 6.47 us                                                    | 7.01 us: 1.08x slower                                  |
| meteor_contest             | 110 ms                                                     | 119 ms: 1.09x slower                                   |
| tornado_http               | 94.6 ms                                                    | 103 ms: 1.09x slower                                   |
| pidigits                   | 191 ms                                                     | 208 ms: 1.09x slower                                   |
| genshi_text                | 23.7 ms                                                    | 25.7 ms: 1.09x slower                                  |
| docutils                   | 2.83 sec                                                   | 3.08 sec: 1.09x slower                                 |
| telco                      | 8.41 ms                                                    | 9.19 ms: 1.09x slower                                  |
| 2to3                       | 274 ms                                                     | 301 ms: 1.10x slower                                   |
| dulwich_log                | 67.2 ms                                                    | 73.8 ms: 1.10x slower                                  |
| sqlglot_transpile          | 1.63 ms                                                    | 1.80 ms: 1.10x slower                                  |
| logging_simple             | 5.74 us                                                    | 6.32 us: 1.10x slower                                  |
| sqlglot_normalize          | 110 ms                                                     | 123 ms: 1.11x slower                                   |
| sqlglot_parse              | 1.32 ms                                                    | 1.48 ms: 1.12x slower                                  |
| deepcopy_memo              | 39.7 us                                                    | 44.8 us: 1.13x slower                                  |
| sympy_expand               | 473 ms                                                     | 533 ms: 1.13x slower                                   |
| float                      | 78.9 ms                                                    | 89.3 ms: 1.13x slower                                  |
| pycparser                  | 1.16 sec                                                   | 1.31 sec: 1.13x slower                                 |
| sympy_integrate            | 20.5 ms                                                    | 23.2 ms: 1.13x slower                                  |
| django_template            | 34.8 ms                                                    | 39.5 ms: 1.13x slower                                  |
| sqlglot_optimize           | 55.5 ms                                                    | 63.1 ms: 1.14x slower                                  |
| sympy_str                  | 282 ms                                                     | 322 ms: 1.14x slower                                   |
| sympy_sum                  | 156 ms                                                     | 178 ms: 1.14x slower                                   |
| genshi_xml                 | 51.6 ms                                                    | 59.0 ms: 1.14x slower                                  |
| scimark_fft                | 392 ms                                                     | 461 ms: 1.18x slower                                   |
| scimark_sor                | 127 ms                                                     | 150 ms: 1.18x slower                                   |
| tomli_loads                | 2.12 sec                                                   | 2.51 sec: 1.18x slower                                 |
| crypto_pyaes               | 77.5 ms                                                    | 91.7 ms: 1.18x slower                                  |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 6.28 ms: 1.19x slower                                  |
| raytrace                   | 267 ms                                                     | 323 ms: 1.21x slower                                   |
| mako                       | 11.2 ms                                                    | 13.6 ms: 1.21x slower                                  |
| fannkuch                   | 402 ms                                                     | 489 ms: 1.22x slower                                   |
| pyflate                    | 484 ms                                                     | 589 ms: 1.22x slower                                   |
| deltablue                  | 3.25 ms                                                    | 4.06 ms: 1.25x slower                                  |
| pprint_safe_repr           | 758 ms                                                     | 947 ms: 1.25x slower                                   |
| go                         | 145 ms                                                     | 182 ms: 1.26x slower                                   |
| spectral_norm              | 116 ms                                                     | 147 ms: 1.26x slower                                   |
| pprint_pformat             | 1.56 sec                                                   | 1.97 sec: 1.27x slower                                 |
| chaos                      | 61.3 ms                                                    | 78.7 ms: 1.28x slower                                  |
| unpickle_pure_python       | 218 us                                                     | 282 us: 1.29x slower                                   |
| regex_compile              | 137 ms                                                     | 177 ms: 1.30x slower                                   |
| scimark_monte_carlo        | 69.2 ms                                                    | 91.3 ms: 1.32x slower                                  |
| nqueens                    | 81.4 ms                                                    | 110 ms: 1.35x slower                                   |
| comprehensions             | 16.6 us                                                    | 22.4 us: 1.35x slower                                  |
| nbody                      | 88.3 ms                                                    | 119 ms: 1.35x slower                                   |
| scimark_lu                 | 122 ms                                                     | 167 ms: 1.38x slower                                   |
| hexiom                     | 6.30 ms                                                    | 9.41 ms: 1.49x slower                                  |
| Geometric mean             | (ref)                                                      | 1.09x slower                                           |

Benchmark hidden because not significant (3): async_tree_none, json_dumps, bench_mp_pool
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 0.99x