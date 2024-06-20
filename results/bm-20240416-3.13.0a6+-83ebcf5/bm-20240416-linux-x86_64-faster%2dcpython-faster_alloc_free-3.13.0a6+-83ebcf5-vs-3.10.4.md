# Results vs. 3.10.4

- fork: faster-cpython
- ref: faster_alloc_free
- machine: linux-x86_64
- commit hash: 83ebcf5
- commit date: 2024-04-16
- overall geometric mean: 1.34x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.24x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240416-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-83ebcf5 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 271 ms: 1.28x faster                                                          |
| chameleon      | 9.68 ms                                                | 7.07 ms: 1.37x faster                                                         |
| docutils       | 3.30 sec                                               | 2.84 sec: 1.16x faster                                                        |
| html5lib       | 88.9 ms                                                | 68.2 ms: 1.30x faster                                                         |
| tornado_http   | 136 ms                                                 | 94.1 ms: 1.45x faster                                                         |
| Geometric mean | (ref)                                                  | 1.31x faster                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240416-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-83ebcf5 |
|-------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 357 ms: 2.04x faster                                                          |
| async_tree_io           | 1.77 sec                                               | 925 ms: 1.91x faster                                                          |
| async_tree_memoization  | 870 ms                                                 | 465 ms: 1.87x faster                                                          |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 607 ms: 1.67x faster                                                          |
| Geometric mean          | (ref)                                                  | 1.87x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240416-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-83ebcf5 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 90.3 ms: 1.70x faster                                                         |
| float          | 117 ms                                                 | 79.8 ms: 1.47x faster                                                         |
| pidigits       | 191 ms                                                 | 190 ms: 1.01x faster                                                          |
| Geometric mean | (ref)                                                  | 1.36x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240416-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-83ebcf5 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 137 ms: 1.37x faster                                                          |
| regex_v8       | 27.8 ms                                                | 24.8 ms: 1.12x faster                                                         |
| regex_dna      | 227 ms                                                 | 226 ms: 1.00x faster                                                          |
| Geometric mean | (ref)                                                  | 1.11x faster                                                                  |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240416-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-83ebcf5 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 302 us: 1.60x faster                                                          |
| unpickle_pure_python | 331 us                                                 | 223 us: 1.48x faster                                                          |
| tomli_loads          | 3.14 sec                                               | 2.22 sec: 1.41x faster                                                        |
| json_dumps           | 14.2 ms                                                | 10.6 ms: 1.33x faster                                                         |
| xml_etree_process    | 79.1 ms                                                | 61.2 ms: 1.29x faster                                                         |
| xml_etree_generate   | 99.4 ms                                                | 88.5 ms: 1.12x faster                                                         |
| json_loads           | 31.2 us                                                | 28.0 us: 1.11x faster                                                         |
| xml_etree_iterparse  | 115 ms                                                 | 108 ms: 1.07x faster                                                          |
| xml_etree_parse      | 168 ms                                                 | 160 ms: 1.05x faster                                                          |
| unpickle_list        | 5.20 us                                                | 4.98 us: 1.04x faster                                                         |
| pickle_list          | 5.08 us                                                | 5.03 us: 1.01x faster                                                         |
| unpickle             | 14.4 us                                                | 15.1 us: 1.05x slower                                                         |
| pickle               | 10.7 us                                                | 11.5 us: 1.08x slower                                                         |
| pickle_dict          | 29.6 us                                                | 33.9 us: 1.15x slower                                                         |
| Geometric mean       | (ref)                                                  | 1.14x faster                                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240416-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-83ebcf5 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                         |
| python_startup_no_site | 5.93 ms                                                | 7.09 ms: 1.20x slower                                                         |
| Geometric mean         | (ref)                                                  | 1.08x faster                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240416-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-83ebcf5 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 11.0 ms: 1.49x faster                                                         |
| django_template | 48.2 ms                                                | 35.6 ms: 1.35x faster                                                         |
| genshi_text     | 31.8 ms                                                | 23.8 ms: 1.34x faster                                                         |
| genshi_xml      | 66.0 ms                                                | 51.8 ms: 1.27x faster                                                         |
| Geometric mean  | (ref)                                                  | 1.36x faster                                                                  |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240416-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-83ebcf5 |
|--------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 113 us: 4.84x faster                                                          |
| generators               | 80.1 ms                                                | 30.1 ms: 2.66x faster                                                         |
| deltablue                | 7.91 ms                                                | 3.29 ms: 2.40x faster                                                         |
| async_tree_none          | 728 ms                                                 | 357 ms: 2.04x faster                                                          |
| raytrace                 | 507 ms                                                 | 265 ms: 1.91x faster                                                          |
| async_tree_io            | 1.77 sec                                               | 925 ms: 1.91x faster                                                          |
| async_tree_memoization   | 870 ms                                                 | 465 ms: 1.87x faster                                                          |
| chaos                    | 115 ms                                                 | 62.2 ms: 1.86x faster                                                         |
| asyncio_tcp              | 922 ms                                                 | 505 ms: 1.83x faster                                                          |
| logging_silent           | 190 ns                                                 | 104 ns: 1.82x faster                                                          |
| scimark_sor              | 220 ms                                                 | 125 ms: 1.76x faster                                                          |
| richards_super           | 94.7 ms                                                | 54.0 ms: 1.76x faster                                                         |
| pylint                   | 551 ms                                                 | 321 ms: 1.72x faster                                                          |
| nbody                    | 154 ms                                                 | 90.3 ms: 1.70x faster                                                         |
| crypto_pyaes             | 128 ms                                                 | 75.6 ms: 1.69x faster                                                         |
| scimark_monte_carlo      | 118 ms                                                 | 70.3 ms: 1.68x faster                                                         |
| sqlglot_parse            | 2.17 ms                                                | 1.29 ms: 1.68x faster                                                         |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 607 ms: 1.67x faster                                                          |
| comprehensions           | 28.8 us                                                | 17.2 us: 1.67x faster                                                         |
| go                       | 240 ms                                                 | 144 ms: 1.67x faster                                                          |
| richards                 | 79.3 ms                                                | 48.2 ms: 1.65x faster                                                         |
| hexiom                   | 10.4 ms                                                | 6.40 ms: 1.63x faster                                                         |
| sqlglot_transpile        | 2.57 ms                                                | 1.60 ms: 1.61x faster                                                         |
| pickle_pure_python       | 484 us                                                 | 302 us: 1.60x faster                                                          |
| pyflate                  | 716 ms                                                 | 469 ms: 1.53x faster                                                          |
| deepcopy_memo            | 58.5 us                                                | 38.5 us: 1.52x faster                                                         |
| coroutines               | 35.1 ms                                                | 23.2 ms: 1.51x faster                                                         |
| mako                     | 16.3 ms                                                | 11.0 ms: 1.49x faster                                                         |
| unpickle_pure_python     | 331 us                                                 | 223 us: 1.48x faster                                                          |
| spectral_norm            | 170 ms                                                 | 115 ms: 1.47x faster                                                          |
| float                    | 117 ms                                                 | 79.8 ms: 1.47x faster                                                         |
| scimark_lu               | 176 ms                                                 | 121 ms: 1.45x faster                                                          |
| tornado_http             | 136 ms                                                 | 94.1 ms: 1.45x faster                                                         |
| logging_simple           | 8.30 us                                                | 5.78 us: 1.44x faster                                                         |
| logging_format           | 9.09 us                                                | 6.43 us: 1.41x faster                                                         |
| tomli_loads              | 3.14 sec                                               | 2.22 sec: 1.41x faster                                                        |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.84 sec: 1.40x faster                                                        |
| python_startup           | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                         |
| regex_compile            | 188 ms                                                 | 137 ms: 1.37x faster                                                          |
| chameleon                | 9.68 ms                                                | 7.07 ms: 1.37x faster                                                         |
| pprint_pformat           | 2.10 sec                                               | 1.54 sec: 1.36x faster                                                        |
| django_template          | 48.2 ms                                                | 35.6 ms: 1.35x faster                                                         |
| pprint_safe_repr         | 1.02 sec                                               | 755 ms: 1.35x faster                                                          |
| pycparser                | 1.58 sec                                               | 1.18 sec: 1.34x faster                                                        |
| genshi_text              | 31.8 ms                                                | 23.8 ms: 1.34x faster                                                         |
| json_dumps               | 14.2 ms                                                | 10.6 ms: 1.33x faster                                                         |
| fannkuch                 | 532 ms                                                 | 399 ms: 1.33x faster                                                          |
| deepcopy                 | 479 us                                                 | 361 us: 1.33x faster                                                          |
| thrift                   | 1.07 ms                                                | 811 us: 1.32x faster                                                          |
| html5lib                 | 88.9 ms                                                | 68.2 ms: 1.30x faster                                                         |
| xml_etree_process        | 79.1 ms                                                | 61.2 ms: 1.29x faster                                                         |
| nqueens                  | 106 ms                                                 | 82.4 ms: 1.28x faster                                                         |
| 2to3                     | 348 ms                                                 | 271 ms: 1.28x faster                                                          |
| deepcopy_reduce          | 4.17 us                                                | 3.26 us: 1.28x faster                                                         |
| sqlglot_normalize        | 143 ms                                                 | 112 ms: 1.28x faster                                                          |
| genshi_xml               | 66.0 ms                                                | 51.8 ms: 1.27x faster                                                         |
| dulwich_log              | 84.3 ms                                                | 66.3 ms: 1.27x faster                                                         |
| sympy_integrate          | 25.8 ms                                                | 20.6 ms: 1.25x faster                                                         |
| sympy_sum                | 196 ms                                                 | 158 ms: 1.25x faster                                                          |
| sqlglot_optimize         | 69.2 ms                                                | 56.0 ms: 1.24x faster                                                         |
| aiohttp                  | 1.44 ms                                                | 1.17 ms: 1.23x faster                                                         |
| scimark_fft              | 466 ms                                                 | 380 ms: 1.23x faster                                                          |
| sympy_str                | 346 ms                                                 | 284 ms: 1.22x faster                                                          |
| djangocms                | 38.4 us                                                | 31.7 us: 1.21x faster                                                         |
| mypy2                    | 894 ms                                                 | 741 ms: 1.21x faster                                                          |
| gunicorn                 | 1.53 ms                                                | 1.27 ms: 1.20x faster                                                         |
| dask                     | 441 ms                                                 | 368 ms: 1.20x faster                                                          |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 5.46 ms: 1.18x faster                                                         |
| sympy_expand             | 566 ms                                                 | 479 ms: 1.18x faster                                                          |
| bench_thread_pool        | 986 us                                                 | 838 us: 1.18x faster                                                          |
| pathlib                  | 20.5 ms                                                | 17.6 ms: 1.16x faster                                                         |
| docutils                 | 3.30 sec                                               | 2.84 sec: 1.16x faster                                                        |
| xml_etree_generate       | 99.4 ms                                                | 88.5 ms: 1.12x faster                                                         |
| regex_v8                 | 27.8 ms                                                | 24.8 ms: 1.12x faster                                                         |
| json_loads               | 31.2 us                                                | 28.0 us: 1.11x faster                                                         |
| json                     | 5.69 ms                                                | 5.21 ms: 1.09x faster                                                         |
| meteor_contest           | 120 ms                                                 | 112 ms: 1.07x faster                                                          |
| xml_etree_iterparse      | 115 ms                                                 | 108 ms: 1.07x faster                                                          |
| mdp                      | 2.85 sec                                               | 2.67 sec: 1.07x faster                                                        |
| xml_etree_parse          | 168 ms                                                 | 160 ms: 1.05x faster                                                          |
| unpickle_list            | 5.20 us                                                | 4.98 us: 1.04x faster                                                         |
| sqlite_synth             | 3.02 us                                                | 2.97 us: 1.02x faster                                                         |
| pickle_list              | 5.08 us                                                | 5.03 us: 1.01x faster                                                         |
| bench_mp_pool            | 24.0 ms                                                | 23.8 ms: 1.01x faster                                                         |
| pidigits                 | 191 ms                                                 | 190 ms: 1.01x faster                                                          |
| regex_dna                | 227 ms                                                 | 226 ms: 1.00x faster                                                          |
| asyncio_websockets       | 559 ms                                                 | 563 ms: 1.01x slower                                                          |
| async_generators         | 444 ms                                                 | 448 ms: 1.01x slower                                                          |
| gc_traversal             | 3.62 ms                                                | 3.76 ms: 1.04x slower                                                         |
| unpickle                 | 14.4 us                                                | 15.1 us: 1.05x slower                                                         |
| create_gc_cycles         | 1.62 ms                                                | 1.73 ms: 1.07x slower                                                         |
| pickle                   | 10.7 us                                                | 11.5 us: 1.08x slower                                                         |
| pickle_dict              | 29.6 us                                                | 33.9 us: 1.15x slower                                                         |
| python_startup_no_site   | 5.93 ms                                                | 7.09 ms: 1.20x slower                                                         |
| telco                    | 7.27 ms                                                | 8.85 ms: 1.22x slower                                                         |
| coverage                 | 79.4 ms                                                | 97.6 ms: 1.23x slower                                                         |
| Geometric mean           | (ref)                                                  | 1.34x faster                                                                  |

Benchmark hidden because not significant (1): regex_effbot
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240416-3.13.0a6+-83ebcf5/bm-20240416-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-83ebcf5.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.28x
- 95% likely to have a speedup of 1.27x
- 99% likely to have a speedup of 1.24x

# Memory
- memory change: 1.10x