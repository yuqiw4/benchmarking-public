# Results vs. 3.12.0

- fork: nineteendo
- ref: use_PyTuple_Pack
- machine: linux-x86_64
- commit hash: 59ac30f
- commit date: 2024-04-29
- overall geometric mean: 1.05x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 0.96x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6+-59ac30f |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 267 ms: 1.03x faster                                                   |
| chameleon      | 7.41 ms                                                | 6.98 ms: 1.06x faster                                                  |
| docutils       | 2.77 sec                                               | 2.79 sec: 1.01x slower                                                 |
| tornado_http   | 103 ms                                                 | 93.9 ms: 1.09x faster                                                  |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6+-59ac30f |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 332 ms: 1.35x faster                                                   |
| async_tree_none            | 472 ms                                                 | 349 ms: 1.35x faster                                                   |
| async_tree_memoization_tg  | 575 ms                                                 | 436 ms: 1.32x faster                                                   |
| async_tree_io              | 1.16 sec                                               | 898 ms: 1.29x faster                                                   |
| async_tree_io_tg           | 1.18 sec                                               | 933 ms: 1.27x faster                                                   |
| async_tree_memoization     | 578 ms                                                 | 462 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 603 ms: 1.20x faster                                                   |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 609 ms: 1.19x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.28x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6+-59ac30f |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 97.0 ms                                                | 88.1 ms: 1.10x faster                                                  |
| float          | 84.7 ms                                                | 77.7 ms: 1.09x faster                                                  |
| pidigits       | 187 ms                                                 | 212 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6+-59ac30f |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 134 ms: 1.10x faster                                                   |
| regex_effbot   | 3.61 ms                                                | 3.65 ms: 1.01x slower                                                  |
| regex_dna      | 212 ms                                                 | 218 ms: 1.03x slower                                                   |
| regex_v8       | 23.1 ms                                                | 24.4 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                  | 1.00x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6+-59ac30f |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                               | 2.15 sec: 1.08x faster                                                 |
| pickle_pure_python   | 324 us                                                 | 300 us: 1.08x faster                                                   |
| unpickle_pure_python | 230 us                                                 | 215 us: 1.07x faster                                                   |
| json_loads           | 28.5 us                                                | 27.4 us: 1.04x faster                                                  |
| xml_etree_process    | 61.7 ms                                                | 59.8 ms: 1.03x faster                                                  |
| pickle_dict          | 35.5 us                                                | 34.6 us: 1.03x faster                                                  |
| xml_etree_generate   | 89.2 ms                                                | 87.2 ms: 1.02x faster                                                  |
| pickle_list          | 5.08 us                                                | 5.02 us: 1.01x faster                                                  |
| pickle               | 11.6 us                                                | 11.7 us: 1.01x slower                                                  |
| json_dumps           | 10.4 ms                                                | 10.5 ms: 1.01x slower                                                  |
| unpickle_list        | 5.29 us                                                | 5.38 us: 1.02x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (3): unpickle, xml_etree_iterparse, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6+-59ac30f |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.09 ms: 1.02x slower                                                  |
| python_startup         | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.06x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6+-59ac30f |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako           | 11.9 ms                                                | 10.7 ms: 1.11x faster                                                  |
| Geometric mean | (ref)                                                  | 1.06x faster                                                           |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6+-59ac30f |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 332 ms: 1.35x faster                                                   |
| async_tree_none            | 472 ms                                                 | 349 ms: 1.35x faster                                                   |
| async_tree_memoization_tg  | 575 ms                                                 | 436 ms: 1.32x faster                                                   |
| comprehensions             | 21.8 us                                                | 16.7 us: 1.30x faster                                                  |
| async_tree_io              | 1.16 sec                                               | 898 ms: 1.29x faster                                                   |
| async_tree_io_tg           | 1.18 sec                                               | 933 ms: 1.27x faster                                                   |
| async_tree_memoization     | 578 ms                                                 | 462 ms: 1.25x faster                                                   |
| raytrace                   | 312 ms                                                 | 259 ms: 1.21x faster                                                   |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 603 ms: 1.20x faster                                                   |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 609 ms: 1.19x faster                                                   |
| deltablue                  | 3.72 ms                                                | 3.19 ms: 1.17x faster                                                  |
| mypy2                      | 830 ms                                                 | 733 ms: 1.13x faster                                                   |
| logging_format             | 7.23 us                                                | 6.46 us: 1.12x faster                                                  |
| chaos                      | 67.0 ms                                                | 60.1 ms: 1.11x faster                                                  |
| mako                       | 11.9 ms                                                | 10.7 ms: 1.11x faster                                                  |
| logging_simple             | 6.46 us                                                | 5.84 us: 1.11x faster                                                  |
| pathlib                    | 19.3 ms                                                | 17.5 ms: 1.11x faster                                                  |
| regex_compile              | 148 ms                                                 | 134 ms: 1.10x faster                                                   |
| nbody                      | 97.0 ms                                                | 88.1 ms: 1.10x faster                                                  |
| sympy_sum                  | 169 ms                                                 | 154 ms: 1.10x faster                                                   |
| deepcopy_memo              | 40.7 us                                                | 37.2 us: 1.10x faster                                                  |
| tornado_http               | 103 ms                                                 | 93.9 ms: 1.09x faster                                                  |
| float                      | 84.7 ms                                                | 77.7 ms: 1.09x faster                                                  |
| crypto_pyaes               | 81.9 ms                                                | 75.4 ms: 1.09x faster                                                  |
| scimark_monte_carlo        | 75.1 ms                                                | 69.4 ms: 1.08x faster                                                  |
| tomli_loads                | 2.33 sec                                               | 2.15 sec: 1.08x faster                                                 |
| sympy_str                  | 300 ms                                                 | 277 ms: 1.08x faster                                                   |
| pickle_pure_python         | 324 us                                                 | 300 us: 1.08x faster                                                   |
| logging_silent             | 104 ns                                                 | 97.2 ns: 1.07x faster                                                  |
| sqlglot_parse              | 1.36 ms                                                | 1.27 ms: 1.07x faster                                                  |
| unpickle_pure_python       | 230 us                                                 | 215 us: 1.07x faster                                                   |
| sqlglot_transpile          | 1.68 ms                                                | 1.57 ms: 1.07x faster                                                  |
| fannkuch                   | 417 ms                                                 | 390 ms: 1.07x faster                                                   |
| chameleon                  | 7.41 ms                                                | 6.98 ms: 1.06x faster                                                  |
| sympy_integrate            | 21.4 ms                                                | 20.2 ms: 1.06x faster                                                  |
| spectral_norm              | 115 ms                                                 | 108 ms: 1.06x faster                                                   |
| pprint_safe_repr           | 776 ms                                                 | 735 ms: 1.05x faster                                                   |
| deepcopy_reduce            | 3.35 us                                                | 3.17 us: 1.05x faster                                                  |
| deepcopy                   | 371 us                                                 | 353 us: 1.05x faster                                                   |
| generators                 | 31.2 ms                                                | 29.7 ms: 1.05x faster                                                  |
| pprint_pformat             | 1.57 sec                                               | 1.50 sec: 1.05x faster                                                 |
| scimark_fft                | 382 ms                                                 | 365 ms: 1.05x faster                                                   |
| async_generators           | 463 ms                                                 | 444 ms: 1.04x faster                                                   |
| hexiom                     | 6.41 ms                                                | 6.15 ms: 1.04x faster                                                  |
| scimark_sor                | 129 ms                                                 | 124 ms: 1.04x faster                                                   |
| json_loads                 | 28.5 us                                                | 27.4 us: 1.04x faster                                                  |
| pycparser                  | 1.18 sec                                               | 1.14 sec: 1.04x faster                                                 |
| coroutines                 | 23.2 ms                                                | 22.4 ms: 1.04x faster                                                  |
| pyflate                    | 482 ms                                                 | 466 ms: 1.03x faster                                                   |
| dulwich_log                | 68.5 ms                                                | 66.3 ms: 1.03x faster                                                  |
| xml_etree_process          | 61.7 ms                                                | 59.8 ms: 1.03x faster                                                  |
| nqueens                    | 83.3 ms                                                | 80.7 ms: 1.03x faster                                                  |
| pickle_dict                | 35.5 us                                                | 34.6 us: 1.03x faster                                                  |
| meteor_contest             | 112 ms                                                 | 110 ms: 1.03x faster                                                   |
| 2to3                       | 274 ms                                                 | 267 ms: 1.03x faster                                                   |
| sympy_expand               | 478 ms                                                 | 467 ms: 1.02x faster                                                   |
| xml_etree_generate         | 89.2 ms                                                | 87.2 ms: 1.02x faster                                                  |
| mdp                        | 2.63 sec                                               | 2.57 sec: 1.02x faster                                                 |
| scimark_lu                 | 118 ms                                                 | 116 ms: 1.02x faster                                                   |
| json                       | 5.26 ms                                                | 5.18 ms: 1.01x faster                                                  |
| sqlglot_normalize          | 110 ms                                                 | 109 ms: 1.01x faster                                                   |
| pickle_list                | 5.08 us                                                | 5.02 us: 1.01x faster                                                  |
| bench_thread_pool          | 842 us                                                 | 831 us: 1.01x faster                                                   |
| dask                       | 372 ms                                                 | 367 ms: 1.01x faster                                                   |
| sqlglot_optimize           | 54.8 ms                                                | 54.4 ms: 1.01x faster                                                  |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.01x faster                                                  |
| pickle                     | 11.6 us                                                | 11.7 us: 1.01x slower                                                  |
| go                         | 139 ms                                                 | 141 ms: 1.01x slower                                                   |
| docutils                   | 2.77 sec                                               | 2.79 sec: 1.01x slower                                                 |
| regex_effbot               | 3.61 ms                                                | 3.65 ms: 1.01x slower                                                  |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 5.12 ms: 1.01x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 10.5 ms: 1.01x slower                                                  |
| richards                   | 45.8 ms                                                | 46.6 ms: 1.02x slower                                                  |
| aiohttp                    | 1.15 ms                                                | 1.17 ms: 1.02x slower                                                  |
| unpickle_list              | 5.29 us                                                | 5.38 us: 1.02x slower                                                  |
| asyncio_websockets         | 551 ms                                                 | 563 ms: 1.02x slower                                                   |
| python_startup_no_site     | 6.94 ms                                                | 7.09 ms: 1.02x slower                                                  |
| gunicorn                   | 1.24 ms                                                | 1.27 ms: 1.02x slower                                                  |
| regex_dna                  | 212 ms                                                 | 218 ms: 1.03x slower                                                   |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.84 sec: 1.03x slower                                                 |
| asyncio_tcp                | 491 ms                                                 | 506 ms: 1.03x slower                                                   |
| richards_super             | 51.5 ms                                                | 53.1 ms: 1.03x slower                                                  |
| sqlite_synth               | 2.83 us                                                | 2.93 us: 1.03x slower                                                  |
| typing_runtime_protocols   | 158 us                                                 | 165 us: 1.04x slower                                                   |
| regex_v8                   | 23.1 ms                                                | 24.4 ms: 1.06x slower                                                  |
| gc_traversal               | 3.79 ms                                                | 4.02 ms: 1.06x slower                                                  |
| python_startup             | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                  |
| pidigits                   | 187 ms                                                 | 212 ms: 1.13x slower                                                   |
| telco                      | 7.10 ms                                                | 8.45 ms: 1.19x slower                                                  |
| create_gc_cycles           | 1.48 ms                                                | 1.76 ms: 1.19x slower                                                  |
| coverage                   | 72.7 ms                                                | 91.6 ms: 1.26x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.05x faster                                                           |

Benchmark hidden because not significant (4): unpickle, django_template, xml_etree_iterparse, xml_etree_parse
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240429-3.13.0a6+-59ac30f/bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6+-59ac30f.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 0.96x