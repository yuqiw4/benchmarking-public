# Results vs. 3.13.0b2

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 752e183
- commit date: 2024-03-31
- overall geometric mean: 1.01x faster
- HPT reliability: 99.71%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.97x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240331-linux-x86_64-python-main-3.13.0a5+-752e183 |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 269 ms: 1.02x faster                                   |
| chameleon      | 7.22 ms                                                    | 6.85 ms: 1.05x faster                                  |
| docutils       | 2.83 sec                                                   | 2.76 sec: 1.02x faster                                 |
| tornado_http   | 94.6 ms                                                    | 95.0 ms: 1.00x slower                                  |
| Geometric mean | (ref)                                                      | 1.02x faster                                           |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240331-linux-x86_64-python-main-3.13.0a5+-752e183 |
|-------------------------|:----------------------------------------------------------:|:------------------------------------------------------:|
| async_tree_cpu_io_mixed | 611 ms                                                     | 596 ms: 1.03x faster                                   |
| async_tree_none         | 378 ms                                                     | 386 ms: 1.02x slower                                   |
| Geometric mean          | (ref)                                                      | 1.01x faster                                           |

Benchmark hidden because not significant (6): async_tree_memoization, async_tree_io_tg, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_none_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240331-linux-x86_64-python-main-3.13.0a5+-752e183 |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------:|
| float          | 78.9 ms                                                    | 77.2 ms: 1.02x faster                                  |
| pidigits       | 191 ms                                                     | 190 ms: 1.01x faster                                   |
| nbody          | 88.3 ms                                                    | 89.5 ms: 1.01x slower                                  |
| Geometric mean | (ref)                                                      | 1.01x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240331-linux-x86_64-python-main-3.13.0a5+-752e183 |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 137 ms                                                     | 134 ms: 1.02x faster                                   |
| regex_effbot   | 3.67 ms                                                    | 3.76 ms: 1.02x slower                                  |
| regex_v8       | 25.1 ms                                                    | 26.2 ms: 1.04x slower                                  |
| Geometric mean | (ref)                                                      | 1.01x slower                                           |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240331-linux-x86_64-python-main-3.13.0a5+-752e183 |
|----------------------|:----------------------------------------------------------:|:------------------------------------------------------:|
| unpickle_list        | 5.34 us                                                    | 5.13 us: 1.04x faster                                  |
| pickle_dict          | 34.8 us                                                    | 33.6 us: 1.04x faster                                  |
| pickle_list          | 5.11 us                                                    | 4.96 us: 1.03x faster                                  |
| json_dumps           | 10.7 ms                                                    | 10.5 ms: 1.03x faster                                  |
| xml_etree_process    | 61.2 ms                                                    | 59.9 ms: 1.02x faster                                  |
| json_loads           | 28.9 us                                                    | 28.6 us: 1.01x faster                                  |
| pickle_pure_python   | 305 us                                                     | 303 us: 1.01x faster                                   |
| xml_etree_generate   | 87.4 ms                                                    | 86.7 ms: 1.01x faster                                  |
| unpickle_pure_python | 218 us                                                     | 220 us: 1.01x slower                                   |
| pickle               | 11.5 us                                                    | 11.6 us: 1.01x slower                                  |
| tomli_loads          | 2.12 sec                                                   | 2.22 sec: 1.05x slower                                 |
| unpickle             | 15.1 us                                                    | 18.5 us: 1.22x slower                                  |
| Geometric mean       | (ref)                                                      | 1.01x slower                                           |

Benchmark hidden because not significant (2): xml_etree_iterparse, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240331-linux-x86_64-python-main-3.13.0a5+-752e183 |
|------------------------|:----------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.6 ms: 1.01x faster                                  |
| python_startup_no_site | 7.11 ms                                                    | 8.99 ms: 1.27x slower                                  |
| Geometric mean         | (ref)                                                      | 1.12x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240331-linux-x86_64-python-main-3.13.0a5+-752e183 |
|-----------------|:----------------------------------------------------------:|:------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 10.9 ms: 1.03x faster                                  |
| django_template | 34.8 ms                                                    | 34.2 ms: 1.02x faster                                  |
| genshi_xml      | 51.6 ms                                                    | 52.6 ms: 1.02x slower                                  |
| genshi_text     | 23.7 ms                                                    | 24.3 ms: 1.03x slower                                  |
| Geometric mean  | (ref)                                                      | 1.00x faster                                           |

All benchmarks:
===============

