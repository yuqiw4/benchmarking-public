# Results vs. 3.12.0

- fork: brandtbucher
- ref: justin_ghccc_cache
- machine: linux-x86_64
- commit hash: f14407b
- commit date: 2024-04-26
- overall geometric mean: 1.04x faster
- HPT reliability: 98.25%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.07x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-f14407b |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 275 ms: 1.00x slower                                                       |
| chameleon      | 7.41 ms                                                | 7.04 ms: 1.05x faster                                                      |
| docutils       | 2.77 sec                                               | 2.93 sec: 1.06x slower                                                     |
| tornado_http   | 103 ms                                                 | 95.6 ms: 1.07x faster                                                      |
| Geometric mean | (ref)                                                  | 1.02x faster                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-f14407b |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 335 ms: 1.34x faster                                                       |
| async_tree_none            | 472 ms                                                 | 355 ms: 1.33x faster                                                       |
| async_tree_memoization_tg  | 575 ms                                                 | 438 ms: 1.31x faster                                                       |
| async_tree_io              | 1.16 sec                                               | 921 ms: 1.25x faster                                                       |
| async_tree_io_tg           | 1.18 sec                                               | 947 ms: 1.25x faster                                                       |
| async_tree_memoization     | 578 ms                                                 | 463 ms: 1.25x faster                                                       |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 607 ms: 1.20x faster                                                       |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 614 ms: 1.18x faster                                                       |
| Geometric mean             | (ref)                                                  | 1.26x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-f14407b |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| nbody          | 97.0 ms                                                | 80.0 ms: 1.21x faster                                                      |
| float          | 84.7 ms                                                | 73.1 ms: 1.16x faster                                                      |
| pidigits       | 187 ms                                                 | 210 ms: 1.12x slower                                                       |
| Geometric mean | (ref)                                                  | 1.08x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-f14407b |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 141 ms: 1.05x faster                                                       |
| regex_dna      | 212 ms                                                 | 225 ms: 1.06x slower                                                       |
| regex_v8       | 23.1 ms                                                | 24.7 ms: 1.07x slower                                                      |
| regex_effbot   | 3.61 ms                                                | 4.23 ms: 1.17x slower                                                      |
| Geometric mean | (ref)                                                  | 1.06x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-f14407b |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                               | 1.93 sec: 1.21x faster                                                     |
| xml_etree_parse      | 159 ms                                                 | 149 ms: 1.07x faster                                                       |
| pickle_pure_python   | 324 us                                                 | 308 us: 1.05x faster                                                       |
| xml_etree_iterparse  | 107 ms                                                 | 102 ms: 1.05x faster                                                       |
| json_loads           | 28.5 us                                                | 27.4 us: 1.04x faster                                                      |
| xml_etree_process    | 61.7 ms                                                | 60.0 ms: 1.03x faster                                                      |
| unpickle_list        | 5.29 us                                                | 5.14 us: 1.03x faster                                                      |
| xml_etree_generate   | 89.2 ms                                                | 86.8 ms: 1.03x faster                                                      |
| pickle_dict          | 35.5 us                                                | 34.8 us: 1.02x faster                                                      |
| unpickle             | 15.9 us                                                | 15.5 us: 1.02x faster                                                      |
| unpickle_pure_python | 230 us                                                 | 226 us: 1.02x faster                                                       |
| json_dumps           | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                      |
| pickle               | 11.6 us                                                | 12.0 us: 1.03x slower                                                      |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                               |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-f14407b |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.66 ms: 1.10x slower                                                      |
| python_startup         | 9.55 ms                                                | 11.1 ms: 1.16x slower                                                      |
| Geometric mean         | (ref)                                                  | 1.13x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-f14407b |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 10.0 ms: 1.18x faster                                                      |
| django_template | 34.6 ms                                                | 36.7 ms: 1.06x slower                                                      |
| Geometric mean  | (ref)                                                  | 1.06x faster                                                               |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-f14407b |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 117 us: 1.35x faster                                                       |
| async_tree_none_tg         | 450 ms                                                 | 335 ms: 1.34x faster                                                       |
| async_tree_none            | 472 ms                                                 | 355 ms: 1.33x faster                                                       |
| async_tree_memoization_tg  | 575 ms                                                 | 438 ms: 1.31x faster                                                       |
| comprehensions             | 21.8 us                                                | 17.2 us: 1.27x faster                                                      |
| async_tree_io              | 1.16 sec                                               | 921 ms: 1.25x faster                                                       |
| async_tree_io_tg           | 1.18 sec                                               | 947 ms: 1.25x faster                                                       |
| async_tree_memoization     | 578 ms                                                 | 463 ms: 1.25x faster                                                       |
| scimark_fft                | 382 ms                                                 | 310 ms: 1.23x faster                                                       |
| nbody                      | 97.0 ms                                                | 80.0 ms: 1.21x faster                                                      |
| crypto_pyaes               | 81.9 ms                                                | 67.6 ms: 1.21x faster                                                      |
| tomli_loads                | 2.33 sec                                               | 1.93 sec: 1.21x faster                                                     |
| scimark_monte_carlo        | 75.1 ms                                                | 62.5 ms: 1.20x faster                                                      |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 607 ms: 1.20x faster                                                       |
| mako                       | 11.9 ms                                                | 10.0 ms: 1.18x faster                                                      |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 614 ms: 1.18x faster                                                       |
| fannkuch                   | 417 ms                                                 | 357 ms: 1.17x faster                                                       |
| float                      | 84.7 ms                                                | 73.1 ms: 1.16x faster                                                      |
| spectral_norm              | 115 ms                                                 | 99.2 ms: 1.16x faster                                                      |
| raytrace                   | 312 ms                                                 | 274 ms: 1.14x faster                                                       |
| pyflate                    | 482 ms                                                 | 434 ms: 1.11x faster                                                       |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 4.55 ms: 1.11x faster                                                      |
| logging_format             | 7.23 us                                                | 6.52 us: 1.11x faster                                                      |
| chaos                      | 67.0 ms                                                | 61.0 ms: 1.10x faster                                                      |
| logging_simple             | 6.46 us                                                | 5.92 us: 1.09x faster                                                      |
| pathlib                    | 19.3 ms                                                | 17.9 ms: 1.08x faster                                                      |
| richards                   | 45.8 ms                                                | 42.4 ms: 1.08x faster                                                      |
| pprint_safe_repr           | 776 ms                                                 | 722 ms: 1.08x faster                                                       |
| tornado_http               | 103 ms                                                 | 95.6 ms: 1.07x faster                                                      |
| pprint_pformat             | 1.57 sec                                               | 1.46 sec: 1.07x faster                                                     |
| xml_etree_parse            | 159 ms                                                 | 149 ms: 1.07x faster                                                       |
| regex_compile              | 148 ms                                                 | 141 ms: 1.05x faster                                                       |
| chameleon                  | 7.41 ms                                                | 7.04 ms: 1.05x faster                                                      |
| pickle_pure_python         | 324 us                                                 | 308 us: 1.05x faster                                                       |
| richards_super             | 51.5 ms                                                | 48.9 ms: 1.05x faster                                                      |
| generators                 | 31.2 ms                                                | 29.8 ms: 1.05x faster                                                      |
| xml_etree_iterparse        | 107 ms                                                 | 102 ms: 1.05x faster                                                       |
| deepcopy_reduce            | 3.35 us                                                | 3.20 us: 1.05x faster                                                      |
| sqlglot_parse              | 1.36 ms                                                | 1.31 ms: 1.04x faster                                                      |
| json_loads                 | 28.5 us                                                | 27.4 us: 1.04x faster                                                      |
| sqlglot_transpile          | 1.68 ms                                                | 1.63 ms: 1.03x faster                                                      |
| xml_etree_process          | 61.7 ms                                                | 60.0 ms: 1.03x faster                                                      |
| unpickle_list              | 5.29 us                                                | 5.14 us: 1.03x faster                                                      |
| xml_etree_generate         | 89.2 ms                                                | 86.8 ms: 1.03x faster                                                      |
| deepcopy                   | 371 us                                                 | 362 us: 1.03x faster                                                       |
| meteor_contest             | 112 ms                                                 | 110 ms: 1.02x faster                                                       |
| deepcopy_memo              | 40.7 us                                                | 39.8 us: 1.02x faster                                                      |
| json                       | 5.26 ms                                                | 5.13 ms: 1.02x faster                                                      |
| pickle_dict                | 35.5 us                                                | 34.8 us: 1.02x faster                                                      |
| sympy_str                  | 300 ms                                                 | 294 ms: 1.02x faster                                                       |
| unpickle                   | 15.9 us                                                | 15.5 us: 1.02x faster                                                      |
| coroutines                 | 23.2 ms                                                | 22.8 ms: 1.02x faster                                                      |
| unpickle_pure_python       | 230 us                                                 | 226 us: 1.02x faster                                                       |
| sympy_sum                  | 169 ms                                                 | 166 ms: 1.02x faster                                                       |
| pycparser                  | 1.18 sec                                               | 1.16 sec: 1.01x faster                                                     |
| logging_silent             | 104 ns                                                 | 104 ns: 1.01x faster                                                       |
| scimark_sor                | 129 ms                                                 | 128 ms: 1.01x faster                                                       |
| 2to3                       | 274 ms                                                 | 275 ms: 1.00x slower                                                       |
| async_generators           | 463 ms                                                 | 470 ms: 1.01x slower                                                       |
| dulwich_log                | 68.5 ms                                                | 69.7 ms: 1.02x slower                                                      |
| gc_traversal               | 3.79 ms                                                | 3.86 ms: 1.02x slower                                                      |
| asyncio_websockets         | 551 ms                                                 | 564 ms: 1.02x slower                                                       |
| sympy_integrate            | 21.4 ms                                                | 21.9 ms: 1.02x slower                                                      |
| hexiom                     | 6.41 ms                                                | 6.57 ms: 1.02x slower                                                      |
| bench_thread_pool          | 842 us                                                 | 863 us: 1.03x slower                                                       |
| sqlglot_normalize          | 110 ms                                                 | 113 ms: 1.03x slower                                                       |
| json_dumps                 | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                      |
| pickle                     | 11.6 us                                                | 12.0 us: 1.03x slower                                                      |
| sympy_expand               | 478 ms                                                 | 496 ms: 1.04x slower                                                       |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.86 sec: 1.04x slower                                                     |
| sqlglot_optimize           | 54.8 ms                                                | 57.1 ms: 1.04x slower                                                      |
| asyncio_tcp                | 491 ms                                                 | 513 ms: 1.05x slower                                                       |
| gunicorn                   | 1.24 ms                                                | 1.30 ms: 1.05x slower                                                      |
| nqueens                    | 83.3 ms                                                | 87.5 ms: 1.05x slower                                                      |
| aiohttp                    | 1.15 ms                                                | 1.21 ms: 1.05x slower                                                      |
| go                         | 139 ms                                                 | 147 ms: 1.05x slower                                                       |
| mdp                        | 2.63 sec                                               | 2.79 sec: 1.06x slower                                                     |
| django_template            | 34.6 ms                                                | 36.7 ms: 1.06x slower                                                      |
| docutils                   | 2.77 sec                                               | 2.93 sec: 1.06x slower                                                     |
| regex_dna                  | 212 ms                                                 | 225 ms: 1.06x slower                                                       |
| scimark_lu                 | 118 ms                                                 | 125 ms: 1.06x slower                                                       |
| regex_v8                   | 23.1 ms                                                | 24.7 ms: 1.07x slower                                                      |
| python_startup_no_site     | 6.94 ms                                                | 7.66 ms: 1.10x slower                                                      |
| pidigits                   | 187 ms                                                 | 210 ms: 1.12x slower                                                       |
| python_startup             | 9.55 ms                                                | 11.1 ms: 1.16x slower                                                      |
| regex_effbot               | 3.61 ms                                                | 4.23 ms: 1.17x slower                                                      |
| create_gc_cycles           | 1.48 ms                                                | 1.75 ms: 1.19x slower                                                      |
| telco                      | 7.10 ms                                                | 8.74 ms: 1.23x slower                                                      |
| coverage                   | 72.7 ms                                                | 98.1 ms: 1.35x slower                                                      |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                               |

Benchmark hidden because not significant (6): mypy2, sqlite_synth, bench_mp_pool, deltablue, pickle_list, dask
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240426-3.13.0a6+-f14407b-JIT/bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-f14407b.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 98.25% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.07x