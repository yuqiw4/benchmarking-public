# Results vs. 3.13.0b2

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: linux-x86_64
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.01x faster
- HPT reliability: 98.47%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 271 ms: 1.01x faster                                                   |
| chameleon      | 7.22 ms                                                    | 7.29 ms: 1.01x slower                                                  |
| html5lib       | 67.2 ms                                                    | 68.3 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                      | 1.00x slower                                                           |

Benchmark hidden because not significant (2): docutils, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 353 ms: 1.07x faster                                                   |
| async_tree_io              | 939 ms                                                     | 908 ms: 1.03x faster                                                   |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 605 ms: 1.03x slower                                                   |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                           |

Benchmark hidden because not significant (5): async_tree_memoization_tg, async_tree_memoization, async_tree_none_tg, async_tree_io_tg, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 191 ms                                                     | 194 ms: 1.01x slower                                                   |
| nbody          | 88.3 ms                                                    | 92.5 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                      | 1.02x slower                                                           |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8       | 25.1 ms                                                    | 24.9 ms: 1.01x faster                                                  |
| regex_compile  | 137 ms                                                     | 136 ms: 1.00x faster                                                   |
| regex_dna      | 221 ms                                                     | 227 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                      | 1.00x slower                                                           |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_loads           | 28.9 us                                                    | 27.6 us: 1.05x faster                                                  |
| pickle_list          | 5.11 us                                                    | 5.02 us: 1.02x faster                                                  |
| xml_etree_process    | 61.2 ms                                                    | 60.7 ms: 1.01x faster                                                  |
| unpickle_list        | 5.34 us                                                    | 5.32 us: 1.00x faster                                                  |
| xml_etree_generate   | 87.4 ms                                                    | 87.8 ms: 1.00x slower                                                  |
| unpickle_pure_python | 218 us                                                     | 219 us: 1.01x slower                                                   |
| unpickle             | 15.1 us                                                    | 15.3 us: 1.01x slower                                                  |
| pickle_dict          | 34.8 us                                                    | 35.8 us: 1.03x slower                                                  |
| tomli_loads          | 2.12 sec                                                   | 2.20 sec: 1.04x slower                                                 |
| pickle               | 11.5 us                                                    | 12.0 us: 1.05x slower                                                  |
| Geometric mean       | (ref)                                                      | 1.00x slower                                                           |

