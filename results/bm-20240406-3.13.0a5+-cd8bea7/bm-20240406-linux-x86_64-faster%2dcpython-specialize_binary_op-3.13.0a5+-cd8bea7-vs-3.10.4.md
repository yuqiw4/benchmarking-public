# Results vs. 3.10.4

- fork: faster-cpython
- ref: specialize_binary_op
- machine: linux-x86_64
- commit hash: cd8bea7
- commit date: 2024-04-06
- overall geometric mean: 1.35x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240406-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-cd8bea7 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 268 ms: 1.30x faster                                                             |
| chameleon      | 9.68 ms                                                | 6.97 ms: 1.39x faster                                                            |
| docutils       | 3.30 sec                                               | 2.80 sec: 1.18x faster                                                           |
| html5lib       | 88.9 ms                                                | 68.2 ms: 1.30x faster                                                            |
| tornado_http   | 136 ms                                                 | 93.9 ms: 1.45x faster                                                            |
| Geometric mean | (ref)                                                  | 1.32x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240406-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-cd8bea7 |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 355 ms: 2.05x faster                                                             |
| async_tree_io           | 1.77 sec                                               | 920 ms: 1.92x faster                                                             |
| async_tree_memoization  | 870 ms                                                 | 457 ms: 1.90x faster                                                             |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 607 ms: 1.67x faster                                                             |
| Geometric mean          | (ref)                                                  | 1.88x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240406-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-cd8bea7 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 94.4 ms: 1.63x faster                                                            |
| float          | 117 ms                                                 | 77.6 ms: 1.51x faster                                                            |
| pidigits       | 191 ms                                                 | 194 ms: 1.02x slower                                                             |
| Geometric mean | (ref)                                                  | 1.34x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240406-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-cd8bea7 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 135 ms: 1.40x faster                                                             |
| regex_v8       | 27.8 ms                                                | 26.2 ms: 1.06x faster                                                            |
| regex_dna      | 227 ms                                                 | 230 ms: 1.01x slower                                                             |
| regex_effbot   | 3.63 ms                                                | 3.81 ms: 1.05x slower                                                            |
| Geometric mean | (ref)                                                  | 1.09x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240406-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-cd8bea7 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 302 us: 1.61x faster                                                             |
| unpickle_pure_python | 331 us                                                 | 219 us: 1.51x faster                                                             |
| tomli_loads          | 3.14 sec                                               | 2.21 sec: 1.42x faster                                                           |
| json_dumps           | 14.2 ms                                                | 10.6 ms: 1.34x faster                                                            |
| xml_etree_process    | 79.1 ms                                                | 60.0 ms: 1.32x faster                                                            |
| xml_etree_generate   | 99.4 ms                                                | 86.7 ms: 1.15x faster                                                            |
| json_loads           | 31.2 us                                                | 28.7 us: 1.09x faster                                                            |
| xml_etree_iterparse  | 115 ms                                                 | 106 ms: 1.08x faster                                                             |
| xml_etree_parse      | 168 ms                                                 | 160 ms: 1.05x faster                                                             |
| unpickle_list        | 5.20 us                                                | 4.98 us: 1.04x faster                                                            |
| pickle_list          | 5.08 us                                                | 5.18 us: 1.02x slower                                                            |
| unpickle             | 14.4 us                                                | 15.4 us: 1.07x slower                                                            |
| pickle               | 10.7 us                                                | 11.8 us: 1.11x slower                                                            |
| pickle_dict          | 29.6 us                                                | 35.5 us: 1.20x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.14x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240406-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-cd8bea7 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.6 ms: 1.38x faster                                                            |
| python_startup_no_site | 5.93 ms                                                | 8.99 ms: 1.52x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.05x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240406-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-cd8bea7 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako           | 16.3 ms                                                | 11.2 ms: 1.46x faster                                                            |
| genshi_text    | 31.8 ms                                                | 23.5 ms: 1.35x faster                                                            |
| genshi_xml     | 66.0 ms                                                | 51.7 ms: 1.28x faster                                                            |
| Geometric mean | (ref)                                                  | 1.36x faster                                                                     |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240406-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-cd8bea7 |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 111 us: 4.89x faster                                                             |
| generators               | 80.1 ms                                                | 29.7 ms: 2.70x faster                                                            |
| deltablue                | 7.91 ms                                                | 3.25 ms: 2.43x faster                                                            |
| async_tree_none          | 728 ms                                                 | 355 ms: 2.05x faster                                                             |
| pylint                   | 551 ms                                                 | 278 ms: 1.98x faster                                                             |
| async_tree_io            | 1.77 sec                                               | 920 ms: 1.92x faster                                                             |
| async_tree_memoization   | 870 ms                                                 | 457 ms: 1.90x faster                                                             |
| raytrace                 | 507 ms                                                 | 267 ms: 1.90x faster                                                             |
| chaos                    | 115 ms                                                 | 61.2 ms: 1.89x faster                                                            |
| logging_silent           | 190 ns                                                 | 102 ns: 1.86x faster                                                             |
| asyncio_tcp              | 922 ms                                                 | 506 ms: 1.82x faster                                                             |
| crypto_pyaes             | 128 ms                                                 | 70.9 ms: 1.80x faster                                                            |
| richards_super           | 94.7 ms                                                | 53.1 ms: 1.78x faster                                                            |
| scimark_monte_carlo      | 118 ms                                                 | 68.4 ms: 1.73x faster                                                            |
| comprehensions           | 28.8 us                                                | 16.7 us: 1.72x faster                                                            |
| scimark_sor              | 220 ms                                                 | 130 ms: 1.70x faster                                                             |
| go                       | 240 ms                                                 | 143 ms: 1.68x faster                                                             |
| richards                 | 79.3 ms                                                | 47.3 ms: 1.68x faster                                                            |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 607 ms: 1.67x faster                                                             |
| sqlglot_parse            | 2.17 ms                                                | 1.30 ms: 1.67x faster                                                            |
| hexiom                   | 10.4 ms                                                | 6.27 ms: 1.66x faster                                                            |
| nbody                    | 154 ms                                                 | 94.4 ms: 1.63x faster                                                            |
| sqlglot_transpile        | 2.57 ms                                                | 1.59 ms: 1.62x faster                                                            |
| pickle_pure_python       | 484 us                                                 | 302 us: 1.61x faster                                                             |
| spectral_norm            | 170 ms                                                 | 107 ms: 1.59x faster                                                             |
| pyflate                  | 716 ms                                                 | 452 ms: 1.59x faster                                                             |
| scimark_lu               | 176 ms                                                 | 114 ms: 1.54x faster                                                             |
| deepcopy_memo            | 58.5 us                                                | 38.2 us: 1.53x faster                                                            |
| coroutines               | 35.1 ms                                                | 23.2 ms: 1.51x faster                                                            |
| float                    | 117 ms                                                 | 77.6 ms: 1.51x faster                                                            |
| unpickle_pure_python     | 331 us                                                 | 219 us: 1.51x faster                                                             |
| logging_simple           | 8.30 us                                                | 5.64 us: 1.47x faster                                                            |
| mako                     | 16.3 ms                                                | 11.2 ms: 1.46x faster                                                            |
| tornado_http             | 136 ms                                                 | 93.9 ms: 1.45x faster                                                            |
| logging_format           | 9.09 us                                                | 6.27 us: 1.45x faster                                                            |
| tomli_loads              | 3.14 sec                                               | 2.21 sec: 1.42x faster                                                           |
| regex_compile            | 188 ms                                                 | 135 ms: 1.40x faster                                                             |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.84 sec: 1.39x faster                                                           |
| chameleon                | 9.68 ms                                                | 6.97 ms: 1.39x faster                                                            |
| pprint_pformat           | 2.10 sec                                               | 1.52 sec: 1.38x faster                                                           |
| python_startup           | 14.6 ms                                                | 10.6 ms: 1.38x faster                                                            |
| pprint_safe_repr         | 1.02 sec                                               | 741 ms: 1.37x faster                                                             |
| deepcopy                 | 479 us                                                 | 352 us: 1.36x faster                                                             |
| genshi_text              | 31.8 ms                                                | 23.5 ms: 1.35x faster                                                            |
| fannkuch                 | 532 ms                                                 | 396 ms: 1.34x faster                                                             |
| json_dumps               | 14.2 ms                                                | 10.6 ms: 1.34x faster                                                            |
| deepcopy_reduce          | 4.17 us                                                | 3.15 us: 1.32x faster                                                            |
| xml_etree_process        | 79.1 ms                                                | 60.0 ms: 1.32x faster                                                            |
| thrift                   | 1.07 ms                                                | 814 us: 1.32x faster                                                             |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 4.92 ms: 1.32x faster                                                            |
| pycparser                | 1.58 sec                                               | 1.20 sec: 1.31x faster                                                           |
| html5lib                 | 88.9 ms                                                | 68.2 ms: 1.30x faster                                                            |
| 2to3                     | 348 ms                                                 | 268 ms: 1.30x faster                                                             |
| sqlglot_normalize        | 143 ms                                                 | 110 ms: 1.30x faster                                                             |
| nqueens                  | 106 ms                                                 | 82.5 ms: 1.28x faster                                                            |
| genshi_xml               | 66.0 ms                                                | 51.7 ms: 1.28x faster                                                            |
| sympy_sum                | 196 ms                                                 | 155 ms: 1.27x faster                                                             |
| sympy_integrate          | 25.8 ms                                                | 20.3 ms: 1.27x faster                                                            |
| sqlglot_optimize         | 69.2 ms                                                | 54.9 ms: 1.26x faster                                                            |
| sympy_str                | 346 ms                                                 | 278 ms: 1.24x faster                                                             |
| dulwich_log              | 84.3 ms                                                | 67.9 ms: 1.24x faster                                                            |
| aiohttp                  | 1.44 ms                                                | 1.16 ms: 1.24x faster                                                            |
| scimark_fft              | 466 ms                                                 | 377 ms: 1.23x faster                                                             |
| sympy_expand             | 566 ms                                                 | 464 ms: 1.22x faster                                                             |
| gunicorn                 | 1.53 ms                                                | 1.26 ms: 1.21x faster                                                            |
| mypy2                    | 894 ms                                                 | 738 ms: 1.21x faster                                                             |
| dask                     | 441 ms                                                 | 368 ms: 1.20x faster                                                             |
| bench_thread_pool        | 986 us                                                 | 828 us: 1.19x faster                                                             |
| docutils                 | 3.30 sec                                               | 2.80 sec: 1.18x faster                                                           |
| xml_etree_generate       | 99.4 ms                                                | 86.7 ms: 1.15x faster                                                            |
| mdp                      | 2.85 sec                                               | 2.57 sec: 1.11x faster                                                           |
| pathlib                  | 20.5 ms                                                | 18.5 ms: 1.11x faster                                                            |
| meteor_contest           | 120 ms                                                 | 109 ms: 1.10x faster                                                             |
| json_loads               | 31.2 us                                                | 28.7 us: 1.09x faster                                                            |
| xml_etree_iterparse      | 115 ms                                                 | 106 ms: 1.08x faster                                                             |
| regex_v8                 | 27.8 ms                                                | 26.2 ms: 1.06x faster                                                            |
| xml_etree_parse          | 168 ms                                                 | 160 ms: 1.05x faster                                                             |
| json                     | 5.69 ms                                                | 5.42 ms: 1.05x faster                                                            |
| unpickle_list            | 5.20 us                                                | 4.98 us: 1.04x faster                                                            |
| sqlite_synth             | 3.02 us                                                | 2.95 us: 1.02x faster                                                            |
| gc_traversal             | 3.62 ms                                                | 3.57 ms: 1.01x faster                                                            |
| async_generators         | 444 ms                                                 | 439 ms: 1.01x faster                                                             |
| bench_mp_pool            | 24.0 ms                                                | 23.8 ms: 1.01x faster                                                            |
| regex_dna                | 227 ms                                                 | 230 ms: 1.01x slower                                                             |
| asyncio_websockets       | 559 ms                                                 | 567 ms: 1.01x slower                                                             |
| pidigits                 | 191 ms                                                 | 194 ms: 1.02x slower                                                             |
| pickle_list              | 5.08 us                                                | 5.18 us: 1.02x slower                                                            |
| regex_effbot             | 3.63 ms                                                | 3.81 ms: 1.05x slower                                                            |
| create_gc_cycles         | 1.62 ms                                                | 1.74 ms: 1.07x slower                                                            |
| unpickle                 | 14.4 us                                                | 15.4 us: 1.07x slower                                                            |
| pickle                   | 10.7 us                                                | 11.8 us: 1.11x slower                                                            |
| telco                    | 7.27 ms                                                | 8.46 ms: 1.16x slower                                                            |
| pickle_dict              | 29.6 us                                                | 35.5 us: 1.20x slower                                                            |
| coverage                 | 79.4 ms                                                | 97.7 ms: 1.23x slower                                                            |
| python_startup_no_site   | 5.93 ms                                                | 8.99 ms: 1.52x slower                                                            |
| Geometric mean           | (ref)                                                  | 1.35x faster                                                                     |
Ignored benchmarks (6) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240406-3.13.0a5+-cd8bea7/bm-20240406-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-cd8bea7.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.28x
- 95% likely to have a speedup of 1.27x
- 99% likely to have a speedup of 1.25x

# Memory
- memory change: 1.09x