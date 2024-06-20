# Results vs. 3.13.0b2

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: linux-x86_64
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.01x slower
- HPT reliability: 99.27%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.07x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 282 ms: 1.03x slower                                                   |
| chameleon      | 7.22 ms                                                    | 7.03 ms: 1.03x faster                                                  |
| docutils       | 2.83 sec                                                   | 2.96 sec: 1.05x slower                                                 |
| html5lib       | 67.2 ms                                                    | 68.5 ms: 1.02x slower                                                  |
| tornado_http   | 94.6 ms                                                    | 96.6 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                      | 1.02x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 361 ms: 1.05x faster                                                   |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 607 ms: 1.03x slower                                                   |
| Geometric mean             | (ref)                                                      | 1.00x slower                                                           |

Benchmark hidden because not significant (6): async_tree_memoization_tg, async_tree_cpu_io_mixed, async_tree_none_tg, async_tree_memoization, async_tree_io, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 78.9 ms                                                    | 76.9 ms: 1.03x faster                                                  |
| pidigits       | 191 ms                                                     | 189 ms: 1.01x faster                                                   |
| nbody          | 88.3 ms                                                    | 92.8 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                      | 1.00x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8       | 25.1 ms                                                    | 24.3 ms: 1.03x faster                                                  |
| regex_dna      | 221 ms                                                     | 218 ms: 1.02x faster                                                   |
| regex_effbot   | 3.67 ms                                                    | 3.64 ms: 1.01x faster                                                  |
| regex_compile  | 137 ms                                                     | 143 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                      | 1.00x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 162 ms                                                     | 152 ms: 1.07x faster                                                   |
| json_loads           | 28.9 us                                                    | 27.3 us: 1.06x faster                                                  |
| tomli_loads          | 2.12 sec                                                   | 2.04 sec: 1.04x faster                                                 |
| xml_etree_iterparse  | 107 ms                                                     | 104 ms: 1.03x faster                                                   |
| json_dumps           | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                                  |
| xml_etree_process    | 61.2 ms                                                    | 60.6 ms: 1.01x faster                                                  |
| pickle_dict          | 34.8 us                                                    | 34.7 us: 1.00x faster                                                  |
| xml_etree_generate   | 87.4 ms                                                    | 87.9 ms: 1.00x slower                                                  |
| unpickle             | 15.1 us                                                    | 15.2 us: 1.01x slower                                                  |
| pickle_pure_python   | 305 us                                                     | 311 us: 1.02x slower                                                   |
| pickle               | 11.5 us                                                    | 11.7 us: 1.02x slower                                                  |
| unpickle_pure_python | 218 us                                                     | 235 us: 1.08x slower                                                   |
| Geometric mean       | (ref)                                                      | 1.01x faster                                                           |

