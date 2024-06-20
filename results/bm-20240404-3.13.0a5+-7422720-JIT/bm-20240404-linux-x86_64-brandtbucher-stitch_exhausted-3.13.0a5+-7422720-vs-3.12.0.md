# Results vs. 3.12.0

- fork: brandtbucher
- ref: stitch_exhausted
- machine: linux-x86_64
- commit hash: 7422720
- commit date: 2024-04-04
- overall geometric mean: 1.02x faster
- HPT reliability: 67.66%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 281 ms: 1.03x slower                                                     |
| chameleon      | 7.41 ms                                                | 6.90 ms: 1.07x faster                                                    |
| docutils       | 2.77 sec                                               | 2.97 sec: 1.07x slower                                                   |
| tornado_http   | 103 ms                                                 | 97.2 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                  | 1.01x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 338 ms: 1.33x faster                                                     |
| async_tree_none            | 472 ms                                                 | 358 ms: 1.32x faster                                                     |
| async_tree_memoization_tg  | 575 ms                                                 | 445 ms: 1.29x faster                                                     |
| async_tree_io_tg           | 1.18 sec                                               | 939 ms: 1.26x faster                                                     |
| async_tree_memoization     | 578 ms                                                 | 460 ms: 1.26x faster                                                     |
| async_tree_io              | 1.16 sec                                               | 940 ms: 1.23x faster                                                     |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 610 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 617 ms: 1.18x faster                                                     |
| Geometric mean             | (ref)                                                  | 1.26x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 84.7 ms                                                | 76.5 ms: 1.11x faster                                                    |
| nbody          | 97.0 ms                                                | 91.3 ms: 1.06x faster                                                    |
| pidigits       | 187 ms                                                 | 189 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                  | 1.05x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 145 ms: 1.02x faster                                                     |
| regex_effbot   | 3.61 ms                                                | 3.70 ms: 1.02x slower                                                    |
| regex_dna      | 212 ms                                                 | 223 ms: 1.05x slower                                                     |
| regex_v8       | 23.1 ms                                                | 25.5 ms: 1.10x slower                                                    |
| Geometric mean | (ref)                                                  | 1.04x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                               | 2.06 sec: 1.13x faster                                                   |
| pickle_pure_python   | 324 us                                                 | 305 us: 1.06x faster                                                     |
| pickle_dict          | 35.5 us                                                | 34.2 us: 1.04x faster                                                    |
| pickle_list          | 5.08 us                                                | 4.90 us: 1.04x faster                                                    |
| xml_etree_process    | 61.7 ms                                                | 60.2 ms: 1.03x faster                                                    |
| xml_etree_generate   | 89.2 ms                                                | 87.8 ms: 1.02x faster                                                    |
| json_loads           | 28.5 us                                                | 28.1 us: 1.01x faster                                                    |
| unpickle             | 15.9 us                                                | 15.6 us: 1.01x faster                                                    |
| xml_etree_iterparse  | 107 ms                                                 | 107 ms: 1.01x slower                                                     |
| json_dumps           | 10.4 ms                                                | 10.5 ms: 1.01x slower                                                    |
| unpickle_list        | 5.29 us                                                | 5.32 us: 1.01x slower                                                    |
| xml_etree_parse      | 159 ms                                                 | 162 ms: 1.02x slower                                                     |
| unpickle_pure_python | 230 us                                                 | 242 us: 1.05x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                             |

