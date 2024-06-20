# Results vs. 3.13.0b2

- fork: python
- ref: 7e6fa5fceddc3f4721c0
- machine: linux-x86_64
- commit hash: 7e6fa5f
- commit date: 2024-04-19
- overall geometric mean: 1.09x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 301 ms: 1.10x slower                                                   |
| chameleon      | 7.22 ms                                                    | 7.58 ms: 1.05x slower                                                  |
| docutils       | 2.83 sec                                                   | 3.08 sec: 1.09x slower                                                 |
| html5lib       | 67.2 ms                                                    | 71.9 ms: 1.07x slower                                                  |
| tornado_http   | 94.6 ms                                                    | 103 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                      | 1.08x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f |
|----------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 611 ms                                                     | 637 ms: 1.04x slower                                                   |
| async_tree_memoization_tg  | 444 ms                                                     | 463 ms: 1.04x slower                                                   |
| async_tree_io              | 939 ms                                                     | 979 ms: 1.04x slower                                                   |
| async_tree_io_tg           | 936 ms                                                     | 980 ms: 1.05x slower                                                   |
| async_tree_none_tg         | 336 ms                                                     | 352 ms: 1.05x slower                                                   |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 624 ms: 1.06x slower                                                   |
| async_tree_memoization     | 463 ms                                                     | 506 ms: 1.09x slower                                                   |
| Geometric mean             | (ref)                                                      | 1.05x slower                                                           |

Benchmark hidden because not significant (1): async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 78.9 ms                                                    | 89.3 ms: 1.13x slower                                                  |
| nbody          | 88.3 ms                                                    | 121 ms: 1.37x slower                                                   |
| Geometric mean | (ref)                                                      | 1.16x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.67 ms                                                    | 3.54 ms: 1.04x faster                                                  |
| regex_dna      | 221 ms                                                     | 222 ms: 1.00x slower                                                   |
| regex_v8       | 25.1 ms                                                    | 25.2 ms: 1.00x slower                                                  |
| regex_compile  | 137 ms                                                     | 179 ms: 1.31x slower                                                   |
| Geometric mean | (ref)                                                      | 1.06x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f |
|----------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 162 ms                                                     | 152 ms: 1.07x faster                                                   |
| json_loads           | 28.9 us                                                    | 27.3 us: 1.06x faster                                                  |
| unpickle_list        | 5.34 us                                                    | 5.10 us: 1.05x faster                                                  |
| unpickle             | 15.1 us                                                    | 15.5 us: 1.02x slower                                                  |
| pickle_pure_python   | 305 us                                                     | 316 us: 1.04x slower                                                   |
| pickle_dict          | 34.8 us                                                    | 36.1 us: 1.04x slower                                                  |
| xml_etree_iterparse  | 107 ms                                                     | 112 ms: 1.04x slower                                                   |
| xml_etree_process    | 61.2 ms                                                    | 63.9 ms: 1.04x slower                                                  |
| pickle_list          | 5.11 us                                                    | 5.37 us: 1.05x slower                                                  |
| pickle               | 11.5 us                                                    | 12.2 us: 1.06x slower                                                  |
| xml_etree_generate   | 87.4 ms                                                    | 93.0 ms: 1.06x slower                                                  |
| tomli_loads          | 2.12 sec                                                   | 2.55 sec: 1.20x slower                                                 |
| unpickle_pure_python | 218 us                                                     | 286 us: 1.31x slower                                                   |
| Geometric mean       | (ref)                                                      | 1.05x slower                                                           |

