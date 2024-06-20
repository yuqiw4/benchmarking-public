# Results vs. 3.10.4

- fork: python
- ref: a74f117dab369e6c5415
- machine: windows-amd64
- commit hash: a74f117
- commit date: 2024-04-14
- overall geometric mean: 1.14x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 246 ms                                                      | 222 ms: 1.11x faster                                                        |
| chameleon      | 5.79 ms                                                     | 4.90 ms: 1.18x faster                                                       |
| docutils       | 1.92 sec                                                    | 1.75 sec: 1.09x faster                                                      |
| html5lib       | 51.0 ms                                                     | 36.9 ms: 1.38x faster                                                       |
| tornado_http   | 108 ms                                                      | 83.9 ms: 1.29x faster                                                       |
| Geometric mean | (ref)                                                       | 1.21x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|-------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_none         | 435 ms                                                      | 226 ms: 1.93x faster                                                        |
| async_tree_memoization  | 526 ms                                                      | 275 ms: 1.92x faster                                                        |
| async_tree_io           | 1.11 sec                                                    | 596 ms: 1.86x faster                                                        |
| async_tree_cpu_io_mixed | 638 ms                                                      | 392 ms: 1.63x faster                                                        |
| Geometric mean          | (ref)                                                       | 1.83x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 61.7 ms                                                     | 57.0 ms: 1.08x faster                                                       |
| pidigits       | 149 ms                                                      | 147 ms: 1.02x faster                                                        |
| nbody          | 71.3 ms                                                     | 79.3 ms: 1.11x slower                                                       |
| Geometric mean | (ref)                                                       | 1.00x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_dna      | 136 ms                                                      | 121 ms: 1.13x faster                                                        |
| regex_effbot   | 1.66 ms                                                     | 1.59 ms: 1.04x faster                                                       |
| regex_compile  | 106 ms                                                      | 103 ms: 1.03x faster                                                        |
| regex_v8       | 15.4 ms                                                     | 15.3 ms: 1.01x faster                                                       |
| Geometric mean | (ref)                                                       | 1.05x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 9.16 ms                                                     | 5.66 ms: 1.62x faster                                                       |
| pickle_pure_python   | 270 us                                                      | 182 us: 1.48x faster                                                        |
| unpickle_pure_python | 183 us                                                      | 155 us: 1.18x faster                                                        |
| tomli_loads          | 1.67 sec                                                    | 1.46 sec: 1.15x faster                                                      |
| xml_etree_process    | 44.5 ms                                                     | 39.1 ms: 1.14x faster                                                       |
| xml_etree_parse      | 96.8 ms                                                     | 92.1 ms: 1.05x faster                                                       |
| unpickle             | 9.09 us                                                     | 8.83 us: 1.03x faster                                                       |
| json_loads           | 14.0 us                                                     | 13.8 us: 1.02x faster                                                       |
| xml_etree_iterparse  | 65.0 ms                                                     | 66.6 ms: 1.02x slower                                                       |
| pickle_list          | 2.75 us                                                     | 2.82 us: 1.02x slower                                                       |
| xml_etree_generate   | 55.5 ms                                                     | 56.9 ms: 1.03x slower                                                       |
| pickle               | 6.85 us                                                     | 7.17 us: 1.05x slower                                                       |
| unpickle_list        | 2.71 us                                                     | 2.88 us: 1.06x slower                                                       |
| pickle_dict          | 17.2 us                                                     | 18.7 us: 1.09x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.08x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 20.6 ms                                                     | 19.7 ms: 1.05x faster                                                       |
| python_startup_no_site | 15.5 ms                                                     | 16.1 ms: 1.04x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.01x faster                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako           | 9.03 ms                                                     | 7.07 ms: 1.28x faster                                                       |
| genshi_text    | 19.8 ms                                                     | 16.7 ms: 1.19x faster                                                       |
| genshi_xml     | 41.0 ms                                                     | 35.8 ms: 1.15x faster                                                       |
| Geometric mean | (ref)                                                       | 1.20x faster                                                                |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|--------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols | 336 us                                                      | 76.6 us: 4.39x faster                                                       |
| async_tree_none          | 435 ms                                                      | 226 ms: 1.93x faster                                                        |
| async_tree_memoization   | 526 ms                                                      | 275 ms: 1.92x faster                                                        |
| async_tree_io            | 1.11 sec                                                    | 596 ms: 1.86x faster                                                        |
| pylint                   | 350 ms                                                      | 198 ms: 1.77x faster                                                        |
| deltablue                | 4.19 ms                                                     | 2.44 ms: 1.72x faster                                                       |
| richards_super           | 52.2 ms                                                     | 31.2 ms: 1.67x faster                                                       |
| logging_silent           | 94.6 ns                                                     | 56.8 ns: 1.66x faster                                                       |
| async_tree_cpu_io_mixed  | 638 ms                                                      | 392 ms: 1.63x faster                                                        |
| json_dumps               | 9.16 ms                                                     | 5.66 ms: 1.62x faster                                                       |
| raytrace                 | 273 ms                                                      | 175 ms: 1.56x faster                                                        |
| richards                 | 42.4 ms                                                     | 27.3 ms: 1.55x faster                                                       |
| asyncio_tcp              | 732 ms                                                      | 479 ms: 1.53x faster                                                        |
| pickle_pure_python       | 270 us                                                      | 182 us: 1.48x faster                                                        |
| sqlglot_parse            | 1.22 ms                                                     | 829 us: 1.46x faster                                                        |
| generators               | 32.4 ms                                                     | 22.6 ms: 1.43x faster                                                       |
| sqlglot_transpile        | 1.48 ms                                                     | 1.05 ms: 1.41x faster                                                       |
| chaos                    | 61.7 ms                                                     | 44.2 ms: 1.40x faster                                                       |
| html5lib                 | 51.0 ms                                                     | 36.9 ms: 1.38x faster                                                       |
| go                       | 139 ms                                                      | 101 ms: 1.37x faster                                                        |
| asyncio_tcp_ssl          | 2.11 sec                                                    | 1.61 sec: 1.31x faster                                                      |
| tornado_http             | 108 ms                                                      | 83.9 ms: 1.29x faster                                                       |
| mako                     | 9.03 ms                                                     | 7.07 ms: 1.28x faster                                                       |
| crypto_pyaes             | 62.5 ms                                                     | 49.5 ms: 1.26x faster                                                       |
| pycparser                | 930 ms                                                      | 743 ms: 1.25x faster                                                        |
| pyflate                  | 409 ms                                                      | 332 ms: 1.23x faster                                                        |
| mypy2                    | 555 ms                                                      | 454 ms: 1.22x faster                                                        |
| deepcopy_memo            | 28.8 us                                                     | 23.5 us: 1.22x faster                                                       |
| coroutines               | 16.0 ms                                                     | 13.2 ms: 1.21x faster                                                       |
| comprehensions           | 16.5 us                                                     | 13.9 us: 1.19x faster                                                       |
| scimark_sor              | 106 ms                                                      | 89.4 ms: 1.19x faster                                                       |
| genshi_text              | 19.8 ms                                                     | 16.7 ms: 1.19x faster                                                       |
| unpickle_pure_python     | 183 us                                                      | 155 us: 1.18x faster                                                        |
| chameleon                | 5.79 ms                                                     | 4.90 ms: 1.18x faster                                                       |
| scimark_monte_carlo      | 57.3 ms                                                     | 49.0 ms: 1.17x faster                                                       |
| sqlite_synth             | 1.91 us                                                     | 1.65 us: 1.16x faster                                                       |
| bench_thread_pool        | 958 us                                                      | 827 us: 1.16x faster                                                        |
| tomli_loads              | 1.67 sec                                                    | 1.46 sec: 1.15x faster                                                      |
| genshi_xml               | 41.0 ms                                                     | 35.8 ms: 1.15x faster                                                       |
| mdp                      | 1.78 sec                                                    | 1.56 sec: 1.14x faster                                                      |
| sympy_sum                | 107 ms                                                      | 93.8 ms: 1.14x faster                                                       |
| dulwich_log              | 50.5 ms                                                     | 44.3 ms: 1.14x faster                                                       |
| xml_etree_process        | 44.5 ms                                                     | 39.1 ms: 1.14x faster                                                       |
| regex_dna                | 136 ms                                                      | 121 ms: 1.13x faster                                                        |
| pprint_pformat           | 1.22 sec                                                    | 1.09 sec: 1.11x faster                                                      |
| pprint_safe_repr         | 592 ms                                                      | 532 ms: 1.11x faster                                                        |
| 2to3                     | 246 ms                                                      | 222 ms: 1.11x faster                                                        |
| hexiom                   | 5.74 ms                                                     | 5.19 ms: 1.11x faster                                                       |
| sympy_integrate          | 15.3 ms                                                     | 13.8 ms: 1.11x faster                                                       |
| deepcopy                 | 255 us                                                      | 231 us: 1.11x faster                                                        |
| deepcopy_reduce          | 2.20 us                                                     | 2.01 us: 1.10x faster                                                       |
| docutils                 | 1.92 sec                                                    | 1.75 sec: 1.09x faster                                                      |
| aiohttp                  | 995 us                                                      | 911 us: 1.09x faster                                                        |
| scimark_lu               | 85.8 ms                                                     | 78.6 ms: 1.09x faster                                                       |
| sqlglot_normalize        | 205 ms                                                      | 189 ms: 1.09x faster                                                        |
| float                    | 61.7 ms                                                     | 57.0 ms: 1.08x faster                                                       |
| sqlglot_optimize         | 39.8 ms                                                     | 36.8 ms: 1.08x faster                                                       |
| sympy_str                | 194 ms                                                      | 182 ms: 1.07x faster                                                        |
| json                     | 3.14 ms                                                     | 2.96 ms: 1.06x faster                                                       |
| xml_etree_parse          | 96.8 ms                                                     | 92.1 ms: 1.05x faster                                                       |
| python_startup           | 20.6 ms                                                     | 19.7 ms: 1.05x faster                                                       |
| regex_effbot             | 1.66 ms                                                     | 1.59 ms: 1.04x faster                                                       |
| regex_compile            | 106 ms                                                      | 103 ms: 1.03x faster                                                        |
| unpickle                 | 9.09 us                                                     | 8.83 us: 1.03x faster                                                       |
| sympy_expand             | 314 ms                                                      | 307 ms: 1.03x faster                                                        |
| logging_format           | 6.76 us                                                     | 6.62 us: 1.02x faster                                                       |
| pidigits                 | 149 ms                                                      | 147 ms: 1.02x faster                                                        |
| json_loads               | 14.0 us                                                     | 13.8 us: 1.02x faster                                                       |
| logging_simple           | 6.22 us                                                     | 6.14 us: 1.01x faster                                                       |
| meteor_contest           | 75.9 ms                                                     | 74.9 ms: 1.01x faster                                                       |
| regex_v8                 | 15.4 ms                                                     | 15.3 ms: 1.01x faster                                                       |
| spectral_norm            | 77.3 ms                                                     | 79.0 ms: 1.02x slower                                                       |
| xml_etree_iterparse      | 65.0 ms                                                     | 66.6 ms: 1.02x slower                                                       |
| pickle_list              | 2.75 us                                                     | 2.82 us: 1.02x slower                                                       |
| xml_etree_generate       | 55.5 ms                                                     | 56.9 ms: 1.03x slower                                                       |
| python_startup_no_site   | 15.5 ms                                                     | 16.1 ms: 1.04x slower                                                       |
| pickle                   | 6.85 us                                                     | 7.17 us: 1.05x slower                                                       |
| bench_mp_pool            | 62.0 ms                                                     | 65.2 ms: 1.05x slower                                                       |
| unpickle_list            | 2.71 us                                                     | 2.88 us: 1.06x slower                                                       |
| scimark_fft              | 187 ms                                                      | 199 ms: 1.06x slower                                                        |
| nqueens                  | 66.6 ms                                                     | 71.2 ms: 1.07x slower                                                       |
| fannkuch                 | 256 ms                                                      | 274 ms: 1.07x slower                                                        |
| pickle_dict              | 17.2 us                                                     | 18.7 us: 1.09x slower                                                       |
| async_generators         | 222 ms                                                      | 245 ms: 1.10x slower                                                        |
| gc_traversal             | 1.41 ms                                                     | 1.56 ms: 1.11x slower                                                       |
| nbody                    | 71.3 ms                                                     | 79.3 ms: 1.11x slower                                                       |
| scimark_sparse_mat_mult  | 2.72 ms                                                     | 3.08 ms: 1.13x slower                                                       |
| create_gc_cycles         | 800 us                                                      | 909 us: 1.14x slower                                                        |
| coverage                 | 39.0 ms                                                     | 46.4 ms: 1.19x slower                                                       |
| telco                    | 3.94 ms                                                     | 5.03 ms: 1.28x slower                                                       |
| thrift                   | 617 us                                                      | 9.24 ms: 14.97x slower                                                      |
| Geometric mean           | (ref)                                                       | 1.14x faster                                                                |

Benchmark hidden because not significant (1): pathlib
Ignored benchmarks (6) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120.json: dask, django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240414-3.13.0a6+-a74f117-PYTHON_UOPS/bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.10x
- 95% likely to have a speedup of 1.10x
- 99% likely to have a speedup of 1.09x

# Memory
- memory change: unknown