# Results vs. 3.13.0b2

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: linux-x86_64
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.11x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 314 ms: 1.15x slower                                                   |
| chameleon      | 7.22 ms                                                    | 7.49 ms: 1.04x slower                                                  |
| docutils       | 2.83 sec                                                   | 3.15 sec: 1.11x slower                                                 |
| html5lib       | 67.2 ms                                                    | 71.8 ms: 1.07x slower                                                  |
| tornado_http   | 94.6 ms                                                    | 102 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                      | 1.09x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 939 ms                                                     | 967 ms: 1.03x slower                                                   |
| async_tree_none_tg         | 336 ms                                                     | 348 ms: 1.03x slower                                                   |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 638 ms: 1.04x slower                                                   |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 623 ms: 1.06x slower                                                   |
| async_tree_memoization     | 463 ms                                                     | 502 ms: 1.08x slower                                                   |
| Geometric mean             | (ref)                                                      | 1.04x slower                                                           |

Benchmark hidden because not significant (3): async_tree_none, async_tree_io_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 191 ms                                                     | 212 ms: 1.11x slower                                                   |
| float          | 78.9 ms                                                    | 90.3 ms: 1.15x slower                                                  |
| nbody          | 88.3 ms                                                    | 127 ms: 1.44x slower                                                   |
| Geometric mean | (ref)                                                      | 1.22x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8       | 25.1 ms                                                    | 26.4 ms: 1.05x slower                                                  |
| regex_dna      | 221 ms                                                     | 233 ms: 1.05x slower                                                   |
| regex_effbot   | 3.67 ms                                                    | 3.89 ms: 1.06x slower                                                  |
| regex_compile  | 137 ms                                                     | 178 ms: 1.30x slower                                                   |
| Geometric mean | (ref)                                                      | 1.11x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 162 ms                                                     | 152 ms: 1.07x faster                                                   |
| json_loads           | 28.9 us                                                    | 27.5 us: 1.05x faster                                                  |
| unpickle_list        | 5.34 us                                                    | 5.29 us: 1.01x faster                                                  |
| pickle_dict          | 34.8 us                                                    | 34.9 us: 1.00x slower                                                  |
| pickle               | 11.5 us                                                    | 11.6 us: 1.01x slower                                                  |
| unpickle             | 15.1 us                                                    | 15.5 us: 1.02x slower                                                  |
| xml_etree_iterparse  | 107 ms                                                     | 112 ms: 1.04x slower                                                   |
| pickle_pure_python   | 305 us                                                     | 319 us: 1.04x slower                                                   |
| xml_etree_process    | 61.2 ms                                                    | 65.2 ms: 1.07x slower                                                  |
| xml_etree_generate   | 87.4 ms                                                    | 94.0 ms: 1.08x slower                                                  |
| tomli_loads          | 2.12 sec                                                   | 2.53 sec: 1.19x slower                                                 |
| unpickle_pure_python | 218 us                                                     | 289 us: 1.33x slower                                                   |
| Geometric mean       | (ref)                                                      | 1.04x slower                                                           |

