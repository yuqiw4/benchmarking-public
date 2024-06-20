# Results vs. 3.13.0b2

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: linux-x86_64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.13x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 313 ms: 1.14x slower                                                   |
| chameleon      | 7.22 ms                                                    | 7.93 ms: 1.10x slower                                                  |
| docutils       | 2.83 sec                                                   | 3.14 sec: 1.11x slower                                                 |
| html5lib       | 67.2 ms                                                    | 73.7 ms: 1.10x slower                                                  |
| tornado_http   | 94.6 ms                                                    | 103 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                      | 1.11x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 611 ms                                                     | 639 ms: 1.05x slower                                                   |
| async_tree_io              | 939 ms                                                     | 996 ms: 1.06x slower                                                   |
| async_tree_memoization_tg  | 444 ms                                                     | 475 ms: 1.07x slower                                                   |
| async_tree_io_tg           | 936 ms                                                     | 1.00 sec: 1.07x slower                                                 |
| async_tree_memoization     | 463 ms                                                     | 501 ms: 1.08x slower                                                   |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 638 ms: 1.09x slower                                                   |
| async_tree_none_tg         | 336 ms                                                     | 365 ms: 1.09x slower                                                   |
| Geometric mean             | (ref)                                                      | 1.06x slower                                                           |

Benchmark hidden because not significant (1): async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 191 ms                                                     | 196 ms: 1.03x slower                                                   |
| float          | 78.9 ms                                                    | 91.6 ms: 1.16x slower                                                  |
| nbody          | 88.3 ms                                                    | 117 ms: 1.33x slower                                                   |
| Geometric mean | (ref)                                                      | 1.17x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8       | 25.1 ms                                                    | 24.8 ms: 1.01x faster                                                  |
| regex_dna      | 221 ms                                                     | 219 ms: 1.01x faster                                                   |
| regex_effbot   | 3.67 ms                                                    | 3.80 ms: 1.03x slower                                                  |
| regex_compile  | 137 ms                                                     | 190 ms: 1.39x slower                                                   |
| Geometric mean | (ref)                                                      | 1.09x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 162 ms                                                     | 152 ms: 1.06x faster                                                   |
| json_loads           | 28.9 us                                                    | 27.5 us: 1.05x faster                                                  |
| unpickle_list        | 5.34 us                                                    | 5.12 us: 1.04x faster                                                  |
| pickle_dict          | 34.8 us                                                    | 34.5 us: 1.01x faster                                                  |
| pickle_list          | 5.11 us                                                    | 5.15 us: 1.01x slower                                                  |
| pickle               | 11.5 us                                                    | 11.7 us: 1.02x slower                                                  |
| xml_etree_iterparse  | 107 ms                                                     | 110 ms: 1.02x slower                                                   |
| pickle_pure_python   | 305 us                                                     | 317 us: 1.04x slower                                                   |
| unpickle             | 15.1 us                                                    | 15.9 us: 1.05x slower                                                  |
| xml_etree_process    | 61.2 ms                                                    | 64.9 ms: 1.06x slower                                                  |
| xml_etree_generate   | 87.4 ms                                                    | 95.6 ms: 1.09x slower                                                  |
| tomli_loads          | 2.12 sec                                                   | 2.63 sec: 1.24x slower                                                 |
| unpickle_pure_python | 218 us                                                     | 334 us: 1.53x slower                                                   |
| Geometric mean       | (ref)                                                      | 1.06x slower                                                           |

