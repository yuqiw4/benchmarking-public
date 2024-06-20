# Results vs. 3.12.0

- fork: brandtbucher
- ref: justin_cache
- machine: linux-x86_64
- commit hash: f4c10d5
- commit date: 2024-04-18
- overall geometric mean: 1.02x faster
- HPT reliability: 78.65%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.07x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6+-f4c10d5 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 278 ms: 1.01x slower                                                 |
| chameleon      | 7.41 ms                                                | 7.08 ms: 1.05x faster                                                |
| docutils       | 2.77 sec                                               | 2.92 sec: 1.06x slower                                               |
| tornado_http   | 103 ms                                                 | 96.6 ms: 1.06x faster                                                |
| Geometric mean | (ref)                                                  | 1.01x faster                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6+-f4c10d5 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 338 ms: 1.33x faster                                                 |
| async_tree_none            | 472 ms                                                 | 362 ms: 1.30x faster                                                 |
| async_tree_memoization_tg  | 575 ms                                                 | 444 ms: 1.29x faster                                                 |
| async_tree_io_tg           | 1.18 sec                                               | 952 ms: 1.24x faster                                                 |
| async_tree_memoization     | 578 ms                                                 | 468 ms: 1.24x faster                                                 |
| async_tree_io              | 1.16 sec                                               | 941 ms: 1.23x faster                                                 |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 609 ms: 1.19x faster                                                 |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 620 ms: 1.17x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.25x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6+-f4c10d5 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| nbody          | 97.0 ms                                                | 87.3 ms: 1.11x faster                                                |
| float          | 84.7 ms                                                | 77.7 ms: 1.09x faster                                                |
| pidigits       | 187 ms                                                 | 210 ms: 1.12x slower                                                 |
| Geometric mean | (ref)                                                  | 1.03x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6+-f4c10d5 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 144 ms: 1.03x faster                                                 |
| regex_effbot   | 3.61 ms                                                | 3.68 ms: 1.02x slower                                                |
| regex_dna      | 212 ms                                                 | 221 ms: 1.04x slower                                                 |
| regex_v8       | 23.1 ms                                                | 25.0 ms: 1.08x slower                                                |
| Geometric mean | (ref)                                                  | 1.03x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6+-f4c10d5 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                               | 2.01 sec: 1.16x faster                                               |
| pickle_pure_python   | 324 us                                                 | 305 us: 1.06x faster                                                 |
| json_loads           | 28.5 us                                                | 27.7 us: 1.03x faster                                                |
| xml_etree_process    | 61.7 ms                                                | 60.4 ms: 1.02x faster                                                |
| xml_etree_generate   | 89.2 ms                                                | 88.1 ms: 1.01x faster                                                |
| unpickle             | 15.9 us                                                | 15.7 us: 1.01x faster                                                |
| pickle_dict          | 35.5 us                                                | 36.0 us: 1.01x slower                                                |
| xml_etree_iterparse  | 107 ms                                                 | 109 ms: 1.02x slower                                                 |
| json_dumps           | 10.4 ms                                                | 10.6 ms: 1.02x slower                                                |
| unpickle_pure_python | 230 us                                                 | 236 us: 1.03x slower                                                 |
| pickle               | 11.6 us                                                | 12.0 us: 1.04x slower                                                |
| pickle_list          | 5.08 us                                                | 5.33 us: 1.05x slower                                                |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                         |