Benchmark hidden because not significant (2): json_dumps, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                  |
| python_startup_no_site | 7.11 ms                                                    | 7.14 ms: 1.00x slower                                                  |
| Geometric mean         | (ref)                                                      | 1.01x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 34.8 ms                                                    | 40.2 ms: 1.16x slower                                                  |
| mako            | 11.2 ms                                                    | 13.5 ms: 1.20x slower                                                  |
| genshi_text     | 23.7 ms                                                    | 30.8 ms: 1.30x slower                                                  |
| genshi_xml      | 51.6 ms                                                    | 69.1 ms: 1.34x slower                                                  |
| Geometric mean  | (ref)                                                      | 1.25x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse            | 162 ms                                                     | 152 ms: 1.07x faster                                                   |
| json_loads                 | 28.9 us                                                    | 27.5 us: 1.05x faster                                                  |
| create_gc_cycles           | 1.82 ms                                                    | 1.78 ms: 1.02x faster                                                  |
| python_startup             | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                  |
| json                       | 5.31 ms                                                    | 5.24 ms: 1.01x faster                                                  |
| unpickle_list              | 5.34 us                                                    | 5.29 us: 1.01x faster                                                  |
| deepcopy_reduce            | 3.35 us                                                    | 3.33 us: 1.01x faster                                                  |
| pickle_dict                | 34.8 us                                                    | 34.9 us: 1.00x slower                                                  |
| python_startup_no_site     | 7.11 ms                                                    | 7.14 ms: 1.00x slower                                                  |
| pickle                     | 11.5 us                                                    | 11.6 us: 1.01x slower                                                  |
| mdp                        | 2.79 sec                                                   | 2.83 sec: 1.01x slower                                                 |
| sqlite_synth               | 2.99 us                                                    | 3.04 us: 1.02x slower                                                  |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.87 sec: 1.02x slower                                                 |
| unpickle                   | 15.1 us                                                    | 15.5 us: 1.02x slower                                                  |
| gc_traversal               | 3.98 ms                                                    | 4.06 ms: 1.02x slower                                                  |
| thrift                     | 823 us                                                     | 844 us: 1.03x slower                                                   |
| async_tree_io              | 939 ms                                                     | 967 ms: 1.03x slower                                                   |
| async_tree_none_tg         | 336 ms                                                     | 348 ms: 1.03x slower                                                   |
| deepcopy                   | 367 us                                                     | 380 us: 1.04x slower                                                   |
| coroutines                 | 23.2 ms                                                    | 24.0 ms: 1.04x slower                                                  |
| chameleon                  | 7.22 ms                                                    | 7.49 ms: 1.04x slower                                                  |
| xml_etree_iterparse        | 107 ms                                                     | 112 ms: 1.04x slower                                                   |
| asyncio_tcp                | 508 ms                                                     | 530 ms: 1.04x slower                                                   |
| pickle_pure_python         | 305 us                                                     | 319 us: 1.04x slower                                                   |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 638 ms: 1.04x slower                                                   |
| gunicorn                   | 1.28 ms                                                    | 1.34 ms: 1.05x slower                                                  |
| dask                       | 369 ms                                                     | 387 ms: 1.05x slower                                                   |
| pathlib                    | 17.3 ms                                                    | 18.2 ms: 1.05x slower                                                  |
| regex_v8                   | 25.1 ms                                                    | 26.4 ms: 1.05x slower                                                  |
| regex_dna                  | 221 ms                                                     | 233 ms: 1.05x slower                                                   |
| aiohttp                    | 1.18 ms                                                    | 1.24 ms: 1.05x slower                                                  |
| regex_effbot               | 3.67 ms                                                    | 3.89 ms: 1.06x slower                                                  |
| generators                 | 29.6 ms                                                    | 31.4 ms: 1.06x slower                                                  |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 623 ms: 1.06x slower                                                   |
| xml_etree_process          | 61.2 ms                                                    | 65.2 ms: 1.07x slower                                                  |
| html5lib                   | 67.2 ms                                                    | 71.8 ms: 1.07x slower                                                  |
| async_generators           | 442 ms                                                     | 475 ms: 1.07x slower                                                   |
| xml_etree_generate         | 87.4 ms                                                    | 94.0 ms: 1.08x slower                                                  |
| tornado_http               | 94.6 ms                                                    | 102 ms: 1.08x slower                                                   |
| bench_thread_pool          | 834 us                                                     | 902 us: 1.08x slower                                                   |
| deepcopy_memo              | 39.7 us                                                    | 43.0 us: 1.08x slower                                                  |
| async_tree_memoization     | 463 ms                                                     | 502 ms: 1.08x slower                                                   |
| richards_super             | 57.4 ms                                                    | 62.4 ms: 1.09x slower                                                  |
| richards                   | 50.9 ms                                                    | 55.5 ms: 1.09x slower                                                  |
| telco                      | 8.41 ms                                                    | 9.18 ms: 1.09x slower                                                  |
| pylint                     | 317 ms                                                     | 350 ms: 1.10x slower                                                   |
| sqlglot_transpile          | 1.63 ms                                                    | 1.81 ms: 1.11x slower                                                  |
| mypy2                      | 742 ms                                                     | 823 ms: 1.11x slower                                                   |
| pidigits                   | 191 ms                                                     | 212 ms: 1.11x slower                                                   |
| docutils                   | 2.83 sec                                                   | 3.15 sec: 1.11x slower                                                 |
| dulwich_log                | 67.2 ms                                                    | 75.0 ms: 1.12x slower                                                  |
| meteor_contest             | 110 ms                                                     | 123 ms: 1.12x slower                                                   |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 5.94 ms: 1.13x slower                                                  |
| sympy_sum                  | 156 ms                                                     | 176 ms: 1.13x slower                                                   |
| sqlglot_parse              | 1.32 ms                                                    | 1.49 ms: 1.13x slower                                                  |
| sympy_expand               | 473 ms                                                     | 537 ms: 1.14x slower                                                   |
| sympy_integrate            | 20.5 ms                                                    | 23.3 ms: 1.14x slower                                                  |
| sympy_str                  | 282 ms                                                     | 322 ms: 1.14x slower                                                   |
| float                      | 78.9 ms                                                    | 90.3 ms: 1.15x slower                                                  |
| 2to3                       | 274 ms                                                     | 314 ms: 1.15x slower                                                   |
| scimark_fft                | 392 ms                                                     | 452 ms: 1.15x slower                                                   |
| pycparser                  | 1.16 sec                                                   | 1.34 sec: 1.15x slower                                                 |
| django_template            | 34.8 ms                                                    | 40.2 ms: 1.16x slower                                                  |
| sqlglot_normalize          | 110 ms                                                     | 128 ms: 1.16x slower                                                   |
| sqlglot_optimize           | 55.5 ms                                                    | 64.5 ms: 1.16x slower                                                  |
| logging_format             | 6.47 us                                                    | 7.62 us: 1.18x slower                                                  |
| logging_simple             | 5.74 us                                                    | 6.81 us: 1.19x slower                                                  |
| crypto_pyaes               | 77.5 ms                                                    | 92.3 ms: 1.19x slower                                                  |
| tomli_loads                | 2.12 sec                                                   | 2.53 sec: 1.19x slower                                                 |
| typing_runtime_protocols   | 165 us                                                     | 197 us: 1.20x slower                                                   |
| mako                       | 11.2 ms                                                    | 13.5 ms: 1.20x slower                                                  |
| raytrace                   | 267 ms                                                     | 324 ms: 1.21x slower                                                   |
| spectral_norm              | 116 ms                                                     | 143 ms: 1.23x slower                                                   |
| scimark_sor                | 127 ms                                                     | 157 ms: 1.23x slower                                                   |
| fannkuch                   | 402 ms                                                     | 497 ms: 1.24x slower                                                   |
| pyflate                    | 484 ms                                                     | 606 ms: 1.25x slower                                                   |
| pprint_safe_repr           | 758 ms                                                     | 956 ms: 1.26x slower                                                   |
| pprint_pformat             | 1.56 sec                                                   | 1.99 sec: 1.28x slower                                                 |
| chaos                      | 61.3 ms                                                    | 79.3 ms: 1.29x slower                                                  |
| genshi_text                | 23.7 ms                                                    | 30.8 ms: 1.30x slower                                                  |
| regex_compile              | 137 ms                                                     | 178 ms: 1.30x slower                                                   |
| scimark_monte_carlo        | 69.2 ms                                                    | 90.6 ms: 1.31x slower                                                  |
| unpickle_pure_python       | 218 us                                                     | 289 us: 1.33x slower                                                   |
| genshi_xml                 | 51.6 ms                                                    | 69.1 ms: 1.34x slower                                                  |
| nqueens                    | 81.4 ms                                                    | 110 ms: 1.35x slower                                                   |
| deltablue                  | 3.25 ms                                                    | 4.40 ms: 1.35x slower                                                  |
| go                         | 145 ms                                                     | 197 ms: 1.36x slower                                                   |
| scimark_lu                 | 122 ms                                                     | 172 ms: 1.41x slower                                                   |
| nbody                      | 88.3 ms                                                    | 127 ms: 1.44x slower                                                   |
| comprehensions             | 16.6 us                                                    | 24.9 us: 1.50x slower                                                  |
| hexiom                     | 6.30 ms                                                    | 9.97 ms: 1.58x slower                                                  |
| Geometric mean             | (ref)                                                      | 1.11x slower                                                           |

Benchmark hidden because not significant (10): json_dumps, async_tree_none, coverage, logging_silent, asyncio_websockets, pickle_list, bench_mp_pool, djangocms, async_tree_io_tg, async_tree_memoization_tg
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 1.00x