Benchmark hidden because not significant (1): json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                  |
| python_startup_no_site | 7.11 ms                                                    | 7.12 ms: 1.00x slower                                                  |
| Geometric mean         | (ref)                                                      | 1.01x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 23.7 ms                                                    | 26.2 ms: 1.11x slower                                                  |
| mako            | 11.2 ms                                                    | 13.4 ms: 1.19x slower                                                  |
| genshi_xml      | 51.6 ms                                                    | 62.5 ms: 1.21x slower                                                  |
| django_template | 34.8 ms                                                    | 43.2 ms: 1.24x slower                                                  |
| Geometric mean  | (ref)                                                      | 1.19x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 124 us: 1.32x faster                                                   |
| gc_traversal               | 3.98 ms                                                    | 3.64 ms: 1.09x faster                                                  |
| xml_etree_parse            | 162 ms                                                     | 152 ms: 1.06x faster                                                   |
| json_loads                 | 28.9 us                                                    | 27.5 us: 1.05x faster                                                  |
| unpickle_list              | 5.34 us                                                    | 5.12 us: 1.04x faster                                                  |
| coroutines                 | 23.2 ms                                                    | 22.3 ms: 1.04x faster                                                  |
| create_gc_cycles           | 1.82 ms                                                    | 1.76 ms: 1.03x faster                                                  |
| json                       | 5.31 ms                                                    | 5.17 ms: 1.03x faster                                                  |
| python_startup             | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                  |
| regex_v8                   | 25.1 ms                                                    | 24.8 ms: 1.01x faster                                                  |
| regex_dna                  | 221 ms                                                     | 219 ms: 1.01x faster                                                   |
| pickle_dict                | 34.8 us                                                    | 34.5 us: 1.01x faster                                                  |
| python_startup_no_site     | 7.11 ms                                                    | 7.12 ms: 1.00x slower                                                  |
| bench_mp_pool              | 23.9 ms                                                    | 24.0 ms: 1.00x slower                                                  |
| pickle_list                | 5.11 us                                                    | 5.15 us: 1.01x slower                                                  |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.87 sec: 1.01x slower                                                 |
| pickle                     | 11.5 us                                                    | 11.7 us: 1.02x slower                                                  |
| deepcopy_reduce            | 3.35 us                                                    | 3.42 us: 1.02x slower                                                  |
| xml_etree_iterparse        | 107 ms                                                     | 110 ms: 1.02x slower                                                   |
| asyncio_tcp                | 508 ms                                                     | 519 ms: 1.02x slower                                                   |
| logging_silent             | 105 ns                                                     | 107 ns: 1.02x slower                                                   |
| generators                 | 29.6 ms                                                    | 30.3 ms: 1.02x slower                                                  |
| pidigits                   | 191 ms                                                     | 196 ms: 1.03x slower                                                   |
| thrift                     | 823 us                                                     | 848 us: 1.03x slower                                                   |
| sqlite_synth               | 2.99 us                                                    | 3.08 us: 1.03x slower                                                  |
| regex_effbot               | 3.67 ms                                                    | 3.80 ms: 1.03x slower                                                  |
| pickle_pure_python         | 305 us                                                     | 317 us: 1.04x slower                                                   |
| dask                       | 369 ms                                                     | 384 ms: 1.04x slower                                                   |
| coverage                   | 93.1 ms                                                    | 96.9 ms: 1.04x slower                                                  |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 639 ms: 1.05x slower                                                   |
| gunicorn                   | 1.28 ms                                                    | 1.34 ms: 1.05x slower                                                  |
| mdp                        | 2.79 sec                                                   | 2.93 sec: 1.05x slower                                                 |
| djangocms                  | 31.5 us                                                    | 33.1 us: 1.05x slower                                                  |
| unpickle                   | 15.1 us                                                    | 15.9 us: 1.05x slower                                                  |
| aiohttp                    | 1.18 ms                                                    | 1.25 ms: 1.06x slower                                                  |
| xml_etree_process          | 61.2 ms                                                    | 64.9 ms: 1.06x slower                                                  |
| async_tree_io              | 939 ms                                                     | 996 ms: 1.06x slower                                                   |
| pathlib                    | 17.3 ms                                                    | 18.4 ms: 1.06x slower                                                  |
| deepcopy                   | 367 us                                                     | 392 us: 1.07x slower                                                   |
| async_tree_memoization_tg  | 444 ms                                                     | 475 ms: 1.07x slower                                                   |
| async_tree_io_tg           | 936 ms                                                     | 1.00 sec: 1.07x slower                                                 |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 5.67 ms: 1.08x slower                                                  |
| async_tree_memoization     | 463 ms                                                     | 501 ms: 1.08x slower                                                   |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 638 ms: 1.09x slower                                                   |
| async_tree_none_tg         | 336 ms                                                     | 365 ms: 1.09x slower                                                   |
| bench_thread_pool          | 834 us                                                     | 910 us: 1.09x slower                                                   |
| tornado_http               | 94.6 ms                                                    | 103 ms: 1.09x slower                                                   |
| xml_etree_generate         | 87.4 ms                                                    | 95.6 ms: 1.09x slower                                                  |
| html5lib                   | 67.2 ms                                                    | 73.7 ms: 1.10x slower                                                  |
| async_generators           | 442 ms                                                     | 485 ms: 1.10x slower                                                   |
| pylint                     | 317 ms                                                     | 348 ms: 1.10x slower                                                   |
| chameleon                  | 7.22 ms                                                    | 7.93 ms: 1.10x slower                                                  |
| mypy2                      | 742 ms                                                     | 819 ms: 1.10x slower                                                   |
| genshi_text                | 23.7 ms                                                    | 26.2 ms: 1.11x slower                                                  |
| docutils                   | 2.83 sec                                                   | 3.14 sec: 1.11x slower                                                 |
| meteor_contest             | 110 ms                                                     | 123 ms: 1.12x slower                                                   |
| dulwich_log                | 67.2 ms                                                    | 75.4 ms: 1.12x slower                                                  |
| telco                      | 8.41 ms                                                    | 9.47 ms: 1.13x slower                                                  |
| pycparser                  | 1.16 sec                                                   | 1.31 sec: 1.13x slower                                                 |
| 2to3                       | 274 ms                                                     | 313 ms: 1.14x slower                                                   |
| sqlglot_transpile          | 1.63 ms                                                    | 1.87 ms: 1.14x slower                                                  |
| logging_format             | 6.47 us                                                    | 7.41 us: 1.15x slower                                                  |
| richards_super             | 57.4 ms                                                    | 65.7 ms: 1.15x slower                                                  |
| richards                   | 50.9 ms                                                    | 58.3 ms: 1.15x slower                                                  |
| sympy_integrate            | 20.5 ms                                                    | 23.8 ms: 1.16x slower                                                  |
| sympy_expand               | 473 ms                                                     | 548 ms: 1.16x slower                                                   |
| sqlglot_normalize          | 110 ms                                                     | 128 ms: 1.16x slower                                                   |
| sympy_sum                  | 156 ms                                                     | 181 ms: 1.16x slower                                                   |
| float                      | 78.9 ms                                                    | 91.6 ms: 1.16x slower                                                  |
| logging_simple             | 5.74 us                                                    | 6.69 us: 1.17x slower                                                  |
| sqlglot_parse              | 1.32 ms                                                    | 1.54 ms: 1.17x slower                                                  |
| sympy_str                  | 282 ms                                                     | 331 ms: 1.17x slower                                                   |
| sqlglot_optimize           | 55.5 ms                                                    | 66.2 ms: 1.19x slower                                                  |
| mako                       | 11.2 ms                                                    | 13.4 ms: 1.19x slower                                                  |
| crypto_pyaes               | 77.5 ms                                                    | 93.0 ms: 1.20x slower                                                  |
| genshi_xml                 | 51.6 ms                                                    | 62.5 ms: 1.21x slower                                                  |
| deepcopy_memo              | 39.7 us                                                    | 48.9 us: 1.23x slower                                                  |
| tomli_loads                | 2.12 sec                                                   | 2.63 sec: 1.24x slower                                                 |
| django_template            | 34.8 ms                                                    | 43.2 ms: 1.24x slower                                                  |
| scimark_sor                | 127 ms                                                     | 162 ms: 1.27x slower                                                   |
| pyflate                    | 484 ms                                                     | 633 ms: 1.31x slower                                                   |
| chaos                      | 61.3 ms                                                    | 80.8 ms: 1.32x slower                                                  |
| raytrace                   | 267 ms                                                     | 352 ms: 1.32x slower                                                   |
| nbody                      | 88.3 ms                                                    | 117 ms: 1.33x slower                                                   |
| deltablue                  | 3.25 ms                                                    | 4.33 ms: 1.33x slower                                                  |
| scimark_monte_carlo        | 69.2 ms                                                    | 92.3 ms: 1.33x slower                                                  |
| fannkuch                   | 402 ms                                                     | 537 ms: 1.34x slower                                                   |
| go                         | 145 ms                                                     | 194 ms: 1.34x slower                                                   |
| scimark_fft                | 392 ms                                                     | 543 ms: 1.38x slower                                                   |
| regex_compile              | 137 ms                                                     | 190 ms: 1.39x slower                                                   |
| scimark_lu                 | 122 ms                                                     | 172 ms: 1.41x slower                                                   |
| pprint_safe_repr           | 758 ms                                                     | 1.12 sec: 1.47x slower                                                 |
| pprint_pformat             | 1.56 sec                                                   | 2.31 sec: 1.49x slower                                                 |
| unpickle_pure_python       | 218 us                                                     | 334 us: 1.53x slower                                                   |
| nqueens                    | 81.4 ms                                                    | 125 ms: 1.54x slower                                                   |
| comprehensions             | 16.6 us                                                    | 25.6 us: 1.54x slower                                                  |
| hexiom                     | 6.30 ms                                                    | 10.3 ms: 1.63x slower                                                  |
| spectral_norm              | 116 ms                                                     | 203 ms: 1.74x slower                                                   |
| Geometric mean             | (ref)                                                      | 1.13x slower                                                           |

Benchmark hidden because not significant (3): json_dumps, asyncio_websockets, async_tree_none
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 0.99x