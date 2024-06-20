# Results vs. 3.10.4

- fork: python
- ref: a74f117dab369e6c5415
- machine: windows-amd64
- commit hash: a74f117
- commit date: 2024-04-14
- overall geometric mean: 1.22x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 246 ms                                                      | 218 ms: 1.13x faster                                                        |
| chameleon      | 5.79 ms                                                     | 4.67 ms: 1.24x faster                                                       |
| docutils       | 1.92 sec                                                    | 1.68 sec: 1.14x faster                                                      |
| html5lib       | 51.0 ms                                                     | 36.0 ms: 1.42x faster                                                       |
| tornado_http   | 108 ms                                                      | 83.0 ms: 1.30x faster                                                       |
| Geometric mean | (ref)                                                       | 1.24x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|-------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_none         | 435 ms                                                      | 219 ms: 1.99x faster                                                        |
| async_tree_memoization  | 526 ms                                                      | 267 ms: 1.97x faster                                                        |
| async_tree_io           | 1.11 sec                                                    | 590 ms: 1.88x faster                                                        |
| async_tree_cpu_io_mixed | 638 ms                                                      | 392 ms: 1.63x faster                                                        |
| Geometric mean          | (ref)                                                       | 1.86x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 61.7 ms                                                     | 46.7 ms: 1.32x faster                                                       |
| nbody          | 71.3 ms                                                     | 58.3 ms: 1.22x faster                                                       |
| pidigits       | 149 ms                                                      | 147 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                       | 1.18x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 106 ms                                                      | 86.8 ms: 1.22x faster                                                       |
| regex_dna      | 136 ms                                                      | 120 ms: 1.13x faster                                                        |
| regex_effbot   | 1.66 ms                                                     | 1.60 ms: 1.04x faster                                                       |
| regex_v8       | 15.4 ms                                                     | 15.0 ms: 1.03x faster                                                       |
| Geometric mean | (ref)                                                       | 1.10x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 9.16 ms                                                     | 5.52 ms: 1.66x faster                                                       |
| pickle_pure_python   | 270 us                                                      | 171 us: 1.58x faster                                                        |
| unpickle_pure_python | 183 us                                                      | 123 us: 1.49x faster                                                        |
| tomli_loads          | 1.67 sec                                                    | 1.18 sec: 1.41x faster                                                      |
| xml_etree_process    | 44.5 ms                                                     | 37.0 ms: 1.20x faster                                                       |
| xml_etree_parse      | 96.8 ms                                                     | 90.0 ms: 1.08x faster                                                       |
| xml_etree_iterparse  | 65.0 ms                                                     | 60.9 ms: 1.07x faster                                                       |
| xml_etree_generate   | 55.5 ms                                                     | 53.0 ms: 1.05x faster                                                       |
| unpickle             | 9.09 us                                                     | 8.80 us: 1.03x faster                                                       |
| pickle               | 6.85 us                                                     | 7.23 us: 1.06x slower                                                       |
| pickle_list          | 2.75 us                                                     | 2.91 us: 1.06x slower                                                       |
| pickle_dict          | 17.2 us                                                     | 18.5 us: 1.08x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.15x faster                                                                |

