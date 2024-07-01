# Results vs. 3.12.0

- fork: Fidget-Spinner
- ref: optimizer_off
- machine: linux-x86_64
- commit hash: 118726c
- commit date: 2024-06-29
- overall geometric mean: 1.07x faster
- HPT reliability: 99.98%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.06x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240629-linux-x86_64-Fidget%2dSpinner-optimizer_off-3.14.0a0-118726c |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 272 ms: 1.01x faster                                                     |
| docutils       | 2.77 sec                                               | 2.86 sec: 1.03x slower                                                   |
| tornado_http   | 103 ms                                                 | 92.8 ms: 1.11x faster                                                    |
| Geometric mean | (ref)                                                  | 1.03x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240629-linux-x86_64-Fidget%2dSpinner-optimizer_off-3.14.0a0-118726c |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 575 ms                                                 | 376 ms: 1.53x faster                                                     |
| async_tree_none_tg         | 450 ms                                                 | 297 ms: 1.51x faster                                                     |
| async_tree_none            | 472 ms                                                 | 326 ms: 1.45x faster                                                     |
| async_tree_memoization     | 578 ms                                                 | 409 ms: 1.41x faster                                                     |
| async_tree_io_tg           | 1.18 sec                                               | 841 ms: 1.41x faster                                                     |
| async_tree_io              | 1.16 sec                                               | 845 ms: 1.37x faster                                                     |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 539 ms: 1.35x faster                                                     |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 566 ms: 1.28x faster                                                     |
| Geometric mean             | (ref)                                                  | 1.41x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240629-linux-x86_64-Fidget%2dSpinner-optimizer_off-3.14.0a0-118726c |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 84.7 ms                                                | 71.2 ms: 1.19x faster                                                    |
| nbody          | 97.0 ms                                                | 84.2 ms: 1.15x faster                                                    |
| pidigits       | 187 ms                                                 | 186 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                  | 1.11x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240629-linux-x86_64-Fidget%2dSpinner-optimizer_off-3.14.0a0-118726c |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 137 ms: 1.08x faster                                                     |
| regex_effbot   | 3.61 ms                                                | 3.73 ms: 1.03x slower                                                    |
| regex_v8       | 23.1 ms                                                | 24.4 ms: 1.06x slower                                                    |
| regex_dna      | 212 ms                                                 | 232 ms: 1.10x slower                                                     |
| Geometric mean | (ref)                                                  | 1.03x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240629-linux-x86_64-Fidget%2dSpinner-optimizer_off-3.14.0a0-118726c |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                               | 1.94 sec: 1.20x faster                                                   |
| xml_etree_parse      | 159 ms                                                 | 146 ms: 1.09x faster                                                     |
| xml_etree_generate   | 89.2 ms                                                | 81.8 ms: 1.09x faster                                                    |
| xml_etree_iterparse  | 107 ms                                                 | 98.1 ms: 1.09x faster                                                    |
| xml_etree_process    | 61.7 ms                                                | 57.5 ms: 1.07x faster                                                    |
| pickle_pure_python   | 324 us                                                 | 303 us: 1.07x faster                                                     |
| unpickle_pure_python | 230 us                                                 | 220 us: 1.04x faster                                                     |
| json_loads           | 28.5 us                                                | 27.4 us: 1.04x faster                                                    |
| json_dumps           | 10.4 ms                                                | 10.5 ms: 1.01x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.08x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240629-linux-x86_64-Fidget%2dSpinner-optimizer_off-3.14.0a0-118726c |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.45 ms: 1.07x slower                                                    |
| python_startup         | 9.55 ms                                                | 10.9 ms: 1.14x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.11x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240629-linux-x86_64-Fidget%2dSpinner-optimizer_off-3.14.0a0-118726c |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 10.1 ms: 1.17x faster                                                    |
| django_template | 34.6 ms                                                | 35.9 ms: 1.04x slower                                                    |
| Geometric mean  | (ref)                                                  | 1.06x faster                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240629-linux-x86_64-Fidget%2dSpinner-optimizer_off-3.14.0a0-118726c |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 575 ms                                                 | 376 ms: 1.53x faster                                                     |
| async_tree_none_tg         | 450 ms                                                 | 297 ms: 1.51x faster                                                     |
| async_tree_none            | 472 ms                                                 | 326 ms: 1.45x faster                                                     |
| deepcopy_memo              | 40.7 us                                                | 28.7 us: 1.42x faster                                                    |
| async_tree_memoization     | 578 ms                                                 | 409 ms: 1.41x faster                                                     |
| async_tree_io_tg           | 1.18 sec                                               | 841 ms: 1.41x faster                                                     |
| async_tree_io              | 1.16 sec                                               | 845 ms: 1.37x faster                                                     |
| deepcopy                   | 371 us                                                 | 273 us: 1.36x faster                                                     |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 539 ms: 1.35x faster                                                     |
| comprehensions             | 21.8 us                                                | 17.0 us: 1.28x faster                                                    |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 566 ms: 1.28x faster                                                     |
| deepcopy_reduce            | 3.35 us                                                | 2.76 us: 1.21x faster                                                    |
| tomli_loads                | 2.33 sec                                               | 1.94 sec: 1.20x faster                                                   |
| crypto_pyaes               | 81.9 ms                                                | 68.4 ms: 1.20x faster                                                    |
| scimark_monte_carlo        | 75.1 ms                                                | 63.0 ms: 1.19x faster                                                    |
| float                      | 84.7 ms                                                | 71.2 ms: 1.19x faster                                                    |
| pathlib                    | 19.3 ms                                                | 16.3 ms: 1.19x faster                                                    |
| logging_format             | 7.23 us                                                | 6.09 us: 1.19x faster                                                    |
| logging_simple             | 6.46 us                                                | 5.46 us: 1.18x faster                                                    |
| scimark_fft                | 382 ms                                                 | 326 ms: 1.17x faster                                                     |
| mako                       | 11.9 ms                                                | 10.1 ms: 1.17x faster                                                    |
| raytrace                   | 312 ms                                                 | 271 ms: 1.15x faster                                                     |
| nbody                      | 97.0 ms                                                | 84.2 ms: 1.15x faster                                                    |
| chaos                      | 67.0 ms                                                | 58.8 ms: 1.14x faster                                                    |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 4.49 ms: 1.13x faster                                                    |
| richards                   | 45.8 ms                                                | 41.1 ms: 1.11x faster                                                    |
| tornado_http               | 103 ms                                                 | 92.8 ms: 1.11x faster                                                    |
| fannkuch                   | 417 ms                                                 | 380 ms: 1.10x faster                                                     |
| xml_etree_parse            | 159 ms                                                 | 146 ms: 1.09x faster                                                     |
| xml_etree_generate         | 89.2 ms                                                | 81.8 ms: 1.09x faster                                                    |
| xml_etree_iterparse        | 107 ms                                                 | 98.1 ms: 1.09x faster                                                    |
| richards_super             | 51.5 ms                                                | 47.5 ms: 1.08x faster                                                    |
| pprint_safe_repr           | 776 ms                                                 | 716 ms: 1.08x faster                                                     |
| regex_compile              | 148 ms                                                 | 137 ms: 1.08x faster                                                     |
| spectral_norm              | 115 ms                                                 | 107 ms: 1.08x faster                                                     |
| xml_etree_process          | 61.7 ms                                                | 57.5 ms: 1.07x faster                                                    |
| pickle_pure_python         | 324 us                                                 | 303 us: 1.07x faster                                                     |
| pprint_pformat             | 1.57 sec                                               | 1.47 sec: 1.07x faster                                                   |
| sqlglot_parse              | 1.36 ms                                                | 1.28 ms: 1.07x faster                                                    |
| pyflate                    | 482 ms                                                 | 455 ms: 1.06x faster                                                     |
| sqlglot_transpile          | 1.68 ms                                                | 1.59 ms: 1.06x faster                                                    |
| meteor_contest             | 112 ms                                                 | 107 ms: 1.05x faster                                                     |
| generators                 | 31.2 ms                                                | 29.7 ms: 1.05x faster                                                    |
| unpickle_pure_python       | 230 us                                                 | 220 us: 1.04x faster                                                     |
| json_loads                 | 28.5 us                                                | 27.4 us: 1.04x faster                                                    |
| pycparser                  | 1.18 sec                                               | 1.14 sec: 1.03x faster                                                   |
| dask                       | 372 ms                                                 | 362 ms: 1.03x faster                                                     |
| json                       | 5.26 ms                                                | 5.12 ms: 1.03x faster                                                    |
| deltablue                  | 3.72 ms                                                | 3.63 ms: 1.02x faster                                                    |
| dulwich_log                | 68.5 ms                                                | 67.2 ms: 1.02x faster                                                    |
| async_generators           | 463 ms                                                 | 455 ms: 1.02x faster                                                     |
| sympy_str                  | 300 ms                                                 | 295 ms: 1.02x faster                                                     |
| pidigits                   | 187 ms                                                 | 186 ms: 1.01x faster                                                     |
| gc_traversal               | 3.79 ms                                                | 3.76 ms: 1.01x faster                                                    |
| bench_thread_pool          | 842 us                                                 | 835 us: 1.01x faster                                                     |
| 2to3                       | 274 ms                                                 | 272 ms: 1.01x faster                                                     |
| coroutines                 | 23.2 ms                                                | 23.0 ms: 1.01x faster                                                    |
| sympy_sum                  | 169 ms                                                 | 168 ms: 1.00x faster                                                     |
| json_dumps                 | 10.4 ms                                                | 10.5 ms: 1.01x slower                                                    |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.80 sec: 1.01x slower                                                   |
| asyncio_websockets         | 551 ms                                                 | 559 ms: 1.01x slower                                                     |
| logging_silent             | 104 ns                                                 | 106 ns: 1.01x slower                                                     |
| asyncio_tcp                | 491 ms                                                 | 500 ms: 1.02x slower                                                     |
| sympy_integrate            | 21.4 ms                                                | 22.0 ms: 1.03x slower                                                    |
| sqlglot_optimize           | 54.8 ms                                                | 56.4 ms: 1.03x slower                                                    |
| docutils                   | 2.77 sec                                               | 2.86 sec: 1.03x slower                                                   |
| mdp                        | 2.63 sec                                               | 2.72 sec: 1.03x slower                                                   |
| regex_effbot               | 3.61 ms                                                | 3.73 ms: 1.03x slower                                                    |
| django_template            | 34.6 ms                                                | 35.9 ms: 1.04x slower                                                    |
| scimark_sor                | 129 ms                                                 | 134 ms: 1.04x slower                                                     |
| sqlglot_normalize          | 110 ms                                                 | 114 ms: 1.04x slower                                                     |
| go                         | 139 ms                                                 | 145 ms: 1.04x slower                                                     |
| sympy_expand               | 478 ms                                                 | 500 ms: 1.05x slower                                                     |
| scimark_lu                 | 118 ms                                                 | 124 ms: 1.05x slower                                                     |
| hexiom                     | 6.41 ms                                                | 6.75 ms: 1.05x slower                                                    |
| nqueens                    | 83.3 ms                                                | 87.8 ms: 1.05x slower                                                    |
| regex_v8                   | 23.1 ms                                                | 24.4 ms: 1.06x slower                                                    |
| python_startup_no_site     | 6.94 ms                                                | 7.45 ms: 1.07x slower                                                    |
| typing_runtime_protocols   | 158 us                                                 | 171 us: 1.09x slower                                                     |
| regex_dna                  | 212 ms                                                 | 232 ms: 1.10x slower                                                     |
| telco                      | 7.10 ms                                                | 8.07 ms: 1.14x slower                                                    |
| python_startup             | 9.55 ms                                                | 10.9 ms: 1.14x slower                                                    |
| create_gc_cycles           | 1.48 ms                                                | 1.75 ms: 1.19x slower                                                    |
| coverage                   | 72.7 ms                                                | 93.5 ms: 1.29x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                             |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (13) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: aiohttp, chameleon, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlite_synth, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20240629-3.14.0a0-118726c-JIT/bm-20240629-linux-x86_64-Fidget%2dSpinner-optimizer_off-3.14.0a0-118726c.json: bpe_tokeniser, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.98% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.06x