# Results vs. 3.13.0b2

- fork: brandtbucher
- ref: stitch_exhausted
- machine: linux-x86_64
- commit hash: 7422720
- commit date: 2024-04-04
- overall geometric mean: 1.02x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.06x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:----------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 291 ms                                                           | 302 ms: 1.04x slower                                                           |
| chameleon      | 7.40 ms                                                          | 7.46 ms: 1.01x slower                                                          |
| docutils       | 2.98 sec                                                         | 3.12 sec: 1.04x slower                                                         |
| tornado_http   | 119 ms                                                           | 123 ms: 1.03x slower                                                           |
| Geometric mean | (ref)                                                            | 1.02x slower                                                                   |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------------|:----------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_io_tg           | 900 ms                                                           | 866 ms: 1.04x faster                                                           |
| async_tree_io              | 873 ms                                                           | 854 ms: 1.02x faster                                                           |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 596 ms: 1.04x slower                                                           |
| async_tree_none            | 365 ms                                                           | 380 ms: 1.04x slower                                                           |
| Geometric mean             | (ref)                                                            | 1.00x slower                                                                   |

Benchmark hidden because not significant (4): async_tree_memoization, async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:----------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| float          | 80.2 ms                                                          | 75.9 ms: 1.06x faster                                                          |
| pidigits       | 254 ms                                                           | 261 ms: 1.03x slower                                                           |
| nbody          | 87.8 ms                                                          | 97.1 ms: 1.11x slower                                                          |
| Geometric mean | (ref)                                                            | 1.03x slower                                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:----------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_dna      | 249 ms                                                           | 238 ms: 1.05x faster                                                           |
| regex_v8       | 26.0 ms                                                          | 25.4 ms: 1.02x faster                                                          |
| regex_effbot   | 3.40 ms                                                          | 3.50 ms: 1.03x slower                                                          |
| Geometric mean | (ref)                                                            | 1.01x faster                                                                   |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------|:----------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| tomli_loads          | 2.40 sec                                                         | 2.13 sec: 1.13x faster                                                         |
| unpickle             | 15.7 us                                                          | 15.2 us: 1.03x faster                                                          |
| json_dumps           | 10.8 ms                                                          | 10.6 ms: 1.02x faster                                                          |
| unpickle_list        | 4.70 us                                                          | 4.61 us: 1.02x faster                                                          |
| xml_etree_process    | 59.7 ms                                                          | 59.2 ms: 1.01x faster                                                          |
| xml_etree_iterparse  | 103 ms                                                           | 102 ms: 1.01x faster                                                           |
| json_loads           | 25.0 us                                                          | 25.3 us: 1.01x slower                                                          |
| pickle               | 10.6 us                                                          | 10.7 us: 1.01x slower                                                          |
| unpickle_pure_python | 224 us                                                           | 227 us: 1.01x slower                                                           |
| xml_etree_parse      | 144 ms                                                           | 147 ms: 1.02x slower                                                           |
| pickle_dict          | 32.8 us                                                          | 33.7 us: 1.03x slower                                                          |
| Geometric mean       | (ref)                                                            | 1.01x faster                                                                   |

Benchmark hidden because not significant (3): pickle_list, pickle_pure_python, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|------------------------|:----------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup         | 13.2 ms                                                          | 13.5 ms: 1.02x slower                                                          |
| python_startup_no_site | 8.85 ms                                                          | 11.8 ms: 1.33x slower                                                          |
| Geometric mean         | (ref)                                                            | 1.17x slower                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:----------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| mako           | 10.4 ms                                                          | 9.98 ms: 1.04x faster                                                          |
| genshi_xml     | 58.1 ms                                                          | 59.5 ms: 1.03x slower                                                          |
| genshi_text    | 25.9 ms                                                          | 27.2 ms: 1.05x slower                                                          |
| Geometric mean | (ref)                                                            | 1.01x slower                                                                   |