Benchmark hidden because not significant (4): xml_etree_parse, json_dumps, xml_etree_iterparse, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                  |
| python_startup_no_site | 7.11 ms                                                    | 7.11 ms: 1.00x slower                                                  |
| Geometric mean         | (ref)                                                      | 1.01x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako           | 11.2 ms                                                    | 11.0 ms: 1.02x faster                                                  |
| genshi_xml     | 51.6 ms                                                    | 54.0 ms: 1.05x slower                                                  |
| genshi_text    | 23.7 ms                                                    | 24.8 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                      | 1.02x slower                                                           |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 353 ms: 1.07x faster                                                   |
| mdp                        | 2.79 sec                                                   | 2.62 sec: 1.07x faster                                                 |
| scimark_fft                | 392 ms                                                     | 369 ms: 1.06x faster                                                   |
| richards                   | 50.9 ms                                                    | 48.0 ms: 1.06x faster                                                  |
| richards_super             | 57.4 ms                                                    | 54.3 ms: 1.06x faster                                                  |
| gc_traversal               | 3.98 ms                                                    | 3.77 ms: 1.05x faster                                                  |
| json_loads                 | 28.9 us                                                    | 27.6 us: 1.05x faster                                                  |
| crypto_pyaes               | 77.5 ms                                                    | 74.8 ms: 1.04x faster                                                  |
| create_gc_cycles           | 1.82 ms                                                    | 1.76 ms: 1.03x faster                                                  |
| async_tree_io              | 939 ms                                                     | 908 ms: 1.03x faster                                                   |
| deepcopy_reduce            | 3.35 us                                                    | 3.24 us: 1.03x faster                                                  |
| sqlglot_parse              | 1.32 ms                                                    | 1.28 ms: 1.03x faster                                                  |
| json                       | 5.31 ms                                                    | 5.16 ms: 1.03x faster                                                  |
| sqlglot_transpile          | 1.63 ms                                                    | 1.59 ms: 1.03x faster                                                  |
| logging_silent             | 105 ns                                                     | 102 ns: 1.03x faster                                                   |
| scimark_lu                 | 122 ms                                                     | 118 ms: 1.03x faster                                                   |
| sqlite_synth               | 2.99 us                                                    | 2.92 us: 1.02x faster                                                  |
| mako                       | 11.2 ms                                                    | 11.0 ms: 1.02x faster                                                  |
| dulwich_log                | 67.2 ms                                                    | 65.8 ms: 1.02x faster                                                  |
| python_startup             | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                  |
| spectral_norm              | 116 ms                                                     | 114 ms: 1.02x faster                                                   |
| pickle_list                | 5.11 us                                                    | 5.02 us: 1.02x faster                                                  |
| deepcopy                   | 367 us                                                     | 361 us: 1.02x faster                                                   |
| deepcopy_memo              | 39.7 us                                                    | 39.1 us: 1.02x faster                                                  |
| thrift                     | 823 us                                                     | 810 us: 1.02x faster                                                   |
| go                         | 145 ms                                                     | 143 ms: 1.01x faster                                                   |
| scimark_sor                | 127 ms                                                     | 126 ms: 1.01x faster                                                   |
| chaos                      | 61.3 ms                                                    | 60.5 ms: 1.01x faster                                                  |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 5.20 ms: 1.01x faster                                                  |
| aiohttp                    | 1.18 ms                                                    | 1.17 ms: 1.01x faster                                                  |
| raytrace                   | 267 ms                                                     | 263 ms: 1.01x faster                                                   |
| 2to3                       | 274 ms                                                     | 271 ms: 1.01x faster                                                   |
| gunicorn                   | 1.28 ms                                                    | 1.26 ms: 1.01x faster                                                  |
| nqueens                    | 81.4 ms                                                    | 80.6 ms: 1.01x faster                                                  |
| logging_format             | 6.47 us                                                    | 6.41 us: 1.01x faster                                                  |
| sympy_integrate            | 20.5 ms                                                    | 20.3 ms: 1.01x faster                                                  |
| regex_v8                   | 25.1 ms                                                    | 24.9 ms: 1.01x faster                                                  |
| xml_etree_process          | 61.2 ms                                                    | 60.7 ms: 1.01x faster                                                  |
| deltablue                  | 3.25 ms                                                    | 3.23 ms: 1.01x faster                                                  |
| asyncio_websockets         | 567 ms                                                     | 564 ms: 1.01x faster                                                   |
| pprint_pformat             | 1.56 sec                                                   | 1.55 sec: 1.00x faster                                                 |
| regex_compile              | 137 ms                                                     | 136 ms: 1.00x faster                                                   |
| unpickle_list              | 5.34 us                                                    | 5.32 us: 1.00x faster                                                  |
| sqlglot_optimize           | 55.5 ms                                                    | 55.3 ms: 1.00x faster                                                  |
| python_startup_no_site     | 7.11 ms                                                    | 7.11 ms: 1.00x slower                                                  |
| sqlglot_normalize          | 110 ms                                                     | 111 ms: 1.00x slower                                                   |
| async_generators           | 442 ms                                                     | 444 ms: 1.00x slower                                                   |
| xml_etree_generate         | 87.4 ms                                                    | 87.8 ms: 1.00x slower                                                  |
| unpickle_pure_python       | 218 us                                                     | 219 us: 1.01x slower                                                   |
| chameleon                  | 7.22 ms                                                    | 7.29 ms: 1.01x slower                                                  |
| comprehensions             | 16.6 us                                                    | 16.8 us: 1.01x slower                                                  |
| hexiom                     | 6.30 ms                                                    | 6.37 ms: 1.01x slower                                                  |
| pidigits                   | 191 ms                                                     | 194 ms: 1.01x slower                                                   |
| typing_runtime_protocols   | 165 us                                                     | 167 us: 1.01x slower                                                   |
| unpickle                   | 15.1 us                                                    | 15.3 us: 1.01x slower                                                  |
| html5lib                   | 67.2 ms                                                    | 68.3 ms: 1.02x slower                                                  |
| meteor_contest             | 110 ms                                                     | 112 ms: 1.02x slower                                                   |
| pathlib                    | 17.3 ms                                                    | 17.7 ms: 1.02x slower                                                  |
| regex_dna                  | 221 ms                                                     | 227 ms: 1.03x slower                                                   |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 605 ms: 1.03x slower                                                   |
| pickle_dict                | 34.8 us                                                    | 35.8 us: 1.03x slower                                                  |
| telco                      | 8.41 ms                                                    | 8.68 ms: 1.03x slower                                                  |
| tomli_loads                | 2.12 sec                                                   | 2.20 sec: 1.04x slower                                                 |
| genshi_xml                 | 51.6 ms                                                    | 54.0 ms: 1.05x slower                                                  |
| genshi_text                | 23.7 ms                                                    | 24.8 ms: 1.05x slower                                                  |
| nbody                      | 88.3 ms                                                    | 92.5 ms: 1.05x slower                                                  |
| pickle                     | 11.5 us                                                    | 12.0 us: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                           |

Benchmark hidden because not significant (34): xml_etree_parse, sympy_str, mypy2, coroutines, async_tree_memoization_tg, coverage, json_dumps, tornado_http, sympy_expand, async_tree_memoization, generators, fannkuch, docutils, async_tree_none_tg, xml_etree_iterparse, pyflate, regex_effbot, asyncio_tcp_ssl, pprint_safe_repr, dask, pickle_pure_python, bench_mp_pool, asyncio_tcp, float, bench_thread_pool, pycparser, async_tree_io_tg, scimark_monte_carlo, django_template, sympy_sum, logging_simple, async_tree_cpu_io_mixed, djangocms, pylint
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 98.47% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.98x