Benchmark hidden because not significant (2): pickle_list, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 11.0 ms: 1.03x slower                                                  |
| python_startup_no_site | 7.11 ms                                                    | 7.61 ms: 1.07x slower                                                  |
| Geometric mean         | (ref)                                                      | 1.05x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 10.7 ms: 1.06x faster                                                  |
| django_template | 34.8 ms                                                    | 37.0 ms: 1.06x slower                                                  |
| genshi_text     | 23.7 ms                                                    | 26.5 ms: 1.12x slower                                                  |
| genshi_xml      | 51.6 ms                                                    | 57.9 ms: 1.12x slower                                                  |
| Geometric mean  | (ref)                                                      | 1.06x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| richards                   | 50.9 ms                                                    | 43.2 ms: 1.18x faster                                                  |
| richards_super             | 57.4 ms                                                    | 49.0 ms: 1.17x faster                                                  |
| scimark_fft                | 392 ms                                                     | 344 ms: 1.14x faster                                                   |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 4.94 ms: 1.07x faster                                                  |
| xml_etree_parse            | 162 ms                                                     | 152 ms: 1.07x faster                                                   |
| mdp                        | 2.79 sec                                                   | 2.62 sec: 1.06x faster                                                 |
| json_loads                 | 28.9 us                                                    | 27.3 us: 1.06x faster                                                  |
| mako                       | 11.2 ms                                                    | 10.7 ms: 1.06x faster                                                  |
| fannkuch                   | 402 ms                                                     | 383 ms: 1.05x faster                                                   |
| async_tree_none            | 378 ms                                                     | 361 ms: 1.05x faster                                                   |
| sqlite_synth               | 2.99 us                                                    | 2.85 us: 1.05x faster                                                  |
| pyflate                    | 484 ms                                                     | 463 ms: 1.04x faster                                                   |
| crypto_pyaes               | 77.5 ms                                                    | 74.3 ms: 1.04x faster                                                  |
| tomli_loads                | 2.12 sec                                                   | 2.04 sec: 1.04x faster                                                 |
| json                       | 5.31 ms                                                    | 5.10 ms: 1.04x faster                                                  |
| regex_v8                   | 25.1 ms                                                    | 24.3 ms: 1.03x faster                                                  |
| xml_etree_iterparse        | 107 ms                                                     | 104 ms: 1.03x faster                                                   |
| deepcopy_reduce            | 3.35 us                                                    | 3.25 us: 1.03x faster                                                  |
| chameleon                  | 7.22 ms                                                    | 7.03 ms: 1.03x faster                                                  |
| float                      | 78.9 ms                                                    | 76.9 ms: 1.03x faster                                                  |
| pprint_safe_repr           | 758 ms                                                     | 740 ms: 1.03x faster                                                   |
| logging_silent             | 105 ns                                                     | 103 ns: 1.02x faster                                                   |
| pprint_pformat             | 1.56 sec                                                   | 1.53 sec: 1.02x faster                                                 |
| create_gc_cycles           | 1.82 ms                                                    | 1.78 ms: 1.02x faster                                                  |
| json_dumps                 | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                                  |
| coroutines                 | 23.2 ms                                                    | 22.8 ms: 1.02x faster                                                  |
| regex_dna                  | 221 ms                                                     | 218 ms: 1.02x faster                                                   |
| spectral_norm              | 116 ms                                                     | 114 ms: 1.01x faster                                                   |
| deepcopy_memo              | 39.7 us                                                    | 39.3 us: 1.01x faster                                                  |
| pidigits                   | 191 ms                                                     | 189 ms: 1.01x faster                                                   |
| coverage                   | 93.1 ms                                                    | 92.2 ms: 1.01x faster                                                  |
| xml_etree_process          | 61.2 ms                                                    | 60.6 ms: 1.01x faster                                                  |
| regex_effbot               | 3.67 ms                                                    | 3.64 ms: 1.01x faster                                                  |
| asyncio_websockets         | 567 ms                                                     | 564 ms: 1.00x faster                                                   |
| pickle_dict                | 34.8 us                                                    | 34.7 us: 1.00x faster                                                  |
| xml_etree_generate         | 87.4 ms                                                    | 87.9 ms: 1.00x slower                                                  |
| deepcopy                   | 367 us                                                     | 369 us: 1.01x slower                                                   |
| unpickle                   | 15.1 us                                                    | 15.2 us: 1.01x slower                                                  |
| sqlglot_parse              | 1.32 ms                                                    | 1.33 ms: 1.01x slower                                                  |
| gc_traversal               | 3.98 ms                                                    | 4.02 ms: 1.01x slower                                                  |
| pycparser                  | 1.16 sec                                                   | 1.17 sec: 1.01x slower                                                 |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.86 sec: 1.01x slower                                                 |
| meteor_contest             | 110 ms                                                     | 111 ms: 1.01x slower                                                   |
| sqlglot_transpile          | 1.63 ms                                                    | 1.66 ms: 1.02x slower                                                  |
| pickle_pure_python         | 305 us                                                     | 311 us: 1.02x slower                                                   |
| dask                       | 369 ms                                                     | 376 ms: 1.02x slower                                                   |
| html5lib                   | 67.2 ms                                                    | 68.5 ms: 1.02x slower                                                  |
| tornado_http               | 94.6 ms                                                    | 96.6 ms: 1.02x slower                                                  |
| pickle                     | 11.5 us                                                    | 11.7 us: 1.02x slower                                                  |
| pathlib                    | 17.3 ms                                                    | 17.7 ms: 1.02x slower                                                  |
| logging_format             | 6.47 us                                                    | 6.63 us: 1.02x slower                                                  |
| gunicorn                   | 1.28 ms                                                    | 1.31 ms: 1.02x slower                                                  |
| generators                 | 29.6 ms                                                    | 30.4 ms: 1.03x slower                                                  |
| python_startup             | 10.8 ms                                                    | 11.0 ms: 1.03x slower                                                  |
| 2to3                       | 274 ms                                                     | 282 ms: 1.03x slower                                                   |
| asyncio_tcp                | 508 ms                                                     | 522 ms: 1.03x slower                                                   |
| telco                      | 8.41 ms                                                    | 8.66 ms: 1.03x slower                                                  |
| djangocms                  | 31.5 us                                                    | 32.5 us: 1.03x slower                                                  |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 607 ms: 1.03x slower                                                   |
| dulwich_log                | 67.2 ms                                                    | 69.6 ms: 1.04x slower                                                  |
| aiohttp                    | 1.18 ms                                                    | 1.22 ms: 1.04x slower                                                  |
| chaos                      | 61.3 ms                                                    | 63.7 ms: 1.04x slower                                                  |
| logging_simple             | 5.74 us                                                    | 5.97 us: 1.04x slower                                                  |
| sqlglot_normalize          | 110 ms                                                     | 115 ms: 1.04x slower                                                   |
| regex_compile              | 137 ms                                                     | 143 ms: 1.04x slower                                                   |
| bench_thread_pool          | 834 us                                                     | 870 us: 1.04x slower                                                   |
| docutils                   | 2.83 sec                                                   | 2.96 sec: 1.05x slower                                                 |
| raytrace                   | 267 ms                                                     | 279 ms: 1.05x slower                                                   |
| sqlglot_optimize           | 55.5 ms                                                    | 58.3 ms: 1.05x slower                                                  |
| async_generators           | 442 ms                                                     | 465 ms: 1.05x slower                                                   |
| nbody                      | 88.3 ms                                                    | 92.8 ms: 1.05x slower                                                  |
| sympy_str                  | 282 ms                                                     | 299 ms: 1.06x slower                                                   |
| typing_runtime_protocols   | 165 us                                                     | 175 us: 1.06x slower                                                   |
| sympy_expand               | 473 ms                                                     | 502 ms: 1.06x slower                                                   |
| django_template            | 34.8 ms                                                    | 37.0 ms: 1.06x slower                                                  |
| python_startup_no_site     | 7.11 ms                                                    | 7.61 ms: 1.07x slower                                                  |
| unpickle_pure_python       | 218 us                                                     | 235 us: 1.08x slower                                                   |
| go                         | 145 ms                                                     | 156 ms: 1.08x slower                                                   |
| pylint                     | 317 ms                                                     | 346 ms: 1.09x slower                                                   |
| sympy_sum                  | 156 ms                                                     | 170 ms: 1.09x slower                                                   |
| mypy2                      | 742 ms                                                     | 813 ms: 1.10x slower                                                   |
| scimark_sor                | 127 ms                                                     | 140 ms: 1.10x slower                                                   |
| comprehensions             | 16.6 us                                                    | 18.3 us: 1.10x slower                                                  |
| sympy_integrate            | 20.5 ms                                                    | 22.6 ms: 1.10x slower                                                  |
| scimark_lu                 | 122 ms                                                     | 136 ms: 1.12x slower                                                   |
| genshi_text                | 23.7 ms                                                    | 26.5 ms: 1.12x slower                                                  |
| genshi_xml                 | 51.6 ms                                                    | 57.9 ms: 1.12x slower                                                  |
| nqueens                    | 81.4 ms                                                    | 92.1 ms: 1.13x slower                                                  |
| hexiom                     | 6.30 ms                                                    | 7.16 ms: 1.14x slower                                                  |
| deltablue                  | 3.25 ms                                                    | 3.85 ms: 1.18x slower                                                  |
| Geometric mean             | (ref)                                                      | 1.01x slower                                                           |

Benchmark hidden because not significant (11): async_tree_memoization_tg, thrift, scimark_monte_carlo, pickle_list, unpickle_list, async_tree_cpu_io_mixed, bench_mp_pool, async_tree_none_tg, async_tree_memoization, async_tree_io, async_tree_io_tg
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 99.27% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.07x