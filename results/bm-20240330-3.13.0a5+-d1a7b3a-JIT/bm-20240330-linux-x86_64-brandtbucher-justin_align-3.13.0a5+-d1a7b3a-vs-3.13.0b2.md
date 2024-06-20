# Results vs. 3.13.0b2

- fork: brandtbucher
- ref: justin_align
- machine: linux-x86_64
- commit hash: d1a7b3a
- commit date: 2024-03-30
- overall geometric mean: 1.02x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.06x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 280 ms: 1.02x slower                                                 |
| chameleon      | 7.22 ms                                                    | 7.00 ms: 1.03x faster                                                |
| docutils       | 2.83 sec                                                   | 2.90 sec: 1.03x slower                                               |
| html5lib       | 67.2 ms                                                    | 68.6 ms: 1.02x slower                                                |
| tornado_http   | 94.6 ms                                                    | 97.3 ms: 1.03x slower                                                |
| Geometric mean | (ref)                                                      | 1.01x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|--------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none_tg | 336 ms                                                     | 344 ms: 1.02x slower                                                 |
| async_tree_none    | 378 ms                                                     | 392 ms: 1.04x slower                                                 |
| Geometric mean     | (ref)                                                      | 1.01x slower                                                         |

Benchmark hidden because not significant (6): async_tree_cpu_io_mixed, async_tree_memoization, async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_io, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 78.9 ms                                                    | 77.2 ms: 1.02x faster                                                |
| pidigits       | 191 ms                                                     | 189 ms: 1.01x faster                                                 |
| nbody          | 88.3 ms                                                    | 92.4 ms: 1.05x slower                                                |
| Geometric mean | (ref)                                                      | 1.00x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_v8       | 25.1 ms                                                    | 25.6 ms: 1.02x slower                                                |
| regex_dna      | 221 ms                                                     | 231 ms: 1.04x slower                                                 |
| regex_effbot   | 3.67 ms                                                    | 3.87 ms: 1.06x slower                                                |
| regex_compile  | 137 ms                                                     | 146 ms: 1.07x slower                                                 |
| Geometric mean | (ref)                                                      | 1.05x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| unpickle_list        | 5.34 us                                                    | 5.06 us: 1.06x faster                                                |
| json_loads           | 28.9 us                                                    | 28.4 us: 1.02x faster                                                |
| xml_etree_parse      | 162 ms                                                     | 159 ms: 1.02x faster                                                 |
| json_dumps           | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                                |
| tomli_loads          | 2.12 sec                                                   | 2.10 sec: 1.01x faster                                               |
| pickle_pure_python   | 305 us                                                     | 309 us: 1.01x slower                                                 |
| pickle_dict          | 34.8 us                                                    | 35.3 us: 1.02x slower                                                |
| xml_etree_generate   | 87.4 ms                                                    | 89.2 ms: 1.02x slower                                                |
| unpickle             | 15.1 us                                                    | 15.6 us: 1.03x slower                                                |
| pickle_list          | 5.11 us                                                    | 5.37 us: 1.05x slower                                                |
| pickle               | 11.5 us                                                    | 12.5 us: 1.09x slower                                                |
| unpickle_pure_python | 218 us                                                     | 240 us: 1.10x slower                                                 |
| Geometric mean       | (ref)                                                      | 1.01x slower                                                         |

Benchmark hidden because not significant (2): xml_etree_process, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 11.1 ms: 1.03x slower                                                |
| python_startup_no_site | 7.11 ms                                                    | 9.55 ms: 1.34x slower                                                |
| Geometric mean         | (ref)                                                      | 1.18x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|-----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 10.8 ms: 1.04x faster                                                |
| django_template | 34.8 ms                                                    | 35.8 ms: 1.03x slower                                                |
| genshi_text     | 23.7 ms                                                    | 24.6 ms: 1.04x slower                                                |
| genshi_xml      | 51.6 ms                                                    | 55.3 ms: 1.07x slower                                                |
| Geometric mean  | (ref)                                                      | 1.03x slower                                                         |

All benchmarks:
===============

