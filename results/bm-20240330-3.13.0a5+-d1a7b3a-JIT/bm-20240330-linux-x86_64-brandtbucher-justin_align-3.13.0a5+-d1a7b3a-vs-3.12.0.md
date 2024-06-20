# Results vs. 3.12.0

- fork: brandtbucher
- ref: justin_align
- machine: linux-x86_64
- commit hash: d1a7b3a
- commit date: 2024-03-30
- overall geometric mean: 1.01x faster
- HPT reliability: 54.07%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 280 ms: 1.02x slower                                                 |
| chameleon      | 7.41 ms                                                | 7.00 ms: 1.06x faster                                                |
| docutils       | 2.77 sec                                               | 2.90 sec: 1.05x slower                                               |
| tornado_http   | 103 ms                                                 | 97.3 ms: 1.06x faster                                                |
| Geometric mean | (ref)                                                  | 1.01x faster                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 344 ms: 1.31x faster                                                 |
| async_tree_memoization_tg  | 575 ms                                                 | 452 ms: 1.27x faster                                                 |
| async_tree_io_tg           | 1.18 sec                                               | 931 ms: 1.27x faster                                                 |
| async_tree_memoization     | 578 ms                                                 | 459 ms: 1.26x faster                                                 |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 582 ms: 1.25x faster                                                 |
| async_tree_io              | 1.16 sec                                               | 955 ms: 1.21x faster                                                 |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 603 ms: 1.20x faster                                                 |
| async_tree_none            | 472 ms                                                 | 392 ms: 1.20x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.25x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 84.7 ms                                                | 77.2 ms: 1.10x faster                                                |
| nbody          | 97.0 ms                                                | 92.4 ms: 1.05x faster                                                |
| pidigits       | 187 ms                                                 | 189 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                  | 1.04x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 146 ms: 1.01x faster                                                 |
| regex_effbot   | 3.61 ms                                                | 3.87 ms: 1.07x slower                                                |
| regex_dna      | 212 ms                                                 | 231 ms: 1.09x slower                                                 |
| regex_v8       | 23.1 ms                                                | 25.6 ms: 1.11x slower                                                |
| Geometric mean | (ref)                                                  | 1.06x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                               | 2.10 sec: 1.11x faster                                               |
| pickle_pure_python   | 324 us                                                 | 309 us: 1.05x faster                                                 |
| unpickle_list        | 5.29 us                                                | 5.06 us: 1.04x faster                                                |
| unpickle             | 15.9 us                                                | 15.6 us: 1.02x faster                                                |
| xml_etree_process    | 61.7 ms                                                | 61.1 ms: 1.01x faster                                                |
| pickle_dict          | 35.5 us                                                | 35.3 us: 1.01x faster                                                |
| json_loads           | 28.5 us                                                | 28.4 us: 1.00x faster                                                |
| xml_etree_iterparse  | 107 ms                                                 | 108 ms: 1.01x slower                                                 |
| json_dumps           | 10.4 ms                                                | 10.6 ms: 1.02x slower                                                |
| unpickle_pure_python | 230 us                                                 | 240 us: 1.04x slower                                                 |
| pickle_list          | 5.08 us                                                | 5.37 us: 1.06x slower                                                |
| pickle               | 11.6 us                                                | 12.5 us: 1.08x slower                                                |
| Geometric mean       | (ref)                                                  | 1.00x faster                                                         |

