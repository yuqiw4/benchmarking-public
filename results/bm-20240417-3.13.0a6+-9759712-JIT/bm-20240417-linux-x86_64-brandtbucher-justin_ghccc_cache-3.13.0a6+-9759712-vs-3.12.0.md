# Results vs. 3.12.0

- fork: brandtbucher
- ref: justin_ghccc_cache
- machine: linux-x86_64
- commit hash: 9759712
- commit date: 2024-04-17
- overall geometric mean: 1.04x faster
- HPT reliability: 97.11%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.07x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-9759712 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 276 ms: 1.01x slower                                                       |
| chameleon      | 7.41 ms                                                | 7.12 ms: 1.04x faster                                                      |
| docutils       | 2.77 sec                                               | 2.91 sec: 1.05x slower                                                     |
| tornado_http   | 103 ms                                                 | 96.2 ms: 1.07x faster                                                      |
| Geometric mean | (ref)                                                  | 1.01x faster                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-9759712 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 335 ms: 1.34x faster                                                       |
| async_tree_none            | 472 ms                                                 | 357 ms: 1.32x faster                                                       |
| async_tree_memoization_tg  | 575 ms                                                 | 441 ms: 1.30x faster                                                       |
| async_tree_io              | 1.16 sec                                               | 922 ms: 1.25x faster                                                       |
| async_tree_io_tg           | 1.18 sec                                               | 951 ms: 1.24x faster                                                       |
| async_tree_memoization     | 578 ms                                                 | 467 ms: 1.24x faster                                                       |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 610 ms: 1.19x faster                                                       |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 616 ms: 1.18x faster                                                       |
| Geometric mean             | (ref)                                                  | 1.26x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-9759712 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| nbody          | 97.0 ms                                                | 77.1 ms: 1.26x faster                                                      |
| float          | 84.7 ms                                                | 72.9 ms: 1.16x faster                                                      |
| pidigits       | 187 ms                                                 | 189 ms: 1.01x slower                                                       |
| Geometric mean | (ref)                                                  | 1.13x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-9759712 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 140 ms: 1.06x faster                                                       |
| regex_effbot   | 3.61 ms                                                | 3.77 ms: 1.05x slower                                                      |
| regex_dna      | 212 ms                                                 | 225 ms: 1.06x slower                                                       |
| regex_v8       | 23.1 ms                                                | 25.8 ms: 1.11x slower                                                      |
| Geometric mean | (ref)                                                  | 1.04x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-9759712 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                               | 1.93 sec: 1.21x faster                                                     |
| pickle_pure_python   | 324 us                                                 | 304 us: 1.06x faster                                                       |
| pickle_dict          | 35.5 us                                                | 34.1 us: 1.04x faster                                                      |
| xml_etree_process    | 61.7 ms                                                | 59.5 ms: 1.04x faster                                                      |
| pickle_list          | 5.08 us                                                | 4.91 us: 1.04x faster                                                      |
| unpickle             | 15.9 us                                                | 15.3 us: 1.04x faster                                                      |
| unpickle_list        | 5.29 us                                                | 5.12 us: 1.03x faster                                                      |
| unpickle_pure_python | 230 us                                                 | 224 us: 1.03x faster                                                       |
| json_loads           | 28.5 us                                                | 27.8 us: 1.03x faster                                                      |
| xml_etree_generate   | 89.2 ms                                                | 87.2 ms: 1.02x faster                                                      |
| xml_etree_iterparse  | 107 ms                                                 | 106 ms: 1.00x faster                                                       |
| json_dumps           | 10.4 ms                                                | 10.5 ms: 1.01x slower                                                      |
| xml_etree_parse      | 159 ms                                                 | 161 ms: 1.01x slower                                                       |
| Geometric mean       | (ref)                                                  | 1.04x faster                                                               |