| Benchmark                | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240331-linux-x86_64-python-main-3.13.0a5+-752e183 |
|--------------------------|:----------------------------------------------------------:|:------------------------------------------------------:|
| typing_runtime_protocols | 165 us                                                     | 112 us: 1.46x faster                                   |
| pylint                   | 317 ms                                                     | 280 ms: 1.13x faster                                   |
| scimark_sparse_mat_mult  | 5.27 ms                                                    | 4.71 ms: 1.12x faster                                  |
| richards                 | 50.9 ms                                                    | 45.9 ms: 1.11x faster                                  |
| richards_super           | 57.4 ms                                                    | 52.6 ms: 1.09x faster                                  |
| create_gc_cycles         | 1.82 ms                                                    | 1.67 ms: 1.09x faster                                  |
| crypto_pyaes             | 77.5 ms                                                    | 72.1 ms: 1.07x faster                                  |
| mdp                      | 2.79 sec                                                   | 2.60 sec: 1.07x faster                                 |
| deepcopy_reduce          | 3.35 us                                                    | 3.15 us: 1.06x faster                                  |
| chameleon                | 7.22 ms                                                    | 6.85 ms: 1.05x faster                                  |
| pyflate                  | 484 ms                                                     | 460 ms: 1.05x faster                                   |
| logging_silent           | 105 ns                                                     | 100 ns: 1.04x faster                                   |
| unpickle_list            | 5.34 us                                                    | 5.13 us: 1.04x faster                                  |
| spectral_norm            | 116 ms                                                     | 112 ms: 1.04x faster                                   |
| deepcopy                 | 367 us                                                     | 353 us: 1.04x faster                                   |
| scimark_lu               | 122 ms                                                     | 117 ms: 1.04x faster                                   |
| fannkuch                 | 402 ms                                                     | 387 ms: 1.04x faster                                   |
| deepcopy_memo            | 39.7 us                                                    | 38.3 us: 1.04x faster                                  |
| pickle_dict              | 34.8 us                                                    | 33.6 us: 1.04x faster                                  |
| go                       | 145 ms                                                     | 140 ms: 1.03x faster                                   |
| pprint_pformat           | 1.56 sec                                                   | 1.51 sec: 1.03x faster                                 |
| mako                     | 11.2 ms                                                    | 10.9 ms: 1.03x faster                                  |
| pprint_safe_repr         | 758 ms                                                     | 735 ms: 1.03x faster                                   |
| sympy_str                | 282 ms                                                     | 274 ms: 1.03x faster                                   |
| scimark_fft              | 392 ms                                                     | 381 ms: 1.03x faster                                   |
| sqlglot_parse            | 1.32 ms                                                    | 1.28 ms: 1.03x faster                                  |
| pickle_list              | 5.11 us                                                    | 4.96 us: 1.03x faster                                  |
| sqlite_synth             | 2.99 us                                                    | 2.90 us: 1.03x faster                                  |
| sqlglot_transpile        | 1.63 ms                                                    | 1.59 ms: 1.03x faster                                  |
| scimark_sor              | 127 ms                                                     | 124 ms: 1.03x faster                                   |
| async_tree_cpu_io_mixed  | 611 ms                                                     | 596 ms: 1.03x faster                                   |
| json_dumps               | 10.7 ms                                                    | 10.5 ms: 1.03x faster                                  |
| docutils                 | 2.83 sec                                                   | 2.76 sec: 1.02x faster                                 |
| regex_compile            | 137 ms                                                     | 134 ms: 1.02x faster                                   |
| scimark_monte_carlo      | 69.2 ms                                                    | 67.6 ms: 1.02x faster                                  |
| sympy_integrate          | 20.5 ms                                                    | 20.0 ms: 1.02x faster                                  |
| nqueens                  | 81.4 ms                                                    | 79.6 ms: 1.02x faster                                  |
| float                    | 78.9 ms                                                    | 77.2 ms: 1.02x faster                                  |
| xml_etree_process        | 61.2 ms                                                    | 59.9 ms: 1.02x faster                                  |
| django_template          | 34.8 ms                                                    | 34.2 ms: 1.02x faster                                  |
| sympy_expand             | 473 ms                                                     | 464 ms: 1.02x faster                                   |
| hexiom                   | 6.30 ms                                                    | 6.18 ms: 1.02x faster                                  |
| 2to3                     | 274 ms                                                     | 269 ms: 1.02x faster                                   |
| chaos                    | 61.3 ms                                                    | 60.4 ms: 1.02x faster                                  |
| sympy_sum                | 156 ms                                                     | 154 ms: 1.01x faster                                   |
| meteor_contest           | 110 ms                                                     | 108 ms: 1.01x faster                                   |
| sqlglot_optimize         | 55.5 ms                                                    | 54.8 ms: 1.01x faster                                  |
| deltablue                | 3.25 ms                                                    | 3.21 ms: 1.01x faster                                  |
| comprehensions           | 16.6 us                                                    | 16.4 us: 1.01x faster                                  |
| python_startup           | 10.8 ms                                                    | 10.6 ms: 1.01x faster                                  |
| json_loads               | 28.9 us                                                    | 28.6 us: 1.01x faster                                  |
| pidigits                 | 191 ms                                                     | 190 ms: 1.01x faster                                   |
| pickle_pure_python       | 305 us                                                     | 303 us: 1.01x faster                                   |
| thrift                   | 823 us                                                     | 816 us: 1.01x faster                                   |
| xml_etree_generate       | 87.4 ms                                                    | 86.7 ms: 1.01x faster                                  |
| sqlglot_normalize        | 110 ms                                                     | 110 ms: 1.01x faster                                   |
| bench_thread_pool        | 834 us                                                     | 830 us: 1.00x faster                                   |
| asyncio_tcp_ssl          | 1.84 sec                                                   | 1.83 sec: 1.00x faster                                 |
| asyncio_tcp              | 508 ms                                                     | 506 ms: 1.00x faster                                   |
| tornado_http             | 94.6 ms                                                    | 95.0 ms: 1.00x slower                                  |
| raytrace                 | 267 ms                                                     | 268 ms: 1.00x slower                                   |
| generators               | 29.6 ms                                                    | 29.8 ms: 1.01x slower                                  |
| gc_traversal             | 3.98 ms                                                    | 4.00 ms: 1.01x slower                                  |
| unpickle_pure_python     | 218 us                                                     | 220 us: 1.01x slower                                   |
| dulwich_log              | 67.2 ms                                                    | 67.6 ms: 1.01x slower                                  |
| pickle                   | 11.5 us                                                    | 11.6 us: 1.01x slower                                  |
| coroutines               | 23.2 ms                                                    | 23.5 ms: 1.01x slower                                  |
| logging_format           | 6.47 us                                                    | 6.56 us: 1.01x slower                                  |
| nbody                    | 88.3 ms                                                    | 89.5 ms: 1.01x slower                                  |
| telco                    | 8.41 ms                                                    | 8.54 ms: 1.01x slower                                  |
| genshi_xml               | 51.6 ms                                                    | 52.6 ms: 1.02x slower                                  |
| async_tree_none          | 378 ms                                                     | 386 ms: 1.02x slower                                   |
| regex_effbot             | 3.67 ms                                                    | 3.76 ms: 1.02x slower                                  |
| logging_simple           | 5.74 us                                                    | 5.90 us: 1.03x slower                                  |
| genshi_text              | 23.7 ms                                                    | 24.3 ms: 1.03x slower                                  |
| regex_v8                 | 25.1 ms                                                    | 26.2 ms: 1.04x slower                                  |
| coverage                 | 93.1 ms                                                    | 97.6 ms: 1.05x slower                                  |
| tomli_loads              | 2.12 sec                                                   | 2.22 sec: 1.05x slower                                 |
| pycparser                | 1.16 sec                                                   | 1.22 sec: 1.05x slower                                 |
| pathlib                  | 17.3 ms                                                    | 19.0 ms: 1.10x slower                                  |
| unpickle                 | 15.1 us                                                    | 18.5 us: 1.22x slower                                  |
| python_startup_no_site   | 7.11 ms                                                    | 8.99 ms: 1.27x slower                                  |
| Geometric mean           | (ref)                                                      | 1.01x faster                                           |

Benchmark hidden because not significant (19): async_tree_memoization, async_tree_io_tg, async_tree_cpu_io_mixed_tg, dask, mypy2, async_tree_io, html5lib, aiohttp, bench_mp_pool, gunicorn, async_generators, xml_etree_iterparse, asyncio_websockets, regex_dna, json, async_tree_none_tg, async_tree_memoization_tg, xml_etree_parse, djangocms
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging
Ignored benchmarks (1) of results/bm-20240331-3.13.0a5+-752e183/bm-20240331-linux-x86_64-python-main-3.13.0a5+-752e183.json: unpack_sequence

# HPT report

- Reliability score: 99.71% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.97x