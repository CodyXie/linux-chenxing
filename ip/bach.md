# Bach

## Bank address for infinity3/mercury5

[detailed here](https://github.com/fifteenhex/SDK_pulbic/blob/c1436fa7446457e8d6547874d27ee4e34be150cf/Mercury5/proj/sc/driver/hal/mercury/audio/inc/hal_bach.h#L41)

- 0x1f2a0400
- 0x1f2a0600
- 0x1f2a0800
- 0x1f206800

## bank 1 - control/DMA registers

| offset | name                            | 15          | 14            | 13             | 12        | 11          | 10          | 9          | 8          | 7        | 6        | 5            | 4        | 3        | 2        | 1        | 0        |
|--------|---------------------------------|-------------|---------------|----------------|-----------|-------------|-------------|------------|------------|----------|----------|--------------|----------|----------|----------|----------|----------|
| 0x000  | enable ctrl                     |             |               |                |           | bp_adc_hpf2 | bp_adc_hpf1 |            |            |          |          |              |          |          |          |          |          |
| 0x004  | sr0 sel                         | cic_1_sel   | cic_1_sel     |                |           | cic_3_sel   | cic_3_sel   | writer_sel | writer_sel | src1_sel | src1_sel | src1_sel     | src1_sel | src2_sel | src2_sel | src2_sel | src2_sel |
| 0x008  | ???                             |             |               |                |           |             |             |            |            |          |          |              |          |          |          |          |          |
| 0x00c  | mux0 sel                        |             |               |                |           |             |             |            |            |          |          | mmc1 src sel |          |          |          |          |          |
| 0x010  | mux1 sel                        | adc_hpf_n   | adc_hpf_n     | adc_hpf_n      | adc_hpf_n |             |             |            |            |          |          |              |          |          |          |          |          |
| 0x014  | mix1 sel                        |             |               |                |           |             |             |            |            |          |          |              |          |          |          |          |          |
| 0x024  | sdm ctrl                        |             |               |                |           |             |             |            |            |          |          |              |          |          |          |          |          |
| 0x04c  | codec i2s tx ctrl               |             |               |                |           |             |             |            |            |          |          |              |          |          |          |          |          |
| 0x074  | synth ctrl                      |             |               |                |           |             |             |            |            |          |          |              |          |          |          |          |          |
| 0x090  | adc dpga cfg1                   |             |               |                |           |             |             |            |            |          |          |              |          |          |          |          |          |
| 0x094  | adc dpga cfg2                   |             |               |                |           |             |             |            |            |          |          |              |          |          |          |          |          |
| 0x1d4  | dma test ctrl 5 (sine wave gen) | sine gen en | sine gen left | sine gen right |           |             |             |            |            | gain     | gain     | gain         | gain     | freq     | freq     | freq     | freq     |
|        |                                 |             |               |                |           |             |             |            |            |          |          |              |          |          |          |          |          |

## bank 2 

| offset | name          | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0      |
|--------|---------------|----|----|----|----|----|----|---|---|---|---|---|---|---|---|---|--------|
| 0x01c  | int en        |    |    |    |    |    |    |   |   |   |   |   |   |   |   |   | int en |
| 0x038  | mux3 sel      |    |    |    |    |    |    |   |   |   |   |   |   |   |   |   |        |
| 0x058  | au sys ctrl1  |    |    |    |    |    |    |   |   |   |   |   |   |   |   |   |        |
| 0x074  | dig mic ctrl0 |    |    |    |    |    |    |   |   |   |   |   |   |   |   |   |        |
| 0x078  | dig mic ctrl1 |    |    |    |    |    |    |   |   |   |   |   |   |   |   |   |        |

## bank 3

| offset | name   | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4      | 3      | 2      | 1      | 0      |
|--------|--------|----|----|----|----|----|----|---|---|---|---|---|--------|--------|--------|--------|--------|
| 0x010  |        |    |    |    |    |    |    |   |   |   |   |   | fs_sel | fs_sel | fs_sel | fs_sel | fs_sel |
|        |        |    |    |    |    |    |    |   |   |   |   |   |        |        |        |        |        |
|        |        |    |    |    |    |    |    |   |   |   |   |   |        |        |        |        |        |

## bank 4

| offset | name         | 15        | 14        | 13        | 12             | 11             | 10            | 9                | 8                | 7              | 6              | 5             | 4             | 3                  | 2                  | 1              | 0              | notes                                 |
|--------|--------------|-----------|-----------|-----------|----------------|----------------|---------------|------------------|------------------|----------------|----------------|---------------|---------------|--------------------|--------------------|----------------|----------------|---------------------------------------|
| 0x000  | analog ctrl0 |           |           |           |                | en msp         | en itest dac  | en dit adc0      | en dac disch     | en ck dac      | en ck dac      | en ck dac     | en ck dac     |                    | en chop adc0       | en byp inmux   | en byp inmux   |                                       |
| 0x004  | analog ctrl1 |           |           |           | en vref sfydch | en vref sfydch | en vref disch | en tst ibias adc | en tst ibias adc | en shrt r adc0 | en shrt l adc0 | en qs ldo dac | en qs ldo adc | en mute mic stg1 r | en mute mic stg1 l | en mute in mux | en mute in mux |                                       |
| 0x008  | analog ctrl2 | en sw tst | en sw tst | en sw tst | en sw tst      | en sw tst      | en sw tst     | en sw tst        | en sw tst        | en sw tst      | en sw tst      | en sw tst     | en sw tst     | en sw tst          | en sw tst          | en sw tst      | en sw tst      |                                       |
| 0x00c  | analog ctrl3 |           |           |           | vref           | vi             | ref_dac       | r0_dac           | mic stg2_l       | mic stg1_l     | ldo dac        | ldo adc       | l0 dac        | inmux              | inmux              | bias dac       | adc0           | power downs, probably 1 to power down |
| 0x010  | analog ctrl4 |           |           |           |                |                |               |                  |                  | rst dac        | rst dac        | rst dac       | rst dac       |                    |                    |                | rst adc0       |                                       |
|        |              |           |           |           |                |                |               |                  |                  |                |                |               |               |                    |                    |                |                |                                       |
|        |              |           |           |           |                |                |               |                  |                  |                |                |               |               |                    |                    |                |                |                                       |
