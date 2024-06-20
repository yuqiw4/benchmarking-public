# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: tier_2_call
- machine: linux-x86_64
- commit hash: 62ff43c
- commit date: 2024-05-03
- overall geometric mean: 1.14x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-62ff43c |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 327 ms: 1.19x slower                                                    |
| chameleon      | 7.22 ms                                                    | 8.06 ms: 1.12x slower                                                   |
| html5lib       | 67.2 ms                                                    | 77.8 ms: 1.16x slower                                                   |
| tornado_http   | 94.6 ms                                                    | 105 ms: 1.11x slower                                                    |
| Geometric mean | (ref)                                                      | 1.14x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-62ff43c |
|----------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 936 ms                                                     | 976 ms: 1.04x slower                                                    |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 640 ms: 1.05x slower                                                    |
| async_tree_io              | 939 ms                                                     | 985 ms: 1.05x slower                                                    |
| async_tree_memoization_tg  | 444 ms                                                     | 468 ms: 1.05x slower                                                    |
| async_tree_none_tg         | 336 ms                                                     | 358 ms: 1.06x slower                                                    |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 631 ms: 1.07x slower                                                    |
| async_tree_memoization     | 463 ms                                                     | 512 ms: 1.11x slower                                                    |
| Geometric mean             | (ref)                                                      | 1.05x slower                                                            |

