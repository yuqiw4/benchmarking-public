# Results vs. 3.10.4

- fork: brandtbucher
- ref: justin_trampolines
- machine: darwin-arm64
- commit hash: 6e8e3d5
- commit date: 2024-05-02
- overall geometric mean: 1.23x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.15x faster
- Memory change: 1.40x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 192 ms                                                 | 170 ms: 1.13x faster                                                       |
| chameleon      | 6.26 ms                                                | 4.43 ms: 1.41x faster                                                      |
| docutils       | 1.73 sec                                               | 1.50 sec: 1.15x faster                                                     |
| html5lib       | 42.4 ms                                                | 30.9 ms: 1.37x faster                                                      |
| tornado_http   | 86.7 ms                                                | 72.1 ms: 1.20x faster                                                      |
| Geometric mean | (ref)                                                  | 1.25x faster                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_none         | 388 ms                                                 | 200 ms: 1.94x faster                                                       |
| async_tree_memoization  | 474 ms                                                 | 267 ms: 1.77x faster                                                       |
| async_tree_io           | 980 ms                                                 | 555 ms: 1.77x faster                                                       |
| async_tree_cpu_io_mixed | 649 ms                                                 | 460 ms: 1.41x faster                                                       |
| Geometric mean          | (ref)                                                  | 1.71x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 69.0 ms                                                | 49.4 ms: 1.40x faster                                                      |
| nbody          | 93.0 ms                                                | 67.8 ms: 1.37x faster                                                      |
| Geometric mean | (ref)                                                  | 1.24x faster                                                               |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 95.3 ms                                                | 71.5 ms: 1.33x faster                                                      |
| regex_dna      | 174 ms                                                 | 149 ms: 1.17x faster                                                       |
| regex_v8       | 17.1 ms                                                | 17.3 ms: 1.01x slower                                                      |
| regex_effbot   | 2.46 ms                                                | 2.57 ms: 1.04x slower                                                      |
| Geometric mean | (ref)                                                  | 1.10x faster                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| pickle_pure_python   | 281 us                                                 | 181 us: 1.55x faster                                                       |
| unpickle_pure_python | 194 us                                                 | 129 us: 1.51x faster                                                       |
| tomli_loads          | 1.71 sec                                               | 1.22 sec: 1.40x faster                                                     |
| xml_etree_process    | 46.5 ms                                                | 35.7 ms: 1.30x faster                                                      |
| json_dumps           | 8.11 ms                                                | 6.32 ms: 1.28x faster                                                      |
| xml_etree_parse      | 108 ms                                                 | 104 ms: 1.04x faster                                                       |
| xml_etree_iterparse  | 72.1 ms                                                | 69.9 ms: 1.03x faster                                                      |
| xml_etree_generate   | 53.5 ms                                                | 53.3 ms: 1.00x faster                                                      |
| json_loads           | 16.4 us                                                | 17.0 us: 1.03x slower                                                      |
| pickle               | 6.97 us                                                | 7.20 us: 1.03x slower                                                      |
| unpickle             | 8.80 us                                                | 9.21 us: 1.05x slower                                                      |
| pickle_dict          | 17.0 us                                                | 18.1 us: 1.07x slower                                                      |
| pickle_list          | 2.74 us                                                | 2.93 us: 1.07x slower                                                      |
| unpickle_list        | 2.69 us                                                | 2.92 us: 1.08x slower                                                      |
| Geometric mean       | (ref)                                                  | 1.11x faster                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 10.9 ms                                                | 14.5 ms: 1.34x slower                                                      |
| python_startup_no_site | 7.91 ms                                                | 11.7 ms: 1.48x slower                                                      |
| Geometric mean         | (ref)                                                  | 1.41x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 9.87 ms                                                | 6.39 ms: 1.55x faster                                                      |
| django_template | 26.4 ms                                                | 21.2 ms: 1.25x faster                                                      |
| genshi_xml      | 33.8 ms                                                | 40.6 ms: 1.20x slower                                                      |
| Geometric mean  | (ref)                                                  | 1.13x faster                                                               |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols | 323 us                                                 | 102 us: 3.18x faster                                                       |
| deltablue                | 4.91 ms                                                | 2.41 ms: 2.04x faster                                                      |
| async_tree_none          | 388 ms                                                 | 200 ms: 1.94x faster                                                       |
| logging_silent           | 117 ns                                                 | 63.2 ns: 1.85x faster                                                      |
| raytrace                 | 301 ms                                                 | 170 ms: 1.78x faster                                                       |
| async_tree_memoization   | 474 ms                                                 | 267 ms: 1.77x faster                                                       |
| async_tree_io            | 980 ms                                                 | 555 ms: 1.77x faster                                                       |
| richards_super           | 57.8 ms                                                | 32.9 ms: 1.76x faster                                                      |
| richards                 | 48.7 ms                                                | 29.2 ms: 1.67x faster                                                      |
| chaos                    | 65.8 ms                                                | 39.6 ms: 1.66x faster                                                      |
| sqlglot_parse            | 1.24 ms                                                | 777 us: 1.60x faster                                                       |
| asyncio_tcp              | 659 ms                                                 | 422 ms: 1.56x faster                                                       |
| pickle_pure_python       | 281 us                                                 | 181 us: 1.55x faster                                                       |
| mako                     | 9.87 ms                                                | 6.39 ms: 1.55x faster                                                      |
| sqlglot_transpile        | 1.44 ms                                                | 943 us: 1.53x faster                                                       |
| pylint                   | 277 ms                                                 | 182 ms: 1.52x faster                                                       |
| unpickle_pure_python     | 194 us                                                 | 129 us: 1.51x faster                                                       |
| scimark_monte_carlo      | 65.6 ms                                                | 43.7 ms: 1.50x faster                                                      |
| deepcopy_memo            | 34.7 us                                                | 23.4 us: 1.48x faster                                                      |
| crypto_pyaes             | 71.8 ms                                                | 48.7 ms: 1.47x faster                                                      |
| go                       | 151 ms                                                 | 105 ms: 1.43x faster                                                       |
| pprint_safe_repr         | 641 ms                                                 | 449 ms: 1.43x faster                                                       |
| logging_simple           | 4.45 us                                                | 3.13 us: 1.42x faster                                                      |
| hexiom                   | 6.19 ms                                                | 4.36 ms: 1.42x faster                                                      |
| logging_format           | 4.83 us                                                | 3.41 us: 1.42x faster                                                      |
| pprint_pformat           | 1.30 sec                                               | 922 ms: 1.41x faster                                                       |
| chameleon                | 6.26 ms                                                | 4.43 ms: 1.41x faster                                                      |
| async_tree_cpu_io_mixed  | 649 ms                                                 | 460 ms: 1.41x faster                                                       |
| tomli_loads              | 1.71 sec                                               | 1.22 sec: 1.40x faster                                                     |
| float                    | 69.0 ms                                                | 49.4 ms: 1.40x faster                                                      |
| comprehensions           | 16.9 us                                                | 12.1 us: 1.39x faster                                                      |
| generators               | 32.3 ms                                                | 23.4 ms: 1.38x faster                                                      |
| nbody                    | 93.0 ms                                                | 67.8 ms: 1.37x faster                                                      |
| html5lib                 | 42.4 ms                                                | 30.9 ms: 1.37x faster                                                      |
| pyflate                  | 427 ms                                                 | 314 ms: 1.36x faster                                                       |
| pycparser                | 877 ms                                                 | 646 ms: 1.36x faster                                                       |
| spectral_norm            | 94.8 ms                                                | 70.1 ms: 1.35x faster                                                      |
| regex_compile            | 95.3 ms                                                | 71.5 ms: 1.33x faster                                                      |
| scimark_lu               | 103 ms                                                 | 78.8 ms: 1.31x faster                                                      |
| xml_etree_process        | 46.5 ms                                                | 35.7 ms: 1.30x faster                                                      |
| fannkuch                 | 303 ms                                                 | 233 ms: 1.30x faster                                                       |
| deepcopy                 | 272 us                                                 | 211 us: 1.29x faster                                                       |
| json_dumps               | 8.11 ms                                                | 6.32 ms: 1.28x faster                                                      |
| thrift                   | 572 us                                                 | 447 us: 1.28x faster                                                       |
| coroutines               | 20.7 ms                                                | 16.3 ms: 1.27x faster                                                      |
| sympy_sum                | 92.2 ms                                                | 72.6 ms: 1.27x faster                                                      |
| deepcopy_reduce          | 2.33 us                                                | 1.84 us: 1.27x faster                                                      |
| django_template          | 26.4 ms                                                | 21.2 ms: 1.25x faster                                                      |
| scimark_sor              | 128 ms                                                 | 103 ms: 1.24x faster                                                       |
| dulwich_log              | 35.3 ms                                                | 29.0 ms: 1.22x faster                                                      |
| mypy2                    | 607 ms                                                 | 499 ms: 1.22x faster                                                       |
| asyncio_tcp_ssl          | 1.60 sec                                               | 1.33 sec: 1.21x faster                                                     |
| sympy_str                | 165 ms                                                 | 137 ms: 1.21x faster                                                       |
| tornado_http             | 86.7 ms                                                | 72.1 ms: 1.20x faster                                                      |
| sympy_integrate          | 13.1 ms                                                | 10.9 ms: 1.20x faster                                                      |
| regex_dna                | 174 ms                                                 | 149 ms: 1.17x faster                                                       |
| scimark_fft              | 224 ms                                                 | 192 ms: 1.17x faster                                                       |
| docutils                 | 1.73 sec                                               | 1.50 sec: 1.15x faster                                                     |
| scimark_sparse_mat_mult  | 3.42 ms                                                | 2.98 ms: 1.15x faster                                                      |
| sympy_expand             | 269 ms                                                 | 235 ms: 1.14x faster                                                       |
| dask                     | 253 ms                                                 | 224 ms: 1.13x faster                                                       |
| 2to3                     | 192 ms                                                 | 170 ms: 1.13x faster                                                       |
| sqlglot_optimize         | 36.8 ms                                                | 33.1 ms: 1.11x faster                                                      |
| nqueens                  | 63.8 ms                                                | 57.5 ms: 1.11x faster                                                      |
| bench_thread_pool        | 527 us                                                 | 481 us: 1.10x faster                                                       |
| sqlglot_normalize        | 190 ms                                                 | 174 ms: 1.09x faster                                                       |
| aiohttp                  | 1.22 ms                                                | 1.12 ms: 1.09x faster                                                      |
| gunicorn                 | 1.30 ms                                                | 1.20 ms: 1.09x faster                                                      |
| mdp                      | 1.63 sec                                               | 1.52 sec: 1.08x faster                                                     |
| meteor_contest           | 77.7 ms                                                | 72.5 ms: 1.07x faster                                                      |
| pathlib                  | 24.5 ms                                                | 23.3 ms: 1.05x faster                                                      |
| json                     | 3.08 ms                                                | 2.94 ms: 1.05x faster                                                      |
| xml_etree_parse          | 108 ms                                                 | 104 ms: 1.04x faster                                                       |
| xml_etree_iterparse      | 72.1 ms                                                | 69.9 ms: 1.03x faster                                                      |
| xml_etree_generate       | 53.5 ms                                                | 53.3 ms: 1.00x faster                                                      |
| asyncio_websockets       | 410 ms                                                 | 408 ms: 1.00x faster                                                       |
| regex_v8                 | 17.1 ms                                                | 17.3 ms: 1.01x slower                                                      |
| json_loads               | 16.4 us                                                | 17.0 us: 1.03x slower                                                      |
| pickle                   | 6.97 us                                                | 7.20 us: 1.03x slower                                                      |
| gc_traversal             | 2.36 ms                                                | 2.46 ms: 1.04x slower                                                      |
| regex_effbot             | 2.46 ms                                                | 2.57 ms: 1.04x slower                                                      |
| unpickle                 | 8.80 us                                                | 9.21 us: 1.05x slower                                                      |
| create_gc_cycles         | 860 us                                                 | 906 us: 1.05x slower                                                       |
| pickle_dict              | 17.0 us                                                | 18.1 us: 1.07x slower                                                      |
| pickle_list              | 2.74 us                                                | 2.93 us: 1.07x slower                                                      |
| sqlite_synth             | 1.46 us                                                | 1.58 us: 1.08x slower                                                      |
| unpickle_list            | 2.69 us                                                | 2.92 us: 1.08x slower                                                      |
| coverage                 | 41.5 ms                                                | 45.4 ms: 1.09x slower                                                      |
| genshi_xml               | 33.8 ms                                                | 40.6 ms: 1.20x slower                                                      |
| bench_mp_pool            | 37.4 ms                                                | 46.7 ms: 1.25x slower                                                      |
| async_generators         | 231 ms                                                 | 291 ms: 1.26x slower                                                       |
| telco                    | 3.49 ms                                                | 4.45 ms: 1.27x slower                                                      |
| python_startup           | 10.9 ms                                                | 14.5 ms: 1.34x slower                                                      |
| python_startup_no_site   | 7.91 ms                                                | 11.7 ms: 1.48x slower                                                      |
| Geometric mean           | (ref)                                                  | 1.23x faster                                                               |

Benchmark hidden because not significant (2): pidigits, genshi_text
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (12) of results/bm-20240502-3.13.0a6+-6e8e3d5-JIT/bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5.json: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.20x
- 95% likely to have a speedup of 1.18x
- 99% likely to have a speedup of 1.15x

# Memory
- memory change: 1.40x