Benchmark hidden because not significant (1): json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f |
|------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                  |
| python_startup_no_site | 7.11 ms                                                    | 7.12 ms: 1.00x slower                                                  |
| Geometric mean         | (ref)                                                      | 1.01x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f |
|-----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 23.7 ms                                                    | 26.2 ms: 1.11x slower                                                  |
| genshi_xml      | 51.6 ms                                                    | 59.7 ms: 1.16x slower                                                  |
| django_template | 34.8 ms                                                    | 40.8 ms: 1.17x slower                                                  |
| mako            | 11.2 ms                                                    | 13.5 ms: 1.20x slower                                                  |
| Geometric mean  | (ref)                                                      | 1.16x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240419-linux-x86_64-python-7e6fa5fceddc3f4721c0-3.13.0a6+-7e6fa5f |
|----------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 119 us: 1.39x faster                                                   |
| xml_etree_parse            | 162 ms                                                     | 152 ms: 1.07x faster                                                   |
| json_loads                 | 28.9 us                                                    | 27.3 us: 1.06x faster                                                  |
| gc_traversal               | 3.98 ms                                                    | 3.76 ms: 1.06x faster                                                  |
| unpickle_list              | 5.34 us                                                    | 5.10 us: 1.05x faster                                                  |
| regex_effbot               | 3.67 ms                                                    | 3.54 ms: 1.04x faster                                                  |
| json                       | 5.31 ms                                                    | 5.12 ms: 1.04x faster                                                  |
| python_startup             | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                  |
| create_gc_cycles           | 1.82 ms                                                    | 1.78 ms: 1.02x faster                                                  |
| coroutines                 | 23.2 ms                                                    | 22.8 ms: 1.02x faster                                                  |
| python_startup_no_site     | 7.11 ms                                                    | 7.12 ms: 1.00x slower                                                  |
| regex_dna                  | 221 ms                                                     | 222 ms: 1.00x slower                                                   |
| regex_v8                   | 25.1 ms                                                    | 25.2 ms: 1.00x slower                                                  |
| generators                 | 29.6 ms                                                    | 30.0 ms: 1.01x slower                                                  |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.87 sec: 1.01x slower                                                 |
| asyncio_tcp                | 508 ms                                                     | 516 ms: 1.01x slower                                                   |
| thrift                     | 823 us                                                     | 838 us: 1.02x slower                                                   |
| logging_silent             | 105 ns                                                     | 107 ns: 1.02x slower                                                   |
| sqlite_synth               | 2.99 us                                                    | 3.05 us: 1.02x slower                                                  |
| unpickle                   | 15.1 us                                                    | 15.5 us: 1.02x slower                                                  |
| djangocms                  | 31.5 us                                                    | 32.4 us: 1.03x slower                                                  |
| dask                       | 369 ms                                                     | 381 ms: 1.03x slower                                                   |
| gunicorn                   | 1.28 ms                                                    | 1.32 ms: 1.03x slower                                                  |
| deepcopy                   | 367 us                                                     | 380 us: 1.03x slower                                                   |
| pickle_pure_python         | 305 us                                                     | 316 us: 1.04x slower                                                   |
| pickle_dict                | 34.8 us                                                    | 36.1 us: 1.04x slower                                                  |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 637 ms: 1.04x slower                                                   |
| async_tree_memoization_tg  | 444 ms                                                     | 463 ms: 1.04x slower                                                   |
| async_tree_io              | 939 ms                                                     | 979 ms: 1.04x slower                                                   |
| xml_etree_iterparse        | 107 ms                                                     | 112 ms: 1.04x slower                                                   |
| xml_etree_process          | 61.2 ms                                                    | 63.9 ms: 1.04x slower                                                  |
| async_tree_io_tg           | 936 ms                                                     | 980 ms: 1.05x slower                                                   |
| aiohttp                    | 1.18 ms                                                    | 1.24 ms: 1.05x slower                                                  |
| async_tree_none_tg         | 336 ms                                                     | 352 ms: 1.05x slower                                                   |
| pathlib                    | 17.3 ms                                                    | 18.2 ms: 1.05x slower                                                  |
| chameleon                  | 7.22 ms                                                    | 7.58 ms: 1.05x slower                                                  |
| pickle_list                | 5.11 us                                                    | 5.37 us: 1.05x slower                                                  |
| coverage                   | 93.1 ms                                                    | 98.1 ms: 1.05x slower                                                  |
| async_generators           | 442 ms                                                     | 468 ms: 1.06x slower                                                   |
| bench_thread_pool          | 834 us                                                     | 884 us: 1.06x slower                                                   |
| pickle                     | 11.5 us                                                    | 12.2 us: 1.06x slower                                                  |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 624 ms: 1.06x slower                                                   |
| xml_etree_generate         | 87.4 ms                                                    | 93.0 ms: 1.06x slower                                                  |
| html5lib                   | 67.2 ms                                                    | 71.9 ms: 1.07x slower                                                  |
| mdp                        | 2.79 sec                                                   | 2.99 sec: 1.07x slower                                                 |
| tornado_http               | 94.6 ms                                                    | 103 ms: 1.08x slower                                                   |
| pylint                     | 317 ms                                                     | 344 ms: 1.09x slower                                                   |
| mypy2                      | 742 ms                                                     | 806 ms: 1.09x slower                                                   |
| richards_super             | 57.4 ms                                                    | 62.4 ms: 1.09x slower                                                  |
| docutils                   | 2.83 sec                                                   | 3.08 sec: 1.09x slower                                                 |
| logging_format             | 6.47 us                                                    | 7.05 us: 1.09x slower                                                  |
| async_tree_memoization     | 463 ms                                                     | 506 ms: 1.09x slower                                                   |
| telco                      | 8.41 ms                                                    | 9.19 ms: 1.09x slower                                                  |
| meteor_contest             | 110 ms                                                     | 120 ms: 1.09x slower                                                   |
| dulwich_log                | 67.2 ms                                                    | 73.4 ms: 1.09x slower                                                  |
| richards                   | 50.9 ms                                                    | 55.9 ms: 1.10x slower                                                  |
| 2to3                       | 274 ms                                                     | 301 ms: 1.10x slower                                                   |
| pycparser                  | 1.16 sec                                                   | 1.28 sec: 1.10x slower                                                 |
| genshi_text                | 23.7 ms                                                    | 26.2 ms: 1.11x slower                                                  |
| sqlglot_transpile          | 1.63 ms                                                    | 1.82 ms: 1.11x slower                                                  |
| sqlglot_normalize          | 110 ms                                                     | 123 ms: 1.11x slower                                                   |
| logging_simple             | 5.74 us                                                    | 6.41 us: 1.12x slower                                                  |
| sympy_integrate            | 20.5 ms                                                    | 23.2 ms: 1.13x slower                                                  |
| float                      | 78.9 ms                                                    | 89.3 ms: 1.13x slower                                                  |
| scimark_fft                | 392 ms                                                     | 445 ms: 1.13x slower                                                   |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 5.98 ms: 1.13x slower                                                  |
| sympy_expand               | 473 ms                                                     | 536 ms: 1.13x slower                                                   |
| sympy_sum                  | 156 ms                                                     | 177 ms: 1.14x slower                                                   |
| sqlglot_optimize           | 55.5 ms                                                    | 63.2 ms: 1.14x slower                                                  |
| sqlglot_parse              | 1.32 ms                                                    | 1.50 ms: 1.14x slower                                                  |
| sympy_str                  | 282 ms                                                     | 322 ms: 1.14x slower                                                   |
| deepcopy_memo              | 39.7 us                                                    | 45.5 us: 1.15x slower                                                  |
| genshi_xml                 | 51.6 ms                                                    | 59.7 ms: 1.16x slower                                                  |
| django_template            | 34.8 ms                                                    | 40.8 ms: 1.17x slower                                                  |
| crypto_pyaes               | 77.5 ms                                                    | 91.6 ms: 1.18x slower                                                  |
| scimark_sor                | 127 ms                                                     | 151 ms: 1.19x slower                                                   |
| mako                       | 11.2 ms                                                    | 13.5 ms: 1.20x slower                                                  |
| tomli_loads                | 2.12 sec                                                   | 2.55 sec: 1.20x slower                                                 |
| raytrace                   | 267 ms                                                     | 322 ms: 1.21x slower                                                   |
| spectral_norm              | 116 ms                                                     | 144 ms: 1.24x slower                                                   |
| pyflate                    | 484 ms                                                     | 600 ms: 1.24x slower                                                   |
| fannkuch                   | 402 ms                                                     | 502 ms: 1.25x slower                                                   |
| deltablue                  | 3.25 ms                                                    | 4.10 ms: 1.26x slower                                                  |
| pprint_safe_repr           | 758 ms                                                     | 966 ms: 1.27x slower                                                   |
| chaos                      | 61.3 ms                                                    | 78.5 ms: 1.28x slower                                                  |
| go                         | 145 ms                                                     | 185 ms: 1.28x slower                                                   |
| scimark_monte_carlo        | 69.2 ms                                                    | 88.8 ms: 1.28x slower                                                  |
| pprint_pformat             | 1.56 sec                                                   | 2.01 sec: 1.29x slower                                                 |
| regex_compile              | 137 ms                                                     | 179 ms: 1.31x slower                                                   |
| unpickle_pure_python       | 218 us                                                     | 286 us: 1.31x slower                                                   |
| nqueens                    | 81.4 ms                                                    | 107 ms: 1.32x slower                                                   |
| nbody                      | 88.3 ms                                                    | 121 ms: 1.37x slower                                                   |
| scimark_lu                 | 122 ms                                                     | 166 ms: 1.37x slower                                                   |
| comprehensions             | 16.6 us                                                    | 23.5 us: 1.42x slower                                                  |
| hexiom                     | 6.30 ms                                                    | 9.55 ms: 1.52x slower                                                  |
| Geometric mean             | (ref)                                                      | 1.09x slower                                                           |

Benchmark hidden because not significant (6): json_dumps, bench_mp_pool, pidigits, async_tree_none, asyncio_websockets, deepcopy_reduce
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 0.99x