```
687: 'organ, pipe organ'
690: 'oxcart'
626: 'lighter, light, igniter, ignitor'

920: 'traffic light, traffic signal, stoplight'
919: 'street sign',

620: 'laptop, laptop computer'
688: 'oscilloscope, scope, cathode-ray oscilloscope, CRO'
782: 'screen, CRT screen'
916: website

973: 'coral reef',

972: 'cliff, drop, drop-off',
974: 'geyser',
975: 'lakeside, lakeshore',
976: 'promontory, headland, head, foreland',
977: 'sandbar, sand bar',
978: 'seashore, coast, seacoast, sea-coast',
979: 'valley, vale'
970: 'alp'
980: 'volcano'

625: 'lifeboat',
628: 'liner, ocean liner',
812: 'space shuttle'
817: 'sports car, sport car',

327: 'starfish, sea star',
328: 'sea urchin',
329: 'sea cucumber, holothurian',

318: 'lacewing, lacewing fly',
319: "dragonfly, darning needle, devil's darning needle, sewing needle, snake feeder, snake doctor, mosquito hawk, skeeter hawk",
320: 'damselfly',
321: 'admiral',
322: 'ringlet, ringlet butterfly',
323: 'monarch, monarch butterfly, milkweed butterfly, Danaus plexippus',
324: 'cabbage butterfly',
325: 'sulphur butterfly, sulfur butterfly',
326: 'lycaenid, lycaenid butterfly',

754: 'radio, wireless',
755: 'radio telescope, radio reflector',

300: 'tiger beetle',
301: 'ladybug, ladybeetle, lady beetle, ladybird, ladybird beetle',
302: 'ground beetle, carabid beetle',
303: 'long-horned beetle, longicorn, longicorn beetle',
304: 'leaf beetle, chrysomelid',
305: 'dung beetle',
306: 'rhinoceros beetle',
307: 'weevil',

310: 'ant, emmet, pismire',
308: 'fly',
309: 'bee',

311: 'grasshopper, hopper',
312: 'cricket',
313: 'walking stick, walkingstick, stick insect',
315: 'mantis, mantid',
317: 'leafhopper',

314: 'cockroach, roach',
316: 'cicada, cicala',

796: 'ski mask'

916: 'web site, website, internet site, site',

917: 'comic book',

918: 'crossword puzzle, crossword',
```

## butterflies
--classes 318 319 320 321 322 323 324 325 326 --num_classes 9

## olschool tech
--classes 620 688 782 916 --num_classes 4


# PARAMS
--pitch_sensitivity     range: 1 - 299             default: 220
--tempo_sensitivity     range: 0.05 - 0.8          default: 0.25
--depth                 range: 0.01 - 1            default: 1
--truncation            range: 0.1 - 1             default: 1
--frame_length          range: Multiples of 64     default: 512
--smooth_factor         range: 10 - 30             default: 20



# COOL PARAMS
python visualize.py --song audio/calmeplat.mp3 --resolution 128 --classes 655 --num_classes 1 --pitch_sensitivity 250 --tempo_sensitivity 0.6 --depth 0.5 --truncation 1 --frame_length 512 --smooth_factor 15 --duration 10

# TODO

- **landscapes**   python visualize.py --song audio/big_drums.mp3 --resolution 256 --classes 972 970 980 --num_classes 3 --pitch_sensitivity 250 --tempo_sensitivity 0.6 --depth 0.5 --truncation 1 --frame_length 512 --smooth_factor 15 --output_file landscapes.mp4
- **papillons**    python visualize.py --song audio/big_drums.mp3 --resolution 256 --classes 318 319 320 321 322 323 324 325 326 --num_classes 9 --pitch_sensitivity 250 --tempo_sensitivity 0.6 --depth 0.5 --truncation 1 --frame_length 512 --smooth_factor 15 --output_file papillons.mp4
- **boats**        python visualize.py --song audio/big_drums.mp3 --resolution 256 --classes 625 628 --num_classes 3 --pitch_sensitivity 250 --tempo_sensitivity 0.6 --depth 0.5 --truncation 1 --frame_length 512 --smooth_factor 15 --output_file boats-big.mp4

python visualize.py --song audio/big_drums.mp3 --resolution 128 --classes 318 319 320 321 322 323 324 325 326 --num_classes 9 --pitch_sensitivity 150 --tempo_sensitivity 0.4 --depth 0.5 --truncation 1 --frame_length 512 --smooth_factor 15 --duration 10 --output_file test2.mp4

python visualize.py --song audio/house.mp3 --resolution 256 --classes 754 755 --num_classes 2 --pitch_sensitivity 150 --tempo_sensitivity 0.4 --depth 0.5 --truncation 1 --frame_length 512 --smooth_factor 15 --output_file final_cool.mp4

python visualize.py --song audio/meloddddd.mp3 --resolution 256 --classes 980 --num_classes 1 --pitch_sensitivity 150 --tempo_sensitivity 0.4 --depth 0.5 --truncation 1 --frame_length 1024 --smooth_factor 15 --output_file drumsssprog-final.mp4