Benchmark hidden because not significant (2): json_loads, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 20.6 ms                                                     | 21.4 ms: 1.04x slower                                                       |
| python_startup_no_site | 15.5 ms                                                     | 17.8 ms: 1.15x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.09x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako           | 9.03 ms                                                     | 5.72 ms: 1.58x faster                                                       |
| genshi_text    | 19.8 ms                                                     | 15.5 ms: 1.28x faster                                                       |
| genshi_xml     | 41.0 ms                                                     | 34.8 ms: 1.18x faster                                                       |
| Geometric mean | (ref)                                                       | 1.34x faster                                                                |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|--------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols | 336 us                                                      | 71.1 us: 4.72x faster                                                       |
| async_tree_none          | 435 ms                                                      | 219 ms: 1.99x faster                                                        |
| async_tree_memoization   | 526 ms                                                      | 267 ms: 1.97x faster                                                        |
| deltablue                | 4.19 ms                                                     | 2.20 ms: 1.91x faster                                                       |
| async_tree_io            | 1.11 sec                                                    | 590 ms: 1.88x faster                                                        |
| pylint                   | 350 ms                                                      | 194 ms: 1.80x faster                                                        |
| logging_silent           | 94.6 ns                                                     | 54.9 ns: 1.72x faster                                                       |
| richards_super           | 52.2 ms                                                     | 30.6 ms: 1.71x faster                                                       |
| json_dumps               | 9.16 ms                                                     | 5.52 ms: 1.66x faster                                                       |
| generators               | 32.4 ms                                                     | 19.8 ms: 1.64x faster                                                       |
| async_tree_cpu_io_mixed  | 638 ms                                                      | 392 ms: 1.63x faster                                                        |
| raytrace                 | 273 ms                                                      | 170 ms: 1.61x faster                                                        |
| chaos                    | 61.7 ms                                                     | 38.9 ms: 1.59x faster                                                       |
| pickle_pure_python       | 270 us                                                      | 171 us: 1.58x faster                                                        |
| mako                     | 9.03 ms                                                     | 5.72 ms: 1.58x faster                                                       |
| richards                 | 42.4 ms                                                     | 27.0 ms: 1.57x faster                                                       |
| sqlglot_parse            | 1.22 ms                                                     | 783 us: 1.55x faster                                                        |
| comprehensions           | 16.5 us                                                     | 10.7 us: 1.54x faster                                                       |
| asyncio_tcp              | 732 ms                                                      | 477 ms: 1.53x faster                                                        |
| pyflate                  | 409 ms                                                      | 269 ms: 1.52x faster                                                        |
| go                       | 139 ms                                                      | 91.8 ms: 1.51x faster                                                       |
| spectral_norm            | 77.3 ms                                                     | 51.3 ms: 1.51x faster                                                       |
| scimark_monte_carlo      | 57.3 ms                                                     | 38.5 ms: 1.49x faster                                                       |
| unpickle_pure_python     | 183 us                                                      | 123 us: 1.49x faster                                                        |
| sqlglot_transpile        | 1.48 ms                                                     | 995 us: 1.48x faster                                                        |
| html5lib                 | 51.0 ms                                                     | 36.0 ms: 1.42x faster                                                       |
| crypto_pyaes             | 62.5 ms                                                     | 44.3 ms: 1.41x faster                                                       |
| tomli_loads              | 1.67 sec                                                    | 1.18 sec: 1.41x faster                                                      |
| deepcopy_memo            | 28.8 us                                                     | 21.0 us: 1.37x faster                                                       |
| asyncio_tcp_ssl          | 2.11 sec                                                    | 1.58 sec: 1.33x faster                                                      |
| float                    | 61.7 ms                                                     | 46.7 ms: 1.32x faster                                                       |
| tornado_http             | 108 ms                                                      | 83.0 ms: 1.30x faster                                                       |
| pprint_pformat           | 1.22 sec                                                    | 943 ms: 1.29x faster                                                        |
| hexiom                   | 5.74 ms                                                     | 4.45 ms: 1.29x faster                                                       |
| scimark_sor              | 106 ms                                                      | 83.1 ms: 1.28x faster                                                       |
| genshi_text              | 19.8 ms                                                     | 15.5 ms: 1.28x faster                                                       |
| pprint_safe_repr         | 592 ms                                                      | 470 ms: 1.26x faster                                                        |
| pycparser                | 930 ms                                                      | 740 ms: 1.26x faster                                                        |
| dulwich_log              | 50.5 ms                                                     | 40.5 ms: 1.25x faster                                                       |
| mypy2                    | 555 ms                                                      | 447 ms: 1.24x faster                                                        |
| chameleon                | 5.79 ms                                                     | 4.67 ms: 1.24x faster                                                       |
| coroutines               | 16.0 ms                                                     | 13.0 ms: 1.23x faster                                                       |
| nbody                    | 71.3 ms                                                     | 58.3 ms: 1.22x faster                                                       |
| regex_compile            | 106 ms                                                      | 86.8 ms: 1.22x faster                                                       |
| sympy_sum                | 107 ms                                                      | 88.3 ms: 1.21x faster                                                       |
| bench_thread_pool        | 958 us                                                      | 791 us: 1.21x faster                                                        |
| sqlite_synth             | 1.91 us                                                     | 1.58 us: 1.21x faster                                                       |
| xml_etree_process        | 44.5 ms                                                     | 37.0 ms: 1.20x faster                                                       |
| scimark_sparse_mat_mult  | 2.72 ms                                                     | 2.27 ms: 1.20x faster                                                       |
| genshi_xml               | 41.0 ms                                                     | 34.8 ms: 1.18x faster                                                       |
| deepcopy                 | 255 us                                                      | 218 us: 1.17x faster                                                        |
| scimark_lu               | 85.8 ms                                                     | 73.2 ms: 1.17x faster                                                       |
| mdp                      | 1.78 sec                                                    | 1.53 sec: 1.16x faster                                                      |
| sympy_str                | 194 ms                                                      | 168 ms: 1.16x faster                                                        |
| sqlglot_normalize        | 205 ms                                                      | 179 ms: 1.15x faster                                                        |
| sqlglot_optimize         | 39.8 ms                                                     | 34.7 ms: 1.15x faster                                                       |
| sympy_integrate          | 15.3 ms                                                     | 13.3 ms: 1.15x faster                                                       |
| docutils                 | 1.92 sec                                                    | 1.68 sec: 1.14x faster                                                      |
| scimark_fft              | 187 ms                                                      | 165 ms: 1.14x faster                                                        |
| deepcopy_reduce          | 2.20 us                                                     | 1.94 us: 1.13x faster                                                       |
| fannkuch                 | 256 ms                                                      | 226 ms: 1.13x faster                                                        |
| regex_dna                | 136 ms                                                      | 120 ms: 1.13x faster                                                        |
| 2to3                     | 246 ms                                                      | 218 ms: 1.13x faster                                                        |
| aiohttp                  | 995 us                                                      | 898 us: 1.11x faster                                                        |
| nqueens                  | 66.6 ms                                                     | 60.5 ms: 1.10x faster                                                       |
| sympy_expand             | 314 ms                                                      | 286 ms: 1.10x faster                                                        |
| logging_format           | 6.76 us                                                     | 6.26 us: 1.08x faster                                                       |
| logging_simple           | 6.22 us                                                     | 5.77 us: 1.08x faster                                                       |
| xml_etree_parse          | 96.8 ms                                                     | 90.0 ms: 1.08x faster                                                       |
| xml_etree_iterparse      | 65.0 ms                                                     | 60.9 ms: 1.07x faster                                                       |
| meteor_contest           | 75.9 ms                                                     | 71.7 ms: 1.06x faster                                                       |
| xml_etree_generate       | 55.5 ms                                                     | 53.0 ms: 1.05x faster                                                       |
| regex_effbot             | 1.66 ms                                                     | 1.60 ms: 1.04x faster                                                       |
| unpickle                 | 9.09 us                                                     | 8.80 us: 1.03x faster                                                       |
| regex_v8                 | 15.4 ms                                                     | 15.0 ms: 1.03x faster                                                       |
| pidigits                 | 149 ms                                                      | 147 ms: 1.02x faster                                                        |
| pathlib                  | 75.7 ms                                                     | 74.8 ms: 1.01x faster                                                       |
| python_startup           | 20.6 ms                                                     | 21.4 ms: 1.04x slower                                                       |
| pickle                   | 6.85 us                                                     | 7.23 us: 1.06x slower                                                       |
| pickle_list              | 2.75 us                                                     | 2.91 us: 1.06x slower                                                       |
| pickle_dict              | 17.2 us                                                     | 18.5 us: 1.08x slower                                                       |
| bench_mp_pool            | 62.0 ms                                                     | 67.2 ms: 1.08x slower                                                       |
| async_generators         | 222 ms                                                      | 240 ms: 1.08x slower                                                        |
| gc_traversal             | 1.41 ms                                                     | 1.54 ms: 1.09x slower                                                       |
| create_gc_cycles         | 800 us                                                      | 884 us: 1.10x slower                                                        |
| python_startup_no_site   | 15.5 ms                                                     | 17.8 ms: 1.15x slower                                                       |
| coverage                 | 39.0 ms                                                     | 46.4 ms: 1.19x slower                                                       |
| telco                    | 3.94 ms                                                     | 4.83 ms: 1.23x slower                                                       |
| thrift                   | 617 us                                                      | 8.76 ms: 14.19x slower                                                      |
| Geometric mean           | (ref)                                                       | 1.22x faster                                                                |

Benchmark hidden because not significant (3): json_loads, unpickle_list, json
Ignored benchmarks (6) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120.json: dask, django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240414-3.13.0a6+-a74f117-JIT/bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.20x
- 95% likely to have a speedup of 1.18x
- 99% likely to have a speedup of 1.16x

# Memory
- memory change: unknown