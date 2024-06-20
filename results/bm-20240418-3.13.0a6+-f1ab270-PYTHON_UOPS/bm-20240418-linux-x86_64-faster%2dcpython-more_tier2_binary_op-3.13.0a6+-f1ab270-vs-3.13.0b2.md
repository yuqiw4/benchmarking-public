# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: more_tier2_binary_op
- machine: linux-x86_64
- commit hash: f1ab270
- commit date: 2024-04-18
- overall geometric mean: 1.23x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240418-linux-x86_64-faster%2dcpython-more_tier2_binary_op-3.13.0a6+-f1ab270 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 330 ms: 1.20x slower                                                             |
| chameleon      | 7.22 ms                                                    | 8.18 ms: 1.13x slower                                                            |
| docutils       | 2.83 sec                                                   | 3.27 sec: 1.15x slower                                                           |
| html5lib       | 67.2 ms                                                    | 73.7 ms: 1.10x slower                                                            |
| tornado_http   | 94.6 ms                                                    | 103 ms: 1.09x slower                                                             |
| Geometric mean | (ref)                                                      | 1.14x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240418-linux-x86_64-faster%2dcpython-more_tier2_binary_op-3.13.0a6+-f1ab270 |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 397 ms: 1.05x slower                                                             |
| async_tree_io              | 939 ms                                                     | 1.01 sec: 1.07x slower                                                           |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 661 ms: 1.08x slower                                                             |
| async_tree_io_tg           | 936 ms                                                     | 1.02 sec: 1.09x slower                                                           |
| async_tree_memoization_tg  | 444 ms                                                     | 485 ms: 1.09x slower                                                             |
| async_tree_none_tg         | 336 ms                                                     | 371 ms: 1.10x slower                                                             |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 651 ms: 1.11x slower                                                             |
| async_tree_memoization     | 463 ms                                                     | 530 ms: 1.14x slower                                                             |
| Geometric mean             | (ref)                                                      | 1.09x slower                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240418-linux-x86_64-faster%2dcpython-more_tier2_binary_op-3.13.0a6+-f1ab270 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 191 ms                                                     | 202 ms: 1.06x slower                                                             |
| float          | 78.9 ms                                                    | 135 ms: 1.71x slower                                                             |
| nbody          | 88.3 ms                                                    | 209 ms: 2.36x slower                                                             |
| Geometric mean | (ref)                                                      | 1.62x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240418-linux-x86_64-faster%2dcpython-more_tier2_binary_op-3.13.0a6+-f1ab270 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_effbot   | 3.67 ms                                                    | 3.61 ms: 1.02x faster                                                            |
| regex_dna      | 221 ms                                                     | 226 ms: 1.02x slower                                                             |
| regex_v8       | 25.1 ms                                                    | 25.8 ms: 1.03x slower                                                            |
| regex_compile  | 137 ms                                                     | 220 ms: 1.61x slower                                                             |
| Geometric mean | (ref)                                                      | 1.13x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240418-linux-x86_64-faster%2dcpython-more_tier2_binary_op-3.13.0a6+-f1ab270 |
|----------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| unpickle_list        | 5.34 us                                                    | 5.08 us: 1.05x faster                                                            |
| xml_etree_parse      | 162 ms                                                     | 154 ms: 1.05x faster                                                             |
| json_loads           | 28.9 us                                                    | 27.9 us: 1.03x faster                                                            |
| pickle_list          | 5.11 us                                                    | 4.97 us: 1.03x faster                                                            |
| pickle_dict          | 34.8 us                                                    | 34.4 us: 1.01x faster                                                            |
| pickle               | 11.5 us                                                    | 11.7 us: 1.02x slower                                                            |
| pickle_pure_python   | 305 us                                                     | 316 us: 1.04x slower                                                             |
| unpickle             | 15.1 us                                                    | 17.0 us: 1.13x slower                                                            |
| xml_etree_process    | 61.2 ms                                                    | 70.8 ms: 1.16x slower                                                            |
| xml_etree_generate   | 87.4 ms                                                    | 104 ms: 1.19x slower                                                             |
| xml_etree_iterparse  | 107 ms                                                     | 130 ms: 1.21x slower                                                             |
| tomli_loads          | 2.12 sec                                                   | 3.52 sec: 1.66x slower                                                           |
| unpickle_pure_python | 218 us                                                     | 404 us: 1.85x slower                                                             |
| Geometric mean       | (ref)                                                      | 1.12x slower                                                                     |