Benchmark hidden because not significant (1): pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 9.55 ms                                                | 11.1 ms: 1.16x slower                                                    |
| python_startup_no_site | 6.94 ms                                                | 9.57 ms: 1.38x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.26x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|-----------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako      | 11.9 ms                                                | 10.6 ms: 1.12x faster                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 116 us: 1.36x faster                                                     |
| async_tree_none_tg         | 450 ms                                                 | 338 ms: 1.33x faster                                                     |
| async_tree_none            | 472 ms                                                 | 358 ms: 1.32x faster                                                     |
| async_tree_memoization_tg  | 575 ms                                                 | 445 ms: 1.29x faster                                                     |
| async_tree_io_tg           | 1.18 sec                                               | 939 ms: 1.26x faster                                                     |
| async_tree_memoization     | 578 ms                                                 | 460 ms: 1.26x faster                                                     |
| async_tree_io              | 1.16 sec                                               | 940 ms: 1.23x faster                                                     |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 610 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 617 ms: 1.18x faster                                                     |
| comprehensions             | 21.8 us                                                | 18.6 us: 1.17x faster                                                    |
| raytrace                   | 312 ms                                                 | 276 ms: 1.13x faster                                                     |
| scimark_fft                | 382 ms                                                 | 337 ms: 1.13x faster                                                     |
| tomli_loads                | 2.33 sec                                               | 2.06 sec: 1.13x faster                                                   |
| mako                       | 11.9 ms                                                | 10.6 ms: 1.12x faster                                                    |
| float                      | 84.7 ms                                                | 76.5 ms: 1.11x faster                                                    |
| logging_format             | 7.23 us                                                | 6.54 us: 1.11x faster                                                    |
| scimark_monte_carlo        | 75.1 ms                                                | 68.2 ms: 1.10x faster                                                    |
| logging_simple             | 6.46 us                                                | 5.93 us: 1.09x faster                                                    |
| crypto_pyaes               | 81.9 ms                                                | 76.0 ms: 1.08x faster                                                    |
| chameleon                  | 7.41 ms                                                | 6.90 ms: 1.07x faster                                                    |
| nbody                      | 97.0 ms                                                | 91.3 ms: 1.06x faster                                                    |
| pickle_pure_python         | 324 us                                                 | 305 us: 1.06x faster                                                     |
| chaos                      | 67.0 ms                                                | 63.1 ms: 1.06x faster                                                    |
| richards                   | 45.8 ms                                                | 43.3 ms: 1.06x faster                                                    |
| tornado_http               | 103 ms                                                 | 97.2 ms: 1.06x faster                                                    |
| gc_traversal               | 3.79 ms                                                | 3.61 ms: 1.05x faster                                                    |
| deepcopy_memo              | 40.7 us                                                | 39.2 us: 1.04x faster                                                    |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 4.86 ms: 1.04x faster                                                    |
| pickle_dict                | 35.5 us                                                | 34.2 us: 1.04x faster                                                    |
| pickle_list                | 5.08 us                                                | 4.90 us: 1.04x faster                                                    |
| richards_super             | 51.5 ms                                                | 49.7 ms: 1.04x faster                                                    |
| generators                 | 31.2 ms                                                | 30.1 ms: 1.04x faster                                                    |
| fannkuch                   | 417 ms                                                 | 403 ms: 1.04x faster                                                     |
| logging_silent             | 104 ns                                                 | 101 ns: 1.03x faster                                                     |
| pprint_safe_repr           | 776 ms                                                 | 754 ms: 1.03x faster                                                     |
| coroutines                 | 23.2 ms                                                | 22.5 ms: 1.03x faster                                                    |
| sqlglot_parse              | 1.36 ms                                                | 1.33 ms: 1.03x faster                                                    |
| xml_etree_process          | 61.7 ms                                                | 60.2 ms: 1.03x faster                                                    |
| deepcopy_reduce            | 3.35 us                                                | 3.27 us: 1.02x faster                                                    |
| regex_compile              | 148 ms                                                 | 145 ms: 1.02x faster                                                     |
| spectral_norm              | 115 ms                                                 | 113 ms: 1.02x faster                                                     |
| sqlglot_transpile          | 1.68 ms                                                | 1.65 ms: 1.02x faster                                                    |
| xml_etree_generate         | 89.2 ms                                                | 87.8 ms: 1.02x faster                                                    |
| json_loads                 | 28.5 us                                                | 28.1 us: 1.01x faster                                                    |
| unpickle                   | 15.9 us                                                | 15.6 us: 1.01x faster                                                    |
| pprint_pformat             | 1.57 sec                                               | 1.55 sec: 1.01x faster                                                   |
| pyflate                    | 482 ms                                                 | 478 ms: 1.01x faster                                                     |
| xml_etree_iterparse        | 107 ms                                                 | 107 ms: 1.01x slower                                                     |
| json_dumps                 | 10.4 ms                                                | 10.5 ms: 1.01x slower                                                    |
| unpickle_list              | 5.29 us                                                | 5.32 us: 1.01x slower                                                    |
| pathlib                    | 19.3 ms                                                | 19.5 ms: 1.01x slower                                                    |
| pidigits                   | 187 ms                                                 | 189 ms: 1.01x slower                                                     |
| mdp                        | 2.63 sec                                               | 2.66 sec: 1.01x slower                                                   |
| sympy_sum                  | 169 ms                                                 | 171 ms: 1.01x slower                                                     |
| xml_etree_parse            | 159 ms                                                 | 162 ms: 1.02x slower                                                     |
| dask                       | 372 ms                                                 | 379 ms: 1.02x slower                                                     |
| sqlite_synth               | 2.83 us                                                | 2.90 us: 1.02x slower                                                    |
| regex_effbot               | 3.61 ms                                                | 3.70 ms: 1.02x slower                                                    |
| 2to3                       | 274 ms                                                 | 281 ms: 1.03x slower                                                     |
| bench_thread_pool          | 842 us                                                 | 864 us: 1.03x slower                                                     |
| dulwich_log                | 68.5 ms                                                | 70.4 ms: 1.03x slower                                                    |
| asyncio_websockets         | 551 ms                                                 | 567 ms: 1.03x slower                                                     |
| deltablue                  | 3.72 ms                                                | 3.82 ms: 1.03x slower                                                    |
| sqlglot_normalize          | 110 ms                                                 | 115 ms: 1.04x slower                                                     |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.86 sec: 1.04x slower                                                   |
| pycparser                  | 1.18 sec                                               | 1.23 sec: 1.04x slower                                                   |
| regex_dna                  | 212 ms                                                 | 223 ms: 1.05x slower                                                     |
| unpickle_pure_python       | 230 us                                                 | 242 us: 1.05x slower                                                     |
| sympy_expand               | 478 ms                                                 | 504 ms: 1.05x slower                                                     |
| aiohttp                    | 1.15 ms                                                | 1.21 ms: 1.06x slower                                                    |
| sympy_integrate            | 21.4 ms                                                | 22.6 ms: 1.06x slower                                                    |
| gunicorn                   | 1.24 ms                                                | 1.31 ms: 1.06x slower                                                    |
| sqlglot_optimize           | 54.8 ms                                                | 58.1 ms: 1.06x slower                                                    |
| scimark_sor                | 129 ms                                                 | 138 ms: 1.07x slower                                                     |
| go                         | 139 ms                                                 | 149 ms: 1.07x slower                                                     |
| docutils                   | 2.77 sec                                               | 2.97 sec: 1.07x slower                                                   |
| asyncio_tcp                | 491 ms                                                 | 527 ms: 1.07x slower                                                     |
| regex_v8                   | 23.1 ms                                                | 25.5 ms: 1.10x slower                                                    |
| scimark_lu                 | 118 ms                                                 | 130 ms: 1.10x slower                                                     |
| nqueens                    | 83.3 ms                                                | 93.1 ms: 1.12x slower                                                    |
| hexiom                     | 6.41 ms                                                | 7.17 ms: 1.12x slower                                                    |
| python_startup             | 9.55 ms                                                | 11.1 ms: 1.16x slower                                                    |
| create_gc_cycles           | 1.48 ms                                                | 1.76 ms: 1.19x slower                                                    |
| telco                      | 7.10 ms                                                | 8.58 ms: 1.21x slower                                                    |
| coverage                   | 72.7 ms                                                | 99.0 ms: 1.36x slower                                                    |
| python_startup_no_site     | 6.94 ms                                                | 9.57 ms: 1.38x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.02x faster                                                             |

Benchmark hidden because not significant (8): mypy2, deepcopy, bench_mp_pool, sympy_str, json, meteor_contest, async_generators, pickle
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240404-3.13.0a5+-7422720-JIT/bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 67.66% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.04x