# COMPARISON
python visualize.py --song audio/think_break_melody.mp3 --resolution 128 --classes 327 328 329 --num_classes 3 --duration 10 --pitch_sensitivity 220 --tempo_sensitivity 0.25 --depth 1    --truncation 1   --frame_length 512  --smooth_factor 20 --output_file comparison/_default-depth_high-truncation_high-frame_length_low-smooth_factor_med.mp4
python visualize.py --song audio/think_break_melody.mp3 --resolution 128 --classes 327 328 329 --num_classes 3 --duration 10 --pitch_sensitivity 299 --tempo_sensitivity 0.25 --depth 1    --truncation 1   --frame_length 512  --smooth_factor 20 --output_file comparison/pitch_sensitivity_high.mp4
python visualize.py --song audio/think_break_melody.mp3 --resolution 128 --classes 327 328 329 --num_classes 3 --duration 10 --pitch_sensitivity 100 --tempo_sensitivity 0.25 --depth 1    --truncation 1   --frame_length 512  --smooth_factor 20 --output_file comparison/pitch_sensitivity_med.mp4
python visualize.py --song audio/think_break_melody.mp3 --resolution 128 --classes 327 328 329 --num_classes 3 --duration 10 --pitch_sensitivity 1   --tempo_sensitivity 0.25 --depth 1    --truncation 1   --frame_length 512  --smooth_factor 20 --output_file comparison/pitch_sensitivity_low.mp4
python visualize.py --song audio/think_break_melody.mp3 --resolution 128 --classes 327 328 329 --num_classes 3 --duration 10 --pitch_sensitivity 220 --tempo_sensitivity 0.05 --depth 1    --truncation 1   --frame_length 512  --smooth_factor 20 --output_file comparison/tempo_sensitivity_high.mp4
python visualize.py --song audio/think_break_melody.mp3 --resolution 128 --classes 327 328 329 --num_classes 3 --duration 10 --pitch_sensitivity 220 --tempo_sensitivity 0.4  --depth 1    --truncation 1   --frame_length 512  --smooth_factor 20 --output_file comparison/tempo_sensitivity_med.mp4
python visualize.py --song audio/think_break_melody.mp3 --resolution 128 --classes 327 328 329 --num_classes 3 --duration 10 --pitch_sensitivity 220 --tempo_sensitivity 0.8  --depth 1    --truncation 1   --frame_length 512  --smooth_factor 20 --output_file comparison/tempo_sensitivity_low.mp4
python visualize.py --song audio/think_break_melody.mp3 --resolution 128 --classes 327 328 329 --num_classes 3 --duration 10 --pitch_sensitivity 220 --tempo_sensitivity 0.25 --depth 0.5  --truncation 1   --frame_length 512  --smooth_factor 20 --output_file comparison/depth_med.mp4
python visualize.py --song audio/think_break_melody.mp3 --resolution 128 --classes 327 328 329 --num_classes 3 --duration 10 --pitch_sensitivity 220 --tempo_sensitivity 0.25 --depth 0.01 --truncation 1   --frame_length 512  --smooth_factor 20 --output_file comparison/depth_low.mp4
python visualize.py --song audio/think_break_melody.mp3 --resolution 128 --classes 327 328 329 --num_classes 3 --duration 10 --pitch_sensitivity 220 --tempo_sensitivity 0.25 --depth 1    --truncation 0.5 --frame_length 512  --smooth_factor 20 --output_file comparison/truncation_med.mp4
python visualize.py --song audio/think_break_melody.mp3 --resolution 128 --classes 327 328 329 --num_classes 3 --duration 10 --pitch_sensitivity 220 --tempo_sensitivity 0.25 --depth 1    --truncation 0.1 --frame_length 512  --smooth_factor 20 --output_file comparison/truncation_low.mp4
python visualize.py --song audio/think_break_melody.mp3 --resolution 128 --classes 327 328 329 --num_classes 3 --duration 10 --pitch_sensitivity 220 --tempo_sensitivity 0.25 --depth 1    --truncation 1   --frame_length 2048 --smooth_factor 20 --output_file comparison/frame_length_high.mp4
python visualize.py --song audio/think_break_melody.mp3 --resolution 128 --classes 327 328 329 --num_classes 3 --duration 10 --pitch_sensitivity 220 --tempo_sensitivity 0.25 --depth 1    --truncation 1   --frame_length 1024 --smooth_factor 20 --output_file comparison/frame_length_med.mp4
python visualize.py --song audio/think_break_melody.mp3 --resolution 128 --classes 327 328 329 --num_classes 3 --duration 10 --pitch_sensitivity 220 --tempo_sensitivity 0.25 --depth 1    --truncation 1   --frame_length 512  --smooth_factor 30 --output_file comparison/smooth_factor_high.mp4
python visualize.py --song audio/think_break_melody.mp3 --resolution 128 --classes 327 328 329 --num_classes 3 --duration 10 --pitch_sensitivity 220 --tempo_sensitivity 0.25 --depth 1    --truncation 1   --frame_length 512  --smooth_factor 10 --output_file comparison/smooth_factor_low.mp4








python visualize.py --song audio/compo_short_ugly.mp3 --song_final audio/compo_short.mp3 --resolution 256 --classes 895 --num_classes 1 --pitch_sensitivity 290 --tempo_sensitivity 0.6 --depth 1 --truncation 1 --frame_length 1024 --smooth_factor 20 --output_file planes_final.mp4


./ffmpeg -i final_cool.mp4 -s 1024x1024 -sws_flags neighbor _FINALS/ia6_out.mp4