Benchmark hidden because not significant (2): unpickle_list, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6+-f4c10d5 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.69 ms: 1.11x slower                                                |
| python_startup         | 9.55 ms                                                | 11.1 ms: 1.17x slower                                                |
| Geometric mean         | (ref)                                                  | 1.14x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6+-f4c10d5 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 11.5 ms: 1.03x faster                                                |
| django_template | 34.6 ms                                                | 36.2 ms: 1.05x slower                                                |
| Geometric mean  | (ref)                                                  | 1.01x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6+-f4c10d5 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 112 us: 1.41x faster                                                 |
| async_tree_none_tg         | 450 ms                                                 | 338 ms: 1.33x faster                                                 |
| async_tree_none            | 472 ms                                                 | 362 ms: 1.30x faster                                                 |
| async_tree_memoization_tg  | 575 ms                                                 | 444 ms: 1.29x faster                                                 |
| async_tree_io_tg           | 1.18 sec                                               | 952 ms: 1.24x faster                                                 |
| async_tree_memoization     | 578 ms                                                 | 468 ms: 1.24x faster                                                 |
| async_tree_io              | 1.16 sec                                               | 941 ms: 1.23x faster                                                 |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 609 ms: 1.19x faster                                                 |
| comprehensions             | 21.8 us                                                | 18.3 us: 1.19x faster                                                |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 620 ms: 1.17x faster                                                 |
| tomli_loads                | 2.33 sec                                               | 2.01 sec: 1.16x faster                                               |
| logging_format             | 7.23 us                                                | 6.36 us: 1.14x faster                                                |
| raytrace                   | 312 ms                                                 | 275 ms: 1.13x faster                                                 |
| logging_simple             | 6.46 us                                                | 5.75 us: 1.12x faster                                                |
| scimark_fft                | 382 ms                                                 | 341 ms: 1.12x faster                                                 |
| nbody                      | 97.0 ms                                                | 87.3 ms: 1.11x faster                                                |
| scimark_monte_carlo        | 75.1 ms                                                | 67.9 ms: 1.11x faster                                                |
| crypto_pyaes               | 81.9 ms                                                | 73.9 ms: 1.11x faster                                                |
| float                      | 84.7 ms                                                | 77.7 ms: 1.09x faster                                                |
| pathlib                    | 19.3 ms                                                | 17.8 ms: 1.08x faster                                                |
| fannkuch                   | 417 ms                                                 | 389 ms: 1.07x faster                                                 |
| deepcopy_memo              | 40.7 us                                                | 38.2 us: 1.07x faster                                                |
| pickle_pure_python         | 324 us                                                 | 305 us: 1.06x faster                                                 |
| tornado_http               | 103 ms                                                 | 96.6 ms: 1.06x faster                                                |
| chaos                      | 67.0 ms                                                | 63.3 ms: 1.06x faster                                                |
| richards                   | 45.8 ms                                                | 43.6 ms: 1.05x faster                                                |
| richards_super             | 51.5 ms                                                | 49.0 ms: 1.05x faster                                                |
| deepcopy_reduce            | 3.35 us                                                | 3.19 us: 1.05x faster                                                |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 4.83 ms: 1.05x faster                                                |
| chameleon                  | 7.41 ms                                                | 7.08 ms: 1.05x faster                                                |
| deepcopy                   | 371 us                                                 | 356 us: 1.04x faster                                                 |
| pprint_safe_repr           | 776 ms                                                 | 751 ms: 1.03x faster                                                 |
| json                       | 5.26 ms                                                | 5.09 ms: 1.03x faster                                                |
| mako                       | 11.9 ms                                                | 11.5 ms: 1.03x faster                                                |
| regex_compile              | 148 ms                                                 | 144 ms: 1.03x faster                                                 |
| json_loads                 | 28.5 us                                                | 27.7 us: 1.03x faster                                                |
| generators                 | 31.2 ms                                                | 30.5 ms: 1.02x faster                                                |
| sqlglot_parse              | 1.36 ms                                                | 1.33 ms: 1.02x faster                                                |
| xml_etree_process          | 61.7 ms                                                | 60.4 ms: 1.02x faster                                                |
| pprint_pformat             | 1.57 sec                                               | 1.54 sec: 1.02x faster                                               |
| sqlglot_transpile          | 1.68 ms                                                | 1.65 ms: 1.02x faster                                                |
| logging_silent             | 104 ns                                                 | 103 ns: 1.02x faster                                                 |
| xml_etree_generate         | 89.2 ms                                                | 88.1 ms: 1.01x faster                                                |
| pycparser                  | 1.18 sec                                               | 1.17 sec: 1.01x faster                                               |
| pyflate                    | 482 ms                                                 | 479 ms: 1.01x faster                                                 |
| unpickle                   | 15.9 us                                                | 15.7 us: 1.01x faster                                                |
| async_generators           | 463 ms                                                 | 460 ms: 1.01x faster                                                 |
| mdp                        | 2.63 sec                                               | 2.64 sec: 1.00x slower                                               |
| spectral_norm              | 115 ms                                                 | 116 ms: 1.01x slower                                                 |
| sympy_sum                  | 169 ms                                                 | 170 ms: 1.01x slower                                                 |
| pickle_dict                | 35.5 us                                                | 36.0 us: 1.01x slower                                                |
| 2to3                       | 274 ms                                                 | 278 ms: 1.01x slower                                                 |
| sqlite_synth               | 2.83 us                                                | 2.88 us: 1.02x slower                                                |
| gc_traversal               | 3.79 ms                                                | 3.85 ms: 1.02x slower                                                |
| regex_effbot               | 3.61 ms                                                | 3.68 ms: 1.02x slower                                                |
| dulwich_log                | 68.5 ms                                                | 69.9 ms: 1.02x slower                                                |
| xml_etree_iterparse        | 107 ms                                                 | 109 ms: 1.02x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 10.6 ms: 1.02x slower                                                |
| scimark_sor                | 129 ms                                                 | 132 ms: 1.03x slower                                                 |
| unpickle_pure_python       | 230 us                                                 | 236 us: 1.03x slower                                                 |
| bench_thread_pool          | 842 us                                                 | 863 us: 1.03x slower                                                 |
| sqlglot_normalize          | 110 ms                                                 | 114 ms: 1.03x slower                                                 |
| asyncio_websockets         | 551 ms                                                 | 568 ms: 1.03x slower                                                 |
| sympy_integrate            | 21.4 ms                                                | 22.1 ms: 1.03x slower                                                |
| pickle                     | 11.6 us                                                | 12.0 us: 1.04x slower                                                |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.86 sec: 1.04x slower                                               |
| regex_dna                  | 212 ms                                                 | 221 ms: 1.04x slower                                                 |
| asyncio_tcp                | 491 ms                                                 | 512 ms: 1.04x slower                                                 |
| django_template            | 34.6 ms                                                | 36.2 ms: 1.05x slower                                                |
| sympy_expand               | 478 ms                                                 | 501 ms: 1.05x slower                                                 |
| pickle_list                | 5.08 us                                                | 5.33 us: 1.05x slower                                                |
| gunicorn                   | 1.24 ms                                                | 1.31 ms: 1.05x slower                                                |
| aiohttp                    | 1.15 ms                                                | 1.21 ms: 1.05x slower                                                |
| sqlglot_optimize           | 54.8 ms                                                | 57.8 ms: 1.05x slower                                                |
| docutils                   | 2.77 sec                                               | 2.92 sec: 1.06x slower                                               |
| go                         | 139 ms                                                 | 148 ms: 1.06x slower                                                 |
| regex_v8                   | 23.1 ms                                                | 25.0 ms: 1.08x slower                                                |
| hexiom                     | 6.41 ms                                                | 7.09 ms: 1.11x slower                                                |
| python_startup_no_site     | 6.94 ms                                                | 7.69 ms: 1.11x slower                                                |
| nqueens                    | 83.3 ms                                                | 93.0 ms: 1.12x slower                                                |
| pidigits                   | 187 ms                                                 | 210 ms: 1.12x slower                                                 |
| scimark_lu                 | 118 ms                                                 | 134 ms: 1.14x slower                                                 |
| python_startup             | 9.55 ms                                                | 11.1 ms: 1.17x slower                                                |
| create_gc_cycles           | 1.48 ms                                                | 1.77 ms: 1.20x slower                                                |
| telco                      | 7.10 ms                                                | 8.56 ms: 1.21x slower                                                |
| coverage                   | 72.7 ms                                                | 98.2 ms: 1.35x slower                                                |
| Geometric mean             | (ref)                                                  | 1.02x faster                                                         |

Benchmark hidden because not significant (9): mypy2, deltablue, unpickle_list, coroutines, sympy_str, bench_mp_pool, meteor_contest, xml_etree_parse, dask
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240418-3.13.0a6+-f4c10d5-JIT/bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6+-f4c10d5.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 78.65% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.07x