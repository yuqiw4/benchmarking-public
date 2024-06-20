# Results vs. 3.10.4

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 1e4a4c4
- commit date: 2024-04-19
- overall geometric mean: 1.21x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240419-linux-x86_64-python-main-3.13.0a6+-1e4a4c4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 301 ms: 1.16x faster                                   |
| chameleon      | 9.68 ms                                                | 7.65 ms: 1.27x faster                                  |
| docutils       | 3.30 sec                                               | 3.08 sec: 1.07x faster                                 |
| html5lib       | 88.9 ms                                                | 72.5 ms: 1.23x faster                                  |
| tornado_http   | 136 ms                                                 | 103 ms: 1.33x faster                                   |
| Geometric mean | (ref)                                                  | 1.21x faster                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240419-linux-x86_64-python-main-3.13.0a6+-1e4a4c4 |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 374 ms: 1.95x faster                                   |
| async_tree_io           | 1.77 sec                                               | 984 ms: 1.80x faster                                   |
| async_tree_memoization  | 870 ms                                                 | 501 ms: 1.73x faster                                   |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 636 ms: 1.60x faster                                   |
| Geometric mean          | (ref)                                                  | 1.77x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240419-linux-x86_64-python-main-3.13.0a6+-1e4a4c4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 117 ms                                                 | 89.3 ms: 1.31x faster                                  |
| nbody          | 154 ms                                                 | 119 ms: 1.29x faster                                   |
| pidigits       | 191 ms                                                 | 208 ms: 1.09x slower                                   |
| Geometric mean | (ref)                                                  | 1.16x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240419-linux-x86_64-python-main-3.13.0a6+-1e4a4c4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 177 ms: 1.06x faster                                   |
| regex_v8       | 27.8 ms                                                | 26.2 ms: 1.06x faster                                  |
| regex_dna      | 227 ms                                                 | 234 ms: 1.03x slower                                   |
| regex_effbot   | 3.63 ms                                                | 3.88 ms: 1.07x slower                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240419-linux-x86_64-python-main-3.13.0a6+-1e4a4c4 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 311 us: 1.56x faster                                   |
| json_dumps           | 14.2 ms                                                | 10.7 ms: 1.32x faster                                  |
| tomli_loads          | 3.14 sec                                               | 2.51 sec: 1.25x faster                                 |
| xml_etree_process    | 79.1 ms                                                | 63.8 ms: 1.24x faster                                  |
| unpickle_pure_python | 331 us                                                 | 282 us: 1.17x faster                                   |
| json_loads           | 31.2 us                                                | 28.0 us: 1.12x faster                                  |
| xml_etree_parse      | 168 ms                                                 | 152 ms: 1.11x faster                                   |
| xml_etree_generate   | 99.4 ms                                                | 93.5 ms: 1.06x faster                                  |
| xml_etree_iterparse  | 115 ms                                                 | 110 ms: 1.05x faster                                   |
| unpickle_list        | 5.20 us                                                | 5.49 us: 1.06x slower                                  |
| unpickle             | 14.4 us                                                | 15.4 us: 1.07x slower                                  |
| pickle               | 10.7 us                                                | 11.8 us: 1.11x slower                                  |
| pickle_dict          | 29.6 us                                                | 34.6 us: 1.17x slower                                  |
| Geometric mean       | (ref)                                                  | 1.09x faster                                           |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240419-linux-x86_64-python-main-3.13.0a6+-1e4a4c4 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.5 ms: 1.38x faster                                  |
| python_startup_no_site | 5.93 ms                                                | 7.13 ms: 1.20x slower                                  |
| Geometric mean         | (ref)                                                  | 1.07x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240419-linux-x86_64-python-main-3.13.0a6+-1e4a4c4 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| genshi_text     | 31.8 ms                                                | 25.7 ms: 1.24x faster                                  |
| django_template | 48.2 ms                                                | 39.5 ms: 1.22x faster                                  |
| mako            | 16.3 ms                                                | 13.6 ms: 1.20x faster                                  |
| genshi_xml      | 66.0 ms                                                | 59.0 ms: 1.12x faster                                  |
| Geometric mean  | (ref)                                                  | 1.19x faster                                           |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240419-linux-x86_64-python-main-3.13.0a6+-1e4a4c4 |
|--------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 119 us: 4.56x faster                                   |
| generators               | 80.1 ms                                                | 30.0 ms: 2.67x faster                                  |
| deltablue                | 7.91 ms                                                | 4.06 ms: 1.95x faster                                  |
| async_tree_none          | 728 ms                                                 | 374 ms: 1.95x faster                                   |
| async_tree_io            | 1.77 sec                                               | 984 ms: 1.80x faster                                   |
| logging_silent           | 190 ns                                                 | 106 ns: 1.79x faster                                   |
| asyncio_tcp              | 922 ms                                                 | 522 ms: 1.77x faster                                   |
| async_tree_memoization   | 870 ms                                                 | 501 ms: 1.73x faster                                   |
| pylint                   | 551 ms                                                 | 342 ms: 1.61x faster                                   |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 636 ms: 1.60x faster                                   |
| raytrace                 | 507 ms                                                 | 323 ms: 1.57x faster                                   |
| pickle_pure_python       | 484 us                                                 | 311 us: 1.56x faster                                   |
| richards_super           | 94.7 ms                                                | 62.0 ms: 1.53x faster                                  |
| coroutines               | 35.1 ms                                                | 23.3 ms: 1.50x faster                                  |
| sqlglot_parse            | 2.17 ms                                                | 1.48 ms: 1.47x faster                                  |
| chaos                    | 115 ms                                                 | 78.7 ms: 1.47x faster                                  |
| scimark_sor              | 220 ms                                                 | 150 ms: 1.46x faster                                   |
| richards                 | 79.3 ms                                                | 55.0 ms: 1.44x faster                                  |
| sqlglot_transpile        | 2.57 ms                                                | 1.80 ms: 1.43x faster                                  |
| crypto_pyaes             | 128 ms                                                 | 91.7 ms: 1.39x faster                                  |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.86 sec: 1.39x faster                                 |
| python_startup           | 14.6 ms                                                | 10.5 ms: 1.38x faster                                  |
| tornado_http             | 136 ms                                                 | 103 ms: 1.33x faster                                   |
| json_dumps               | 14.2 ms                                                | 10.7 ms: 1.32x faster                                  |
| go                       | 240 ms                                                 | 182 ms: 1.32x faster                                   |
| logging_simple           | 8.30 us                                                | 6.32 us: 1.31x faster                                  |
| float                    | 117 ms                                                 | 89.3 ms: 1.31x faster                                  |
| deepcopy_memo            | 58.5 us                                                | 44.8 us: 1.31x faster                                  |
| logging_format           | 9.09 us                                                | 7.01 us: 1.30x faster                                  |
| scimark_monte_carlo      | 118 ms                                                 | 91.3 ms: 1.29x faster                                  |
| nbody                    | 154 ms                                                 | 119 ms: 1.29x faster                                   |
| comprehensions           | 28.8 us                                                | 22.4 us: 1.28x faster                                  |
| thrift                   | 1.07 ms                                                | 838 us: 1.28x faster                                   |
| deepcopy                 | 479 us                                                 | 378 us: 1.27x faster                                   |
| chameleon                | 9.68 ms                                                | 7.65 ms: 1.27x faster                                  |
| deepcopy_reduce          | 4.17 us                                                | 3.30 us: 1.26x faster                                  |
| tomli_loads              | 3.14 sec                                               | 2.51 sec: 1.25x faster                                 |
| xml_etree_process        | 79.1 ms                                                | 63.8 ms: 1.24x faster                                  |
| genshi_text              | 31.8 ms                                                | 25.7 ms: 1.24x faster                                  |
| html5lib                 | 88.9 ms                                                | 72.5 ms: 1.23x faster                                  |
| django_template          | 48.2 ms                                                | 39.5 ms: 1.22x faster                                  |
| pyflate                  | 716 ms                                                 | 589 ms: 1.22x faster                                   |
| pycparser                | 1.58 sec                                               | 1.31 sec: 1.20x faster                                 |
| mako                     | 16.3 ms                                                | 13.6 ms: 1.20x faster                                  |
| djangocms                | 38.4 us                                                | 32.7 us: 1.18x faster                                  |
| unpickle_pure_python     | 331 us                                                 | 282 us: 1.17x faster                                   |
| aiohttp                  | 1.44 ms                                                | 1.23 ms: 1.17x faster                                  |
| sqlglot_normalize        | 143 ms                                                 | 123 ms: 1.16x faster                                   |
| dask                     | 441 ms                                                 | 379 ms: 1.16x faster                                   |
| 2to3                     | 348 ms                                                 | 301 ms: 1.16x faster                                   |
| spectral_norm            | 170 ms                                                 | 147 ms: 1.16x faster                                   |
| gunicorn                 | 1.53 ms                                                | 1.32 ms: 1.16x faster                                  |
| dulwich_log              | 84.3 ms                                                | 73.8 ms: 1.14x faster                                  |
| pathlib                  | 20.5 ms                                                | 18.2 ms: 1.12x faster                                  |
| genshi_xml               | 66.0 ms                                                | 59.0 ms: 1.12x faster                                  |
| bench_thread_pool        | 986 us                                                 | 882 us: 1.12x faster                                   |
| json_loads               | 31.2 us                                                | 28.0 us: 1.12x faster                                  |
| mypy2                    | 894 ms                                                 | 803 ms: 1.11x faster                                   |
| sympy_integrate          | 25.8 ms                                                | 23.2 ms: 1.11x faster                                  |
| xml_etree_parse          | 168 ms                                                 | 152 ms: 1.11x faster                                   |
| hexiom                   | 10.4 ms                                                | 9.41 ms: 1.10x faster                                  |
| sympy_sum                | 196 ms                                                 | 178 ms: 1.10x faster                                   |
| json                     | 5.69 ms                                                | 5.19 ms: 1.10x faster                                  |
| sqlglot_optimize         | 69.2 ms                                                | 63.1 ms: 1.10x faster                                  |
| fannkuch                 | 532 ms                                                 | 489 ms: 1.09x faster                                   |
| pprint_safe_repr         | 1.02 sec                                               | 947 ms: 1.07x faster                                   |
| sympy_str                | 346 ms                                                 | 322 ms: 1.07x faster                                   |
| docutils                 | 3.30 sec                                               | 3.08 sec: 1.07x faster                                 |
| pprint_pformat           | 2.10 sec                                               | 1.97 sec: 1.07x faster                                 |
| xml_etree_generate       | 99.4 ms                                                | 93.5 ms: 1.06x faster                                  |
| regex_compile            | 188 ms                                                 | 177 ms: 1.06x faster                                   |
| regex_v8                 | 27.8 ms                                                | 26.2 ms: 1.06x faster                                  |
| sympy_expand             | 566 ms                                                 | 533 ms: 1.06x faster                                   |
| scimark_lu               | 176 ms                                                 | 167 ms: 1.05x faster                                   |
| xml_etree_iterparse      | 115 ms                                                 | 110 ms: 1.05x faster                                   |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 6.28 ms: 1.03x faster                                  |
| scimark_fft              | 466 ms                                                 | 461 ms: 1.01x faster                                   |
| meteor_contest           | 120 ms                                                 | 119 ms: 1.00x faster                                   |
| asyncio_websockets       | 559 ms                                                 | 564 ms: 1.01x slower                                   |
| mdp                      | 2.85 sec                                               | 2.91 sec: 1.02x slower                                 |
| regex_dna                | 227 ms                                                 | 234 ms: 1.03x slower                                   |
| nqueens                  | 106 ms                                                 | 110 ms: 1.04x slower                                   |
| unpickle_list            | 5.20 us                                                | 5.49 us: 1.06x slower                                  |
| regex_effbot             | 3.63 ms                                                | 3.88 ms: 1.07x slower                                  |
| unpickle                 | 14.4 us                                                | 15.4 us: 1.07x slower                                  |
| async_generators         | 444 ms                                                 | 476 ms: 1.07x slower                                   |
| gc_traversal             | 3.62 ms                                                | 3.94 ms: 1.09x slower                                  |
| pidigits                 | 191 ms                                                 | 208 ms: 1.09x slower                                   |
| create_gc_cycles         | 1.62 ms                                                | 1.77 ms: 1.10x slower                                  |
| pickle                   | 10.7 us                                                | 11.8 us: 1.11x slower                                  |
| pickle_dict              | 29.6 us                                                | 34.6 us: 1.17x slower                                  |
| python_startup_no_site   | 5.93 ms                                                | 7.13 ms: 1.20x slower                                  |
| coverage                 | 79.4 ms                                                | 99.4 ms: 1.25x slower                                  |
| telco                    | 7.27 ms                                                | 9.19 ms: 1.27x slower                                  |
| Geometric mean           | (ref)                                                  | 1.21x faster                                           |

Benchmark hidden because not significant (3): bench_mp_pool, pickle_list, sqlite_synth
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240419-3.13.0a6+-1e4a4c4-PYTHON_UOPS/bm-20240419-linux-x86_64-python-main-3.13.0a6+-1e4a4c4.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.13x
- 95% likely to have a speedup of 1.11x
- 99% likely to have a speedup of 1.10x

# Memory
- memory change: 1.11x