All benchmarks:
===============

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------------|:----------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 171 us                                                           | 121 us: 1.41x faster                                                           |
| richards                   | 53.4 ms                                                          | 45.3 ms: 1.18x faster                                                          |
| richards_super             | 61.2 ms                                                          | 51.9 ms: 1.18x faster                                                          |
| tomli_loads                | 2.40 sec                                                         | 2.13 sec: 1.13x faster                                                         |
| create_gc_cycles           | 2.00 ms                                                          | 1.87 ms: 1.07x faster                                                          |
| float                      | 80.2 ms                                                          | 75.9 ms: 1.06x faster                                                          |
| regex_dna                  | 249 ms                                                           | 238 ms: 1.05x faster                                                           |
| spectral_norm              | 97.3 ms                                                          | 92.8 ms: 1.05x faster                                                          |
| sqlite_synth               | 2.80 us                                                          | 2.68 us: 1.04x faster                                                          |
| mako                       | 10.4 ms                                                          | 9.98 ms: 1.04x faster                                                          |
| async_tree_io_tg           | 900 ms                                                           | 866 ms: 1.04x faster                                                           |
| unpickle                   | 15.7 us                                                          | 15.2 us: 1.03x faster                                                          |
| scimark_sparse_mat_mult    | 4.28 ms                                                          | 4.18 ms: 1.02x faster                                                          |
| regex_v8                   | 26.0 ms                                                          | 25.4 ms: 1.02x faster                                                          |
| async_tree_io              | 873 ms                                                           | 854 ms: 1.02x faster                                                           |
| json_dumps                 | 10.8 ms                                                          | 10.6 ms: 1.02x faster                                                          |
| unpickle_list              | 4.70 us                                                          | 4.61 us: 1.02x faster                                                          |
| asyncio_tcp                | 378 ms                                                           | 372 ms: 1.02x faster                                                           |
| generators                 | 33.5 ms                                                          | 33.0 ms: 1.01x faster                                                          |
| asyncio_websockets         | 395 ms                                                           | 390 ms: 1.01x faster                                                           |
| xml_etree_process          | 59.7 ms                                                          | 59.2 ms: 1.01x faster                                                          |
| deepcopy_memo              | 37.3 us                                                          | 37.0 us: 1.01x faster                                                          |
| xml_etree_iterparse        | 103 ms                                                           | 102 ms: 1.01x faster                                                           |
| gc_traversal               | 4.69 ms                                                          | 4.66 ms: 1.01x faster                                                          |
| asyncio_tcp_ssl            | 1.58 sec                                                         | 1.58 sec: 1.00x faster                                                         |
| chameleon                  | 7.40 ms                                                          | 7.46 ms: 1.01x slower                                                          |
| pyflate                    | 482 ms                                                           | 486 ms: 1.01x slower                                                           |
| json                       | 5.35 ms                                                          | 5.41 ms: 1.01x slower                                                          |
| json_loads                 | 25.0 us                                                          | 25.3 us: 1.01x slower                                                          |
| pickle                     | 10.6 us                                                          | 10.7 us: 1.01x slower                                                          |
| sqlglot_parse              | 1.39 ms                                                          | 1.41 ms: 1.01x slower                                                          |
| coroutines                 | 22.0 ms                                                          | 22.2 ms: 1.01x slower                                                          |
| unpickle_pure_python       | 224 us                                                           | 227 us: 1.01x slower                                                           |
| dulwich_log                | 67.3 ms                                                          | 68.2 ms: 1.01x slower                                                          |
| deepcopy_reduce            | 3.39 us                                                          | 3.45 us: 1.02x slower                                                          |
| pycparser                  | 1.22 sec                                                         | 1.24 sec: 1.02x slower                                                         |
| thrift                     | 880 us                                                           | 897 us: 1.02x slower                                                           |
| logging_silent             | 96.3 ns                                                          | 98.2 ns: 1.02x slower                                                          |
| python_startup             | 13.2 ms                                                          | 13.5 ms: 1.02x slower                                                          |
| xml_etree_parse            | 144 ms                                                           | 147 ms: 1.02x slower                                                           |
| genshi_xml                 | 58.1 ms                                                          | 59.5 ms: 1.03x slower                                                          |
| pickle_dict                | 32.8 us                                                          | 33.7 us: 1.03x slower                                                          |
| tornado_http               | 119 ms                                                           | 123 ms: 1.03x slower                                                           |
| sqlglot_transpile          | 1.76 ms                                                          | 1.81 ms: 1.03x slower                                                          |
| regex_effbot               | 3.40 ms                                                          | 3.50 ms: 1.03x slower                                                          |
| pprint_safe_repr           | 818 ms                                                           | 841 ms: 1.03x slower                                                           |
| pidigits                   | 254 ms                                                           | 261 ms: 1.03x slower                                                           |
| scimark_fft                | 312 ms                                                           | 322 ms: 1.03x slower                                                           |
| deepcopy                   | 377 us                                                           | 390 us: 1.03x slower                                                           |
| coverage                   | 83.5 ms                                                          | 86.4 ms: 1.04x slower                                                          |
| 2to3                       | 291 ms                                                           | 302 ms: 1.04x slower                                                           |
| pprint_pformat             | 1.66 sec                                                         | 1.72 sec: 1.04x slower                                                         |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 596 ms: 1.04x slower                                                           |
| go                         | 165 ms                                                           | 172 ms: 1.04x slower                                                           |
| dask                       | 391 ms                                                           | 407 ms: 1.04x slower                                                           |
| async_tree_none            | 365 ms                                                           | 380 ms: 1.04x slower                                                           |
| sympy_expand               | 501 ms                                                           | 522 ms: 1.04x slower                                                           |
| docutils                   | 2.98 sec                                                         | 3.12 sec: 1.04x slower                                                         |
| async_generators           | 363 ms                                                           | 379 ms: 1.05x slower                                                           |
| bench_thread_pool          | 908 us                                                           | 952 us: 1.05x slower                                                           |
| sqlglot_normalize          | 120 ms                                                           | 126 ms: 1.05x slower                                                           |
| genshi_text                | 25.9 ms                                                          | 27.2 ms: 1.05x slower                                                          |
| crypto_pyaes               | 73.6 ms                                                          | 77.6 ms: 1.05x slower                                                          |
| sympy_str                  | 295 ms                                                           | 311 ms: 1.06x slower                                                           |
| raytrace                   | 260 ms                                                           | 275 ms: 1.06x slower                                                           |
| meteor_contest             | 128 ms                                                           | 136 ms: 1.06x slower                                                           |
| gunicorn                   | 1.04 ms                                                          | 1.11 ms: 1.06x slower                                                          |
| aiohttp                    | 1.07 ms                                                          | 1.14 ms: 1.07x slower                                                          |
| sympy_sum                  | 155 ms                                                           | 165 ms: 1.07x slower                                                           |
| mdp                        | 2.46 sec                                                         | 2.63 sec: 1.07x slower                                                         |
| fannkuch                   | 353 ms                                                           | 381 ms: 1.08x slower                                                           |
| sqlglot_optimize           | 59.5 ms                                                          | 64.5 ms: 1.08x slower                                                          |
| scimark_monte_carlo        | 65.5 ms                                                          | 72.1 ms: 1.10x slower                                                          |
| nbody                      | 87.8 ms                                                          | 97.1 ms: 1.11x slower                                                          |
| sympy_integrate            | 23.2 ms                                                          | 25.7 ms: 1.11x slower                                                          |
| chaos                      | 59.6 ms                                                          | 66.1 ms: 1.11x slower                                                          |
| mypy2                      | 764 ms                                                           | 849 ms: 1.11x slower                                                           |
| deltablue                  | 3.37 ms                                                          | 3.78 ms: 1.12x slower                                                          |
| nqueens                    | 88.4 ms                                                          | 101 ms: 1.14x slower                                                           |
| hexiom                     | 6.35 ms                                                          | 7.30 ms: 1.15x slower                                                          |
| pathlib                    | 17.1 ms                                                          | 19.7 ms: 1.15x slower                                                          |
| comprehensions             | 17.0 us                                                          | 19.7 us: 1.16x slower                                                          |
| scimark_lu                 | 97.5 ms                                                          | 115 ms: 1.18x slower                                                           |
| scimark_sor                | 119 ms                                                           | 150 ms: 1.26x slower                                                           |
| python_startup_no_site     | 8.85 ms                                                          | 11.8 ms: 1.33x slower                                                          |
| Geometric mean             | (ref)                                                            | 1.02x slower                                                                   |

Benchmark hidden because not significant (14): bench_mp_pool, async_tree_memoization, async_tree_none_tg, telco, pickle_list, pickle_pure_python, xml_etree_generate, logging_format, html5lib, logging_simple, regex_compile, pylint, async_tree_cpu_io_mixed, async_tree_memoization_tg
Ignored benchmarks (3) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, django_template, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.06x