Benchmark hidden because not significant (2): xml_etree_parse, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 9.55 ms                                                | 11.1 ms: 1.16x slower                                                |
| python_startup_no_site | 6.94 ms                                                | 9.55 ms: 1.38x slower                                                |
| Geometric mean         | (ref)                                                  | 1.27x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 10.8 ms: 1.10x faster                                                |
| django_template | 34.6 ms                                                | 35.8 ms: 1.04x slower                                                |
| Geometric mean  | (ref)                                                  | 1.03x faster                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 115 us: 1.38x faster                                                 |
| async_tree_none_tg         | 450 ms                                                 | 344 ms: 1.31x faster                                                 |
| async_tree_memoization_tg  | 575 ms                                                 | 452 ms: 1.27x faster                                                 |
| async_tree_io_tg           | 1.18 sec                                               | 931 ms: 1.27x faster                                                 |
| async_tree_memoization     | 578 ms                                                 | 459 ms: 1.26x faster                                                 |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 582 ms: 1.25x faster                                                 |
| async_tree_io              | 1.16 sec                                               | 955 ms: 1.21x faster                                                 |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 603 ms: 1.20x faster                                                 |
| async_tree_none            | 472 ms                                                 | 392 ms: 1.20x faster                                                 |
| comprehensions             | 21.8 us                                                | 18.3 us: 1.19x faster                                                |
| scimark_fft                | 382 ms                                                 | 343 ms: 1.11x faster                                                 |
| tomli_loads                | 2.33 sec                                               | 2.10 sec: 1.11x faster                                               |
| logging_format             | 7.23 us                                                | 6.53 us: 1.11x faster                                                |
| crypto_pyaes               | 81.9 ms                                                | 74.4 ms: 1.10x faster                                                |
| float                      | 84.7 ms                                                | 77.2 ms: 1.10x faster                                                |
| mako                       | 11.9 ms                                                | 10.8 ms: 1.10x faster                                                |
| logging_simple             | 6.46 us                                                | 5.94 us: 1.09x faster                                                |
| chaos                      | 67.0 ms                                                | 63.0 ms: 1.06x faster                                                |
| raytrace                   | 312 ms                                                 | 294 ms: 1.06x faster                                                 |
| scimark_monte_carlo        | 75.1 ms                                                | 70.9 ms: 1.06x faster                                                |
| chameleon                  | 7.41 ms                                                | 7.00 ms: 1.06x faster                                                |
| tornado_http               | 103 ms                                                 | 97.3 ms: 1.06x faster                                                |
| deltablue                  | 3.72 ms                                                | 3.52 ms: 1.05x faster                                                |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 4.80 ms: 1.05x faster                                                |
| fannkuch                   | 417 ms                                                 | 397 ms: 1.05x faster                                                 |
| nbody                      | 97.0 ms                                                | 92.4 ms: 1.05x faster                                                |
| pickle_pure_python         | 324 us                                                 | 309 us: 1.05x faster                                                 |
| unpickle_list              | 5.29 us                                                | 5.06 us: 1.04x faster                                                |
| pprint_safe_repr           | 776 ms                                                 | 746 ms: 1.04x faster                                                 |
| deepcopy_reduce            | 3.35 us                                                | 3.22 us: 1.04x faster                                                |
| generators                 | 31.2 ms                                                | 30.1 ms: 1.04x faster                                                |
| sympy_sum                  | 169 ms                                                 | 164 ms: 1.03x faster                                                 |
| pprint_pformat             | 1.57 sec                                               | 1.52 sec: 1.03x faster                                               |
| sympy_str                  | 300 ms                                                 | 291 ms: 1.03x faster                                                 |
| deepcopy_memo              | 40.7 us                                                | 39.6 us: 1.03x faster                                                |
| coroutines                 | 23.2 ms                                                | 22.5 ms: 1.03x faster                                                |
| logging_silent             | 104 ns                                                 | 102 ns: 1.02x faster                                                 |
| deepcopy                   | 371 us                                                 | 365 us: 1.02x faster                                                 |
| unpickle                   | 15.9 us                                                | 15.6 us: 1.02x faster                                                |
| regex_compile              | 148 ms                                                 | 146 ms: 1.01x faster                                                 |
| sqlglot_transpile          | 1.68 ms                                                | 1.66 ms: 1.01x faster                                                |
| meteor_contest             | 112 ms                                                 | 111 ms: 1.01x faster                                                 |
| sqlglot_parse              | 1.36 ms                                                | 1.35 ms: 1.01x faster                                                |
| xml_etree_process          | 61.7 ms                                                | 61.1 ms: 1.01x faster                                                |
| pickle_dict                | 35.5 us                                                | 35.3 us: 1.01x faster                                                |
| json_loads                 | 28.5 us                                                | 28.4 us: 1.00x faster                                                |
| async_generators           | 463 ms                                                 | 465 ms: 1.01x slower                                                 |
| bench_mp_pool              | 24.0 ms                                                | 24.2 ms: 1.01x slower                                                |
| xml_etree_iterparse        | 107 ms                                                 | 108 ms: 1.01x slower                                                 |
| pidigits                   | 187 ms                                                 | 189 ms: 1.01x slower                                                 |
| json                       | 5.26 ms                                                | 5.32 ms: 1.01x slower                                                |
| dask                       | 372 ms                                                 | 377 ms: 1.01x slower                                                 |
| bench_thread_pool          | 842 us                                                 | 856 us: 1.02x slower                                                 |
| sqlglot_normalize          | 110 ms                                                 | 112 ms: 1.02x slower                                                 |
| sympy_integrate            | 21.4 ms                                                | 21.8 ms: 1.02x slower                                                |
| spectral_norm              | 115 ms                                                 | 117 ms: 1.02x slower                                                 |
| 2to3                       | 274 ms                                                 | 280 ms: 1.02x slower                                                 |
| pyflate                    | 482 ms                                                 | 493 ms: 1.02x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 10.6 ms: 1.02x slower                                                |
| sympy_expand               | 478 ms                                                 | 491 ms: 1.03x slower                                                 |
| scimark_sor                | 129 ms                                                 | 133 ms: 1.03x slower                                                 |
| sqlite_synth               | 2.83 us                                                | 2.92 us: 1.03x slower                                                |
| asyncio_websockets         | 551 ms                                                 | 570 ms: 1.03x slower                                                 |
| richards_super             | 51.5 ms                                                | 53.3 ms: 1.03x slower                                                |
| richards                   | 45.8 ms                                                | 47.5 ms: 1.04x slower                                                |
| django_template            | 34.6 ms                                                | 35.8 ms: 1.04x slower                                                |
| gc_traversal               | 3.79 ms                                                | 3.94 ms: 1.04x slower                                                |
| dulwich_log                | 68.5 ms                                                | 71.2 ms: 1.04x slower                                                |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.86 sec: 1.04x slower                                               |
| asyncio_tcp                | 491 ms                                                 | 510 ms: 1.04x slower                                                 |
| unpickle_pure_python       | 230 us                                                 | 240 us: 1.04x slower                                                 |
| docutils                   | 2.77 sec                                               | 2.90 sec: 1.05x slower                                               |
| pycparser                  | 1.18 sec                                               | 1.24 sec: 1.05x slower                                               |
| gunicorn                   | 1.24 ms                                                | 1.31 ms: 1.06x slower                                                |
| aiohttp                    | 1.15 ms                                                | 1.22 ms: 1.06x slower                                                |
| pickle_list                | 5.08 us                                                | 5.37 us: 1.06x slower                                                |
| sqlglot_optimize           | 54.8 ms                                                | 58.0 ms: 1.06x slower                                                |
| regex_effbot               | 3.61 ms                                                | 3.87 ms: 1.07x slower                                                |
| mdp                        | 2.63 sec                                               | 2.83 sec: 1.07x slower                                               |
| pickle                     | 11.6 us                                                | 12.5 us: 1.08x slower                                                |
| regex_dna                  | 212 ms                                                 | 231 ms: 1.09x slower                                                 |
| regex_v8                   | 23.1 ms                                                | 25.6 ms: 1.11x slower                                                |
| nqueens                    | 83.3 ms                                                | 92.7 ms: 1.11x slower                                                |
| go                         | 139 ms                                                 | 157 ms: 1.13x slower                                                 |
| scimark_lu                 | 118 ms                                                 | 133 ms: 1.13x slower                                                 |
| hexiom                     | 6.41 ms                                                | 7.24 ms: 1.13x slower                                                |
| create_gc_cycles           | 1.48 ms                                                | 1.69 ms: 1.15x slower                                                |
| python_startup             | 9.55 ms                                                | 11.1 ms: 1.16x slower                                                |
| telco                      | 7.10 ms                                                | 8.48 ms: 1.19x slower                                                |
| coverage                   | 72.7 ms                                                | 97.1 ms: 1.34x slower                                                |
| python_startup_no_site     | 6.94 ms                                                | 9.55 ms: 1.38x slower                                                |
| unpack_sequence            | 54.0 ns                                                | 87.6 ns: 1.62x slower                                                |
| Geometric mean             | (ref)                                                  | 1.01x faster                                                         |

Benchmark hidden because not significant (4): mypy2, pathlib, xml_etree_parse, xml_etree_generate
Ignored benchmarks (2) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (6) of results/bm-20240330-3.13.0a5+-d1a7b3a-JIT/bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 54.07% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.03x