| Benchmark                | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|--------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| typing_runtime_protocols | 165 us                                                     | 115 us: 1.44x faster                                                 |
| scimark_fft              | 392 ms                                                     | 343 ms: 1.14x faster                                                 |
| scimark_sparse_mat_mult  | 5.27 ms                                                    | 4.80 ms: 1.10x faster                                                |
| richards_super           | 57.4 ms                                                    | 53.3 ms: 1.08x faster                                                |
| richards                 | 50.9 ms                                                    | 47.5 ms: 1.07x faster                                                |
| create_gc_cycles         | 1.82 ms                                                    | 1.69 ms: 1.07x faster                                                |
| pylint                   | 317 ms                                                     | 299 ms: 1.06x faster                                                 |
| unpickle_list            | 5.34 us                                                    | 5.06 us: 1.06x faster                                                |
| crypto_pyaes             | 77.5 ms                                                    | 74.4 ms: 1.04x faster                                                |
| deepcopy_reduce          | 3.35 us                                                    | 3.22 us: 1.04x faster                                                |
| mako                     | 11.2 ms                                                    | 10.8 ms: 1.04x faster                                                |
| chameleon                | 7.22 ms                                                    | 7.00 ms: 1.03x faster                                                |
| coroutines               | 23.2 ms                                                    | 22.5 ms: 1.03x faster                                                |
| logging_silent           | 105 ns                                                     | 102 ns: 1.03x faster                                                 |
| sqlite_synth             | 2.99 us                                                    | 2.92 us: 1.02x faster                                                |
| pprint_pformat           | 1.56 sec                                                   | 1.52 sec: 1.02x faster                                               |
| float                    | 78.9 ms                                                    | 77.2 ms: 1.02x faster                                                |
| json_loads               | 28.9 us                                                    | 28.4 us: 1.02x faster                                                |
| pprint_safe_repr         | 758 ms                                                     | 746 ms: 1.02x faster                                                 |
| xml_etree_parse          | 162 ms                                                     | 159 ms: 1.02x faster                                                 |
| fannkuch                 | 402 ms                                                     | 397 ms: 1.01x faster                                                 |
| pidigits                 | 191 ms                                                     | 189 ms: 1.01x faster                                                 |
| json_dumps               | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                                |
| gc_traversal             | 3.98 ms                                                    | 3.94 ms: 1.01x faster                                                |
| tomli_loads              | 2.12 sec                                                   | 2.10 sec: 1.01x faster                                               |
| deepcopy                 | 367 us                                                     | 365 us: 1.01x faster                                                 |
| thrift                   | 823 us                                                     | 819 us: 1.00x faster                                                 |
| asyncio_tcp              | 508 ms                                                     | 510 ms: 1.00x slower                                                 |
| asyncio_websockets       | 567 ms                                                     | 570 ms: 1.01x slower                                                 |
| spectral_norm            | 116 ms                                                     | 117 ms: 1.01x slower                                                 |
| asyncio_tcp_ssl          | 1.84 sec                                                   | 1.86 sec: 1.01x slower                                               |
| logging_format           | 6.47 us                                                    | 6.53 us: 1.01x slower                                                |
| meteor_contest           | 110 ms                                                     | 111 ms: 1.01x slower                                                 |
| bench_mp_pool            | 23.9 ms                                                    | 24.2 ms: 1.01x slower                                                |
| pickle_pure_python       | 305 us                                                     | 309 us: 1.01x slower                                                 |
| mdp                      | 2.79 sec                                                   | 2.83 sec: 1.01x slower                                               |
| generators               | 29.6 ms                                                    | 30.1 ms: 1.01x slower                                                |
| pickle_dict              | 34.8 us                                                    | 35.3 us: 1.02x slower                                                |
| sqlglot_transpile        | 1.63 ms                                                    | 1.66 ms: 1.02x slower                                                |
| pyflate                  | 484 ms                                                     | 493 ms: 1.02x slower                                                 |
| sqlglot_normalize        | 110 ms                                                     | 112 ms: 1.02x slower                                                 |
| xml_etree_generate       | 87.4 ms                                                    | 89.2 ms: 1.02x slower                                                |
| sqlglot_parse            | 1.32 ms                                                    | 1.35 ms: 1.02x slower                                                |
| html5lib                 | 67.2 ms                                                    | 68.6 ms: 1.02x slower                                                |
| 2to3                     | 274 ms                                                     | 280 ms: 1.02x slower                                                 |
| regex_v8                 | 25.1 ms                                                    | 25.6 ms: 1.02x slower                                                |
| dask                     | 369 ms                                                     | 377 ms: 1.02x slower                                                 |
| async_tree_none_tg       | 336 ms                                                     | 344 ms: 1.02x slower                                                 |
| gunicorn                 | 1.28 ms                                                    | 1.31 ms: 1.03x slower                                                |
| scimark_monte_carlo      | 69.2 ms                                                    | 70.9 ms: 1.03x slower                                                |
| docutils                 | 2.83 sec                                                   | 2.90 sec: 1.03x slower                                               |
| bench_thread_pool        | 834 us                                                     | 856 us: 1.03x slower                                                 |
| chaos                    | 61.3 ms                                                    | 63.0 ms: 1.03x slower                                                |
| tornado_http             | 94.6 ms                                                    | 97.3 ms: 1.03x slower                                                |
| aiohttp                  | 1.18 ms                                                    | 1.22 ms: 1.03x slower                                                |
| django_template          | 34.8 ms                                                    | 35.8 ms: 1.03x slower                                                |
| sympy_str                | 282 ms                                                     | 291 ms: 1.03x slower                                                 |
| unpickle                 | 15.1 us                                                    | 15.6 us: 1.03x slower                                                |
| djangocms                | 31.5 us                                                    | 32.5 us: 1.03x slower                                                |
| logging_simple           | 5.74 us                                                    | 5.94 us: 1.03x slower                                                |
| python_startup           | 10.8 ms                                                    | 11.1 ms: 1.03x slower                                                |
| async_tree_none          | 378 ms                                                     | 392 ms: 1.04x slower                                                 |
| sympy_expand             | 473 ms                                                     | 491 ms: 1.04x slower                                                 |
| genshi_text              | 23.7 ms                                                    | 24.6 ms: 1.04x slower                                                |
| scimark_sor              | 127 ms                                                     | 133 ms: 1.04x slower                                                 |
| coverage                 | 93.1 ms                                                    | 97.1 ms: 1.04x slower                                                |
| regex_dna                | 221 ms                                                     | 231 ms: 1.04x slower                                                 |
| sqlglot_optimize         | 55.5 ms                                                    | 58.0 ms: 1.04x slower                                                |
| nbody                    | 88.3 ms                                                    | 92.4 ms: 1.05x slower                                                |
| sympy_sum                | 156 ms                                                     | 164 ms: 1.05x slower                                                 |
| pickle_list              | 5.11 us                                                    | 5.37 us: 1.05x slower                                                |
| async_generators         | 442 ms                                                     | 465 ms: 1.05x slower                                                 |
| regex_effbot             | 3.67 ms                                                    | 3.87 ms: 1.06x slower                                                |
| dulwich_log              | 67.2 ms                                                    | 71.2 ms: 1.06x slower                                                |
| sympy_integrate          | 20.5 ms                                                    | 21.8 ms: 1.06x slower                                                |
| mypy2                    | 742 ms                                                     | 789 ms: 1.06x slower                                                 |
| pycparser                | 1.16 sec                                                   | 1.24 sec: 1.07x slower                                               |
| regex_compile            | 137 ms                                                     | 146 ms: 1.07x slower                                                 |
| genshi_xml               | 51.6 ms                                                    | 55.3 ms: 1.07x slower                                                |
| deltablue                | 3.25 ms                                                    | 3.52 ms: 1.08x slower                                                |
| pickle                   | 11.5 us                                                    | 12.5 us: 1.09x slower                                                |
| go                       | 145 ms                                                     | 157 ms: 1.09x slower                                                 |
| scimark_lu               | 122 ms                                                     | 133 ms: 1.10x slower                                                 |
| unpickle_pure_python     | 218 us                                                     | 240 us: 1.10x slower                                                 |
| comprehensions           | 16.6 us                                                    | 18.3 us: 1.10x slower                                                |
| raytrace                 | 267 ms                                                     | 294 ms: 1.10x slower                                                 |
| pathlib                  | 17.3 ms                                                    | 19.3 ms: 1.11x slower                                                |
| nqueens                  | 81.4 ms                                                    | 92.7 ms: 1.14x slower                                                |
| hexiom                   | 6.30 ms                                                    | 7.24 ms: 1.15x slower                                                |
| python_startup_no_site   | 7.11 ms                                                    | 9.55 ms: 1.34x slower                                                |
| Geometric mean           | (ref)                                                      | 1.02x slower                                                         |

Benchmark hidden because not significant (11): async_tree_cpu_io_mixed, async_tree_memoization, async_tree_cpu_io_mixed_tg, async_tree_io_tg, deepcopy_memo, xml_etree_process, json, xml_etree_iterparse, telco, async_tree_io, async_tree_memoization_tg
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging
Ignored benchmarks (1) of results/bm-20240330-3.13.0a5+-d1a7b3a-JIT/bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a.json: unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.06x