# Results vs. 3.12.0

- fork: nohlson
- ref: enable_fcf_protectio
- machine: linux-x86_64
- commit hash: 34aead4
- commit date: 2024-06-25
- overall geometric mean: 1.06x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240625-linux-x86_64-nohlson-enable_fcf_protectio-3.14.0a0-34aead4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 265 ms: 1.04x faster                                                   |
| docutils       | 2.77 sec                                               | 2.71 sec: 1.02x faster                                                 |
| tornado_http   | 103 ms                                                 | 90.9 ms: 1.13x faster                                                  |
| Geometric mean | (ref)                                                  | 1.06x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240625-linux-x86_64-nohlson-enable_fcf_protectio-3.14.0a0-34aead4 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 324 ms: 1.39x faster                                                   |
| async_tree_none            | 472 ms                                                 | 363 ms: 1.30x faster                                                   |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 570 ms: 1.27x faster                                                   |
| async_tree_memoization_tg  | 575 ms                                                 | 452 ms: 1.27x faster                                                   |
| async_tree_io              | 1.16 sec                                               | 920 ms: 1.26x faster                                                   |
| async_tree_io_tg           | 1.18 sec                                               | 984 ms: 1.20x faster                                                   |
| async_tree_memoization     | 578 ms                                                 | 481 ms: 1.20x faster                                                   |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 610 ms: 1.19x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.26x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240625-linux-x86_64-nohlson-enable_fcf_protectio-3.14.0a0-34aead4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 97.0 ms                                                | 88.2 ms: 1.10x faster                                                  |
| float          | 84.7 ms                                                | 77.1 ms: 1.10x faster                                                  |
| Geometric mean | (ref)                                                  | 1.06x faster                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240625-linux-x86_64-nohlson-enable_fcf_protectio-3.14.0a0-34aead4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 132 ms: 1.12x faster                                                   |
| regex_effbot   | 3.61 ms                                                | 3.76 ms: 1.04x slower                                                  |
| regex_dna      | 212 ms                                                 | 232 ms: 1.09x slower                                                   |
| regex_v8       | 23.1 ms                                                | 26.9 ms: 1.16x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240625-linux-x86_64-nohlson-enable_fcf_protectio-3.14.0a0-34aead4 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                               | 2.13 sec: 1.10x faster                                                 |
| pickle_pure_python   | 324 us                                                 | 304 us: 1.07x faster                                                   |
| unpickle_pure_python | 230 us                                                 | 216 us: 1.06x faster                                                   |
| xml_etree_generate   | 89.2 ms                                                | 84.2 ms: 1.06x faster                                                  |
| xml_etree_process    | 61.7 ms                                                | 59.0 ms: 1.05x faster                                                  |
| unpickle             | 15.9 us                                                | 15.3 us: 1.04x faster                                                  |
| xml_etree_parse      | 159 ms                                                 | 157 ms: 1.02x faster                                                   |
| xml_etree_iterparse  | 107 ms                                                 | 106 ms: 1.01x faster                                                   |
| pickle               | 11.6 us                                                | 11.5 us: 1.01x faster                                                  |
| pickle_dict          | 35.5 us                                                | 35.3 us: 1.01x faster                                                  |
| pickle_list          | 5.08 us                                                | 5.12 us: 1.01x slower                                                  |
| json_dumps           | 10.4 ms                                                | 10.6 ms: 1.03x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (2): json_loads, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240625-linux-x86_64-nohlson-enable_fcf_protectio-3.14.0a0-34aead4 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 6.94 ms: 1.00x slower                                                  |
| python_startup         | 9.55 ms                                                | 10.4 ms: 1.09x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.05x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240625-linux-x86_64-nohlson-enable_fcf_protectio-3.14.0a0-34aead4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako           | 11.9 ms                                                | 11.2 ms: 1.06x faster                                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240625-linux-x86_64-nohlson-enable_fcf_protectio-3.14.0a0-34aead4 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| deepcopy                   | 371 us                                                 | 262 us: 1.42x faster                                                   |
| async_tree_none_tg         | 450 ms                                                 | 324 ms: 1.39x faster                                                   |
| deepcopy_memo              | 40.7 us                                                | 29.5 us: 1.38x faster                                                  |
| comprehensions             | 21.8 us                                                | 16.5 us: 1.32x faster                                                  |
| async_tree_none            | 472 ms                                                 | 363 ms: 1.30x faster                                                   |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 570 ms: 1.27x faster                                                   |
| async_tree_memoization_tg  | 575 ms                                                 | 452 ms: 1.27x faster                                                   |
| async_tree_io              | 1.16 sec                                               | 920 ms: 1.26x faster                                                   |
| deepcopy_reduce            | 3.35 us                                                | 2.71 us: 1.23x faster                                                  |
| pathlib                    | 19.3 ms                                                | 15.9 ms: 1.22x faster                                                  |
| async_tree_io_tg           | 1.18 sec                                               | 984 ms: 1.20x faster                                                   |
| async_tree_memoization     | 578 ms                                                 | 481 ms: 1.20x faster                                                   |
| logging_format             | 7.23 us                                                | 6.07 us: 1.19x faster                                                  |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 610 ms: 1.19x faster                                                   |
| raytrace                   | 312 ms                                                 | 265 ms: 1.18x faster                                                   |
| logging_simple             | 6.46 us                                                | 5.48 us: 1.18x faster                                                  |
| deltablue                  | 3.72 ms                                                | 3.20 ms: 1.16x faster                                                  |
| tornado_http               | 103 ms                                                 | 90.9 ms: 1.13x faster                                                  |
| regex_compile              | 148 ms                                                 | 132 ms: 1.12x faster                                                   |
| chaos                      | 67.0 ms                                                | 59.6 ms: 1.12x faster                                                  |
| sympy_sum                  | 169 ms                                                 | 152 ms: 1.11x faster                                                   |
| crypto_pyaes               | 81.9 ms                                                | 74.4 ms: 1.10x faster                                                  |
| nbody                      | 97.0 ms                                                | 88.2 ms: 1.10x faster                                                  |
| float                      | 84.7 ms                                                | 77.1 ms: 1.10x faster                                                  |
| tomli_loads                | 2.33 sec                                               | 2.13 sec: 1.10x faster                                                 |
| scimark_monte_carlo        | 75.1 ms                                                | 68.9 ms: 1.09x faster                                                  |
| sympy_str                  | 300 ms                                                 | 276 ms: 1.08x faster                                                   |
| generators                 | 31.2 ms                                                | 29.0 ms: 1.08x faster                                                  |
| async_generators           | 463 ms                                                 | 430 ms: 1.08x faster                                                   |
| sympy_integrate            | 21.4 ms                                                | 19.9 ms: 1.07x faster                                                  |
| pickle_pure_python         | 324 us                                                 | 304 us: 1.07x faster                                                   |
| bench_thread_pool          | 842 us                                                 | 791 us: 1.06x faster                                                   |
| unpickle_pure_python       | 230 us                                                 | 216 us: 1.06x faster                                                   |
| dulwich_log                | 68.5 ms                                                | 64.4 ms: 1.06x faster                                                  |
| mako                       | 11.9 ms                                                | 11.2 ms: 1.06x faster                                                  |
| fannkuch                   | 417 ms                                                 | 393 ms: 1.06x faster                                                   |
| xml_etree_generate         | 89.2 ms                                                | 84.2 ms: 1.06x faster                                                  |
| sqlglot_transpile          | 1.68 ms                                                | 1.59 ms: 1.06x faster                                                  |
| nqueens                    | 83.3 ms                                                | 78.8 ms: 1.06x faster                                                  |
| pprint_safe_repr           | 776 ms                                                 | 735 ms: 1.06x faster                                                   |
| sqlglot_parse              | 1.36 ms                                                | 1.29 ms: 1.05x faster                                                  |
| scimark_lu                 | 118 ms                                                 | 113 ms: 1.05x faster                                                   |
| xml_etree_process          | 61.7 ms                                                | 59.0 ms: 1.05x faster                                                  |
| meteor_contest             | 112 ms                                                 | 108 ms: 1.04x faster                                                   |
| pprint_pformat             | 1.57 sec                                               | 1.50 sec: 1.04x faster                                                 |
| dask                       | 372 ms                                                 | 357 ms: 1.04x faster                                                   |
| hexiom                     | 6.41 ms                                                | 6.17 ms: 1.04x faster                                                  |
| unpickle                   | 15.9 us                                                | 15.3 us: 1.04x faster                                                  |
| scimark_fft                | 382 ms                                                 | 369 ms: 1.04x faster                                                   |
| coroutines                 | 23.2 ms                                                | 22.4 ms: 1.04x faster                                                  |
| 2to3                       | 274 ms                                                 | 265 ms: 1.04x faster                                                   |
| logging_silent             | 104 ns                                                 | 101 ns: 1.03x faster                                                   |
| mdp                        | 2.63 sec                                               | 2.55 sec: 1.03x faster                                                 |
| asyncio_tcp                | 491 ms                                                 | 477 ms: 1.03x faster                                                   |
| sympy_expand               | 478 ms                                                 | 467 ms: 1.02x faster                                                   |
| spectral_norm              | 115 ms                                                 | 112 ms: 1.02x faster                                                   |
| docutils                   | 2.77 sec                                               | 2.71 sec: 1.02x faster                                                 |
| sqlglot_normalize          | 110 ms                                                 | 108 ms: 1.02x faster                                                   |
| xml_etree_parse            | 159 ms                                                 | 157 ms: 1.02x faster                                                   |
| sqlglot_optimize           | 54.8 ms                                                | 54.1 ms: 1.01x faster                                                  |
| gc_traversal               | 3.79 ms                                                | 3.76 ms: 1.01x faster                                                  |
| xml_etree_iterparse        | 107 ms                                                 | 106 ms: 1.01x faster                                                   |
| pickle                     | 11.6 us                                                | 11.5 us: 1.01x faster                                                  |
| pickle_dict                | 35.5 us                                                | 35.3 us: 1.01x faster                                                  |
| pyflate                    | 482 ms                                                 | 480 ms: 1.01x faster                                                   |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.78 sec: 1.00x faster                                                 |
| python_startup_no_site     | 6.94 ms                                                | 6.94 ms: 1.00x slower                                                  |
| pickle_list                | 5.08 us                                                | 5.12 us: 1.01x slower                                                  |
| asyncio_websockets         | 551 ms                                                 | 556 ms: 1.01x slower                                                   |
| json                       | 5.26 ms                                                | 5.34 ms: 1.01x slower                                                  |
| scimark_sor                | 129 ms                                                 | 132 ms: 1.02x slower                                                   |
| sqlite_synth               | 2.83 us                                                | 2.89 us: 1.02x slower                                                  |
| go                         | 139 ms                                                 | 143 ms: 1.02x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 10.6 ms: 1.03x slower                                                  |
| richards                   | 45.8 ms                                                | 47.6 ms: 1.04x slower                                                  |
| richards_super             | 51.5 ms                                                | 53.6 ms: 1.04x slower                                                  |
| regex_effbot               | 3.61 ms                                                | 3.76 ms: 1.04x slower                                                  |
| typing_runtime_protocols   | 158 us                                                 | 165 us: 1.04x slower                                                   |
| python_startup             | 9.55 ms                                                | 10.4 ms: 1.09x slower                                                  |
| regex_dna                  | 212 ms                                                 | 232 ms: 1.09x slower                                                   |
| telco                      | 7.10 ms                                                | 8.24 ms: 1.16x slower                                                  |
| regex_v8                   | 23.1 ms                                                | 26.9 ms: 1.16x slower                                                  |
| create_gc_cycles           | 1.48 ms                                                | 1.73 ms: 1.17x slower                                                  |
| coverage                   | 72.7 ms                                                | 92.5 ms: 1.27x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                           |

Benchmark hidden because not significant (7): scimark_sparse_mat_mult, json_loads, bench_mp_pool, pidigits, django_template, pycparser, unpickle_list
Ignored benchmarks (7) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: aiohttp, chameleon, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240625-3.14.0a0-34aead4/bm-20240625-linux-x86_64-nohlson-enable_fcf_protectio-3.14.0a0-34aead4.json: bpe_tokeniser, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 0.98x