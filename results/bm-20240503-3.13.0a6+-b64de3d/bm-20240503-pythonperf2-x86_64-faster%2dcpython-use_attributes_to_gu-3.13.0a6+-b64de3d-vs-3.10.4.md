# Results vs. 3.10.4

- fork: faster-cpython
- ref: use_attributes_to_gu
- machine: linux-x86_64
- commit hash: b64de3d
- commit date: 2024-05-03
- overall geometric mean: 1.28x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.21x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-b64de3d |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| 2to3           | 350 ms                                                       | 291 ms: 1.20x faster                                                                   |
| chameleon      | 9.44 ms                                                      | 7.52 ms: 1.26x faster                                                                  |
| docutils       | 3.41 sec                                                     | 3.02 sec: 1.13x faster                                                                 |
| html5lib       | 94.6 ms                                                      | 75.9 ms: 1.25x faster                                                                  |
| tornado_http   | 157 ms                                                       | 119 ms: 1.32x faster                                                                   |
| Geometric mean | (ref)                                                        | 1.23x faster                                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-b64de3d |
|-------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| async_tree_none         | 692 ms                                                       | 376 ms: 1.84x faster                                                                   |
| async_tree_io           | 1.60 sec                                                     | 907 ms: 1.76x faster                                                                   |
| async_tree_memoization  | 819 ms                                                       | 475 ms: 1.73x faster                                                                   |
| async_tree_cpu_io_mixed | 936 ms                                                       | 622 ms: 1.50x faster                                                                   |
| Geometric mean          | (ref)                                                        | 1.70x faster                                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-b64de3d |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| nbody          | 134 ms                                                       | 91.0 ms: 1.47x faster                                                                  |
| float          | 111 ms                                                       | 80.9 ms: 1.37x faster                                                                  |
| pidigits       | 271 ms                                                       | 255 ms: 1.06x faster                                                                   |
| Geometric mean | (ref)                                                        | 1.29x faster                                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-b64de3d |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| regex_compile  | 190 ms                                                       | 143 ms: 1.33x faster                                                                   |
| regex_dna      | 261 ms                                                       | 237 ms: 1.10x faster                                                                   |
| regex_v8       | 27.2 ms                                                      | 25.6 ms: 1.06x faster                                                                  |
| regex_effbot   | 3.09 ms                                                      | 3.52 ms: 1.14x slower                                                                  |
| Geometric mean | (ref)                                                        | 1.08x faster                                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-b64de3d |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| unpickle_pure_python | 312 us                                                       | 213 us: 1.46x faster                                                                   |
| pickle_pure_python   | 455 us                                                       | 326 us: 1.40x faster                                                                   |
| json_dumps           | 14.5 ms                                                      | 11.1 ms: 1.31x faster                                                                  |
| xml_etree_process    | 75.9 ms                                                      | 59.1 ms: 1.29x faster                                                                  |
| json_loads           | 30.3 us                                                      | 24.6 us: 1.23x faster                                                                  |
| tomli_loads          | 2.92 sec                                                     | 2.38 sec: 1.22x faster                                                                 |
| xml_etree_parse      | 160 ms                                                       | 145 ms: 1.10x faster                                                                   |
| xml_etree_generate   | 92.3 ms                                                      | 84.7 ms: 1.09x faster                                                                  |
| xml_etree_iterparse  | 110 ms                                                       | 104 ms: 1.07x faster                                                                   |
| unpickle_list        | 4.65 us                                                      | 4.68 us: 1.01x slower                                                                  |
| pickle_list          | 4.12 us                                                      | 4.49 us: 1.09x slower                                                                  |
| pickle               | 9.89 us                                                      | 10.9 us: 1.10x slower                                                                  |
| pickle_dict          | 29.5 us                                                      | 32.9 us: 1.12x slower                                                                  |
| unpickle             | 13.5 us                                                      | 15.1 us: 1.12x slower                                                                  |
| Geometric mean       | (ref)                                                        | 1.11x faster                                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-b64de3d |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| python_startup         | 11.5 ms                                                      | 12.8 ms: 1.12x slower                                                                  |
| python_startup_no_site | 7.33 ms                                                      | 8.80 ms: 1.20x slower                                                                  |
| Geometric mean         | (ref)                                                        | 1.16x slower                                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-b64de3d |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| mako            | 14.7 ms                                                      | 10.4 ms: 1.41x faster                                                                  |
| genshi_text     | 31.4 ms                                                      | 24.8 ms: 1.27x faster                                                                  |
| django_template | 50.2 ms                                                      | 39.6 ms: 1.27x faster                                                                  |
| genshi_xml      | 63.3 ms                                                      | 53.3 ms: 1.19x faster                                                                  |
| Geometric mean  | (ref)                                                        | 1.28x faster                                                                           |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-b64de3d |
|--------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| typing_runtime_protocols | 537 us                                                       | 175 us: 3.07x faster                                                                   |
| deltablue                | 7.50 ms                                                      | 3.46 ms: 2.17x faster                                                                  |
| asyncio_tcp              | 779 ms                                                       | 373 ms: 2.09x faster                                                                   |
| asyncio_tcp_ssl          | 3.10 sec                                                     | 1.58 sec: 1.97x faster                                                                 |
| go                       | 262 ms                                                       | 134 ms: 1.95x faster                                                                   |
| async_tree_none          | 692 ms                                                       | 376 ms: 1.84x faster                                                                   |
| raytrace                 | 489 ms                                                       | 270 ms: 1.81x faster                                                                   |
| async_tree_io            | 1.60 sec                                                     | 907 ms: 1.76x faster                                                                   |
| chaos                    | 109 ms                                                       | 62.1 ms: 1.75x faster                                                                  |
| async_tree_memoization   | 819 ms                                                       | 475 ms: 1.73x faster                                                                   |
| logging_silent           | 167 ns                                                       | 98.0 ns: 1.71x faster                                                                  |
| generators               | 57.3 ms                                                      | 33.6 ms: 1.70x faster                                                                  |
| scimark_lu               | 167 ms                                                       | 99.5 ms: 1.68x faster                                                                  |
| pylint                   | 566 ms                                                       | 345 ms: 1.64x faster                                                                   |
| sqlglot_parse            | 2.24 ms                                                      | 1.39 ms: 1.61x faster                                                                  |
| comprehensions           | 26.7 us                                                      | 17.1 us: 1.56x faster                                                                  |
| pyflate                  | 733 ms                                                       | 474 ms: 1.55x faster                                                                   |
| richards_super           | 90.6 ms                                                      | 58.8 ms: 1.54x faster                                                                  |
| sqlglot_transpile        | 2.68 ms                                                      | 1.78 ms: 1.51x faster                                                                  |
| async_tree_cpu_io_mixed  | 936 ms                                                       | 622 ms: 1.50x faster                                                                   |
| hexiom                   | 9.42 ms                                                      | 6.38 ms: 1.48x faster                                                                  |
| nbody                    | 134 ms                                                       | 91.0 ms: 1.47x faster                                                                  |
| richards                 | 75.1 ms                                                      | 51.2 ms: 1.47x faster                                                                  |
| unpickle_pure_python     | 312 us                                                       | 213 us: 1.46x faster                                                                   |
| scimark_monte_carlo      | 107 ms                                                       | 73.8 ms: 1.46x faster                                                                  |
| crypto_pyaes             | 119 ms                                                       | 82.0 ms: 1.45x faster                                                                  |
| coroutines               | 30.3 ms                                                      | 21.5 ms: 1.41x faster                                                                  |
| mako                     | 14.7 ms                                                      | 10.4 ms: 1.41x faster                                                                  |
| pickle_pure_python       | 455 us                                                       | 326 us: 1.40x faster                                                                   |
| scimark_sor              | 180 ms                                                       | 130 ms: 1.39x faster                                                                   |
| spectral_norm            | 139 ms                                                       | 101 ms: 1.38x faster                                                                   |
| float                    | 111 ms                                                       | 80.9 ms: 1.37x faster                                                                  |
| bench_mp_pool            | 6.37 ms                                                      | 4.66 ms: 1.37x faster                                                                  |
| fannkuch                 | 483 ms                                                       | 362 ms: 1.33x faster                                                                   |
| pycparser                | 1.67 sec                                                     | 1.26 sec: 1.33x faster                                                                 |
| regex_compile            | 190 ms                                                       | 143 ms: 1.33x faster                                                                   |
| deepcopy_memo            | 49.8 us                                                      | 37.5 us: 1.33x faster                                                                  |
| tornado_http             | 157 ms                                                       | 119 ms: 1.32x faster                                                                   |
| json_dumps               | 14.5 ms                                                      | 11.1 ms: 1.31x faster                                                                  |
| thrift                   | 1.18 ms                                                      | 898 us: 1.31x faster                                                                   |
| logging_simple           | 8.88 us                                                      | 6.81 us: 1.30x faster                                                                  |
| pprint_pformat           | 2.15 sec                                                     | 1.66 sec: 1.30x faster                                                                 |
| pprint_safe_repr         | 1.05 sec                                                     | 814 ms: 1.29x faster                                                                   |
| xml_etree_process        | 75.9 ms                                                      | 59.1 ms: 1.29x faster                                                                  |
| nqueens                  | 115 ms                                                       | 90.2 ms: 1.27x faster                                                                  |
| bench_thread_pool        | 1.14 ms                                                      | 897 us: 1.27x faster                                                                   |
| genshi_text              | 31.4 ms                                                      | 24.8 ms: 1.27x faster                                                                  |
| django_template          | 50.2 ms                                                      | 39.6 ms: 1.27x faster                                                                  |
| logging_format           | 9.64 us                                                      | 7.67 us: 1.26x faster                                                                  |
| chameleon                | 9.44 ms                                                      | 7.52 ms: 1.26x faster                                                                  |
| sympy_sum                | 193 ms                                                       | 154 ms: 1.25x faster                                                                   |
| html5lib                 | 94.6 ms                                                      | 75.9 ms: 1.25x faster                                                                  |
| deepcopy                 | 468 us                                                       | 378 us: 1.24x faster                                                                   |
| json_loads               | 30.3 us                                                      | 24.6 us: 1.23x faster                                                                  |
| dulwich_log              | 81.1 ms                                                      | 66.2 ms: 1.22x faster                                                                  |
| tomli_loads              | 2.92 sec                                                     | 2.38 sec: 1.22x faster                                                                 |
| pathlib                  | 21.4 ms                                                      | 17.5 ms: 1.22x faster                                                                  |
| sympy_str                | 360 ms                                                       | 298 ms: 1.21x faster                                                                   |
| 2to3                     | 350 ms                                                       | 291 ms: 1.20x faster                                                                   |
| dask                     | 472 ms                                                       | 392 ms: 1.20x faster                                                                   |
| mdp                      | 3.01 sec                                                     | 2.50 sec: 1.20x faster                                                                 |
| sympy_integrate          | 28.2 ms                                                      | 23.4 ms: 1.20x faster                                                                  |
| mypy2                    | 933 ms                                                       | 778 ms: 1.20x faster                                                                   |
| genshi_xml               | 63.3 ms                                                      | 53.3 ms: 1.19x faster                                                                  |
| scimark_sparse_mat_mult  | 5.08 ms                                                      | 4.29 ms: 1.18x faster                                                                  |
| sympy_expand             | 600 ms                                                       | 506 ms: 1.18x faster                                                                   |
| sqlglot_normalize        | 144 ms                                                       | 122 ms: 1.18x faster                                                                   |
| deepcopy_reduce          | 4.01 us                                                      | 3.43 us: 1.17x faster                                                                  |
| sqlglot_optimize         | 70.1 ms                                                      | 60.1 ms: 1.17x faster                                                                  |
| async_generators         | 421 ms                                                       | 368 ms: 1.14x faster                                                                   |
| scimark_fft              | 361 ms                                                       | 317 ms: 1.14x faster                                                                   |
| docutils                 | 3.41 sec                                                     | 3.02 sec: 1.13x faster                                                                 |
| gunicorn                 | 1.16 ms                                                      | 1.05 ms: 1.11x faster                                                                  |
| xml_etree_parse          | 160 ms                                                       | 145 ms: 1.10x faster                                                                   |
| regex_dna                | 261 ms                                                       | 237 ms: 1.10x faster                                                                   |
| json                     | 5.86 ms                                                      | 5.38 ms: 1.09x faster                                                                  |
| aiohttp                  | 1.19 ms                                                      | 1.09 ms: 1.09x faster                                                                  |
| xml_etree_generate       | 92.3 ms                                                      | 84.7 ms: 1.09x faster                                                                  |
| xml_etree_iterparse      | 110 ms                                                       | 104 ms: 1.07x faster                                                                   |
| pidigits                 | 271 ms                                                       | 255 ms: 1.06x faster                                                                   |
| regex_v8                 | 27.2 ms                                                      | 25.6 ms: 1.06x faster                                                                  |
| meteor_contest           | 138 ms                                                       | 131 ms: 1.06x faster                                                                   |
| sqlite_synth             | 2.99 us                                                      | 2.82 us: 1.06x faster                                                                  |
| unpickle_list            | 4.65 us                                                      | 4.68 us: 1.01x slower                                                                  |
| asyncio_websockets       | 390 ms                                                       | 395 ms: 1.01x slower                                                                   |
| flaskblogging            | 4.39 ms                                                      | 4.75 ms: 1.08x slower                                                                  |
| pickle_list              | 4.12 us                                                      | 4.49 us: 1.09x slower                                                                  |
| pickle                   | 9.89 us                                                      | 10.9 us: 1.10x slower                                                                  |
| pickle_dict              | 29.5 us                                                      | 32.9 us: 1.12x slower                                                                  |
| python_startup           | 11.5 ms                                                      | 12.8 ms: 1.12x slower                                                                  |
| unpickle                 | 13.5 us                                                      | 15.1 us: 1.12x slower                                                                  |
| create_gc_cycles         | 1.76 ms                                                      | 2.01 ms: 1.14x slower                                                                  |
| regex_effbot             | 3.09 ms                                                      | 3.52 ms: 1.14x slower                                                                  |
| telco                    | 7.23 ms                                                      | 8.27 ms: 1.14x slower                                                                  |
| python_startup_no_site   | 7.33 ms                                                      | 8.80 ms: 1.20x slower                                                                  |
| coverage                 | 63.3 ms                                                      | 77.4 ms: 1.22x slower                                                                  |
| gc_traversal             | 3.42 ms                                                      | 4.82 ms: 1.41x slower                                                                  |
| Geometric mean           | (ref)                                                        | 1.28x faster                                                                           |
Ignored benchmarks (3) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240503-3.13.0a6+-b64de3d/bm-20240503-pythonperf2-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-b64de3d.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.23x
- 95% likely to have a speedup of 1.22x
- 99% likely to have a speedup of 1.21x

# Memory
- memory change: 1.11x