Benchmark hidden because not significant (1): json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240418-linux-x86_64-faster%2dcpython-more_tier2_binary_op-3.13.0a6+-f1ab270 |
|------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                            |
| python_startup_no_site | 7.11 ms                                                    | 7.12 ms: 1.00x slower                                                            |
| Geometric mean         | (ref)                                                      | 1.01x faster                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240418-linux-x86_64-faster%2dcpython-more_tier2_binary_op-3.13.0a6+-f1ab270 |
|-----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_text     | 23.7 ms                                                    | 26.9 ms: 1.14x slower                                                            |
| genshi_xml      | 51.6 ms                                                    | 64.0 ms: 1.24x slower                                                            |
| django_template | 34.8 ms                                                    | 43.3 ms: 1.24x slower                                                            |
| mako            | 11.2 ms                                                    | 21.1 ms: 1.88x slower                                                            |
| Geometric mean  | (ref)                                                      | 1.35x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240418-linux-x86_64-faster%2dcpython-more_tier2_binary_op-3.13.0a6+-f1ab270 |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 130 us: 1.26x faster                                                             |
| unpickle_list              | 5.34 us                                                    | 5.08 us: 1.05x faster                                                            |
| xml_etree_parse            | 162 ms                                                     | 154 ms: 1.05x faster                                                             |
| json_loads                 | 28.9 us                                                    | 27.9 us: 1.03x faster                                                            |
| coroutines                 | 23.2 ms                                                    | 22.5 ms: 1.03x faster                                                            |
| json                       | 5.31 ms                                                    | 5.16 ms: 1.03x faster                                                            |
| pickle_list                | 5.11 us                                                    | 4.97 us: 1.03x faster                                                            |
| python_startup             | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                            |
| gc_traversal               | 3.98 ms                                                    | 3.90 ms: 1.02x faster                                                            |
| regex_effbot               | 3.67 ms                                                    | 3.61 ms: 1.02x faster                                                            |
| create_gc_cycles           | 1.82 ms                                                    | 1.79 ms: 1.02x faster                                                            |
| pickle_dict                | 34.8 us                                                    | 34.4 us: 1.01x faster                                                            |
| python_startup_no_site     | 7.11 ms                                                    | 7.12 ms: 1.00x slower                                                            |
| generators                 | 29.6 ms                                                    | 29.7 ms: 1.00x slower                                                            |
| deepcopy_reduce            | 3.35 us                                                    | 3.39 us: 1.01x slower                                                            |
| asyncio_tcp                | 508 ms                                                     | 514 ms: 1.01x slower                                                             |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.87 sec: 1.01x slower                                                           |
| thrift                     | 823 us                                                     | 836 us: 1.02x slower                                                             |
| regex_dna                  | 221 ms                                                     | 226 ms: 1.02x slower                                                             |
| pickle                     | 11.5 us                                                    | 11.7 us: 1.02x slower                                                            |
| regex_v8                   | 25.1 ms                                                    | 25.8 ms: 1.03x slower                                                            |
| pickle_pure_python         | 305 us                                                     | 316 us: 1.04x slower                                                             |
| logging_silent             | 105 ns                                                     | 109 ns: 1.04x slower                                                             |
| gunicorn                   | 1.28 ms                                                    | 1.34 ms: 1.05x slower                                                            |
| dask                       | 369 ms                                                     | 388 ms: 1.05x slower                                                             |
| async_tree_none            | 378 ms                                                     | 397 ms: 1.05x slower                                                             |
| sqlite_synth               | 2.99 us                                                    | 3.15 us: 1.06x slower                                                            |
| coverage                   | 93.1 ms                                                    | 98.5 ms: 1.06x slower                                                            |
| pidigits                   | 191 ms                                                     | 202 ms: 1.06x slower                                                             |
| aiohttp                    | 1.18 ms                                                    | 1.25 ms: 1.06x slower                                                            |
| pathlib                    | 17.3 ms                                                    | 18.5 ms: 1.07x slower                                                            |
| deepcopy                   | 367 us                                                     | 395 us: 1.07x slower                                                             |
| async_tree_io              | 939 ms                                                     | 1.01 sec: 1.07x slower                                                           |
| mdp                        | 2.79 sec                                                   | 3.01 sec: 1.08x slower                                                           |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 661 ms: 1.08x slower                                                             |
| async_tree_io_tg           | 936 ms                                                     | 1.02 sec: 1.09x slower                                                           |
| async_tree_memoization_tg  | 444 ms                                                     | 485 ms: 1.09x slower                                                             |
| tornado_http               | 94.6 ms                                                    | 103 ms: 1.09x slower                                                             |
| html5lib                   | 67.2 ms                                                    | 73.7 ms: 1.10x slower                                                            |
| async_tree_none_tg         | 336 ms                                                     | 371 ms: 1.10x slower                                                             |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 651 ms: 1.11x slower                                                             |
| bench_thread_pool          | 834 us                                                     | 928 us: 1.11x slower                                                             |
| mypy2                      | 742 ms                                                     | 831 ms: 1.12x slower                                                             |
| unpickle                   | 15.1 us                                                    | 17.0 us: 1.13x slower                                                            |
| dulwich_log                | 67.2 ms                                                    | 75.8 ms: 1.13x slower                                                            |
| chameleon                  | 7.22 ms                                                    | 8.18 ms: 1.13x slower                                                            |
| pylint                     | 317 ms                                                     | 360 ms: 1.13x slower                                                             |
| genshi_text                | 23.7 ms                                                    | 26.9 ms: 1.14x slower                                                            |
| async_generators           | 442 ms                                                     | 503 ms: 1.14x slower                                                             |
| logging_format             | 6.47 us                                                    | 7.39 us: 1.14x slower                                                            |
| async_tree_memoization     | 463 ms                                                     | 530 ms: 1.14x slower                                                             |
| logging_simple             | 5.74 us                                                    | 6.58 us: 1.15x slower                                                            |
| docutils                   | 2.83 sec                                                   | 3.27 sec: 1.15x slower                                                           |
| xml_etree_process          | 61.2 ms                                                    | 70.8 ms: 1.16x slower                                                            |
| telco                      | 8.41 ms                                                    | 9.78 ms: 1.16x slower                                                            |
| pycparser                  | 1.16 sec                                                   | 1.35 sec: 1.16x slower                                                           |
| sympy_expand               | 473 ms                                                     | 556 ms: 1.18x slower                                                             |
| xml_etree_generate         | 87.4 ms                                                    | 104 ms: 1.19x slower                                                             |
| 2to3                       | 274 ms                                                     | 330 ms: 1.20x slower                                                             |
| sqlglot_transpile          | 1.63 ms                                                    | 1.97 ms: 1.21x slower                                                            |
| sqlglot_normalize          | 110 ms                                                     | 133 ms: 1.21x slower                                                             |
| xml_etree_iterparse        | 107 ms                                                     | 130 ms: 1.21x slower                                                             |
| sympy_sum                  | 156 ms                                                     | 191 ms: 1.23x slower                                                             |
| sympy_str                  | 282 ms                                                     | 347 ms: 1.23x slower                                                             |
| sqlglot_parse              | 1.32 ms                                                    | 1.63 ms: 1.24x slower                                                            |
| sympy_integrate            | 20.5 ms                                                    | 25.3 ms: 1.24x slower                                                            |
| genshi_xml                 | 51.6 ms                                                    | 64.0 ms: 1.24x slower                                                            |
| django_template            | 34.8 ms                                                    | 43.3 ms: 1.24x slower                                                            |
| deepcopy_memo              | 39.7 us                                                    | 49.9 us: 1.26x slower                                                            |
| sqlglot_optimize           | 55.5 ms                                                    | 70.4 ms: 1.27x slower                                                            |
| meteor_contest             | 110 ms                                                     | 145 ms: 1.32x slower                                                             |
| scimark_sor                | 127 ms                                                     | 174 ms: 1.37x slower                                                             |
| raytrace                   | 267 ms                                                     | 378 ms: 1.42x slower                                                             |
| richards_super             | 57.4 ms                                                    | 81.6 ms: 1.42x slower                                                            |
| richards                   | 50.9 ms                                                    | 75.2 ms: 1.48x slower                                                            |
| deltablue                  | 3.25 ms                                                    | 5.02 ms: 1.54x slower                                                            |
| go                         | 145 ms                                                     | 229 ms: 1.58x slower                                                             |
| regex_compile              | 137 ms                                                     | 220 ms: 1.61x slower                                                             |
| scimark_fft                | 392 ms                                                     | 633 ms: 1.61x slower                                                             |
| pprint_safe_repr           | 758 ms                                                     | 1.25 sec: 1.65x slower                                                           |
| crypto_pyaes               | 77.5 ms                                                    | 128 ms: 1.66x slower                                                             |
| tomli_loads                | 2.12 sec                                                   | 3.52 sec: 1.66x slower                                                           |
| pprint_pformat             | 1.56 sec                                                   | 2.60 sec: 1.67x slower                                                           |
| chaos                      | 61.3 ms                                                    | 103 ms: 1.68x slower                                                             |
| scimark_lu                 | 122 ms                                                     | 208 ms: 1.71x slower                                                             |
| float                      | 78.9 ms                                                    | 135 ms: 1.71x slower                                                             |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 9.00 ms: 1.71x slower                                                            |
| pyflate                    | 484 ms                                                     | 878 ms: 1.81x slower                                                             |
| unpickle_pure_python       | 218 us                                                     | 404 us: 1.85x slower                                                             |
| nqueens                    | 81.4 ms                                                    | 153 ms: 1.87x slower                                                             |
| mako                       | 11.2 ms                                                    | 21.1 ms: 1.88x slower                                                            |
| fannkuch                   | 402 ms                                                     | 764 ms: 1.90x slower                                                             |
| scimark_monte_carlo        | 69.2 ms                                                    | 139 ms: 2.01x slower                                                             |
| spectral_norm              | 116 ms                                                     | 242 ms: 2.08x slower                                                             |
| comprehensions             | 16.6 us                                                    | 36.1 us: 2.18x slower                                                            |
| nbody                      | 88.3 ms                                                    | 209 ms: 2.36x slower                                                             |
| hexiom                     | 6.30 ms                                                    | 15.1 ms: 2.40x slower                                                            |
| Geometric mean             | (ref)                                                      | 1.23x slower                                                                     |

Benchmark hidden because not significant (4): asyncio_websockets, json_dumps, bench_mp_pool, djangocms
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.14x
- 95% likely to have a slowdown of 1.13x
- 99% likely to have a slowdown of 1.12x

# Memory
- memory change: 0.99x