Benchmark hidden because not significant (1): pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-9759712 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.66 ms: 1.10x slower                                                      |
| python_startup         | 9.55 ms                                                | 11.1 ms: 1.16x slower                                                      |
| Geometric mean         | (ref)                                                  | 1.13x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-9759712 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 10.1 ms: 1.18x faster                                                      |
| django_template | 34.6 ms                                                | 35.6 ms: 1.03x slower                                                      |
| Geometric mean  | (ref)                                                  | 1.07x faster                                                               |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-9759712 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 112 us: 1.41x faster                                                       |
| async_tree_none_tg         | 450 ms                                                 | 335 ms: 1.34x faster                                                       |
| async_tree_none            | 472 ms                                                 | 357 ms: 1.32x faster                                                       |
| async_tree_memoization_tg  | 575 ms                                                 | 441 ms: 1.30x faster                                                       |
| comprehensions             | 21.8 us                                                | 17.2 us: 1.27x faster                                                      |
| nbody                      | 97.0 ms                                                | 77.1 ms: 1.26x faster                                                      |
| scimark_fft                | 382 ms                                                 | 304 ms: 1.26x faster                                                       |
| async_tree_io              | 1.16 sec                                               | 922 ms: 1.25x faster                                                       |
| async_tree_io_tg           | 1.18 sec                                               | 951 ms: 1.24x faster                                                       |
| async_tree_memoization     | 578 ms                                                 | 467 ms: 1.24x faster                                                       |
| tomli_loads                | 2.33 sec                                               | 1.93 sec: 1.21x faster                                                     |
| crypto_pyaes               | 81.9 ms                                                | 68.5 ms: 1.20x faster                                                      |
| fannkuch                   | 417 ms                                                 | 350 ms: 1.19x faster                                                       |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 610 ms: 1.19x faster                                                       |
| scimark_monte_carlo        | 75.1 ms                                                | 63.4 ms: 1.18x faster                                                      |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 616 ms: 1.18x faster                                                       |
| mako                       | 11.9 ms                                                | 10.1 ms: 1.18x faster                                                      |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 4.34 ms: 1.16x faster                                                      |
| float                      | 84.7 ms                                                | 72.9 ms: 1.16x faster                                                      |
| raytrace                   | 312 ms                                                 | 270 ms: 1.16x faster                                                       |
| spectral_norm              | 115 ms                                                 | 99.8 ms: 1.15x faster                                                      |
| logging_format             | 7.23 us                                                | 6.37 us: 1.14x faster                                                      |
| logging_simple             | 6.46 us                                                | 5.74 us: 1.13x faster                                                      |
| chaos                      | 67.0 ms                                                | 60.2 ms: 1.11x faster                                                      |
| pathlib                    | 19.3 ms                                                | 17.6 ms: 1.10x faster                                                      |
| pyflate                    | 482 ms                                                 | 441 ms: 1.09x faster                                                       |
| pprint_safe_repr           | 776 ms                                                 | 722 ms: 1.07x faster                                                       |
| richards                   | 45.8 ms                                                | 42.9 ms: 1.07x faster                                                      |
| tornado_http               | 103 ms                                                 | 96.2 ms: 1.07x faster                                                      |
| pickle_pure_python         | 324 us                                                 | 304 us: 1.06x faster                                                       |
| pprint_pformat             | 1.57 sec                                               | 1.48 sec: 1.06x faster                                                     |
| richards_super             | 51.5 ms                                                | 48.5 ms: 1.06x faster                                                      |
| regex_compile              | 148 ms                                                 | 140 ms: 1.06x faster                                                       |
| generators                 | 31.2 ms                                                | 29.6 ms: 1.05x faster                                                      |
| deepcopy_reduce            | 3.35 us                                                | 3.19 us: 1.05x faster                                                      |
| pickle_dict                | 35.5 us                                                | 34.1 us: 1.04x faster                                                      |
| chameleon                  | 7.41 ms                                                | 7.12 ms: 1.04x faster                                                      |
| sqlglot_parse              | 1.36 ms                                                | 1.31 ms: 1.04x faster                                                      |
| xml_etree_process          | 61.7 ms                                                | 59.5 ms: 1.04x faster                                                      |
| deepcopy_memo              | 40.7 us                                                | 39.3 us: 1.04x faster                                                      |
| pickle_list                | 5.08 us                                                | 4.91 us: 1.04x faster                                                      |
| unpickle                   | 15.9 us                                                | 15.3 us: 1.04x faster                                                      |
| sqlglot_transpile          | 1.68 ms                                                | 1.63 ms: 1.04x faster                                                      |
| deepcopy                   | 371 us                                                 | 359 us: 1.04x faster                                                       |
| json                       | 5.26 ms                                                | 5.08 ms: 1.03x faster                                                      |
| unpickle_list              | 5.29 us                                                | 5.12 us: 1.03x faster                                                      |
| meteor_contest             | 112 ms                                                 | 109 ms: 1.03x faster                                                       |
| unpickle_pure_python       | 230 us                                                 | 224 us: 1.03x faster                                                       |
| json_loads                 | 28.5 us                                                | 27.8 us: 1.03x faster                                                      |
| scimark_sor                | 129 ms                                                 | 126 ms: 1.03x faster                                                       |
| coroutines                 | 23.2 ms                                                | 22.7 ms: 1.02x faster                                                      |
| xml_etree_generate         | 89.2 ms                                                | 87.2 ms: 1.02x faster                                                      |
| sympy_str                  | 300 ms                                                 | 295 ms: 1.02x faster                                                       |
| logging_silent             | 104 ns                                                 | 103 ns: 1.01x faster                                                       |
| sympy_sum                  | 169 ms                                                 | 168 ms: 1.01x faster                                                       |
| xml_etree_iterparse        | 107 ms                                                 | 106 ms: 1.00x faster                                                       |
| 2to3                       | 274 ms                                                 | 276 ms: 1.01x slower                                                       |
| pidigits                   | 187 ms                                                 | 189 ms: 1.01x slower                                                       |
| json_dumps                 | 10.4 ms                                                | 10.5 ms: 1.01x slower                                                      |
| xml_etree_parse            | 159 ms                                                 | 161 ms: 1.01x slower                                                       |
| dulwich_log                | 68.5 ms                                                | 69.1 ms: 1.01x slower                                                      |
| sqlite_synth               | 2.83 us                                                | 2.87 us: 1.01x slower                                                      |
| async_generators           | 463 ms                                                 | 471 ms: 1.02x slower                                                       |
| asyncio_websockets         | 551 ms                                                 | 564 ms: 1.02x slower                                                       |
| sqlglot_normalize          | 110 ms                                                 | 113 ms: 1.02x slower                                                       |
| bench_thread_pool          | 842 us                                                 | 864 us: 1.03x slower                                                       |
| sympy_integrate            | 21.4 ms                                                | 22.0 ms: 1.03x slower                                                      |
| django_template            | 34.6 ms                                                | 35.6 ms: 1.03x slower                                                      |
| pycparser                  | 1.18 sec                                               | 1.22 sec: 1.03x slower                                                     |
| sympy_expand               | 478 ms                                                 | 496 ms: 1.04x slower                                                       |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.86 sec: 1.04x slower                                                     |
| asyncio_tcp                | 491 ms                                                 | 512 ms: 1.04x slower                                                       |
| sqlglot_optimize           | 54.8 ms                                                | 57.3 ms: 1.05x slower                                                      |
| regex_effbot               | 3.61 ms                                                | 3.77 ms: 1.05x slower                                                      |
| mdp                        | 2.63 sec                                               | 2.75 sec: 1.05x slower                                                     |
| hexiom                     | 6.41 ms                                                | 6.71 ms: 1.05x slower                                                      |
| gunicorn                   | 1.24 ms                                                | 1.30 ms: 1.05x slower                                                      |
| scimark_lu                 | 118 ms                                                 | 124 ms: 1.05x slower                                                       |
| aiohttp                    | 1.15 ms                                                | 1.21 ms: 1.05x slower                                                      |
| docutils                   | 2.77 sec                                               | 2.91 sec: 1.05x slower                                                     |
| go                         | 139 ms                                                 | 147 ms: 1.05x slower                                                       |
| gc_traversal               | 3.79 ms                                                | 4.00 ms: 1.06x slower                                                      |
| nqueens                    | 83.3 ms                                                | 88.2 ms: 1.06x slower                                                      |
| regex_dna                  | 212 ms                                                 | 225 ms: 1.06x slower                                                       |
| python_startup_no_site     | 6.94 ms                                                | 7.66 ms: 1.10x slower                                                      |
| regex_v8                   | 23.1 ms                                                | 25.8 ms: 1.11x slower                                                      |
| python_startup             | 9.55 ms                                                | 11.1 ms: 1.16x slower                                                      |
| create_gc_cycles           | 1.48 ms                                                | 1.75 ms: 1.18x slower                                                      |
| telco                      | 7.10 ms                                                | 8.52 ms: 1.20x slower                                                      |
| coverage                   | 72.7 ms                                                | 97.8 ms: 1.35x slower                                                      |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                               |

Benchmark hidden because not significant (5): mypy2, deltablue, pickle, bench_mp_pool, dask
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240417-3.13.0a6+-9759712-JIT/bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-9759712.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 97.11% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.07x