Benchmark hidden because not significant (1): async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-62ff43c |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 191 ms                                                     | 196 ms: 1.02x slower                                                    |
| float          | 78.9 ms                                                    | 90.6 ms: 1.15x slower                                                   |
| nbody          | 88.3 ms                                                    | 122 ms: 1.38x slower                                                    |
| Geometric mean | (ref)                                                      | 1.18x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-62ff43c |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.67 ms                                                    | 3.69 ms: 1.00x slower                                                   |
| regex_v8       | 25.1 ms                                                    | 25.6 ms: 1.02x slower                                                   |
| regex_dna      | 221 ms                                                     | 227 ms: 1.02x slower                                                    |
| regex_compile  | 137 ms                                                     | 190 ms: 1.39x slower                                                    |
| Geometric mean | (ref)                                                      | 1.10x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-62ff43c |
|----------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_parse      | 162 ms                                                     | 152 ms: 1.07x faster                                                    |
| json_loads           | 28.9 us                                                    | 27.8 us: 1.04x faster                                                   |
| pickle_dict          | 34.8 us                                                    | 34.0 us: 1.02x faster                                                   |
| unpickle_list        | 5.34 us                                                    | 5.23 us: 1.02x faster                                                   |
| pickle_list          | 5.11 us                                                    | 5.13 us: 1.00x slower                                                   |
| xml_etree_iterparse  | 107 ms                                                     | 111 ms: 1.03x slower                                                    |
| pickle               | 11.5 us                                                    | 11.9 us: 1.03x slower                                                   |
| json_dumps           | 10.7 ms                                                    | 11.1 ms: 1.04x slower                                                   |
| unpickle             | 15.1 us                                                    | 15.7 us: 1.04x slower                                                   |
| xml_etree_generate   | 87.4 ms                                                    | 97.6 ms: 1.12x slower                                                   |
| xml_etree_process    | 61.2 ms                                                    | 68.4 ms: 1.12x slower                                                   |
| tomli_loads          | 2.12 sec                                                   | 2.65 sec: 1.25x slower                                                  |
| unpickle_pure_python | 218 us                                                     | 285 us: 1.31x slower                                                    |
| pickle_pure_python   | 305 us                                                     | 405 us: 1.33x slower                                                    |
| Geometric mean       | (ref)                                                      | 1.07x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-62ff43c |
|------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.7 ms: 1.00x faster                                                   |
| python_startup_no_site | 7.11 ms                                                    | 7.23 ms: 1.02x slower                                                   |
| Geometric mean         | (ref)                                                      | 1.01x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-62ff43c |
|-----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 14.0 ms: 1.24x slower                                                   |
| django_template | 34.8 ms                                                    | 44.5 ms: 1.28x slower                                                   |
| genshi_text     | 23.7 ms                                                    | 32.0 ms: 1.35x slower                                                   |
| genshi_xml      | 51.6 ms                                                    | 72.9 ms: 1.41x slower                                                   |
| Geometric mean  | (ref)                                                      | 1.32x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-62ff43c |
|----------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal               | 3.98 ms                                                    | 3.62 ms: 1.10x faster                                                   |
| xml_etree_parse            | 162 ms                                                     | 152 ms: 1.07x faster                                                    |
| json_loads                 | 28.9 us                                                    | 27.8 us: 1.04x faster                                                   |
| pickle_dict                | 34.8 us                                                    | 34.0 us: 1.02x faster                                                   |
| unpickle_list              | 5.34 us                                                    | 5.23 us: 1.02x faster                                                   |
| create_gc_cycles           | 1.82 ms                                                    | 1.79 ms: 1.02x faster                                                   |
| json                       | 5.31 ms                                                    | 5.24 ms: 1.01x faster                                                   |
| asyncio_websockets         | 567 ms                                                     | 563 ms: 1.01x faster                                                    |
| python_startup             | 10.8 ms                                                    | 10.7 ms: 1.00x faster                                                   |
| pickle_list                | 5.11 us                                                    | 5.13 us: 1.00x slower                                                   |
| regex_effbot               | 3.67 ms                                                    | 3.69 ms: 1.00x slower                                                   |
| bench_mp_pool              | 23.9 ms                                                    | 24.0 ms: 1.01x slower                                                   |
| mdp                        | 2.79 sec                                                   | 2.81 sec: 1.01x slower                                                  |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.87 sec: 1.02x slower                                                  |
| python_startup_no_site     | 7.11 ms                                                    | 7.23 ms: 1.02x slower                                                   |
| regex_v8                   | 25.1 ms                                                    | 25.6 ms: 1.02x slower                                                   |
| pidigits                   | 191 ms                                                     | 196 ms: 1.02x slower                                                    |
| regex_dna                  | 221 ms                                                     | 227 ms: 1.02x slower                                                    |
| xml_etree_iterparse        | 107 ms                                                     | 111 ms: 1.03x slower                                                    |
| generators                 | 29.6 ms                                                    | 30.6 ms: 1.03x slower                                                   |
| pickle                     | 11.5 us                                                    | 11.9 us: 1.03x slower                                                   |
| thrift                     | 823 us                                                     | 851 us: 1.03x slower                                                    |
| json_dumps                 | 10.7 ms                                                    | 11.1 ms: 1.04x slower                                                   |
| unpickle                   | 15.1 us                                                    | 15.7 us: 1.04x slower                                                   |
| async_tree_io_tg           | 936 ms                                                     | 976 ms: 1.04x slower                                                    |
| asyncio_tcp                | 508 ms                                                     | 532 ms: 1.05x slower                                                    |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 640 ms: 1.05x slower                                                    |
| async_tree_io              | 939 ms                                                     | 985 ms: 1.05x slower                                                    |
| async_tree_memoization_tg  | 444 ms                                                     | 468 ms: 1.05x slower                                                    |
| djangocms                  | 31.5 us                                                    | 33.2 us: 1.05x slower                                                   |
| dask                       | 369 ms                                                     | 393 ms: 1.06x slower                                                    |
| async_tree_none_tg         | 336 ms                                                     | 358 ms: 1.06x slower                                                    |
| async_generators           | 442 ms                                                     | 471 ms: 1.07x slower                                                    |
| pathlib                    | 17.3 ms                                                    | 18.6 ms: 1.07x slower                                                   |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 631 ms: 1.07x slower                                                    |
| coroutines                 | 23.2 ms                                                    | 24.9 ms: 1.08x slower                                                   |
| gunicorn                   | 1.28 ms                                                    | 1.38 ms: 1.08x slower                                                   |
| aiohttp                    | 1.18 ms                                                    | 1.28 ms: 1.08x slower                                                   |
| bench_thread_pool          | 834 us                                                     | 914 us: 1.10x slower                                                    |
| async_tree_memoization     | 463 ms                                                     | 512 ms: 1.11x slower                                                    |
| tornado_http               | 94.6 ms                                                    | 105 ms: 1.11x slower                                                    |
| xml_etree_generate         | 87.4 ms                                                    | 97.6 ms: 1.12x slower                                                   |
| chameleon                  | 7.22 ms                                                    | 8.06 ms: 1.12x slower                                                   |
| xml_etree_process          | 61.2 ms                                                    | 68.4 ms: 1.12x slower                                                   |
| meteor_contest             | 110 ms                                                     | 123 ms: 1.12x slower                                                    |
| dulwich_log                | 67.2 ms                                                    | 75.5 ms: 1.12x slower                                                   |
| logging_format             | 6.47 us                                                    | 7.30 us: 1.13x slower                                                   |
| scimark_fft                | 392 ms                                                     | 443 ms: 1.13x slower                                                    |
| logging_simple             | 5.74 us                                                    | 6.55 us: 1.14x slower                                                   |
| telco                      | 8.41 ms                                                    | 9.60 ms: 1.14x slower                                                   |
| deepcopy_reduce            | 3.35 us                                                    | 3.84 us: 1.15x slower                                                   |
| float                      | 78.9 ms                                                    | 90.6 ms: 1.15x slower                                                   |
| html5lib                   | 67.2 ms                                                    | 77.8 ms: 1.16x slower                                                   |
| pylint                     | 317 ms                                                     | 367 ms: 1.16x slower                                                    |
| mypy2                      | 742 ms                                                     | 859 ms: 1.16x slower                                                    |
| richards_super             | 57.4 ms                                                    | 66.6 ms: 1.16x slower                                                   |
| richards                   | 50.9 ms                                                    | 59.4 ms: 1.17x slower                                                   |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 6.17 ms: 1.17x slower                                                   |
| typing_runtime_protocols   | 165 us                                                     | 194 us: 1.18x slower                                                    |
| sympy_sum                  | 156 ms                                                     | 184 ms: 1.18x slower                                                    |
| crypto_pyaes               | 77.5 ms                                                    | 91.9 ms: 1.19x slower                                                   |
| 2to3                       | 274 ms                                                     | 327 ms: 1.19x slower                                                    |
| sqlglot_optimize           | 55.5 ms                                                    | 66.6 ms: 1.20x slower                                                   |
| spectral_norm              | 116 ms                                                     | 140 ms: 1.20x slower                                                    |
| sympy_integrate            | 20.5 ms                                                    | 24.8 ms: 1.21x slower                                                   |
| fannkuch                   | 402 ms                                                     | 487 ms: 1.21x slower                                                    |
| sympy_str                  | 282 ms                                                     | 344 ms: 1.22x slower                                                    |
| sympy_expand               | 473 ms                                                     | 578 ms: 1.22x slower                                                    |
| pycparser                  | 1.16 sec                                                   | 1.42 sec: 1.22x slower                                                  |
| sqlglot_normalize          | 110 ms                                                     | 137 ms: 1.24x slower                                                    |
| raytrace                   | 267 ms                                                     | 331 ms: 1.24x slower                                                    |
| mako                       | 11.2 ms                                                    | 14.0 ms: 1.24x slower                                                   |
| scimark_sor                | 127 ms                                                     | 159 ms: 1.25x slower                                                    |
| tomli_loads                | 2.12 sec                                                   | 2.65 sec: 1.25x slower                                                  |
| deepcopy                   | 367 us                                                     | 459 us: 1.25x slower                                                    |
| sqlglot_transpile          | 1.63 ms                                                    | 2.05 ms: 1.25x slower                                                   |
| go                         | 145 ms                                                     | 181 ms: 1.26x slower                                                    |
| pyflate                    | 484 ms                                                     | 609 ms: 1.26x slower                                                    |
| sqlglot_parse              | 1.32 ms                                                    | 1.67 ms: 1.27x slower                                                   |
| pprint_safe_repr           | 758 ms                                                     | 968 ms: 1.28x slower                                                    |
| django_template            | 34.8 ms                                                    | 44.5 ms: 1.28x slower                                                   |
| pprint_pformat             | 1.56 sec                                                   | 1.99 sec: 1.28x slower                                                  |
| deepcopy_memo              | 39.7 us                                                    | 51.4 us: 1.29x slower                                                   |
| scimark_monte_carlo        | 69.2 ms                                                    | 90.1 ms: 1.30x slower                                                   |
| unpickle_pure_python       | 218 us                                                     | 285 us: 1.31x slower                                                    |
| pickle_pure_python         | 305 us                                                     | 405 us: 1.33x slower                                                    |
| nqueens                    | 81.4 ms                                                    | 109 ms: 1.34x slower                                                    |
| deltablue                  | 3.25 ms                                                    | 4.37 ms: 1.34x slower                                                   |
| genshi_text                | 23.7 ms                                                    | 32.0 ms: 1.35x slower                                                   |
| scimark_lu                 | 122 ms                                                     | 167 ms: 1.37x slower                                                    |
| chaos                      | 61.3 ms                                                    | 84.4 ms: 1.38x slower                                                   |
| nbody                      | 88.3 ms                                                    | 122 ms: 1.38x slower                                                    |
| regex_compile              | 137 ms                                                     | 190 ms: 1.39x slower                                                    |
| logging_silent             | 105 ns                                                     | 146 ns: 1.40x slower                                                    |
| genshi_xml                 | 51.6 ms                                                    | 72.9 ms: 1.41x slower                                                   |
| comprehensions             | 16.6 us                                                    | 25.1 us: 1.51x slower                                                   |
| hexiom                     | 6.30 ms                                                    | 9.66 ms: 1.53x slower                                                   |
| Geometric mean             | (ref)                                                      | 1.14x slower                                                            |

Benchmark hidden because not significant (3): coverage, sqlite_synth, async_tree_none
Ignored benchmarks (3) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, docutils, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.11x
- 95% likely to have a slowdown of 1.10x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.00x