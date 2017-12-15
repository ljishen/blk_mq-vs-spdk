== blk_mq  ==
sudo schedtool -F -p 49 -a 0,1,2,3,4,5,12,13,14,15,16,17 -e $HOME/fio/fio $HOME/configs/example_config_blk_mq.fio | tee example_config_kyber_1jbs_polling.log


== perf ==
sudo $HOME/spdk/examples/nvme/perf/perf -q 128 -s 4096 -w read -t 5 -r 'trtype:PCIe traddr:0000:07:00.0' -d 1024 -c 0x1
